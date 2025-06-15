# Urban-Traffic-Optimization-with-ML
This project aims to develop a smart urban traffic management system that leverages Reinforcement Learning (RL) and YOLO-based vehicle detection to optimize traffic light timings in real-time, reduce congestion, and improve traffic flow.

📌 Project Overview
Simulation Tool: SUMO (Simulation of Urban MObility)

Vehicle Detection: YOLOv8 (Ultralytics)

Machine Learning: Reinforcement Learning (PPO using Stable-Baselines3)

Language: Python

Objective: To minimize waiting time, queue length, and maximize vehicle throughput in an urban grid.

🗺 System Design
Grid: 3x3 SUMO network with traffic signals at key junctions (A1, B0, B1, B2, C1).

Input: Real-time video feed or recorded video (processed using YOLOv8 for vehicle detection).

Control: RL agent adjusts traffic light phases based on live vehicle counts.

🛠 Folder Structure
graphql
Copy
Edit
urban_traffic_optimizer/
├── configs/
│   ├── grid.net.xml         # Network file
│   ├── grid.rou.xml         # Route file
│   └── grid.sumocfg         # SUMO configuration
├── models/
│   └── trained_model.zip    # Saved RL model (after training)
├── videos/
│   └── traffic_input.mp4    # Traffic video for YOLO
├── outputs/
│   ├── yolo_output.csv      # Vehicle counts from YOLO
│   └── simulation_logs/     # SUMO and RL logs
├── traffic_light_rl.py      # RL traffic light controller
├── yolo_detection.py        # YOLOv8 vehicle detection script
├── simulate.py              # Runs SUMO with RL agent
├── visualize.py             # Visualization of traffic and performance
├── requirements.txt         # Required Python packages
└── README.md                # Project documentation
⚙ How to Run
1️⃣ Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
2️⃣ Run YOLO vehicle detection

bash
Copy
Edit
python yolo_detection.py --input videos/traffic_input.mp4 --output outputs/yolo_output.csv
3️⃣ Train RL agent with SUMO

bash
Copy
Edit
python traffic_light_rl.py
4️⃣ Run the simulation

bash
Copy
Edit
python simulate.py
✅ Key Features
Smart traffic light control using reinforcement learning.

Real-time vehicle detection using YOLOv8.

SUMO simulation for realistic traffic scenarios.

Performance metrics: queue length, waiting time, throughput.

💡 Technologies Used
Python 3

SUMO

YOLOv8 (Ultralytics)

Stable-Baselines3 (PPO)

OpenCV

TraCI API

