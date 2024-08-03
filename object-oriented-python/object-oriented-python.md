# Object-Oriented Python

This book covered the basics of OOP and how it pretains to python. Some of the major topics covered are

- Why use objects
- How to model classes after real world
- The pillars of OOP AKA P-I-E
  - Polymorphisim
  - Inheritance
  - Encapsulation
- how self works
- how super works

* The OOP style lends it self to dealing with data and functions (or methods as they are known in classes)
  that operate on that data all encapsulated in a single location

* Classes are the blueprints which produce objects. Think of classes as like a cake mold. You can make many cakes with
  this one mold each with different toppings and filings. But they will all be made from the same mold

* The first parameter for any method in a class should be `self`. While this can be named anything `self` is the python
  convention

* When you call a method of a class you don't to specify the parameter for self. For example if we have the following class

```python
class Mixin:
    lookup_field = 'pk'

    def get_lookup_field(self):
        return self.lookup_field

mix = Mixin()
mix.get_lookup_field()
```

on the last line `mix` gets passed into the method automatically this is because python rearranges the call so that the
object making the call becomes the first argument passed in

- when you think of self you should think the current object

- When you hear the words interface think of what is presented to the client
- When you hear the words implementation think of how it does the job internally abstracted from the client

- You will also often here program to an interface not an implmentation. What they mean by that is the following example

```python
from abc import ABC, abstractmethod

# Interface
class PaymentProcessor(ABC):
    @abstractmethod
    def process_payment(self, amount: float):
        pass

# Implementation 1
class PayPalProcessor(PaymentProcessor):
    def process_payment(self, amount: float):
        print(f"Processing {amount} payment through PayPal")

# Implementation 2
class StripeProcessor(PaymentProcessor):
    def process_payment(self, amount: float):
        print(f"Processing {amount} payment through Stripe")

# Using the interface
class PaymentService:
    def __init__(self, payment_processor: PaymentProcessor):
        self.payment_processor = payment_processor

    def make_payment(self, amount: float):
        self.payment_processor.process_payment(amount)

# Example usage
paypal_processor = PayPalProcessor()
payment_service = PaymentService(paypal_processor)
payment_service.make_payment(100.0)

stripe_processor = StripeProcessor()
payment_service = PaymentService(stripe_processor)
payment_service.make_payment(200.0)
```

In this example you can see that we can pass in the payment processor of our choosing to the Payment Service and it will
still operate the same way. We could even add another Processor and it would still function properly

## Solid Principals

- The SOLID principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion) are important in Python development for creating clean, maintainable, and scalable code.

### Single Responsibility Principle (SRP):

Each class should have only one responsibility. In the example, PayPalProcessor and StripeProcessor each have the responsibility of processing payments.

### Open/Closed Principle (OCP):

Classes should be open for extension but closed for modification. The PaymentProcessor interface can be extended by adding new payment processors without modifying existing code.

### Liskov Substitution Principle (LSP):

Subtypes must be substitutable for their base types. Any class implementing PaymentProcessor should be able to be used interchangeably without affecting the PaymentService.

### Interface Segregation Principle (ISP):

Clients should not be forced to depend on interfaces they do not use. The PaymentProcessor interface is simple and focused, adhering to ISP.

### Dependency Inversion Principle (DIP):

High-level modules should not depend on low-level modules. Both should depend on abstractions. The PaymentService depends on the PaymentProcessor interface, not the concrete implementations.

## Encapsulation

- Hiding internal details of state and behavor from an external client
- getters and setters are a formal way of data hiding and protecting
  - \_\_private_variables
  - @properties

## Polymorphisim

- many forms meaning inherited methods can change in the child class or do different things but the method exists
  at both the parent and sub class

## Inheritance

- Data and Methods that are inherited by a child class. Similar to how kids inherit attributes from their parents
- Base Class / Parent Class think of these as the starting point for the sub class. however a sub class can also be a parent
  class to another sub class. A -> (B) -> C here B is both a parent class and a sub class
- Sub Class is the class that inherits from a parent class
- Typically used for Taking a Generic and make a more Specific Class
