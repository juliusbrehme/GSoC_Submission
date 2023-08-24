---
layout: page
title:  "Google Summer of Code 2023 Final Submission"
date:   2023-08-24 13:50:57 +0900
categories: jekyll update
---
## Introduction 
- Organisation Name: [Software and Computaional Systems Lab, LMU Munich, Germany](https://www.sosy-lab.org/)
- Project Idea: [JavaSMT](https://github.com/sosy-lab/java-smt) - Integrating the SMT solver [dReal](http://dreal.github.io/) to the framework JavaSMT
- Mentor Daniel Baier
- Student: Julius Brehme
- Project Proposal: Link?

## Description
### Introduction to [JavaSMT](https://github.com/sosy-lab/java-smt)
SMT solvers are widely utilized in computer-guided verification of computer programs and artificial intelligence. With a multitude of theories employed in these solvers, it is beneficial to have access to a diverse range of solvers and to minimize the challenge of learning a new API for each of them. Using the solver's own API directly makes it difficult to switch to another solver without rewriting extensive parts of the application, as there is no standardized binary API for SMT solvers.
JavaSMT has exactly these attributes, a common API for SMT solvers. The framework provides access to a variety of solvers created using Java and other programming languages. Although most solvers share a common set of supported theories and features, their availability of extra theories and performance may differ.

### Project Description
The goal of the project was to integrate anotehr SMT solver, [dReal](http://dreal.github.io/), into the JavaSMT framework. The SMT solver dReal is a solver that solves nonlinear formulas over the reals. The solver can handle various nonlinear real functions such as polyynomials, trigonometric functions, exponentioal functions, etc. 

## Project Goals
The project has been completed within the duration of GSoC and is ready to be integrated into the `master` branch of [JavaSMT](https://github.com/sosy-lab/java-smt).
- Milestone 1: The SMT solver [dReal](http://dreal.github.io/) is written in C++ and the first part was to create an interface, so that the solver can be accesed via Java code. Therefore, an Java Native Interface (JNI) was used, which allows to use different programming languages in C++. The JNI-Wrapper was mostly created with the programm [SWIG](https://www.swig.org/).
- Milestone 2: Testing the native methods and resolving issues
- Milestone 3: Integrating dReal into the JavaSMT framework. The SolverContext interface was expanded and the interfaces for the different function in JavaSMT needed to be conntected with the functions of the new SMT solver.
- Milestone 4: Unit testing the integration of dReal and adjust the test environment for not supported functions

## Code Contribution
I worked on the branch `313-adding-dreal-to-javasmt`. A pull reqeust was made to integrate the dReal solver to JavaSMT.
- Project Repository: https://github.com/sosy-lab/java-smt
- Pull request: https://github.com/sosy-lab/java-smt/pull/328

## Future Improvements
dReal does not support the usage of uninterpreted functions. If in the future dReal does support uninterpreted functions, the functionality of uninterpreted functions should also be integrated to JavaSMT, as it is quite a useful and important feature.   
In dReal it is possible to use trigonometric functions, exponentioal functions etc., but JavaSMT does not support those functions. If in the feature JavaSMT does support the usage of those functions, this can be integrated as well for dReal.

## Final Words
As my Google Summer of Code journey comes to a close, I wanted to take a moment to express my gratitude for this incredible experience. These past few months have been amazing experience and I am grateful for the opportunity to have been a part of the Software and Computaional Systems Lab. 
Reflecting on the past few months, I am amazed at how much I have learned. 
When I first embarked on this journey, the thought of immersing myself in a vast codebase was both thrilling and daunting. However, under Daniel's guidance and support, I found myself gaining profound insights into the art of reading, understanding, and working with extensive codebases.
I discovered the significance of comprehensive documentation, version control practices, and code commenting.
And lastly I acquired valuable skills in effectively immersing myself in new topics.
Lastly, I want to extend my gratitude to my mentor Daniel for your incredible guidance and support throughout this journey. Your dedication and expertise have been truly invaluable to me.

