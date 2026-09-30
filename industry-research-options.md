# IEEE TSYP14 IAS Challenge — Industrial Problem Options and Research Resources

## Challenge context

The IEEE TSYP14 IAS Challenge, **“Engineering Industry for a Dynamic Future,”** requires:

- A real or realistic industrial problem
- AS-IS process mapping, including information flows, resources, constraints, and bottlenecks
- Scientific state-of-the-art, standards, patents, and modern industrial practices
- Exploration of 2–3 alternative solutions with comparative analysis
- Solution development and a PoC/MVP
- Technical validation and quantitative impact assessment

The main focus areas are:

- Resilient industrial systems
- Efficient and sustainable industrial systems
- Digitalised industrial systems

This document compares candidate topics before selecting a final problem.

---

## 1. Candidate problems at a glance

| Candidate industrial problem | Scientific literature | Open-source data/code | Standards and frameworks | Industrial case-study potential | Student PoC feasibility |
|---|---:|---:|---:|---:|---:|
| Predictive maintenance for motors, pumps, compressors, or bearings | Very high | High | Very high | High | Very high |
| AI visual inspection and defect detection | Very high | Very high | High | High | Very high |
| Energy optimization of compressed-air systems | Medium–high | Medium | Very high | High | High |
| Energy-aware production scheduling | High | High | High | Medium–high | High |
| Industrial cybersecurity and OT network monitoring | Very high | High | Very high | High | Medium |
| Human–robot collaboration and worker safety | High | Medium | Very high | High | Medium |
| Smart warehouse and autonomous mobile robots | High | High | High | High | High |
| Industrial water-leak detection and resource efficiency | Medium–high | Medium | High | Medium | High |

### Recommended shortlist

1. **Predictive maintenance for critical motors or pumps** — strongest overall balance of technical depth, Industry 4.0 relevance, standards, and measurable impact.
2. **AI visual inspection** — easiest to demonstrate convincingly in a student-level PoC.
3. **Compressed-air energy optimization** — strongest sustainability and energy-efficiency angle.

---

# 2. Detailed candidate topics

## Topic 1 — Predictive maintenance and digital twin for critical motors

### Possible problem statement

> Reduce unplanned downtime and maintenance cost of critical induction motors by combining low-cost sensors, anomaly detection, and a lightweight digital twin.

### Available resources

**Scientific literature:** Very strong availability covering vibration and temperature monitoring, anomaly detection, remaining-useful-life estimation, hybrid physics/AI models, and digital twins.

**Datasets and repositories:**

