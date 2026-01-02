+++
title = 'Generative Lo-Fi Station'
date = 2025-05-10T10:00:00+01:00
draft = false
featured = false
description = "Radio web infinita generata in tempo reale da reti neurali ricorrenti (RNN)."

# Tech Stack & Links
tech_stack = ["Web Audio API", "Magenta.js", "React", "Node.js"]
live_url = "https://tuo-lofi-radio.app"
github_repo_url = "https://github.com/iltuouser/generative-music-web"
featured_image = ""

# S.T.A.R. Method
[star]
  situation = "La maggior parte della musica generativa manca di 'feeling' umano e struttura a lungo termine, risultando ripetitiva o caotica. Volevo creare uno strumento per il deep work che fosse sempre nuovo ma coerente."
  task = "Sviluppare una web app in grado di generare stream audio infiniti in stile Lo-Fi Hip Hop direttamente nel browser, senza dipendere da file MP3 pre-registrati."
  action = "Vorrei utilizzare **Magenta.js** (basato su TensorFlow) pre-addestrando una rete RNN (MusicRNN) su un dataset di progressioni jazz. Vorrei costruire un sintetizzatore personalizzato usando la **Web Audio API** per convertire i dati MIDI generati in suoni caldi e analogici, applicando filtri low-pass e noise injection dinamico."
  result = "La 'stazione' genera tracce uniche infinite. Il carico server è quasi nullo poiché la generazione avviene client-side. Vorrei ottenere ottimo feedback dalla community di sviluppatori per l'uso innovativo dell'Audio Context."
+++

## Architettura Audio

Il core dell'applicazione non usa file audio statici, ma sintetizza tutto in tempo reale.
Il grafo audio include:
1.  **Oscillatori**: Onde sinusoidali e triangolari per i pad.
2.  **ConvolverNode**: Per applicare riverberi a impulsi reali.
3.  **GainNode dinamico**: Per simulare l'effetto "sidechain compression" tipico del Lo-Fi quando colpisce la cassa (kick).