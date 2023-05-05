# Functional Requirement Document

## 1. Introduction

This purpose of this document is to present the different stakeholders with the needs and requirement for the implementation of an algorithm destined to blend differents variety of grapes to create a consistent flavor profile.
This document is intended  to be read by all responsible for the management of the project development initiative including business users, user representatives and sponsors, and other interested parties.

### 1.1 Background

For this project we are working with Krug Champagne and we are tasked with building the software for their new winery, we will focus on the forth part of the “méthode champenoise”: the Blending.
Our goal is to produce the closest result to the formula with the minimum number of steps.

### 1.2 Requirement

    - No crash;
    - No half empty/half full tanks;
    - The product must be as precise as possible;
    - The code is easy to maintain and test;
    - Few steps need to be carried out to get the result;
    - The process needs to be fast;
    - The product can handle different coplexity level of formulas;

There are no specific language for this project.

## 2. Personae

### 2.1 Fred

Fred is part of the team of Julie CAVIL and is responsible of the blending part of the “méthode champenoise”. He is 34 years old, married recently. He likes doing sports and particularly running.

Fred lives in the center of Reims and goes to work with using public transport or a byke.

He will need access to Powershell in order to provide input and output files to the algorythm and he need to access the files for the steps.

### 2.2 Jerry

Jerry is working in the IT department of Krug. He is 26 years old, single. He likes playing video games
and listening to music.

Jerry lives in Muizon and takes his car to go to work.

He will need access to the code of the algorythm in order to update or verify the code and ensure it works.

## 3. Use cases

    - UC1 (Creating a Blend)
        Fred open Powershell
        He enter a command line containing two input file and one output file
        The algorythm return the output file
        He read the output file
        Case closed

    - UC2 (Testing the algorythm)
        Jerry open Powershell
        He enter a command line containing two input file and one output file
        The algorythm return the output file
        He verify the precision of the algorythm by reading the output file
        Case Closed
    
    - UC3 (Maintenance)
        Jerry open the files of the algorythm
        He does his maintenance
        He does a Test to verify the algorythm function
        Case Closed

## 4. Functional Requirement

The code must be able to:

    - allow user to input values representing the percentages of a certain wine;
    - return a result to the user detailling the steps carried out and the final blend;
    - identify tanks via their size, wether or not they are empty and wich wine do they contain (volumes is usually expressed in hectoliters);
    - stop you from leaving a tank half empty;

### 4.1 Assumption

    - The size of the tanks will not be a problem;
    - The units in the formulas are standardized;

### 4.2 Risk

    - We might have trouble balancing simplicity, speed and precision;

## 5. Non-Functional Requirement

### 5.1 Security

Krug being an important group, security is de facto extremly important for them. We are assuming that they already have some network security policy and so adding another security layer would be excessive.

### 5.2 Availability

The algorythm is to be present on a computer with a password, known by a few employes to complement the security policy.

### 5.3 Scalability

The algorythm is expected to handle formulas with a finite amount of wine (i-e 4 types of wines/grapes).
