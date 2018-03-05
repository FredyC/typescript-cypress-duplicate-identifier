# Reproduction repo

 * Install dependencies with Yarn
 * Run `yarn tsc`
 * Errors are output

Cypress test framework is using Mocha underneath and it installs `@types/mocha`. Project that wants to use `@types/jest` runs into a following duplicate issues.


```
node_modules/@types/jest/index.d.ts(18,13): error TS2300: Duplicate identifier 'beforeEach'.
node_modules/@types/jest/index.d.ts(20,13): error TS2300: Duplicate identifier 'afterEach'.
node_modules/@types/mocha/index.d.ts(36,13): error TS2403: Subsequent variable declarations must have the same type.  Variable 'describe' must be of type 'Describe', but here
has type 'IContextDefinition'.
node_modules/@types/mocha/index.d.ts(37,13): error TS2403: Subsequent variable declarations must have the same type.  Variable 'xdescribe' must be of type 'Describe', but here has type 'IContextDefinition'.
node_modules/@types/mocha/index.d.ts(42,13): error TS2403: Subsequent variable declarations must have the same type.  Variable 'it' must be of type 'It', but here has type 'ITestDefinition'.
node_modules/@types/mocha/index.d.ts(43,13): error TS2403: Subsequent variable declarations must have the same type.  Variable 'xit' must be of type 'It', but here has type 'ITestDefinition'.
node_modules/@types/mocha/index.d.ts(45,13): error TS2403: Subsequent variable declarations must have the same type.  Variable 'test' must be of type 'It', but here has type 'ITestDefinition'.
node_modules/@types/mocha/index.d.ts(63,18): error TS2300: Duplicate identifier 'beforeEach'.
node_modules/@types/mocha/index.d.ts(64,18): error TS2300: Duplicate identifier 'beforeEach'.
node_modules/@types/mocha/index.d.ts(65,18): error TS2300: Duplicate identifier 'afterEach'.
node_modules/@types/mocha/index.d.ts(66,18): error TS2300: Duplicate identifier 'afterEach'.
```