# ⚛️ Quantum Waveform Analysis with QFT: Harmonic Extraction, Simulation, and Error-Mitigation

This project investigates how the **Quantum Fourier Transform (QFT)** can be used to extract and analyze frequency components of quantum-encoded waveforms. Using Qiskit and real IBM Quantum hardware, several waveform families (sine-like and square-like) are prepared and transformed using QFT. The project explores harmonic structure, noise effects, and the impact of error mitigation on spectral accuracy.

<p align="center"><b>🌀 Waveforms → ⚛️ QFT → 🔍 Frequency Spectrum</b></p>

---

## 🌐 Project Highlights

### ⚛️ Waveform Encoding Through Phase Manipulation
Quantum states are initialized in superposition and modified using selective Z-phase flips.  
Each Z-gate applied to a qubit produces a distinct periodic structure:

- **Z(0)** → Sine-like pattern (period 2)  
- **Z(1), Z(2), Z(3), …** → Square-like patterns with periods 4, 8, 16, …  

These patterns correspond to characteristic peaks in the QFT spectrum.

---

## 🔍 Frequency and Harmonic Structure

### 🧭 Fundamental Harmonics  
The QFT transforms amplitude-encoded patterns into frequency components:

- Sine-like patterns produce a **single dominant peak**  
- Square-like patterns produce:
  - A **fundamental frequency**
  - **Odd harmonics** (3f, 5f, 7f, …)
  - Symmetric distributions in the Fourier domain

This behavior mirrors classical Fourier analysis, highlighting the QFT’s capability as a quantum frequency analyzer.

---

## 💠 Multi-Qubit Experiments

### 🧩 3-Qubit System  
Shows clear sine-wave frequency behavior after QFT.

### 🔷 4-Qubit System  
Includes sine-like and multiple square-like encodings.  
Results display clean harmonic structure in simulation and more noise-affected spectra on hardware.

### 🔶 5-Qubit System  
Reveals richer harmonic patterns and highlights increasing susceptibility to hardware noise as systems scale.

---

## 🛰 Real Hardware vs Simulation

Experiments were executed on several IBM Quantum devices, including:

- **ibm_osaka**  
- **ibm_kyoto**  
- **ibm_brisbane**  
- **ibm_sherbrooke** (127-qubit architecture)

### Observations
- Simulators generate clean, textbook Fourier spectra.  
- Hardware introduces:
  - Peak broadening  
  - Amplitude shifts  
  - Noise-induced harmonics  
  - Device-dependent variation  

Higher-qubit systems yield more complex spectra and increased noise sensitivity.

---

## 🧹 Error-Mitigation Experiments

Error mitigation was applied to evaluate how hardware noise affects QFT outputs.

### ✨ Improvements Observed
- Enhanced dominant peaks  
- Suppressed background noise  
- Better alignment with ideal QFT spectra when the raw pattern is reasonably close

### ⚠️ Limitations
- If noise heavily distorts the distribution, mitigation may amplify incorrect peaks  
- Harmonic ratios may still deviate from theory due to decoherence and readout error  

---

## 🧰 Tools & Frameworks

| Tool | Purpose |
|------|---------|
| **Qiskit** ⚛️ | QFT construction, quantum circuit execution |
| **Qiskit Aer** 🧪 | Statevector and shot-based simulation |
| **IBM Quantum Runtime** 🛰 | Execution on real devices |
| **Matplotlib & NumPy** 📊 | Visualization and waveform construction |
| **Jupyter Notebooks** 📓 | Experiment workflow, analysis, and plotting |

---


```
## 📂 Project Structure
Quantum Fourier Transfrorm/
│── QFT.ipynb # Wave creation and QFT simulations
│── Error mitigation on QFT.ipynb # # Mitigated vs raw spectra
│── README.md # Project documentation

```


---

## 🔦 Key Insights

- QFT effectively extracts frequency and harmonic content from phase-encoded quantum waveforms.  
- Square-wave encodings produce characteristic **odd harmonics**, visible even under hardware noise.  
- Real hardware introduces non-idealities, but primary frequency information remains detectable.  
- Error mitigation enhances spectral clarity when primary harmonics are present.  
- Scaling to larger qubit systems increases both harmonic richness and noise sensitivity.

---

## 🧭 Conclusion

This project demonstrates how classical signal-processing intuition translates into quantum circuits.  
Using QFT, we extract harmonic information from quantum waveforms, compare simulator vs hardware performance, and evaluate how mitigation techniques reshape noisy spectra. The results highlight both the promise and practical challenges of quantum spectral analysis in the NISQ era.

---


