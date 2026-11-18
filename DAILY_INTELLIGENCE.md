# 🤖 Embodied AI & Robotics Frontier Briefing (2026-11-18)

> *Automated Intelligence Briefing generated via custom ETL scoring pipeline. Prioritizes foundation models, manipulation, locomotion, and physical AI systems.*

---

### Top 1: CADENCE: Learning Acyclic Gaits for Model-Based Quadruped Locomotion
- **Priority Score**: `140 pts` | **Published**: `2026-11-17`
- **Focus Tracks**: `#quadruped` `#reinforcement learning` `#locomotion`
- **Key Authors**: Owen Sullivan, Sourav Selvaraj, Mahdi Agheli
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.23102v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.23102v1)

**Executive Abstract**:
> Model-based quadruped controllers usually step on a cyclic gait, which lifts the legs in a fixed order on a fixed period, wherever the safe footholds are. We present CADENCE, a learned step planner with a small action space. Every 40 ms, it picks one of at most 65 discrete choices: no step, or one leg's step to a safe foothold. It also predicts a swing time. We train CADENCE by reinforcement learning on top of a convex model predictive controller (MPC). Nothing prescribes a gait: there is no gait schedule, and the reward has no gait term, only a cost per step. The one structural constraint is that at most two legs may swing at once. The policy we analyzed developed an acyclic gait, with no fixed period or stepping order, yet it still paired diagonal legs. An inverse footstep model (IFM), fitted on a controller's logged steps, turns each foothold into a command. With only the IFM refitted, on fewer than 20,000 steps, CADENCE ran frozen on OCS2's nonlinear MPC. In simulated trials on a range of terrains (26% to 49% voids) and speeds (0.1 m/s and 0.2 m/s), it succeeded in 85.1% (mean of five seeds), against 67.8% for OCS2-Trot, 65.5% for OCS2-Single, and 39.6% in a static walk ablation of CADENCE. At 49% voids, it succeeded in 72.9%, against 43.0% for OCS2-Trot.

---

### Top 2: PAIR: Bringing Household Robots into the Smart Home
- **Priority Score**: `140 pts` | **Published**: `2026-11-17`
- **Focus Tracks**: `#embodied ai` `#vla`
- **Key Authors**: Junseong Pyo, Hyeongjin Kim, Jongwook Han et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.23070v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.23070v1)

**Executive Abstract**:
> Household robots often need to operate appliances, and smart appliances offer both control panels and device APIs. Existing embodied AI simulation environments, however, model appliances solely as physical objects. We introduce PAIR, a smart-home simulation environment grounded in the Matter protocol~\footnote{https://csa-iot.org/all-solutions/matter/}, the industry standard for smart-home devices. PAIR provides 84 smart-device assets whose functional control panels and APIs act on a shared device state, with ambient conditions that evolve in response to both. From a survey of 1,443 requests, we construct a benchmark of 40 tasks that all require object manipulation yet remain solvable without API access, with 340 human demonstrations for policy training. Whether run alone, with a high-level planner, or with an API-enabled planner, two fine-tuned VLA policies complete none of the 120 evaluation episodes. Robots rarely get far enough to use the API: even with oracle plans and API access, over 90\% of failed rollouts stall at navigating, grasping, or operating a door. With a perfect oracle in place of the robot's body, the best planner still gets through only 57.3\% of its plan. When choosing between pressing a button and calling an API, several planners go by whether they can read the panel, not by API latency.\footnote{We will release our code and data upon publication.}

---

### Top 3: Auditing a Learned Simulator for Legged Robots: The Robotic World Model on ANYmal D
- **Priority Score**: `125 pts` | **Published**: `2026-11-17`
- **Focus Tracks**: `#world model` `#quadruped`
- **Key Authors**: Joyjeet Singh
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.23118v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.23118v1)

