# WSharp Conformance Tests 101–200

This pack adds 100 backend-agnostic `.we` language tests intended to help verify behavior during the C/C++ native rewrite.

The tests deliberately focus on observable language/runtime behavior instead of the current C# implementation details.

## Coverage

| Range | Area |
|---|---|
| 101–110 | Arithmetic, precedence, comparison and assignment |
| 111–120 | Control flow and scope |
| 121–130 | Functions, recursion, closures and higher-order functions |
| 131–140 | Lists, mutation, iteration and ranges |
| 141–150 | Dictionaries and strings |
| 151–160 | Numeric helpers, statistics and math functions |
| 161–170 | Functional collection operations |
| 171–180 | Algorithms and matrix/list logic |
| 181–190 | Scientific and neural-computing style cases |
| 191–200 | Error handling, stress and integration/regression |

## Migration goal

A native C/C++ implementation should produce the same PASS/FAIL behavior for these programs as the existing language runtime, unless an intentional language change is documented.

## Notes

- These are additive tests; existing tests 01–100 are left untouched.
- Each test prints its own file name, PASS/FAIL markers and a final `test_N done` line.
- The pack does not assume internal C#, C or C++ classes. It exercises the `.we` language surface.
- Error tests use existing `try/catch` language behavior.
