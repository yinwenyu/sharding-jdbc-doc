+++
title = "Conventions"
weight = 2
prev = "/02-contribute/contributor/"
next = "/03-company/"
chapter = true
+++

# Development conventions

## Development idea

 - Write extremely clean, simplify and graceful code. Fully agree with <Refactoring: Improving the Design of Existing Code> and <Clean Code: A Handbook of Agile Software Craftsma>.

## Code push conventions

 - Make sure all test cases passed.
 - Make sure test coverage not lower than dev branch.
 - Use checkstyle to check code style, provide special reason if rule violated. Find checkstyle template from `sharding-jdbc/src/resources/dd_checks.xml`.
 - Make sure `mvn clean install` can be success.
 - Delete unused code in time.
 
## Code Conventions

 - Use linux line seperator.
 - Indent (including blank lines) is consistent with the previous line.
 - No unnecessary blank line.
 - All logs and java docs are in English.
 - Commit allow javadoc, todo and fixme only.
 - Static import is forbidden.
 - Give a meaningful variable name. The name of return value is result; The name of unit value is each in for each sentence, instead of entry for map iterator.
 - Name of properties file is camel-case, first letter is lowercase.
 - The nested loop should extract to a new private method.
 - Replace Nested Conditional with Guard Clauses.
 - Access permissions for classes and methods should minimal as possible.
 - Parameters and return value are not allowed to be null.
 - If use comment to explain the code, try to split several small methods, and use method name to explain it. 
 - Use lombok instead of the constructor, getter, setter methods and log variable.
 - keep style consistent with existed code.
 - No duplicate code and configuration.

## Unit Test Conventions

 - Test code and production code equality, should follow the same code conventions.
 - Test cases should fully covered if no special reason.
 - Separate environment preparation codes and test codes.
 - Only assertXXX, hamcrest for junit and mocktio related can use static import.
 - For single parameter assert, should use `assertTrue`, `assertFalse`, `assertNull` and `assertNotNull`.
 - For multiple parameters assert, should use `assertThat`.
 - Assert accurately, do not use `not`, `containsString` and so on.
 - Use actualXXX and expectedXXX to name related variable.
