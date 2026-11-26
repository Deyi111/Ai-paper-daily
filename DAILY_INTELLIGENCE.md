# 🤖 Embodied AI & Robotics Frontier Briefing (2026-11-26)

> *Automated Intelligence Briefing generated via custom ETL scoring pipeline. Prioritizes foundation models, manipulation, locomotion, and physical AI systems.*

---

### Top 1: Cairn: Object-Centric 3D Trajectory Priors for Steering Frozen VLAs
- **Priority Score**: `135 pts` | **Published**: `2026-11-25`
- **Focus Tracks**: `#vision-language-action` `#vla`
- **Key Authors**: Agelos Kratimenos, Kostas Daniilidis, Evangelos Chatzipantazis
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.34914v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.34914v1)

**Executive Abstract**:
> Vision-language-action models (VLAs) are capable low-level controllers, but they tie where objects go to the layouts they were trained on: when objects are moved or obstacles block the way, they carry them to the wrong place or into collisions. Fine-tuning on new layouts needs robot data for each one and erodes skills the model already has. We introduce Cairn, which keeps the VLA frozen and steers it at test time along learned 3D trajectories of the object in its gripper. A small prior reads point clouds of the scene and the held object, along with its pose when grasped and the instruction, and samples SE(3) trajectories up to its release that lead it around obstacles and turn it to fit through gaps. The prior and the VLA form the two levels of a hierarchical planner in which feedback runs both ways: the VLA's intended motion chooses and reshapes the trajectories, and the chosen one guides the VLA's denoising. Its predicted actions, mapped to the held object's poses through the grasp, are pulled toward the next waypoint, while the VLA's weights stay untouched. Across 1,941 held-out LIBERO scenes with displaced objects and obstacles, Cairn raises the success rate of a frozen π0.5 from 24.5% to 95.1%, above that of a π0.5 fine-tuned on our training layouts, without hurting standard LIBERO. On the third-party LIBERO-PRO benchmark, it raises success from 27.3% to 38.0%, and from 54.4% to 81.1% on the episodes it steers. On a real Franka, with a prior trained purely in simulation, it guides the frozen DROID π0.5 around an obstacle and to a placement at the limit of the arm's reach, where it otherwise fails. All code, models and data will be made public.

---

### Top 2: RePace: Reasoning about Demonstration Speedup for Faster Vision-Language-Action Policies
- **Priority Score**: `135 pts` | **Published**: `2026-11-25`
- **Focus Tracks**: `#vision-language-action` `#vla`
- **Key Authors**: Insup Lee, Hojin Jeon, Sunguk Shin et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.34864v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.34864v1)

**Executive Abstract**:
> Since vision-language-action (VLA) policies can inherit the slow pace of human demonstrations, accelerating these demonstrations before fine-tuning can lead to faster VLA policies without an additional speed-selection module at deployment. Several offline speedup methods have focused on identifying segments that require less precision and assigning predefined speedup factors to the segments. However, even within a single segment, a speedup factor suitable for steady motion may be too high when precise alignment is required. To this end, this paper presents RePace, an offline reasoning framework that determines how much to accelerate each part of a demonstration. For the same recorded movement, RePace measures how much each candidate speedup factor shortens the sequence and compares the resulting observation-action pairs used for training. Given the task instruction, a pretrained language model uses the visual context and original motion of successive windows to interpret these candidate retiming effects and select a speedup profile for the complete episode. Experimental results demonstrate that RePace outperforms the baselines in overall task execution efficiency on both LIBERO and RoboCasa-Kitchen. On all three tasks with a gripper-equipped Franka Research 3 arm, RePace matches or exceeds the acceleration baselines in success rate and completes successful trials faster.

---

### Top 3: Toward Agentic Robotics: A Large-Scale Study of Harness Design for Robot-Use Agents
- **Priority Score**: `135 pts` | **Published**: `2026-11-25`
- **Focus Tracks**: `#vision-language-action` `#vla`
- **Key Authors**: Yuxiang Lai, Jike Zhong, Yu-Jhe Li et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.34778v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.34778v1)

