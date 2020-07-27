# APT-DIFT-HSL-algorithm
Dynamic Information Flow Tracking (DIFT) is a defense mechanism that dynamically track the usage of information flows in a computer system during program executions. Advanced Persistent Threats (APTs) are sophisticated, stealthy, long-term cyberattacks that target specific systems. Although DIFT has been used for detecting APTs, wide range security analysis using DIFT results in a significant increase in performance overhead and high rates of false-positives and false-negatives. This code presents a game-theoretic implementation of the strategic interaction between APT and DIFT. The APT-DIFT game is a constant-sum stochastic game with total reward structure and imperfect information structure. We consider two scenarios of the game (i) when the false-positive and false-negative rates are known to both players and (ii) when the false-positive and false-negative rates are unknown to both players. Case (i) translates to a game with complete information and case (ii) translates to an incomplete information game with unknown transition probabilities. For case (i), we implement a value iteration algorithm with guaranteed convergence. For case (ii), we implement Hierarchical Supervised Learning (HSL), a supervised learning-based algorithm. 
The code presents the implementation of the value iteration algorithm and the HSL algorithm. The HSL algorithm integrates a neural network, to predict the value vector of the game, with a policy iteration algorithm to compute an approximate equilibrium. The HSL algorithm utilizes the hierarchical structure of the state space of the APT-DIFT game to compute an approximate equilibrium of the game. The code used a sequential neural network   with two hidden layer each of 1000 neurons and a maximum absolute error loss function. The neural network approximated the value vector with an accuracy of more than 95%. The experiments in this code used nation state and ransomware attack datasets collected using Refinable Attack INvestigation (RAIN) framework. For more details about algorithms and results see [1].

[1] Shana Moothedath, Dinuka Sahabandu, Joey Allen, Linda Bushnell, Wenke Lee, and Radha Poovendran, “Stochastic Dynamic Information Flow Tracking Game using Supervised Learning for Detecting Advanced Persistent Threats”. Link: https://arxiv.org/pdf/2007.12327.pdf

[2] Ji, Yang, Sangho Lee, Mattia Fazzini, Joey Allen, Evan Downing, Taesoo Kim, Alessandro Orso, and Wenke Lee. "Enabling refinable cross-host attack investigation with efficient data flow tagging and tracking." In 27th USENIX Security Symposium (USENIX Security 18), pp. 1705-1722. 2018.
