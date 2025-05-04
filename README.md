# Smart Grid Simulator

This project models a modular, physics-informed smart grid system composed of decentralized household agents, each with local power generation, consumption, and battery storage. It simulates energy flows, system balancing, overload responses, and basic market dynamics across a neighborhood-scale power grid.

---

## 🔋 Project Goals

- Simulate real-time power distribution across household agents
- Model storage, transfer, and loss mechanisms within a local grid
- Implement overload handling (e.g. dump nodes / fail-safe agents)
- Capture system behavior under generation/load imbalances
- Provide a framework to test decentralized energy trading and pricing

---

## 🛠️ Key Features

- Household agents with solar generation, demand profiles, and battery systems
- Power balancing across agents and with grid connection
- Resistance-based line loss (Ohmic model)
- Dump load logic to absorb excess power in overload conditions
- Hour-by-hour time loop simulation over multiple days
- Optional pricing/market logic for peer-to-peer energy trades
- Modular structure for extensibility and experimentation

---

## 🧱 Architecture  
  
smart-grid-simulator/  
│  
├── agents/  
│ ├── household.py # Generation, consumption, battery  
│ ├── dumpnode.py # Absorbs overload / excess energy  
│  
├── network/  
│ ├── transmission.py # Power flow and resistive losses  
│  
├── market/  
│ ├── pricing.py # Optional pricing logic and P2P trades  
│  
├── planner/  
│ ├── simulate_day.py # Time-loop simulation and event management  
│  
├── data/  
│ └── sample_inputs/ # Example load/gen profiles  
│  
├── notebooks/  
│ └── demo_run.ipynb # Example use and visualization  
│  
├── README.md  
└── requirements.txt  
  
  
---

## 📈 Sample Use Case

- 10 households with hourly solar and consumption profiles
- Shared local battery capacity or individual storage
- Hour-by-hour simulation for a 7-day period
- Visualization of power flow, battery charge, and overload events
- Optional price signal simulation or peer-to-peer trading activation

---

## 🌱 Future Directions

- Integration of real ISO data (PJM, MISO, CAISO)
- Bayesian modeling of generation uncertainty (weather-based)
- Grid frequency & voltage fluctuation modeling
- Streamlit dashboard or REST API for grid planning
- Quantum-inspired optimization integration (AWS Braket)

---

## 📚 Tools & Technologies

- Python 3.x
- `pandas`, `numpy`, `matplotlib`
- Modular class structure
- Optional: `streamlit`, `plotly`, `boto3` (AWS integration)

---

## 📄 License

MIT License — open for educational and non-commercial adaptation.

---

## ✍️ Author

Developed by Milad Alibabaie, with focus on modeling energy systems & designing infrastructure.
