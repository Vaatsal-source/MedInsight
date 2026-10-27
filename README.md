```markdown
# CareSathi: AI-Powered Rural Healthcare Suite

CareSathi is an AI-powered healthcare platform designed to support frontline medical workers in rural and low-resource settings. It combines local AI models for triage, voice-assisted data entry, visual diagnostics, and inventory tracking into a single offline-friendly system.

This project is built for healthcare workers who need fast clinical decision support, even with limited internet access and minimal infrastructure.

## Why This Project?

Rural healthcare facilities often face:
- limited connectivity
- shortage of trained specialists
- delayed patient referrals
- inefficient manual record keeping
- poor inventory visibility for essential medicines

CareSathi helps bridge these gaps by giving workers an intelligent, multilingual, and offline-capable assistant for everyday clinical workflows.

---

## Key Features

- Smart Triage Assistant  
  Analyzes patient symptoms and vitals such as temperature, SpO2, and blood pressure using a local LLM.

- Voice-to-Text Integration  
  Supports hands-free data entry using multilingual speech recognition for offline use.

- AI Visual Diagnostics  
  Performs automated analysis for chest X-rays and skin lesion images using computer vision techniques.

- Live Inventory Manager  
  Tracks and updates medical stock such as paracetamol, ORS, and antibiotics in real time.

- Multilingual Support  
  Supports English, Hindi, Odia, and Urdu.

- Referral Generation  
  Generates patient referral documents as PDF files for transfer to higher-level care centers.

---

## Technical Architecture

### Frontend
- HTML5
- CSS3
- JavaScript (Vanilla)
- Responsive UI with localized text rendering
- jsPDF for generating medical reports

### Backend
- Python Flask
- Flask-CORS
- Local JSON-based storage
- Browser LocalStorage for patient queue/session persistence

### AI & Processing Components
- LLM: TinyLlama 1.1B (GGUF format) via llama-cpp-python
- Speech Recognition: Vosk (offline Hindi speech model)
- Computer Vision: OpenCV and NumPy
- Local model-based inference for offline operation

---

## Installation & Setup

### Prerequisites
- Python 3.8+
- Modern browser (Chrome or Edge recommended for voice API support)
- Sufficient local system resources to run AI models

### 1. Clone the Repository
```bash
git clone https://github.com/Vaatsal-source/MedInsight.git
cd MedInsight
```

### 2. Install Python Dependencies
```bash
pip install flask flask-cors llama-cpp-python vosk numpy opencv-python
```

### 3. Add Required AI Models
Create a `models/` directory in the project root and place the following files:

- `tinyllama-1.1b-chat-v1.0.Q4_K_M.gguf`
- `vosk-model-small-hi-0.22/`

Example structure:
```text
models/
├── tinyllama-1.1b-chat-v1.0.Q4_K_M.gguf
└── vosk-model-small-hi-0.22/
```

### 4. Run the Backend Server
```bash
python server.py
```

The server is expected to run at:
```text
http://127.0.0.1:5005
```

### 5. Open the Frontend
Open `index.html` in a browser to access the CareSathi dashboard and patient workflow.

---

## Project Structure

```text
MedInsight/
├── index.html              # Main dashboard and patient queue
├── triage.html             # Symptom and vital analysis
├── analysis.html           # X-ray and skin scan processing
├── inventory.html          # Stock management interface
├── server.py               # Flask API and AI model integration
├── inventory.json          # Local stock database
├── models/                 # Local AI model files
├── README.md               # Project documentation
└── assets/                 # Optional frontend resources
```

---

## Typical Workflow

1. Capture patient details and symptoms
2. Enter vital signs such as temperature, BP, and SpO2
3. Use voice input for hands-free data entry
4. Receive AI-assisted triage suggestions
5. Review visual analysis for X-ray or skin lesion scans
6. Update medicine inventory status
7. Generate referral documents in PDF format

---

## Use Cases

- Community health centers
- Rural clinics
- Mobile health outreach programs
- Nurse-led primary care units
- Frontline healthcare facilities with limited digital infrastructure

---

## Limitations

CareSathi is a decision-support tool intended to assist trained healthcare personnel. It does not replace clinical expertise, licensed medical judgment, or formal diagnosis by a qualified doctor.

The system is best used as an aid for:
- preliminary triage
- workflow support
- patient referral preparation
- stock tracking
- documentation support

It should not be used as the sole basis for diagnosis or treatment decisions.

---

## Safety Disclaimer

This project is designed as a diagnostic support aid for healthcare workers and clinicians. Final medical decisions must always be made by qualified medical officers or licensed physicians. The product should be used responsibly and ethically, with human oversight in all clinical decisions.

---

## Contributing

Contributions are welcome. You can help by:
- improving the user interface
- adding multilingual enhancements
- improving model performance
- refining clinical workflows
- enhancing offline reliability
- documenting technical usage and deployment steps

If you’d like to contribute:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Open a pull request with a clear description

---

## License

This project currently does not specify a license.  
Please add a license file such as MIT, Apache 2.0, or GPL if you intend to publish it publicly.

Example:
```text
MIT
```

---

## Roadmap

Planned improvements include:
- stronger multilingual speech recognition
- better diagnostic confidence scoring
- expanded image analysis models
- improved patient record export
- more robust inventory analytics
- offline patient referral workflows
- enhanced UI accessibility and localization

---

## Contact

For questions, collaboration, or project updates, please contact the repository owner or maintainers through the GitHub project page.

---

## Summary

CareSathi aims to make frontline healthcare more efficient, more structured, and more accessible in low-resource environments by combining local AI, multilingual voice support, clinician-focused workflows, and offline-first design.
```
