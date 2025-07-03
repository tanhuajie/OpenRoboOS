<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/logo2.png" width="200"/>
</div>

# 🤖 RoboOS
RoboOS: A Hierarchical Embodied Framework for Cross-Embodiment and Multi-Agent Collaboration.
***We provide a real-world demo video in ./demo.mp4***

<section class="section">
    <div align="center", class="container is-max-desktop">
        <div class="columns is-centered has-text-centered">
            <h2 class="title is-3"></h2>
            <video id="put_grapes" autoplay controls muted loop playsinline width="900">
                <source src="https://anonymous.4open.science/r/OpenRoboOS-4355/demo.mp4"
                        type="video/mp4">
            </video>
        </div>    
    </div>
</section>
<!-- ***We provide a real-world demo video in [demo.mp4](https://anonymous.4open.science/r/OpenRoboOS-4355/demo.mp4)*** -->


## 🔥 Overview
The rise of embodied intelligence has intensified the need for robust multi-agent collaboration in industrial automation, service robotics, and smart manufacturing. However, current robotic systems struggle with critical limitations, including poor cross-embodiment adaptability, inefficient task scheduling, and inadequate dynamic error correction. While end-to-end vision-language-action (VLA) models (e.g., OpenVLA, RDT, Pi-0) exhibit weak long-horizon planning and task generalization, hierarchical VLA models (e.g., Helix, Gemini-Robotics, GR00T-N1) lack cross-embodiment compatibility and multi-agent coordination capabilities.
To address these challenges, we present **RoboOS**, the first open-source embodied operating system based on a *Brain-Cerebellum* hierarchical architecture, facilitating a paradigm shift from single-agent to swarm intelligence. Specifically, RoboOS comprises three key components: **(1) the Embodied Cloud Model**, a multimodal large language model (MLLM) for global perception and high-level decision-making;  **(2) the Cerebellum Skill Library**, a modular, plug-and-play toolkit for seamless multi-skill execution; and  **(3) Real-Time Shared Memory**, a spatiotemporal synchronization mechanism for multi-agent state coordination. By integrating hierarchical information flow, RoboOS bridges the Embodied Brain and Cerebellum Skill Library, enabling robust planning, scheduling, and error correction for long-horizon tasks while ensuring efficient multi-agent collaboration by Real-Time Shared Memory. Moreover, we optimize edge-cloud communication and cloud-based distributed inference to support high-frequency interactions and scalable deployment.
Extensive real-world experiments across diverse scenarios (e.g., restaurant, household, supermarket) demonstrate RoboOS’s versatility, supporting heterogeneous embodiments (single-arm, dual-arm, humanoid, wheeled), which provides a scalable and practical solution for cross-embodiment collaboration, pushing the boundaries of embodied intelligence.

## ✨ Framework for RoboOS 1.0
<div align="center">
<figure>
    <img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/overview.png", width="900" />
    <figcaption>
        <strong>Framework of RoboOS 1.0.</strong> RoboOS is a Brain-Cerebellum hierarchical architecture for multi-robot collaboration that comprises three core components: 
        (a) Cloud-based Embodied Brain model for high-level cognition and multi-agent coordination; 
        (b) Distributed Cerebellum Modules for executing robot-specific skills; 
        and (c) Real-Time Shared Memory for enhanced environmental awareness.
    </figcaption>
</figure>
</div>

## ✨ Framework for RoboOS 2.0 (SaaS + MCP)
<div align="center">
<figure>
    <img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/overview2.png", width="600" />
    <figcaption>
        <strong>Framework of RoboOS 2.0 (SaaS + MCP).</strong> RoboOS is a Brain-Cerebellum hierarchical architecture for multi-robot collaboration that comprises three core components: 
        (a) Cloud-based Embodied Brain model for high-level cognition and multi-agent coordination; 
        (b) Distributed Cerebellum Modules for executing robot-specific skills; 
        and (c) Real-Time Shared Memory for enhanced environmental awareness.
    </figcaption>
</figure>
</div>

## 🚀 Pipeline of RoboOS
<div align="center">
<figure>
    <img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/pipeline.png" alt="teaser" width="900" />
    <figcaption>
        <strong>Pipeline of RoboOS.</strong> The RoboOS framework implements a workflow pipeline for multi-robot collaboration, consisting of four key phases: (1) hierarchical task decomposition, 
            (2) topology-aware subtask allocation, (3) distributed agent-based execution, and (4) dynamic memory updating. 
            This integrated workflow enables coordinated task completion while maintaining adaptability to environmental and operational constraints.
    </figcaption>
</figure>
</div>

## 🤖 Real-world RoboOS Demonstrations
<div align="center">
<figure>
    <img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/scene_demos.png" alt="teaser" width="900" />
    <figcaption>
        <strong>Real-world RoboOS Demonstrations.</strong> We showcase multi-robot collaboration in three scenarios: 
        (a) Restaurant: Unitree G1 and Agilex robots prepare burgers. (b) Household: Realman and Agilex robots fetch items. (c) Supermarket: Robots coordinate gift selection and packaging.
    </figcaption>
</figure>
</div>

## ⭐️ Simple Guide Manual

***We provide a simple usage guidance video in ./manual.mp4***

<section class="section">
    <div align="center", class="container is-max-desktop">
        <div class="columns is-centered has-text-centered">
            <h2 class="title is-3"></h2>
            <video id="put_grapes" autoplay controls muted loop playsinline width="900">
                <source src="https://anonymous.4open.science/r/OpenRoboOS-4355/manual.mp4"
                        type="video/mp4">
            </video>
        </div>    
    </div>
</section>

### Step 1. Prerequisites

- Python 3.8+
- Redis server
- pip package manager

### Step 2. Installation

```bash
# Clone the repository (we replace username with xxx temporarily, due to double-blind policy)
git clone https://github.com/xxx/RoboOS.git
cd RoboOS

# Install dependencies
pip install -r requirements.txt

```

### Step 3. Quick Start
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

## ✨ Example for Interative UI

### ⭐️ Master & Slaver Console (RoboOS 2.0)
<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/master_example_2.png" , width="800"/>
</div>

### 🔍 Master Console (RoboOS 1.0)

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/master_example_0.png" , width="800"/>
</div>

<div align="center">
<img src="https://anonymous.4open.science/r/OpenRoboOS-4355/assets/master_example_1.png" , width="800"/>
</div>

### 🤖 Slaver Console (RoboOS 1.0)

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
