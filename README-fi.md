# 🇬🇧 [English](README.md) | 🇫🇮 [Suomi](README-fi.md)

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Qiskit](https://img.shields.io/badge/Qiskit-1.0-purple)
![License](https://img.shields.io/badge/License-AGPLv3-green)
![Build](https://img.shields.io/badge/Status-Working-success)

# 🧠 Kvanttikokeet – Bellin tila & VQE-simulaatio (tekoälyavusteinen)

Tämä projekti on **opetuksellinen kvanttilaskennan demonstraatio**, joka hyödyntää  
**Qiskit-kirjastoa** ja **VS Code Jupyter** -ympäristöä.  
Kokonaisuus rakennettiin ja viimeisteltiin **OpenAI Codex** -integraation avulla.

---

## 🎯 Tavoite

Käytännönläheinen johdatus kvanttilaskentaan ja sen keskeisiin periaatteisiin:  
- miten **kvanttibittejä (qubitteja)** luodaan ja kytketään toisiinsa  
- miten **entanglement (lomittuminen)** toimii  
- ja miten **VQE (Variational Quantum Eigensolver)** löytää järjestelmän pienimmän energiatilan.

---

## 🚀 Sisältö (6 harjoitetta)

1. **Bellin tilan luonti ja Bloch-visualisointi**  
   Luodaan |Φ⁺⟩ = (|00⟩ + |11⟩)/√2 ja visualisoidaan qubitit Bloch-palloina.

2. **Bell-piirin visualisointi**  
   Piirretään H + CNOT -porttipiiri Matplotlibin avulla.

3. **VQE-optimoija – energian minimointi**  
   Ratkaistaan Hamiltoninoni **H = ZI + IZ** variatiivisesti.  
   Tulostetaan pienin energia (~−2.0) ja optimoidut parametrit, sekä näytetään lopullinen piiri.

4. **Bell-tilan mittaus ja korrelaation todentaminen**  
   Suoritetaan 2000 mittausta. Histogrammi näyttää vain **00** ja **11**, mikä osoittaa täydellisen lomittumisen.  
   Lisäksi lasketaan odotusarvo ⟨Z⊗Z⟩ ≈ 1.0.

5. **VQE-energian maisema (lämpökartta)**  
   2D-lämpökartta näyttää energian vaihtelun (θ, φ) -tasossa. Minimit erottuvat selvästi.

6. **Kohinan ja decoherenssin vaikutus**  
   Lisätään **depolarisoiva kohina (p=0.05)** ja verrataan histogrammeja:  
   puhdas vs. meluinen Bell.  
   Havainnollistaa, miten kohina hajottaa kvanttilomittumisen.

Kaikki harjoitteet löytyvät tiedostosta:  
`exercises/vqe_demo/quantum_demo.ipynb`

---

## 🧩 Miksi nämä harjoitteet ovat tärkeitä

- **Bellin tila**: perustaa kvanttisalaus, kvanttitietoliikenne ja teleportaatio.  
- **VQE**: tärkein hybridi-algoritmi nykyisille NISQ-laitteille (kemia, optimointi).  
- **Kohina**: muistuttaa todellisuudesta – mikään kvanttiprosessori ei ole virheetön.

---

## 📦 Tarvittavat kirjastot

```txt
qiskit
qiskit-aer
numpy
matplotlib
pylatexenc
```

> Asennus: `pip install -r requirements.txt`

Jos Matplotlib-piirto antaa virheilmoituksen LaTeXista, varmista että `pylatexenc` on asennettu.

---

## ▶️ Ajo-ohjeet

1. Avaa VS Code projektin juureen.  
2. Valitse Python 3.11+ virtuaaliympäristö (`.venv`).  
3. Avaa notebook:  
   `exercises/vqe_demo/quantum_demo.ipynb`  
4. Suorita kaikki solut (Run All).

Näet tuloksina:
- Bloch-pallot (Bell)
- Piirikaaviot (Bell & optimoitu VQE)
- Histogrammit (puhdas & meluinen Bell)
- VQE-energian tulostuksen ja lämpökartan

---

## 📁 Projektirakenne

```
quantum-experiments/
├─ exercises/
│  └─ vqe_demo/
│     └─ quantum_demo.ipynb     # Kaikki 6 harjoitetta samassa notebookissa
├─ requirements.txt
├─ .gitignore
├─ README.md                    # Englanninkielinen versio
└─ README-fi.md                 # Tämä suomenkielinen versio
```

---

## 🧠 Havainnolliset tulokset

- **Bell-histogrammi:** vain `00` ja `11`  
- **VQE:** minimi-energia ≈ -2.0 ja optimoitu piiri (kaksi RY + CNOT)  
- **Lämpökartta:** energian vaihtelut H = ZI + IZ  
- **Kohinademo:** melun vaikutus lomittumisen hajoamiseen

---

## 🔐 Huomioita ja toistettavuus

- Pidä riippuvuudet kiinnitettyinä (`requirements.txt`).  
- Käytä satunnaissiementä deterministiseen ajamiseen.  
- Dokumentoi kohinaparametrit, jos simuloit virheitä tai hyökkäyksiä.

---

## 🧠 Kvanttikokeiden visualisoinnit

| ![Bloch pallot](images/bloch_spheres.png) | ![Optimoitu piiri](images/optimized_circuit.png) |
|:--:|:--:|
| *Qubittien Bloch-pallojen visualisointi* | *VQE-simulaation optimoitu piiri* |

| ![Energiamaisema](images/energy_landscape.png) | ![Kohinasimulaatio](images/noise_simulation.png) |
|:--:|:--:|
| *Hamiltonin H = ZI + IZ energiamaisema* | *Kohinasimulaation vertailu (p = 0.05)* |

<p align="center"><em>Kuvat on tuotettu todellisista Qiskit-simulaatioista, suoritetuista VS Code + OpenAI Codex -ympäristössä.</em></p>

---

## ✍️ Tekijä ja tekoälyavusteisuus

Projektin rakensi ja viimeisteli **Teppo ("RebelCoding84")**.  
Koodi ja dokumentaatio luotiin yhteistyössä **VS Code Codex + ChatGPT** -agenttien kanssa.

> “Tämä harjoituskokonaisuus syntyi osana kvanttilaskennan ja kyberturvallisuuden itseopiskelua.”
