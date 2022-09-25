# Unit testing
	
* Unit testing is a methodology where units of code are tested in isolation from the rest of the application. 
	
* A unit test might test a particular function, object, class, or module. 

* Unit tests are great to learn whether or not individual parts of an application work.

# Integration testing
	
* unit tests don’t test whether or not units work together when they’re composed to form a whole application. 

* You need integration tests, which can be collaboration tests between two or more units, or full end-to-end functional tests of the whole running application (aka system testing). 

# Behavior Driven Development / Behavior testing

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
* Notice that this language is focused exclusively on the business value that a customer should get from the software rather than describing the user interface of the software, or how the software should accomplish the goals. 

* This is the kind of language you could use as input for the UX design process. Designing these kinds of user requirements up front can save a lot of rework later in the process by helping the team and customers get on the same page about what product you’re building.

## Issue
I typically translate user requirements into functional tests rather than keep up BDD tests, mostly because of the complexity of integrating BDD frameworks with modern applications, and the cost of maintaining custom, English-like DSL whose definitions may end up spanning several systems, and even several implementation languages.

## Solution
I find the layman-readable DSL useful for very high-level specifications as a communications tool between stakeholders, but a typical software system will require orders of magnitude more low-level tests in order to produce adequate code and case coverage to prevent show-stopping bugs from reaching production.
