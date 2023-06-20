### Good rules-of-thumb include having:
- a separate TestClass for each model or view
- a separate test method for each set of conditions you want to test
- test method names that describe their function
- integrate coverage tool, to check how much source code has been tested

### coverage, refer this doc [here](https://coverage.readthedocs.io/en/)
- `coverage run --source='.' manage.py test myapp`
- We can also generate a test report with coverage tool `coverage report`
- If we want to exclude some code from coverage report then add this comment on that line `# pragma: no cover`
-  Excluded code is executed as usual, and its execution is recorded in the coverage data as usual but not included in report.

