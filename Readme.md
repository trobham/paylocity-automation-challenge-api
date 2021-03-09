This automation challenge repository contains api test collection that contains three folders.
  1. 'EmployeeRequestTests' - tests positive scenarious. It uses iteration data 'testdata/employees.json'
  2. 'ErrorHandlingTests' - tests responses when invalid data is sent to server. This also uses iteration data 'testdata/employees-invalid.json'
  3. 'SchemaValidationTests' - validates the schema structure in the responses. 
 Common tests and verifications are performed at folder level. Only few unique features to a specific request is cover in it's respective test.
 
 Best way to run the collection is from jenkins, or run the following newman scripts from command line:
   1. newman run tests/employee-benefits-tests.postman_collection.json --folder EmployeeRequestTests --environment tests/employee-benefits.postman_environment.json --iteration-data testdata/employees.json
   2. newman run tests/employee-benefits-tests.postman_collection.json --folder ErrorHandlingTests --environment tests/employee-benefits.postman_environment.json --iteration-data testdata/employees-invalid.json
   3. newman run tests/employee-benefits-tests.postman_collection.json --folder SchemaValidationTests --environment tests/employee-benefits.postman_environment.json
 