**Executive Abstract**:
> Recent vision-language models (VLMs) can act as robot-use agents that understand diverse scenes and control robots through policy code and tools. However, they predict 3D gripper poses poorly even with extended reasoning, struggling with precise manipulation. Vision-language-action (VLA) and world-action (WAM) models are the opposite: they execute fast, smooth control on trained tasks, yet fail under domain shifts or when tasks require long-horizon memory and reasoning. Agentic robots therefore combine VLM reasoning and perception with precise VLA/WAM control through a policy harness. Yet harness design spans thousands of configurations, shifting success by tens of points with the same models. Moreover, testing even one design takes thousands of rollouts at high API and GPU cost, so prior works often commit to a single design chosen from few alternatives. To guide harness design, we evaluate over 470,000 rollouts across eight simulation benchmarks, six VLMs, and 15 VLA/WAM checkpoints. Seven controlled studies show effective harnesses must adapt to both VLM and VLA/WAM capabilities. Our findings specify what structure the VLM's policy code needs, where VLA manipulation needs help from tools and policy code, and when to involve the VLM at test time. The reference recipe X-Harness shows that these findings compose without weight updates, lifting base policies up to $+42.8$ points across memory, reasoning, and domain shifts.

---

### Top 4: FineDex: Bridging Fine-Grained Human-Object Interaction Generation to Dexterous Humanoid Manipulation
- **Priority Score**: `125 pts` | **Published**: `2026-11-25`
- **Focus Tracks**: `#humanoid` `#dexterous manipulation`
- **Key Authors**: Yujia Zeng, Yuxin Chen, Yuzhen Song et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.34884v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.34884v1)

**Executive Abstract**:
> Dexterity is, at its core, finger-level control, yet existing dexterous manipulation and human-object interaction (HOI) generation methods rarely let one specify how an interaction is performed: five-fingered hands are often reduced to grippers, or finger usage is copied from individual human demonstrations. We present FineDex, a framework that makes finger-level intent both expressible and executable. FineDex learns coordinated human body, hand, and object motions that follow fine-grained instructions on hand selection, individual fingers, and contacts with articulated objects. To bridge generation and execution, FineDex leverages generated interactions as actionable priors for an agent that discovers physically feasible contact strategies through practice in a physics-based digital twin. By adapting at test time without per-instance retraining, FineDex generalizes across fine-grained instructions and object configurations. Experiments demonstrate state-of-the-art HOI generation quality and fine-grained controllability, substantial improvements in dexterous manipulation success, and successful deployment on a real dexterous humanoid robot.

---

### Top 5: DexLink: Synthesizing Dexterous Behaviors from Chained Hand-object Poses
- **Priority Score**: `110 pts` | **Published**: `2026-11-25`
- **Focus Tracks**: `#reinforcement learning` `#dexterous manipulation`
- **Key Authors**: Meenal Parakh, Deep Patel, Beining Han et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.34936v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.34936v1)

**Executive Abstract**:
> Synthesizing diverse dexterous manipulation policies is challenging: existing simulation-based approaches rely on human demonstrations which are difficult to scale, or use generic reward functions, which provide limited control over the hand-object interactions. We propose DexLink, which addresses these limitations by synthesizing diverse dexterous behaviors from sparse, reusable hand-object interaction templates. Given key task waypoints, DexLink retargets static interaction templates to target objects using an optimization that preserves spatial hand-object relationships. It then links the retargeted poses into an approximate reference trajectory and uses residual reinforcement learning to refine this reference into a closed-loop policy in simulation. Experiments spanning single-hand, bimanual, articulated, and dynamic tasks demonstrate that DexLink provides fine-grained control over task timing, grasp types, and high-level execution. The modular interaction templates transfer reliably across object scales, instances, and categories; without object-specific human demonstrations, the framework also matches the performance of dense reference-tracking methods. Finally, zero-shot deployment of policies trained purely in simulation shows promise for the simulation-based framework.

---

