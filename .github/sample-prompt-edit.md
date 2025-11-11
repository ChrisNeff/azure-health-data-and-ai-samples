# Create Unit Test

Create ONE new unit test following the established conventions in this repository.

## Required Conventions

1. **Test Framework**: xUnit with NSubstitute for mocking
2. **File Header**: Include the MIT license header used in other test files
3. **Naming Convention**: Use Given-When-Then pattern
   - Format: `Given{Context}_When{Action}_Then{ExpectedOutcome}`
4. **Test Structure**: Follow AAA (Arrange-Act-Assert) pattern
5. **Mocking**: Use NSubstitute.For<T>() for all mocks
6. **Assertions**: Use xUnit Assert methods

## Steps

1. Ask which class/method needs a test
2. Review existing test files to understand the pattern
3. Create the test file with proper header and structure
4. Write ONE focused test case
5. Ensure it follows all conventions found in the codebase

## Example Pattern

```csharp
// -------------------------------------------------------------------------------------------------
// Copyright (c) Microsoft Corporation. All rights reserved.
// Licensed under the MIT License (MIT). See LICENSE in the repo root for license information.
// -------------------------------------------------------------------------------------------------

[Fact]
public async Task GivenValidInput_WhenMethodCalled_ThenExpectedResultReturned()
{
    // Arrange
    var logger = Substitute.For<ILogger<ClassUnderTest>>();
    var sut = new ClassUnderTest(logger);

    // Act
    var result = await sut.MethodAsync(input);

    // Assert
    Assert.Equal(expected, result);
}
```

What would you like to create a test for?
