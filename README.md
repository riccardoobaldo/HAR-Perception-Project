# Human Activity Recognition (HAR): A Biological & Gestalt Approach 

**Corso:** Principi e Modelli della Percezione - Prof. [Nome Professore]
**Anno Accademico:** 2025/2026

## 👥 Team Members
* **Riccardo Baldo** - 33036A
* **Matteo Airoldi** - 44928A

---

## 📄 Project Overview
Questo progetto esplora il riconoscimento delle attività umane (HAR) utilizzando i dati dei sensori inerziali di uno smartphone (UCI HAR Dataset).
L'obiettivo non è solo ottenere un'alta accuratezza numerica, ma indagare come la macchina percepisce il movimento e se esistono paralleli con la percezione biologica umana.

### 🎯 Key Goals
1.  **Analisi Biomimetica:** Confronto tra l'elaborazione dei sensori (accelerometro/giroscopio) e il **sistema vestibolare umano**.
2.  **Analisi Gestaltica:** Visualizzazione della struttura dei dati (t-SNE) per cercare principi di organizzazione percettiva (Prossimità, Similarità).
3.  **Classificazione:** Implementazione di una **Random Forest** (Ensemble Learning) per classificare 6 attività (Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying).

---

## 📊 Methodology & Insights

### 1. Visualizzazione dei Dati (t-SNE)
Abbiamo proiettato lo spazio a 561 dimensioni su un piano 2D.
* **Risultato:** I dati si organizzano spontaneamente in cluster definiti, rispettando il **Principio di Prossimità** della Gestalt.
* **Osservazione:** Emerge una netta separazione tra "Mondo Dinamico" (camminate) e "Mondo Statico" (posture), dimostrando una coerenza interna dei dati senza supervisione.

### 2. Il Ruolo della Gravità (Feature Importance)
Interrogando la Random Forest, abbiamo scoperto che le feature più importanti sono legate alla gravità (`tGravityAcc`).
* **Analisi:** L'IA distingue "Laying" (Sdraiato) dalle altre posture misurando l'orientamento rispetto al vettore gravitazionale.
* **Conclusione:** Questo conferma l'analogia con gli **otoliti** dell'orecchio interno umano, che usano la gravità come riferimento spaziale.

### 3. Performance del Modello
* **Accuratezza Globale:** **97.89%** (Test Set).
* **Laying:** 100% Precision (0 errori).
* **Limitazioni:** Lieve ambiguità percettiva tra *Sitting* e *Standing* dovuta alla posizione del sensore (in vita), che rende l'inclinazione del busto identica nelle due posture.

---

## 📂 Repository Structure

* `data/`: Link al dataset originale UCI HAR.
* `notebooks/`: Jupyter Notebook contenente l'intero flusso di lavoro (Preprocessing, t-SNE, Random Forest Training, Evaluation).
* `presentation/`: Slide del progetto presentate all'esame.
* `images/`: Grafici generati (Confusion Matrix, Feature Importance, t-SNE).

## 🚀 How to Run
Il progetto è sviluppato in Python. Le librerie principali sono: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`.

1.  Clona il repository.
2.  Apri il notebook `Progetto_HAR.ipynb`.
3.  Esegui le celle per riprodurre l'analisi e l'addestramento.

---
*Progetto realizzato per l'esame di Principi e Modelli della Percezione, Università degli Studi di Milano.*
