+++
title = 'Decentralized AI Inference su IPFS'
date = 2025-11-15T10:00:00+01:00
draft = false
featured = true
description = "Architettura per l'esecuzione distribuita di modelli ML usando IPFS per lo storage e Smart Contracts per la validazione."

# Tech Stack & Links
tech_stack = ["IPFS", "Solidity", "TensorFlow.js", "Libp2p"]
live_url = "https://tuo-demo-ipfs.com" # (Esempio)
github_repo_url = "https://github.com/iltuouser/ipfs-ai-inference"
featured_image = "" 

# S.T.A.R. Method
[star]
  situation = "L'inferenza AI centralizzata soffre di due problemi critici: single-point-of-failure e censura dei modelli. I costi di API per modelli LLM stanno inoltre centralizzando il potere computazionale."
  task = "Progettare un'architettura DApp proof-of-concept che permettesse l'hosting decentralizzato dei pesi del modello e l'inferenza verificabile client-side."
  action = "Ho sviluppato un sistema dove i pesi del modello (sharded) sono caricati su IPFS per garantirne l'immutabilità. Ho scritto Smart Contracts in Solidity per gestire un marketplace di potenza computazionale e utilizzato TensorFlow.js per eseguire l'inferenza direttamente nel browser del client (Edge Computing), eliminando la necessità di backend costosi."
  result = "Il prototipo dimostra una riduzione dei costi infrastrutturali del 90% rispetto a soluzioni cloud standard e garantisce la disponibilità del modello anche in caso di downtime dei server centrali."
+++

## Approfondimento Tecnico

### Architettura del Nodo
Il sistema utilizza **Libp2p** per la discovery dei peer. Quando un client richiede un'inferenza:
1.  L'hash del modello viene recuperato dalla blockchain (Ethereum/Polygon testnet).
2.  I chunk del modello vengono scaricati da **IPFS** in parallelo.
3.  L'assemblaggio avviene in un Web Worker per non bloccare il thread principale della UI.

> "La decentralizzazione non è solo politica, è una necessità di resilienza architetturale."