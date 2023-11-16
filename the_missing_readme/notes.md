# This Missing README
This book is a guide for new developers to help them on ther journey as they start out their development career. This book walks you through everything from how to work with managers and coworkers to progressing in your career as well as how to navigate daily tasks like jira, working with code, and code reviews. Each section below represents the chapters and the notes that I found most useful to me. 

## The Journey Ahead
this chapter was all about mapping your journey from start to finish as an engineer. Do you choose to continue down the path of contributor or take a different route and become a manager. This chapter helps you look at all paths

When starting at a new company
- Learn about their processes
- What tools they use
- How they structure their PULL REQUESTS
- CI/CD or any other build tools
- Where is their documentation
- What documentation is missing 
    - Great way to contribute early on by filling in or creating that document
- Learn about your Manager
    - How to work with them
    - Tell them about your goals
    - Understand their expectations of you

## Getting to Conscious Competence
this is about the 4 stages of competence
- unconscious incompetence
    - unable to perfom task and unaware of gaps
- conscious incompetence
    - unable to perform a task correctly but are aware of the gap
- unconscious competence
    - able to perform a task effortlessly
- conscious competence
    - capable of performaing a task with effort

- Learn by doing because we learn a little by reading but a lot by practicing
- Do the best to understand the impact of my work
- Timebox how long your research a problem before asking a question
- Show your work. Don't just share raw notes or ask for help without showing what you have already done
- Beat imposter syndrom down with keep records of accomplishments

## Working with Code
This chapter is all about how we work with not only new code but legacy code and how best to address technical debt

- Best path to address technical debt
    1. State the situation factually
    2. Describe the risk and the cost of the debt
    3. Propose a solution
    4. Discuss alternatives
    5. Weigh the trade-offs

- Safely changing code
    1. Identify change points
    2. Find tests
    3. Break Dependencies
    4. Write tests
    5. Make Changes and Refactor

- Keep changes and commits small
- Leave code cleaner than you found it

## Writing Operable Code
This chapter expended upon chapter 3 by talking about how to make code more readable and and some best practices

- Always be defensive. Never trust inputs from any source
- Avoid null values if possible. Return sensible defaults
- Type hinting and static checkers are your friends
- Retry intelligently. Watch for potential floods or endless retry loops
- Logs are very important. Don't just log to log. Make them actionable so that you or other developers know what happened and what to do next

## Managing Dependencies
This chapter was all about managing dependcies. How to get out of dependency hell and why we should introduce dependencies

- Pin dependcies in order to help aid in avoiding dependency hell
- Use battle tested libraries, don't write your own
- Understand the risk of bringing in a new dependency and what is it actually trying to solve

## Testing
This chapter was all about testing. Everything from the kids of test, to the tools, to how we should craft our tests

- Tests are like our first users of our code. They can show us potential bugs, to difficult code
- Types of Tests
    - integration tests
    - User Acceptance Tests
    - Unit tests
- Test Tools
    - Testing Frameworks like pytest
    - Mocking tools
    - Code coverage

- 100% code coverage != great tests or full coverage just simply you have tested every line
- Test Scenarios
    - black box testing where we test but don't know the implementation details
    - performace tests
    - pre refactoring tests

- Clean Tests
    - Documents code functionality
    - Tests for bad inputs
    - Finds edge cases
    - Ensures regressions don't happen
    - Tests for functionality not implementation
    
## Code Reviews
This chapter was all about how we should review code. Why they are important, how we can learn from them, don't take them personally and above all else how to give and receive a code review

- Don't always use the ide in the web, pull down the changes and review in your editor to get a bigger picture
- Make time for reviews and never feel pressure to just auto aprove
- Be empathetic when giving reviews
- Understand what is changing, why and how it will affect surrounding code
- Acknowledge good changes, you don't always have to do a review just to point out what is wrong
- Start with tests, that will help you understand what is changing

## Delivering Software

## Going On - Call
## Technical Design Process
## Creating Evolvable Architectures
## Agile Planning
## Working with Managers
## Navigating Your Career