**Executive Abstract**:
> A legged robot can learn to walk inside a learned simulator: a neural network that predicts the robot's next state and is run forward on its own predictions. They are usually trained and checked one step ahead, although a policy uses them for a hundred steps or more. We audit one published system end to end, without a GPU: the dynamics model of the Robotic World Model (RWM) for the ANYmal D quadruped, and the uncertainty estimate of its follow-up, RWM-U. We rebuilt the model to match the released code's outputs, losses and gradients exactly, measured 101 trained simulators, 200 compressed copies and 38 simulators of three other architectures, and trained policies inside simulators that we tested in a hand-built MuJoCo model of the robot. Training on the model's own rollouts beat one-step training at 368 steps on all ten held-out episodes (registered), although one-step training was better one step ahead. One-step checks therefore misjudge design choices: pruning 30% of the weights kept 90% of the model's skill one step ahead and 39% at 2 s. Ensemble disagreement ranked rollout error well (Spearman +0.90 at 100 steps), yet covered 4.6% of outcomes at one sigma, against 68% for a calibrated estimate, as each network's own variance collapses under the implemented loss. Two checks that need no recorded future ranked some pools of simulators well, but neither was shown better than 8-step error in a primary test. At the robot level, accuracy has not predicted walking: all 18 fine-tuned copies we tested predicted better than the released model one and eight steps ahead, yet 13 gave failing policies, and registered tests of whether any check ranks simulators by their policies were not settled. In a secondary test, running the authors' policy inside each simulator ranked them well. We also report nine of our own claims that we withdrew. Scope: one robot, one gait, simulated data, no hardware.

---

### Top 4: Residual-Guided Lightweight Reinforcement Learning for Risk-Aware Trajectory Selection with a Frozen World Model
- **Priority Score**: `120 pts` | **Published**: `2026-11-17`
- **Focus Tracks**: `#world model` `#reinforcement learning`
- **Key Authors**: Jiaqi Wu, Yongqi Dong, Yijie Zhong et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.22998v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.22998v1)

**Executive Abstract**:
> In automated driving, world models provide future scene predictions for evaluating candidate trajectories, but fixed selection rules may not capture scene-dependent trade-offs. We propose a residual-guided reinforcement learning (RL) framework for lightweight trajectory selection with a frozen world model and a fixed candidate bank. The framework uses proximal policy optimization (PPO) to fine-tune a joint policy over candidate selection and bounded trajectory residuals. A context-conditioned ranking network learns candidate preferences from feedback obtained by evaluating local perturbations of the selected trajectories. At inference, the selector combines learned preference and predicted risk ranks using fixed weights and returns the selected candidate trajectory without modification. Fine-tuning updates 16,106 parameters across the actor and critic, while the deployed selector retains only the 11,725-parameter ranking network, with the residual branch and critic used exclusively during training. In open-loop evaluation on the nuScenes validation set, the method reduces average Euclidean trajectory error (L2) by 3.99% relative to the RiskWorld model baseline without RL-based selection. Under matched budgets for feedback accesses and actor updates, residual exploration reduces L2 by 0.83% relative to the categorical PPO variant trained without residuals. The method also maintains lower L2 than RiskWorld when risk features are removed or shuffled.

---

### Top 5: Sim2CBF: From Forward Simulations to Implicit Control Barrier Function Safety Filtering without Model Derivatives
- **Priority Score**: `90 pts` | **Published**: `2026-11-17`
- **Focus Tracks**: `#world model`
- **Key Authors**: Luzia Knoedler, Yihan Liu, Shaohang Han et al.
- **Direct Access**: [arXiv Abstract](http://arxiv.org/abs/2611.22954v1) | [PDF Fulltext](http://arxiv.org/pdf/2611.22954v1)

**Executive Abstract**:
> Failure avoidance in complex robot-environment interactions is challenging because the underlying dynamics are difficult to model accurately, and available predictive models may not provide reliable derivatives. We present Sim2CBF, a failure-avoidance framework that solves the Control Barrier Function (CBF)-Safety Filter (SF) optimization problem using only forward-model evaluations, thereby avoiding differentiation of the predictive model. Specifically, we approximate the CBF constraint using finite differences and local linear interpolation over sampled control inputs while preserving failure-avoidance guarantees. The underlying CBF is implicit and constructed from backup-policy rollouts, enabling the use of expressive predictive models such as physics-based simulators and learned world models. Compared with purely sampling-based SFs, our formulation requires fewer control samples and yields less conservative behavior than direct nominal-backup blending. We evaluate Sim2CBF in simulation, hardware box-toppling, and vision-based control tasks, demonstrating its applicability to contact-rich and learned dynamics, as well as its adaptability to changes in the predictive model.

---

