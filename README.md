# README IS A CURRENT WIP. PLEASE CHECK BACK SOON FOR UPDATED INFO!

## What is SofaBrute?
SofaBrute is a tool written in Python which aims to help researchers understand the rotation path of the (conjectured) omptimal sofa as a function of the hallway angle. SofaBrute does this by "brute forcing" (see algorithm section) its way to a (conjectured) optimal sofa, and then saving plots of the sofa in the hallway at various points through its rotation to the local folder. SofaBrute was originally concieved as companion software to a research paper I wrote during the last quarter of my undergraduate degree in Math and Scientific Computation at UC Davis. 

## Table of Contents
- [A Brief History of the Problem](#a-brief-history-of-the-problem)
- [Algorithm](#algorithm)

## A Brief History of the Problem
In 1996, Leo Moser asked the question "what is the shape of largest area in the plane that can be moved around a right-angled corner in a two-dimensional hallway of width 1?" This problem statement became known as the moving sofa problem. A specific construction was given by Joseph Gerver in 1992 which he conjectured to be the solution to Moser's problem. However, Gerver was unable to give proof and to this day his conjecture remains unproven.

## Algorithm
The algorithm aims to solve a reformulated (but equivalent) version of the problem. Since GitHub does not support LaTex markdown, see the below image for the formulation.

<img src="formulation.png">

The algorithm aims to solve this optimization problem by modifying the positions of H_0, ..., H_N one at a time. Starting with H_0, the algorithm will "wiggle" the hallway and see if the wiggle resulted in a larger intersection area. If the wiggle resutls in a decrease or no change at all to the area, the algorithm places H_0 back in its pre-wiggle position and moves to H_1, H_2, etc. Wiggling is always done by pushing H_i parallel to its edges. This method was inspired by Joseph Gerver's "balanced condition" which a solution to the moving sofa problem must satisfy. See theorem 1 of his paper for more information.


