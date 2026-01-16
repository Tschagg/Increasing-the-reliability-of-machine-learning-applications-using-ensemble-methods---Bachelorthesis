# Increasing-the-reliability-of-machine-learning-applications-using-ensemble-methods---Bachelorthesis
**Note:** The full text of this thesis is written in **German**. This repository provides an English summary and documentation to facilitate international research applications.

## Abstract
As Machine Learning (ML) is increasingly deployed in safety-critical infrastructures—such as medical diagnostics, autonomous driving, and aviation—ensuring the reliability and robustness of these systems is paramount. In medical contexts, for instance, incorrect predictions can have life-threatening consequences, necessitating models that can withstand both natural noise and adversarial interference.

This thesis investigates the effectiveness of Ensemble Methods, specifically Voting and Blending, in enhancing classification performance and robustness without sacrificing accuracy. The research evaluates seven base classifiers (including Support Vector Machines, Neural Networks, and Random Forests) across six diverse classification tasks, incorporating datasets from the MedMNISTv2 suite to reflect real-world medical challenges.

## Methodology & Robustness Testing:
To assess reliability beyond standard metrics, the models were subjected to systematic Fault Injections, including:
- Salt & Pepper Noise and Gaussian Noise to simulate sensor errors.
- Gaussian Blur to simulate focus or motion-related artifacts.
- Adversarial Attacks (using the Fast Gradient Sign Method - FGSM) to evaluate "Adversarial Robustness" against intentional manipulations.

## Key Findings:
- Performance Gain: Ensemble methods improved classification results across all datasets, with Blending (utilizing a Logistic Regression meta-learner) consistently achieving the highest accuracy.
- Enhanced Robustness: The results demonstrate that ensembles are significantly more resilient to input perturbations and noise compared to individual classifiers.
- Limitations: While effective against moderate noise, ensemble methods alone do not provide adequate protection against sophisticated adversarial attacks that compromise multiple base classifiers simultaneously. The study concludes that for maximum safety, these methods should be integrated with specialized techniques such as adversarial training and data denoising

## Repository Highlights
- Implementation: Developed a comprehensive framework for training and evaluating ensemble models using Python.
- Evaluated Models: Logistic Regression, LDA, SGD, SVM, CNNs, Decision Trees, and Random Forests.
- Datasets: MNIST Digits, Fashion MNIST, and MedMNISTv2 (OrganA, OrganC, Breast, Pneumonia).
- Robustness Analysis: Includes custom scripts for noise injection and adversarial example generation using the Adversarial Robustness Toolbox (ART).
