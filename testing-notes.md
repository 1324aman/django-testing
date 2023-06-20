### Good rules-of-thumb include having:
- a separate TestClass for each model or view
- a separate test method for each set of conditions you want to test
- test method names that describe their function
- integrate coverage tool, to check how much source code has been tested

### coverage
- `python3 -m pip install coverage`
- `coverage run --source='.' manage.py test myapp`
- we can also generate a test report with coverage tool `coverage report`
- If we want to exclude any line of code from coverage then add this comment on that line `# pragma: no cover`

