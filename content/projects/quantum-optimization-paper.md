+++
title = 'Quantum Optimization: QAOA vs Classical Annealing'
date = 2025-08-20T10:00:00+01:00
draft = false
featured = true
description = "Analisi comparativa e simulazione di algoritmi quantistici per problemi di ottimizzazione combinatoria."

# Tech Stack & Links
tech_stack = ["Qiskit", "Python", "NumPy", "LaTeX"]
live_url = "" 
github_repo_url = "https://github.com/iltuouser/quantum-qaoa-research"
featured_image = ""

# S.T.A.R. Method
[star]
  situation = "I problemi di ottimizzazione combinatoria (come il Max-Cut) diventano intrattabili per i computer classici all'aumentare delle variabili. Le attuali soluzioni euristiche spesso si bloccano in minimi locali."
  task = "Valutare se l'algoritmo QAOA (Quantum Approximate Optimization Algorithm) offre un vantaggio quantistico tangibile rispetto al Simulated Annealing classico su hardware NISQ (Noisy Intermediate-Scale Quantum)."
  action = "Ho implementato circuiti quantistici utilizzando il framework **Qiskit** di IBM. Ho modellato il problema Max-Cut su grafi randomici e confrontato la convergenza delle soluzioni eseguendo simulazioni sia su simulatori QASM che su backend quantistici reali (IBM Osaka)."
  result = "Pubblicazione di un paper di ricerca (o tesi). I risultati hanno evidenziato che, sebbene il rumore (noise) limiti l'hardware attuale, QAOA scala meglio in termini di depth del circuito per grafi specifici."
+++

## Dettagli della Ricerca

### Implementazione Qiskit
L'ansatz variazionale è stato costruito con una profondità `p=3`. L'ottimizzazione classica dei parametri $\gamma$ e $\beta$ è stata gestita tramite l'algoritmo COBYLA.

Snippet del circuito di mixing:
```python
# Creazione del mixer Hamiltonian
beta = Parameter('β')
ws_mixer = QuantumCircuit(n_qubits)
for i in range(n_qubits):
    ws_mixer.rx(2 * beta, i)