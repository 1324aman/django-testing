### Good rules-of-thumb include having:
- a separate TestClass for each model or view
- a separate test method for each set of conditions you want to test
- test method names that describe their function
- integrate coverage tool, to check how much source code has been tested
- initially we can have tests.py but as our tests grow, we can define test_views.py,test_models.py or test_forms.py etc.

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

- Reporting: Coverage.py combines the results of execution and analysis to produce a coverage number and an indication of missing execution and generates a report in html, json etc formats.

### Note
If your tests rely on database access such as creating or querying models, be sure to create your test classes as subclasses of `django.test.TestCase` rather than `unittest.TestCase`.

Using unittest.TestCase avoids the cost of running each test in a transaction and flushing the database, but if your tests interact with the database their behavior will vary based on the order that the test runner executes them. This can lead to unit tests that pass when run in isolation but fail when run in a suite.

### How to run tests in django project
- #### Run all the tests in the animals.tests module
- `./manage.py test animals.tests`
- #### Run all the tests found within the 'animals' app
- `./manage.py test animals`
- #### Run just one test case
- `./manage.py test animals.tests.AnimalTestCase`
- #### Run just one test method
- `./manage.py test animals.tests.AnimalTestCase.test_animals_can_speak`
- #### You can specify a custom filename pattern match using the -p (or --pattern) option, if your test files are named differently from the test*.py pattern
- `./manage.py test --pattern="tests_*.py"`
  
