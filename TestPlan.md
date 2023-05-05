# Test plan for the algorithmic project

<details>
<summary> Table of content</summary>

- [Test plan for the algorithmic project](#test-plan-for-the-algorithmic-project)
  - [Introduction](#introduction)
  - [Scope of the test plan](#scope-of-the-test-plan)
  - [Risk analysis](#risk-analysis)
  - [Ressources](#ressources)
    - [Tools used for the project](#tools-used-for-the-project)
  - [Expected architecture](#expected-architecture)
  - [testing approach](#testing-approach)
    - [Short term tests](#short-term-tests)
    - [Long term tests](#long-term-tests)
    - [Test deliverables](#test-deliverables)
    - [Success criteria](#success-criteria)

</details>

## Introduction

This document outlines the steps performed by the Quality Assurance(which is abbreviated to QA) during the project.

The main goal of this project is to create an algorithm to mix different types of wines into tanks and determine the fastest way to create the best champagne.

## Scope of the test plan

The test plan is designed to test the program created by our group, it will cover every possible uses of the program and will permit to detect every bug or unintented results. The main goal of this test plan is to prevent any crash and help our software engineer to optimise the program.

## Risk analysis

The project is containing major risks.
The major risks are:

- The program crashes or fail to compile correctly.
- The tanks are not completely full or empty which will lead to the oxidation of the wine, thus creating a waste of wine.
- The inputs are not correctly read, which will entails to an error or a miscalculation from our program, leading to a waste of wine.
- The ouput is not correctly written, making the next operation of the process impossible to perform.
- The program is slow, which leads to a slowdown of the production
- The data files are not correctly secured, which entails to a possible risk of human manipulation leading to a different process from the one given by the program.
  
A risk that cannot be forgotten is that testing cannot prevent every bug or unwanted result, testing helps reducing the number of bugs as much as possible.

## Ressources

### Tools used for the project

Hardware

```txt
- 4 MacBook Air M1 running on macOS Monterey
- 1 ThinkBook running on Windows 11
```

Software

```txt
- Github
- Visual studio community
- Visual studio code
- C#
```

## Expected architecture

The program will have a fairly small architecture, it has to be well organised to optimise the execution time and to allow future modifications by future development teams.

```txt
- waiting for further information
```

## testing approach

The tests will be divided into two types short term and long term tests.

### Short term tests

Tests defined as short term tests are the following:

- Program testing, testing the program as a user might use it.
- Testing the program flexibility, how the program will handle wrong input files or wrong command lines.

### Long term tests

Tests defined as long term test are:

- TDD tests, it will test the integrity of the code during the whole project, they have to be updated following a function's update, these tests cannot be passed by bypassing the function(we can't write result= true)
- Spaghetti code, we have to ensure that the code is optimal and easy to read, we have to give the more optimised code we can provide to the client given our ressources.

### Test deliverables

```txt
- Test plan
- Test cases
- Test results
```

### Success criteria

```txt
- All test must pass
- The program does not crash
- The program should not take more than 2 minutes to execute
- The input and output files are used correctly
```
