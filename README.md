# .Net Unit Test Guidlines

## Disclaimer
> Based on [ Roy Osherove's "Art of Unit Testing"](https://www.amazon.com/Art-Unit-Testing-examples/dp/1617290890)

## 1. Naming

Object to be tested | Name
------------ | -------------
Project | [ProjectUnderTest].UnitTests
Class | [ClassName]Tests
Unit of work | [UnitOfWorkName]\_[ScenarioUnderTest]\_[ExpectedBehavior] (When  I  call  method  X  with  a  null  value,  then  it should do Y. *IsValidFileName_BadExtension_ReturnsFalse(),  AnalyzeFile_FileWith3LinesAndFileProvider_ReadsFileUsingProvider()*)

## 2. Styling
* The test name can be very long.
* Use **AAA** pattern.  Empty line between the **A**rrange, **A**ct, and **A**ssert stages in each test

## 3. Mocks, stubs and fakes

- **Mock** can fail tests. The mock object is the object you use to see if the test failed or not. In a test where you test only one thing, there should be no more than one mock object. All other fake objects will act as stubs.
  
- **Stub** replace an object so that you can test another object without problems. It can never fail your test and is strictly there to simulate various situations. 

- **Fake** is a generic term that can be used to describe either a stub
or a mock object (handwritten or otherwise), because they both look like the
real object. Whether a fake is a stub or a mock depends on how it’s used in
the current test.

## 4  Avoid logic & control flow statements in tests
- `switch, if`, or `else` statements
- `foreach`, `for`, or `while` loops
- `try-catch-finally`

## 5. Testing only one concern per test

## 6. Separate unit from integration tests

## 7. Assuring code review with code coverage

## 8. Use isolation frameworks 
An isolation framework is a set of programmable APIs that makes creating fake objects much simpler, faster, and shorter than hand-coding them.

- **constrained** (generate code and compile it at runtime, constrained by runtime, IL. Unable  to  fake  static  methods,  nonvirtual methods, nonpublic methods, and more)
  - Rhino 
  - Mocks
  - Moq
  - NMock
  - EasyMock,
  - NSubstitute
  - FakeItEasy
- **unconstrained** (profiler-based, use a set of
unmanaged APIs called the profiling APIs that are wrapped around the running instance of the CLR. Can effectively inject and change the behavior of any code they wish, in any class, in any library, even if it wasn’t compiled by you)
    - Typemock Isolator
    - JustMock
    - Moles (MS Fakes)

    [List of Testing Tools and Frameworks for.NET](https://github.com/dariusz-wozniak/List-of-Testing-Tools-and-Frameworks-for-.NET "Заголовок ссылки")


## 9. Avoid anything that tells you it will generate unit tests or test-related stuff for you, unless you have absolutely no choice.


## 10. Test class inheritance patterns
- Abstract test infrastructure class
- Template test class
- Abstract test driver class

>...to be continued