- [UTK-ASL Dataset Digital Twin Predictive Maintenance](https://github.com/UTK-ASL/Dataset_digital_twin_predictive_maintenance) — motor vibration and temperature data, multiple fault types, and cross-platform validation.
- [Industrial Predictive Maintenance Twin](https://github.com/vicena-labs/industrial-predictive-maintenance-twin) — rotating-equipment baseline using synthetic vibration, temperature, current, speed, and load signals.
- [Digital Twin for Predictive Maintenance using AI and Simulation](https://github.com/VS1245/Digital-Twin-for-Predictive-Maintenance-using-AI-and-Simulation) — combines remaining-useful-life prediction, anomaly detection, and simulation.
- [Predictive-Maintenance-System](https://github.com/Amalmotamed/Predictive-Maintenance-System) — beginner-friendly project using vibration, temperature, current, pressure, RPM, and maintenance-history variables.

**Relevant standards:**

- ISO 55000/55001/55002 for asset-management strategy and lifecycle decisions.
- ISO 22400 for manufacturing KPIs and performance measurement.
- ISA-95/IEC 62264 for integrating sensors, maintenance systems, MES, and ERP.
- IEC 62541/OPC UA for industrial interoperability.
- IEC 62443 for cybersecurity of connected monitoring architectures.

### Student-level MVP

1. ESP32 or Raspberry Pi sensor node.
2. Accelerometer, temperature sensor, and current sensor.
3. MQTT communication.
4. Python anomaly-detection model.
5. Grafana dashboard.
6. Lightweight digital twin showing motor health state.
7. Maintenance recommendation: normal, inspect, or urgent intervention.

### Quantitative impact metrics

- Reduction in unplanned downtime.
- Mean time between failures.
- Mean time to repair.
- False-alarm rate.
- Missed-failure rate.
- Maintenance cost per operating hour.
- Energy consumption before and after intervention.
- OEE availability component.
- Return on investment and payback period.

**Overall assessment:** Probably the strongest all-round topic.

---

## Topic 2 — AI-based visual inspection and defect detection

### Possible problem statement

> Improve quality inspection on a manufacturing line using camera-based anomaly detection that learns normal products and identifies unknown defects.

### Available resources

**Scientific literature:** Extremely strong availability covering convolutional neural networks, autoencoders, PatchCore, PaDiM, vision transformers, few-shot learning, and zero-shot industrial anomaly detection.

**Datasets and repositories:**

- [Intel Visual Quality Inspection](https://github.com/intel/visual-quality-inspection) — industrial visual-inspection reference solution based on anomaly detection and the MVTec AD dataset.
- [Industrial Anomaly Detection](https://github.com/mtaha-ai/industrial-anomaly-detection) — PatchCore and PaDiM implementations with MVTec AD, evaluation metrics, and heatmaps.
- [Open-IAD](https://github.com/M-3LAB/open-iad) — benchmark covering MVTec AD, MVTec 3D, MPDD, BTAD, and other industrial datasets.
- [Anomaly Detection MVTec](https://github.com/slam-wise/anomaly-detection-mvtec) — PatchCore and convolutional-autoencoder baselines.
- [ReMP-AD](https://github.com/cshcma/ReMP-AD) — few-shot industrial visual anomaly detection using multimodal prompt fusion.
- [CVPR VAND Industrial Track](https://github.com/cvpr-vand/vand-2026/blob/main/tracks/industrial/README.md) — benchmark structure for industrial pixel-level anomaly segmentation.

**Relevant standards:**

- ISO 9001 for quality-management processes.
- ISO 22400 for production and quality KPIs.
- ISA-95/IEC 62264 for integrating inspection results with MES and production orders.
- IEC 62443 for connected cameras and inspection systems.
- ISO 12100 if inspection equipment interacts with operators or machinery.

### Student-level MVP

1. Webcam or industrial camera.
2. Controlled lighting.
3. MVTec AD or a locally collected dataset.
4. PatchCore or convolutional autoencoder.
5. Dashboard showing image, anomaly score, defect heatmap, and accept/reject decision.
6. Optional actuator simulation for removing defective products.

### Quantitative impact metrics

- Defect-detection accuracy.
- Precision, recall, and F1-score.
- Image-level AUROC.
- Pixel-level AUROC.
- False-reject rate.
- False-accept rate.
- Inspection time per product.
- Labor hours saved.
- Scrap and rework reduction.
- Cost of poor quality.
- Production throughput.

**Overall assessment:** The easiest topic for a convincing technical demonstration.

---

## Topic 3 — Energy optimization of compressed-air systems

### Possible problem statement

> Detect energy losses and optimize compressor operation by monitoring pressure, flow, temperature, and compressor load.

### Available resources

**Scientific literature:** Good availability on machine learning, model-predictive control, reinforcement learning, leakage detection, and compressor scheduling.

**Data and tools:**

- Public compressed-air datasets are less abundant than predictive-maintenance and computer-vision datasets.
- A realistic PoC can use a digital process model based on pressure, flow, compressor-state, and energy equations.
- Data can be collected from a laboratory compressor or generated using Python.
- Industrial energy-audit methodologies are available from organizations such as the U.S. Department of Energy and Oak Ridge National Laboratory.

**Relevant standards:**

- ISO 50001 for energy-management systems.
- ISO 50002-1 and ISO 50002-3 for energy audits.
- ISO 11011 for compressed-air-system energy assessment.
- ISO 1217 for compressor performance testing.
- ISO 8573 for compressed-air quality.

### Student-level MVP

1. Pressure sensor.
2. Flow sensor.
3. Power meter.
4. Compressor-state data.
5. Controlled leak simulation using valves.
6. Leak-detection model.
7. Optimization algorithm recommending compressor combinations and setpoints.

### Quantitative impact metrics

- kWh per cubic metre of compressed air.
- Pressure stability.
- Compressor loading percentage.
- Leakage rate.
- Energy wasted by leaks.
- Energy cost per production batch.
- CO2-equivalent emissions.
- Peak-demand reduction.
- Compressor operating hours.
- Payback period.

**Overall assessment:** Excellent for the efficient and sustainable industrial-systems focus.

---

## Topic 4 — Energy-aware production scheduling

### Possible problem statement

> Optimize production schedules to reduce energy consumption and carbon emissions while respecting delivery deadlines, machine availability, and production constraints.

### Available resources

**Scientific literature:** Strong availability covering simulation optimization, Industry 4.0 production scheduling, energy-efficient manufacturing scheduling, and multi-objective optimization.

**Open-source software:**

- [Google OR-Tools](https://github.com/google/or-tools) — mature Apache-2.0 optimization suite supporting constraint programming, linear programming, mixed-integer optimization, scheduling, and routing.
- Pyomo, PuLP, SimPy, and DEAP can be combined with OR-Tools.
- Synthetic job-shop datasets are easy to create.

**Relevant standards:**

- ISA-95/IEC 62264 for production-planning and manufacturing-operations integration.
- ISO 22400 for production KPIs.
- ISO 50001 for energy-performance management.
- ISO 14001 for environmental-management objectives and continual improvement.

### Student-level MVP

Compare:

1. First-Come-First-Served scheduling.
2. Genetic-algorithm scheduling.
3. Mixed-integer optimization or OR-Tools CP-SAT.
4. Multi-objective optimization minimizing tardiness, energy cost, setup time, and CO2 emissions.

### Quantitative impact metrics

- Total production time.
- Makespan.
- Average tardiness.
- On-time delivery rate.
- Machine utilization.
- Setup time.
- kWh per product.
- CO2 per production order.
- Electricity cost.
- OEE.
- Schedule-computation time.

**Overall assessment:** Very good for a team with operations-research or industrial-engineering skills.

---

## Topic 5 — Industrial cybersecurity and OT network monitoring

### Possible problem statement

> Detect abnormal communication and cyberattacks in an industrial-control network without disrupting PLC and SCADA operation.

### Available resources

**Scientific literature:** Very strong availability covering intrusion detection, anomaly detection, digital twins, network segmentation, attack classification, and secure-by-design industrial systems.

**Open-source resources:**

- [Zeek](https://github.com/zeek/zeek) for network-security monitoring.
- [Suricata](https://github.com/OISF/suricata) for intrusion detection.
- Wireshark and PyShark for packet analysis.
- [OpenPLC](https://github.com/thiagoralves/OpenPLC_v3) for a legal educational PLC environment.
- Node-RED and MQTT for simulating industrial data flows.
- Public ICS datasets such as SWaT, WADI, and BATADAL.

**Relevant standards:**

- IEC 62443 series for industrial automation and control-system cybersecurity.
- IEC 62443-2-2 for security-protection schemes.
- IEC 62443-3-3 for system-security requirements and security levels.
- ISA-95 for system boundaries and information flows.
- NIST SP 800-82 for industrial-control-system security.
- ISO/IEC 27001 for information-security management.

### Student-level MVP

Use a virtual laboratory rather than a real industrial network:

1. OpenPLC simulated process.
2. MQTT or Modbus communication.
3. Normal traffic generation.
4. Simulated scanning, replay, or abnormal-command events.
5. Network anomaly detector.
6. Risk dashboard based on IEC 62443 zones and conduits.

### Quantitative impact metrics

- Detection rate.
- False-positive rate.
- Detection latency.
- Number of protected assets.
- Mean time to detect.
- Mean time to respond.
- Network overhead.
- Availability impact.
- Security-level improvement.
- Risk-reduction score.

**Overall assessment:** Strong and original, but harder to validate economically.

---

## Topic 6 — Human–robot collaboration and worker safety

### Possible problem statement

> Improve safety and productivity in a collaborative assembly workstation using human-presence detection, risk-aware robot-speed control, and ergonomic monitoring.

### Available resources

**Scientific literature:** Strong and aligned with Industry 5.0, including collaborative robots, worker safety, human-centered design, digital twins, augmented reality, and multimodal human–robot interaction.

**Open-source resources:**

- ROS 2.
- Gazebo or Ignition simulation.
- MoveIt.
- OpenPose or MediaPipe for human-pose estimation.
- YOLO for human detection.
- Webots or CoppeliaSim for robot-cell simulation.
- RoboDK for educational robot-cell modelling.

**Relevant standards:**

- ISO 10218-1 and ISO 10218-2 for industrial-robot safety.
- ISO/TS 15066 for collaborative robot operation.
- ISO 12100 for machinery-risk assessment.
- ISO 13849 for safety-related control systems.
- IEC 61508 for functional safety.
- ISO 45001 for occupational health and safety.
- ISO 22400 for productivity measurements.

### Student-level MVP

1. Robot arm and human workstation simulation.
2. Human-presence detection.
3. Safety zones.
4. Dynamic robot-speed reduction.
5. Operator workload or ergonomic-risk indicator.
6. Productivity comparison between conventional and collaborative operation.

### Quantitative impact metrics

- Worker–robot separation distance.
- Emergency-stop events.
- Near-miss count.
- Reaction time.
- Cycle time.
- Throughput.
- Robot utilization.
- Operator walking distance.
- Ergonomic risk score.
- Worker acceptance score.
- Productivity/safety trade-off.

**Overall assessment:** Excellent for the Industry 5.0 and human-centric dimension, but safety claims must be limited if the PoC is simulated.

---

## Topic 7 — Smart warehouse and autonomous mobile robots

### Possible problem statement

> Optimize warehouse order picking and internal transport using autonomous mobile robots and dynamic task allocation.

### Available resources

**Scientific literature:** Good availability covering autonomous mobile robots, path planning, fleet management, warehouse layout, and human–robot cooperation.

**Open-source resources:**

- ROS 2 Navigation Stack.
- Gazebo/Ignition.
- Open-RMF for multi-robot fleet management.
- OR-Tools for task assignment and routing.
- SimPy for warehouse discrete-event simulation.
- Custom warehouse layouts.

**Relevant standards:**

- ISO 3691-4 for driverless industrial trucks and automated mobile robots.
- ISO 10218 for industrial robots.
- ISO 9001 for logistics quality processes.
- ISA-95 for connecting warehouse-management and manufacturing systems.
- ISO 22400 for operational KPIs.

### Student-level MVP

Compare:

1. Manual picking.
2. Fixed-path AGV.
3. Dynamic AMR routing.
4. Multi-robot task allocation.

### Quantitative impact metrics

- Orders completed per hour.
- Average delivery time.
- Robot utilization.
- Travel distance.
- Battery consumption.
- Congestion.
- Picking errors.
- Labor walking distance.
- Warehouse throughput.
- Investment payback.

**Overall assessment:** Good for a simulation-heavy project, especially for robotics or operations-research teams.

---

## Topic 8 — Industrial water-leak detection and resource efficiency

### Possible problem statement

> Detect and localize water leaks in an industrial utility network using IoT sensors and lightweight machine learning.

### Available resources

**Scientific literature:** Moderate to strong availability covering IoT-based water-leak detection and localization with lightweight deep-learning models.

**Open-source resources:**

- ESP32 or Arduino sensor systems.
- Flow, pressure, and acoustic sensors.
- MQTT and Node-RED.
- InfluxDB and Grafana.
- Python anomaly-detection models.
- EPANET for hydraulic-network simulation.
- Synthetic leak-generation models.

**Relevant standards:**

- ISO 46001 for water-efficiency management systems.
- ISO 14001 for environmental management.
- ISO 50001 if pumping energy is included.
- ISA-95 for utility-data integration.
- ISO 22400 for operational KPIs.

### Student-level MVP

1. Flow and pressure sensors.
2. Simulated pipes and valves.
3. Leak injection.
4. Anomaly detection.
5. Leak-location estimation.
6. Water and energy savings calculation.

### Quantitative impact metrics

- Litres of water saved.
- Leak-detection time.
- Leak-localization error.
- False alarms.
- Pumping-energy reduction.
- CO2-equivalent reduction.
- Maintenance-response time.
- Water-cost reduction.
- Payback period.

**Overall assessment:** A good sustainability project, particularly when connected to cooling, process water, or industrial utilities.

---

# 3. Standards useful across almost all topics

| Standard or framework | Main use |
|---|---|
| ISA-95 / IEC 62264 | Information exchange between enterprise systems, MES, manufacturing operations, and control systems. |
| ISO 22400 | Industry-neutral manufacturing KPI framework covering performance, quality, time, and energy indicators. |
| ISO 55001:2024 | Asset lifecycle, maintenance, risk, cost, and performance management. |
| ISO 50001:2018 | Energy-performance improvement and energy-management projects. |
| ISO 14001 | Environmental objectives, resource efficiency, emissions, and continual improvement. |
| IEC 62443 | Cybersecurity of industrial automation and control systems. |
| OPC UA / IEC 62541 | Secure and interoperable industrial-data exchange. |
| RAMI 4.0 | Structuring Industry 4.0 architecture and asset information. |
| Digital Twin Consortium framework | Digital-twin terminology, architecture, and lifecycle concepts. |
| NIST SP 800-82 | Industrial-control-system cybersecurity methodology. |

---

# 4. Suggested quantitative impact assessment

The final project should establish a baseline and compare it with the proposed solution. Recommended categories include:

## Technical impact

- Accuracy, precision, recall, F1-score, AUROC.
- Detection latency.
- False positives and false negatives.
- System availability.
- Data-processing latency.
- Sensor uptime and data completeness.
- Model inference time.
- OEE, availability, performance, and quality.
- Mean time between failures and mean time to repair.

## Economic impact

- Investment cost.
- Installation and integration cost.
- Operating and maintenance cost.
- Avoided downtime cost.
- Reduced scrap and rework cost.
- Energy-cost savings.
- Labor-hour savings.
- Annual net benefit.
- ROI.
- Payback period.
- Net present value where appropriate.

## Environmental impact

- Electricity saved in kWh.
- Fuel or compressed-air savings.
- CO2-equivalent reduction.
- Water saved.
- Material and scrap reduction.
- Waste-treatment reduction.
- Equipment lifetime extension.

## Resilience impact

- Recovery time after a fault.
- Number of critical failure modes covered.
- Spare-parts availability.
- Dependency on manual intervention.
- Continuity of production during disruptions.
- Cybersecurity risk reduction.

---

# 5. Methodological points of attention

## Phase 1 poster

- Define one concrete industrial context, not only a generic technology.
- Explain the operational pain point using measurable baseline values.
- Include a clear AS-IS process map showing people, machines, data, decisions, and bottlenecks.
- Identify the critical resources and constraints.
- Use a simple problem tree or fishbone diagram.
- State the target KPIs before presenting the solution.
- Make the link to resilience, sustainability, digitalisation, or Industry 5.0 explicit.
- Show why existing manual or conventional practice is insufficient.

## Phase 2 technical report

- Separate the state-of-the-art review from the proposed contribution.
- Compare at least 2–3 alternative solutions using explicit criteria.
- Include technical, economic, environmental, organisational, and cybersecurity criteria.
- Define the system boundary and assumptions.
- Describe the data source, data quality, sampling frequency, and preprocessing.
- Use train/validation/test separation and avoid data leakage.
- Report baseline performance, not just the proposed-model result.
- Include explainability or operator interpretability where AI is used.
- Address cybersecurity, safety, privacy, and failure modes.
- Map the architecture to relevant standards.
- Distinguish clearly between a simulation, laboratory demonstrator, and industrial deployment.
- Include limitations and a credible deployment roadmap.

## Validation recommendations

- Test the system under normal and abnormal operating conditions.
- Use repeated experiments or cross-validation where appropriate.
- Perform sensitivity analysis for thresholds, sensor quality, and workload.
- Evaluate robustness to missing, noisy, delayed, or drifting data.
- Compare the PoC with a simple baseline.
- Report confidence intervals or uncertainty where possible.
- Connect technical results to financial and environmental outcomes.
- Explain how the solution would be maintained after deployment.

---

# 6. Final recommendation

## Best overall choice

### Predictive maintenance for critical motors

Suggested title:

> **A Low-Cost Edge-AI and Digital-Twin System for Predictive Maintenance of Critical Industrial Motors**

This topic offers the best balance of:

- Strong scientific literature.
- Accessible datasets and repositories.
- Sensors and AI.
- Digital-twin architecture.
- Maintenance and resilience.
- Sustainability through energy and equipment-life improvements.
- Standards such as ISO 55001, ISO 22400, ISA-95, OPC UA, and IEC 62443.
- Clear technical, economic, and environmental metrics.

## Best for a reliable visual MVP

### AI visual inspection

Suggested title:

> **Explainable Vision-Based Anomaly Detection for Real-Time Quality Inspection in Smart Manufacturing**

## Best for sustainability

### Compressed-air optimization

Suggested title:

> **IoT-Based Leak Detection and Energy Optimization of Industrial Compressed-Air Systems**

## Best for Industry 5.0

### Human–robot collaboration

Suggested title:

> **Human-Centered Collaborative Robotics with Real-Time Safety and Ergonomic Monitoring**

---

## Note on source verification

The repository links and standards listed here should be checked again before being cited in the final IEEE submission. For the final report, record the exact paper title, authors, publication venue, year, DOI, repository commit or release, and the edition/date of each standard used.
