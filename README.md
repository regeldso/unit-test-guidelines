# .Net Unit Test Guidlines

## Disclaimer
> Based on [ Roy Osherove's "Art of Unit Testing"](https://www.amazon.com/Art-Unit-Testing-examples/dp/1617290890)


##1. Naming

Object to be tested | Name
------------ | -------------
Project | [ProjectUnderTest].UnitTests
Class | [ClassName]Tests
Unit of work | [UnitOfWorkName]\_[ScenarioUnderTest]\_[ExpectedBehavior] (*for exaple IsValidFileName_BadExtension_ReturnsFalse()*)

##2. Styling
* The test name can be very long.
* Empty line between the arrange, act, and assert stages in each test

>...to be continued
