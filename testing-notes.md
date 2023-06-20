### Good rules-of-thumb include having:
- a separate TestClass for each model or view
- a separate test method for each set of conditions you want to test
- test method names that describe their function
- integrate coverage tool, to check how much source code has been tested

### coverage, refer this doc [here](https://coverage.readthedocs.io/en/)
Coverage.py is a tool for measuring code coverage of Python programs. It monitors your program, noting which parts of the code have been executed, then analyzes the source to identify code that could have been executed but was not.

Coverage measurement is typically used to gauge the effectiveness of tests. It can show which parts of your code are being exercised by tests, and which are not.

- `coverage run --source='.' manage.py test myapp`
- We can also generate a test report with coverage tool `coverage report`
- If we want to exclude some code from coverage report then add this comment on that line `# pragma: no cover`
-  Excluded code is executed as usual, and its execution is recorded in the coverage data as usual but not included in report.

### How coverage works
Coverage.py works in three phases:

- Execution: Coverage.py runs your code, and monitors it to see what lines were executed.

- Analysis: Coverage.py examines your code to determine what lines could have run.

- Reporting: Coverage.py combines the results of execution and analysis to produce a coverage number and an indication of missing execution.
