# ✈️ OptSuite Crew Pairing Module

This repository provides an extension of the **OptSuite** quantum optimization framework presented in:

> *arXiv:2504.11899*

to model and experimentally evaluate **Airline Crew Pairing problems** using hybrid quantum-classical variational algorithms such as the **Quantum Approximate Optimization Algorithm (QAOA)**.

The project adapts the operator-centric optimization workflow implemented in OptSuite to support airline scheduling use cases through the construction of a **Quadratic Unconstrained Binary Optimization (QUBO)** formulation of the Crew Pairing problem.

---

## 🎯 Purpose

The objective of this repository is to:

- Encode Crew Pairing as a binary set-partitioning model  
- Transform flight coverage and legality constraints into penalty-based QUBO terms  
- Automatically map the resulting cost function into Pauli-Z operator blocks using the OptSuite Hamiltonian construction pipeline  
- Enable execution of QAOA-based hybrid optimization workflows on simulators or quantum hardware backends  
- Provide simplified ("toy-model") airline optimization instances for benchmarking and scalability analysis of variational quantum optimization algorithms  

This implementation serves as a domain-specific extension layer on top of the backend-agnostic operator construction methodology developed in OptSuite.

---

## 🏗️ Framework Integration

The workflow implemented in this repository follows:
Crew Pairing Model
↓
Binary Decision Variables
↓
Constraint Penalty Encoding
↓
QUBO Cost Function
↓
Pauli Operator Decomposition
↓
QAOA Circuit Construction
↓
Hybrid Classical–Quantum Optimization Loop

Crew pairing feasibility requirements such as:

- Flight coverage constraints  
- Duty legality rules  
- Pairing selection consistency  

are incorporated into the objective through quadratic penalty expansions, allowing the resulting Hamiltonian to be directly constructed using commuting operator blocks within the OptSuite framework.

---

## 🔬 Research Scope

This repository is intended for:

- Scalability analysis of QAOA-based optimization methods  
- Evaluation of problem-aware mixer designs  
- Comparison of variational circuit depth vs solution quality  
- Feasibility studies of quantum-assisted airline scheduling  

The implemented models are simplified representations of the operational Crew Pairing problem and are designed to support experimentation with near-term hybrid quantum optimization workflows.

---

## 🔗 Relation to Upstream Repository

This project is maintained as an experimental fork of the original OptSuite framework. It introduces airline-specific optimization models while preserving compatibility with future upstream updates to operator construction, circuit synthesis, and backend execution interfaces.

---

## 📌 Disclaimer

This repository is intended for research and prototyping purposes. The Crew Pairing formulations implemented here represent simplified problem instances and do not constitute production-grade airline scheduling solutions.