# Unit Tests
	
* Unit testing is a methodology where units of code are tested in isolation from the rest of the application. 
	
* A unit test might test a particular function, object, class, or module. 

* Unit tests are great to learn whether or not individual parts of an application work.

* A Unit Test (UT) verifies if one of the smallest pieces in your software works as expected.

* The smallest piece in your software is usually a function or a class.

![Alt text](./images/unit-test.png?raw=true "Unit Tests")


# Integration Tests
	
* unit tests don’t test whether or not units work together when they’re composed to form a whole application. 

* You need integration tests, which can be collaboration tests between two or more units, or full end-to-end functional tests of the whole running application (aka system testing). 

![Alt text](./images/integration-test.png?raw=true "Integration Tests")

* An Integration Test (IT) verifies whether a cluster of units works together nicely.

* When one of your functions calls another of your functions, then this would be a cluster of units. But a cluster can also be made of one of your classes that interacts with other classes. Any combination is possible.

* Whenever your test interacts with more than just one unit – directly or indirectly, it becomes an Integration Test.

# Acceptance Tests

# Behavior Driven Development / Behavior Tests

* When working on a software project in a team that includes people with different roles, such as in agile environments, there is always a risk of misalignment in the understanding of end-user requirements and what the software should actually do. The developer may not fully understand because they may not be clearly formulated by the product owner. The product owner may not realize the complexity of the task being assigned for development and the impact it may have on its delivery. The tester may reason about different edge cases or scenarios that would have been easier to account at an early stage of the development.

* To help improve the development approach through better collaboration between business and developers, behavior-driven development (BDD) was established as a relatively recent software development approach, building on the main ideas of test-driven development (TDD) and using a higher-level granularity in the test approach: instead of unit tests for classes and methods, the tests are acceptance tests that validate the behavior of the application. 

* These acceptance tests are derived from concrete examples that are formulated by the team members so that the behavior of the system is better understood. When these example scenarios are formulated during conversations between the different members, the requirements are likely to be expressed more clearly, the input of the developer will likely be incorporated into them, and the tester will contribute with more scenarios to cover in the tests.

* BDD is a branch of Test Driven Development (TDD). 

* BDD uses human-readable descriptions of software user requirements as the basis for software tests.

* Like Domain Driven Design (DDD), an early step in BDD is the definition of a shared vocabulary between stakeholders, domain experts, and engineers. 

* This process involves the definition of entities, events, and outputs that the users care about, and giving them names that everybody can agree on.

* BDD practitioners then use that vocabulary to create a domain specific language they can use to encode system tests such as User Acceptance Tests (UAT).

* Each test is based on a user story written in the formally specified ubiquitous language based on English. (A ubiquitous language is a vocabulary shared by all stakeholders.)

	* A test for a transfer in a cryptocurrency wallet might look like this:

```
	Story: Transfers change balances
	As a wallet user
	In order to send money
	I want wallet balances to update
	Given that I have $40 in my balance
	And my friend has $10 is their balance
	When I transfer $20 to my friend
	Then I should have $20 in my balance
	And my friend should have $30 in their balance.
```
## Steps Guide
* The scenarios act as executable specifications for the behavior of the feature under test.
* These specifications can be executed as automated regression tests.
* The scenarios act as documentation about the feature that follows the main code in a version control system.

* Notice that this language is focused exclusively on the business value that a customer should get from the software rather than describing the user interface of the software, or how the software should accomplish the goals. 

* This is the kind of language you could use as input for the UX design process. Designing these kinds of user requirements up front can save a lot of rework later in the process by helping the team and customers get on the same page about what product you’re building.

## Issue
I typically translate user requirements into functional tests rather than keep up BDD tests, mostly because of the complexity of integrating BDD frameworks with modern applications, and the cost of maintaining custom, English-like DSL whose definitions may end up spanning several systems, and even several implementation languages.

## Solution
I find the layman-readable DSL useful for very high-level specifications as a communications tool between stakeholders, but a typical software system will require orders of magnitude more low-level tests in order to produce adequate code and case coverage to prevent show-stopping bugs from reaching production.


