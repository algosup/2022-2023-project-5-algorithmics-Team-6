# Functional Requirement Document

---
<details>

<summary>Table of Contents</summary>

- [Functional Requirement Document](#functional-requirement-document)
  - [1. Introduction](#1-introduction)
    - [1.1 Background](#11-background)
    - [1.2 Requirement](#12-requirement)
  - [2. Personae](#2-personae)
    - [2.1 Fred](#21-fred)
    - [2.2 Jerry](#22-jerry)
  - [3. Use Cases](#3-use-cases)
  - [4. Functional Requirement](#4-functional-requirement)
    - [4.1 Assuption](#41-assumption)
    - [4.2 Risk](#42-risk)
    - [4.2 Logic](#43-logic)
  - [5. Non Functional Requirement](#5-non-functional-requirement)
    - [5.1 Security](#51-security)
    - [5.2 Availability](#52-availability)
    - [5.3 Scalability](#53-scalability)

</details>

---

## 1. Introduction

This purpose of this document is to present the different stakeholders with the needs and requirements for the implementation of an algorithm[^algorythm] destined to blend different variety of wines to create a consistent flavor profile.
This document is intended to be read by all parties responsible for the management of the project development initiative including but not limited to business users, user representatives and sponsors, and other interested parties.

---

### 1.1 Background

For this project we are working with Krug Champagne a House of champagne founded in 1843. We are tasked with building the software for their new winery, we will focus on the fourth part of the “méthode champenoise”: the Blending[^blending].
Our goal is to produce the closest result to the formula with the minimum number of steps.

---

### 1.2 Requirement

- No crash [^crash];
- No half empty/half full tanks;
- The product must be working on multiple OS[^os];
- The product must be as precise as possible;
- The code is easy to maintain and test;
- Few steps need to be carried out to get the result;
- The process needs to be fast;
- The product can handle different complexity level of formulas;

There are no specific language for this project.

---

## 2. Personae

The Personae represent the potential users of a product/service, their number scale with the size of the user base. In our case since we are targeting for our user base[^base] something very specific: the fourth part of the “méthode champenoise” we have few personae.

---

### 2.1 Fred

Fred is part of the team of Julie CAVIL and is responsible of the blending part of the “méthode champenoise”. He is 34 years old, married recently. He likes doing sports and particularly running.

Fred lives in the center of Reims and goes to work with using public transport or his bike.

He will need access to Powershell[^powershell] in order to provide input and output files to the algorythm and he need to access the output files for the steps.

---

### 2.2 Jerry

Jerry is working in the IT department of Krug. He is 26 years old, single. He likes playing video games
and listening to music.

Jerry lives in Muizon and takes his car to go to work.

He will need access to the code of the algorythm in order to update or verify the code and ensure it works.

---

## 3. Use cases

    - UC1 (Creating a Blend)
        Fred open Powershell
        Expected input --> He enter a command line containing two input file and one output file
        Expected output --> The algorithm return the output file
        He read the output file
        Case closed

    - UC2 (Testing the algorithm)
        Jerry open Powershell
        Expected input --> He enter a command line containing two input file and one output file
        Expected output --> The algorithm return the output file
        He verify the precision of the algorithm by reading the output file
        Case Closed
    
    - UC3 (Maintenance)
        Jerry open the files of the algorithm
        He does his maintenance
        He does a Test to verify the algorithm function
        Case Closed

---

## 4. Functional Requirement

The code must be able to:

    - allow user to input values representing the percentages of a certain wine;
    - return a result to the user detailling the steps carried out and the final blend;
    - identify tanks via their size, whether or not they are empty and which wine do they contain (volumes is usually expressed in hectoliters);
    - stop you from leaving a tank half empty;

---

### 4.1 Assumption

    - The size of the tanks will not be a problem, since we are working  with percentages;
    - The units in the formulas are standardized;

---

### 4.2 Risk

    - We might have trouble balancing simplicity, speed and precision;

---

### 4.3 Logic

    Data Input and Storage

Import the list of 250 wines of the year,the 150 reserve wines into the software .
Store the wines in a database[^database] or data structure[^structure] that can be easily manipulated.

Formula Calculation

1.2% of wine 1 +2.7% of wine 2 + etc is what we have for now.
Convert the percentages of the input formula into decimal to determine proportions; then use the proportions to create a vector of wine blend.

Tank Allocation

Determine the minimum number of tanks needed to hold the wine blends.
Allocate the wines to the tanks taking into account the capacity of each tanks and the number of steps needed to produce the final product, while making sure that all the tanks are either full or empty.

Blending

Using the proportions determined in Formula Calculation start the blending process and monitor it using sensors to verify the quality of the wine.

Testing and Adjusting

Using multiple quality control measures, test and evaluates the final product. Adjust the formula if necessary.

Optimization

Optimize the algorithm to minimize the number of steps needed to produce the final product, taking into account the need for precision and consistency(dynamic programming[^programming] or genitic[^genetic] algorythms could be interesting lead).

---

## 5. Non-Functional Requirement

### 5.1 Security

Krug being an important group, security is, de facto extremely important for them. We are assuming that they already have some network security policy[^policy] and so adding another security layer would be excessive.

---

### 5.2 Availability

The algorythm is to be present on a computer with a password, known by a few employees to complement the security policy.

---

### 5.3 Scalability

The algorythm is expected to handle formulas with a finite amount of wines (i-e 4 types of wines/grapes).

---

## Glossary

[^algorythm]: Refers to a sequence of actions performed on data;
[^blending]: The still wines from different vineyards and grape varieties are blended together to create a consistent flavor profile;
[^crash]: A carsh is a abnormal interuption of the software, due to a failure, an incident or a bug;
[^os]: OS or Operating System is a set of programs that directs the use of a computer's ressources;
[^base]:  A user base refers to the number of people who use a particular product or service, especially one available on the internet
[^powershell]: PowerShell is a task automation and configuration management program from Microsoft, consisting of a command-line shell and the associated scripting language
[^database]: Database refers to a structured set of data held in a computer, especially one that is accessible in various ways;
[^structure]: Data structure are a specialized format for organizing, processing, retrieving and storing data;
[^programming]: Dynamic programming is a computer programming technique where an algorithmic problem is broken down into sub-problems;
[^genetic]: Genetic programing is a method for solving optimization problems that is based on natural selection;
[^policy]: A network security policy delineates guidelines for computer network access, determines policy enforcement, and lays out the architecture of the organization's network security environment;

---
