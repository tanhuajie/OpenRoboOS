<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/logo2.png" width="200"/>
</div>

# RoboOS
RoboOS: A Hierarchical Embodied Framework for Cross-Embodiment and Multi-Agent Collaboration.

<div align="center">
<video src="https://anonymous.4open.science/r/OpenRoboOS-4355/demo.mp4" , width="800"/>
</div>

<!-- ***We provide a real-world demo video in [demo.mp4](https://anonymous.4open.science/r/OpenRoboOS-4355/demo.mp4) and a guidance video in [launch.mp4](https://anonymous.4open.science/r/OpenRoboOS-4355/launch.mp4)*** -->


## 🔥 Overview
The rise of embodied intelligence has intensified the need for robust multi-agent collaboration in industrial automation, service robotics, and smart manufacturing. However, current robotic systems struggle with critical limitations, including poor cross-embodiment adaptability, inefficient task scheduling, and inadequate dynamic error correction. While end-to-end vision-language-action (VLA) models (e.g., OpenVLA, RDT, Pi-0) exhibit weak long-horizon planning and task generalization, hierarchical VLA models (e.g., Helix, Gemini-Robotics, GR00T-N1) lack cross-embodiment compatibility and multi-agent coordination capabilities.
To address these challenges, we present **RoboOS**, the first open-source embodied operating system based on a *Brain-Cerebellum* hierarchical architecture, facilitating a paradigm shift from single-agent to swarm intelligence. Specifically, RoboOS comprises three key components: **(1) the Embodied Cloud Model**, a multimodal large language model (MLLM) for global perception and high-level decision-making;  **(2) the Cerebellum Skill Library**, a modular, plug-and-play toolkit for seamless multi-skill execution; and  **(3) Real-Time Shared Memory**, a spatiotemporal synchronization mechanism for multi-agent state coordination. By integrating hierarchical information flow, RoboOS bridges the Embodied Brain and Cerebellum Skill Library, enabling robust planning, scheduling, and error correction for long-horizon tasks while ensuring efficient multi-agent collaboration by Real-Time Shared Memory. Moreover, we optimize edge-cloud communication and cloud-based distributed inference to support high-frequency interactions and scalable deployment.
Extensive real-world experiments across diverse scenarios (e.g., restaurant, household, supermarket) demonstrate RoboOS’s versatility, supporting heterogeneous embodiments (single-arm, dual-arm, humanoid, wheeled), which provides a scalable and practical solution for cross-embodiment collaboration, pushing the boundaries of embodied intelligence.

### Structure for RoboOS 2.0 (SaaS + MCP)
<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/overview2.png", width="800" />
</div>

### Structure for RoboOS 1.0
<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/overview.png", width="800" />
</div>


## <a id="Manual"> ⭐️ Simple Guide Manual</a>

<div align="center">
<video src="https://anonymous.4open.science/r/OpenRoboOS-4355/guidance.mp4" , width="800"/>
</div>

### 1. Prerequisites

- Python 3.8+
- Redis server
- pip package manager

### 2. Installation

```bash
# Clone the repository (we replace username with xxx temporarily, due to double-blind policy)
git clone https://github.com/xxx/RoboOS.git
cd RoboOS

# Install dependencies
pip install -r requirements.txt

```

### 3. Quick Start
```bash
# 1. Start Redis
redis-server

# 2. Start Master
python master/run.py

# 3. Start Slaver (for multi-agent, your should run at different robots respectively)
python slaver/run.py

# 4. Launch Web Interface
python gradio_ui.py

# Then, access the web interface at: http://localhost:7861
```

## ✨ Example Demo

### ⭐️ Master & Slaver Console (Examples for RoboOS 2.0)
<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/master_example_2.png" , width="800"/>
</div>

### 🔍 Master Console (Examples for RoboOS 1.0)

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/master_example_0.png" , width="800"/>
</div>

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/master_example_1.png" , width="800"/>
</div>

### 🤖 Slaver Console (Examples for RoboOS 1.0)

#### Subtask_1 for Realman Single-ARM Robot

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/slaver_subtask_1.png" , width="800"/>
</div>


#### Subtask_2 for Agilex Dual-ARM Robot

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/slaver_subtask_2.png" , width="800"/>
</div>


#### Subtask_3 for Realman Single-ARM Robot

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/slaver_subtask_3.png" , width="800"/>
</div>
