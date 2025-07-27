---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
sidebar:
  nav: "research-subnav"
---

The rapid advancement of communication, vehicle automation technologies, and artificial intelligence (AI) is transforming intelligent transportation systems (ITS), offering opportunities to enhance safety, efficiency, and energy. Motivated by these developments, my research focuses on 1) interactive driving behavior modeling and prediction, 2) optimal control of connected and automated vehicles (CAVs) in mixed traffic environments, and 3) traffic management. My research philosophy hinges on addressing challenges in these areas by integrating traditional analytical methods, such as physics-based modeling, control theory, and traffic flow theory, with emerging technologies like machine learning (ML) and foundation models (FMs)/large language models (LLMs). In line with my research philosophy, I have developed generic and interpretable methodological frameworks and computational models to analyze and improve transportation system performance in terms of mobility, safety, stability, and energy consumption. These models are validated through field implementations using Level 3 CAVs.

## Major Research Areas <br>
Over the years, I have investigated the following three broad areas of research: 1) interactive driving behavior modeling and prediction, 2) optimal control of connected and automated vehicles (CAV) in mixed traffic environments, and 3) traffic management. A selection of my papers is provided in the reference section for further reading.

<!-- ===== Tabs: CSS + HTML + JS 仅在本页生效 ===== -->
<style>
/* ===== Tabs 配色与可访问性增强（无内容边框） ===== */
.research-tabs {
  /* 可调色变量（浅/深色模式分别定义） */
  --tab-border: #c9d1d9;
  --tab-inactive-bg: #f2f4f8;
  --tab-inactive-text: #4b5563;
  --tab-active-bg: #ffffff;
  --tab-active-text: #111827;
  --tab-hover-bg: #e5e7eb;
  --tab-accent: #3b82f6; /* 激活标签底部强调色 */
  margin: 0 0 1rem 0;
}

@media (prefers-color-scheme: dark) {
  .research-tabs {
    --tab-border: #30363d;
    --tab-inactive-bg: #161b22;
    --tab-inactive-text: #c9d1d9;
    --tab-active-bg: #0d1117;
    --tab-active-text: #ffffff;
    --tab-hover-bg: #1f2937;
    --tab-accent: #60a5fa;
  }
}

/* 隐藏原始 radio */
.research-tabs input[type="radio"] {
  position: absolute; left: -9999px;
}

/* 标签栏 */
.research-tabs .tab-labels {
  display: flex; flex-wrap: wrap; gap: 6px;
  border-bottom: 2px solid var(--tab-border);
  margin-bottom: 0;
}

/* 标签默认态：浅底+中灰字 */
.research-tabs label {
  padding: 10px 14px;
  border-radius: 10px 10px 0 0;
  cursor: pointer;
  background: var(--tab-inactive-bg);
  color: var(--tab-inactive-text);
  font-weight: 700;
  transition: background .15s ease, color .15s ease, box-shadow .15s ease, transform .05s ease;
}

/* 悬停：稍深一些 */
.research-tabs label:hover {
  background: var(--tab-hover-bg);
}

/* 激活态：白底/深字 + 底部强调线（不加内容边框） */
#tab-behavior:checked    ~ .tab-labels label[for="tab-behavior"],
#tab-cav-control:checked ~ .tab-labels label[for="tab-cav-control"],
#tab-management:checked  ~ .tab-labels label[for="tab-management"] {
  background: var(--tab-active-bg);
  color: var(--tab-active-text);
  /* 用 box-shadow 画一条“底部强调线”，对比更强 */
  box-shadow: 0 2px 0 var(--tab-accent);
  position: relative;
  z-index: 1;
  transform: translateY(1px);
}

/* 键盘可达性 */
.research-tabs label:focus-visible {
  outline: 2px solid var(--tab-accent);
  outline-offset: 2px;
}

/* 面板：默认隐藏；不加边框 */
.tab-panel { display: none; padding-top: 12px; }

/* 显示被选中的面板（不加边框，仅保留内边距） */
#tab-behavior:checked    ~ #panel-behavior,
#tab-cav-control:checked ~ #panel-cav-control,
#tab-management:checked  ~ #panel-management {
  display: block;
  padding: 12px 0 0 0;  /* 可按需调节；不加边框 */
}

/* 内文分隔线与间距微调 */
.tab-panel hr { margin-top: 1.2rem; }
</style>

<div class="research-tabs" id="tabs-top">
  <!-- 3 个 radio 控件 -->
  <input type="radio" name="research-tabs" id="tab-behavior" checked>
  <input type="radio" name="research-tabs" id="tab-cav-control">
  <input type="radio" name="research-tabs" id="tab-management">

  <!-- 标签栏（点击即可切换） -->
  <div class="tab-labels">
    <label for="tab-behavior"     title="Interactive driving behavior modeling and prediction">1) Driving Behavior Modeling & Prediction</label>
    <label for="tab-cav-control"  title="Optimal control of CAVs in mixed traffic environments">2) CAV Control</label>
    <label for="tab-management"   title="Traffic management for urban, rural, and tribal regions">3) Traffic Management</label>
  </div>

  <!-- 面板 1：Behavior Modeling & Prediction -->
  <section id="panel-behavior" class="tab-panel" markdown="1">
  <a id="behavior"></a>

### 1 Interactive driving behavior modeling and prediction
With the integration of Autonomous Vehicles (AVs) and CAVs, the dynamics of mixed traffic flows have shifted significantly compared to traditional traffic conditions. In mixed traffic, human-driven vehicle (HV) behaviors exhibit greater variability and uncertainty, particularly in longitudinal car-following and lateral maneuvers. These factors heighten traffic safety risks and complicate the decision-making processes of AVs. To address these challenges, we have developed novel modeling and prediction methodologies for both AVs and HVs, focusing on longitudinal and lateral driving behaviors. These methodologies leverage approaches including physics-based models, machine learning (ML), physics-informed machine learning (PIML), and foundation models (FMs)/large language models (LLMs).

### 1.1  Multi-scale car-following and traffic dynamics modeling methodologies for HVs and AVs
In a mixed traffic environment, it is crucial to model and accurately calibrate car-following behaviors of both HVs and AVs. This provides critical information about the driving characteristics of surrounding vehicles for CAVs to optimize their decision-making processes. However, current car-following models based on either physics or ML often struggle to accurately capture the uncertainty in driving behaviors and typically overlook the influence of macroscopic traffic flow (traffic dynamics) on individual driving behaviors. In this regard, We have developed models using both physics-based approaches and ML techniques. 

### [Generative adversarial network for car following trajectory generation and anomaly detection](https://www.tandfonline.com/doi/abs/10.1080/15472450.2023.2301691)  
<p>
  <img src="/images/gan.png" alt="TrajGAN overview"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  Car-following trajectory generation and anomaly detection are critical functions in the sensing module of an automated vehicle. However, developing models that capture realistic trajectory data distribution and detect anomalous driving behaviors could be challenging. This paper proposes ‘TrajGAN’, an unsupervised learning approach based on the Generative Adversarial Network (GAN) to exploit vehicle car following trajectory data for generation and anomaly detection. The proposed TrajGAN consists of two modules, an encoder-decoder Long Short-Term Memory (LSTM)-based generator and an LSTM-multilayer perceptron (MLP) based discriminator, whose former component is used to generate vehicular car following trajectories and the latter one is for trajectory anomaly detection. By letting these two modules game with each other in training, we can simultaneously achieve robust trajectory generators and anomaly detectors. Trained with the Next Generation Simulation (NGSIM) dataset, TrajGAN can generate realistic trajectories with a similar distribution of training data and identify a manifold of anomalous trajectories based on an anomaly scoring scheme. Simulation results indicate that the proposed approach is efficient in reproducing artificial trajectories and identifying anomalous driving behaviors.
</p>

<div style="clear: both;"></div>
<hr/>

### [Bi-scale car-following model calibration based on corridor-level trajectory](https://www.sciencedirect.com/science/article/abs/pii/S1366554524000887)  
<p>
  <img src="/images/BiScale.png" alt="Bi-scale calibration illustration"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  The precise estimation of macroscopic traffic parameters, such as travel time and fuel consumption, is essential for the optimization of traffic management systems. Despite its importance, the comprehensive acquisition of vehicle trajectory data for the calculation of these macroscopic measures presents a challenge. To bridge this gap, this study aims to calibrate car-following models capable of predicting both microscopic measures and macroscopic measures. We conduct a numerical analysis to trace the cumulative process of model prediction errors across various measurements, and our findings indicate that macroscopic measures encapsulate the accumulation of model errors. By incorporating macroscopic measures into vehicle model calibration, we can mitigate the impact of noise on microscopic data measurements. We compare three car-following model calibration methods: MiC (using microscopic measurements), MaC (using macroscopic measurements), and BiC (using both microscopic and macroscopic measurements)—utilizing real-world trajectory data. The BiC method emerges as the most successful in reconstructing vehicle trajectories and accurately estimating travel time and fuel consumption, whereas the MiC method leads to overfitting and inaccurate macro-measurement predictions. This study underscores the importance of bi-scale calibration for precise traffic and energy consumption predictions, laying the groundwork for future research aimed at enhancing traffic management strategies.
</p>

<div style="clear: both;"></div>
<hr/>

### [Development, Calibration, and validation of a Novel nonlinear Car-Following Model: Multivariate piecewise linear approach for adaptive cruise control vehicles](https://www.sciencedirect.com/science/article/pii/S1366554525000729)  
<p>
  <img src="/images/MPL.png" alt="MPL model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  As advanced driver-assistance systems (ADAS) are more widely implemented—particularly the adaptive cruise control (ACC) system in car-following behavior—accurate modeling of ACC vehicles’ behavior is needed. Currently, each vehicle manufacturer develops its ACC systems with unique controllers, creating “black boxes” that are not openly accessible for analysis. In addition, the vehicle dynamics that use sensor and dynamics systems introduce complicated inherent nonlinearity in ACC-equipped vehicles’ behaviors (hereinafter referred to as ACC vehicles). Given the complex inherent nonlinearity of ACC systems, traditional vehicle behavior modeling methods have to trade off between modeling accuracy and interpretability. To address these challenges, this study introduces an innovative multivariate piecewise linear (MPL) car-following modeling methodology to emulate any ACC system from observational data. The MPL modeling methodology allows for several empirical quantifications of the unknown design parameters of the different ACC systems as they are manifested in the vehicles’ driving behavior. This approach distinguishes itself from traditional piecewise linear models by incorporating multiple breakpoints. These breakpoints serve to capture the inherent nonlinearity of ACC vehicle dynamics across a range of linear functions. Simultaneously, these breakpoints are empirically derived from actual trajectory data, thereby enhancing modeling accuracy. A case study illustrates four calibrated MPL models based on a large-scale field automated vehicle experiment dataset. Compared to other models, the MPL models show sufficient accuracy and interpretability. This robust and transparent modeling methodology may serve as an analytical tool for future transportation planning.
</p>

<div style="clear: both;"></div>
<hr/>

### [Physically Analyzable AI-Based Nonlinear Platoon Dynamics Modeling During Traffic Oscillation: A Koopman Approach](https://ieeexplore.ieee.org/abstract/document/10954270)  
<p>
  <img src="/images/Koopman.png" alt="Koopman approach"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  Given the complexity and nonlinearity inherent in traffic dynamics within vehicular platoons, there exists a critical need for a modeling methodology with high accuracy while concurrently achieving physical analyzability. Currently, there are two predominant approaches: the physics model-based approach and the Artificial Intelligence (AI)–based approach. Knowing the facts that the physical-based model usually lacks sufficient modeling accuracy and potential function mismatches and the pure-AI-based method lacks analyzability, this paper innovatively proposes an AI-based Koopman approach to model the unknown nonlinear platoon dynamics harnessing the power of AI and simultaneously maintaining physical analyzability, with a particular focus on periods of traffic oscillation. Specifically, this research first employs a deep learning framework to generate the embedding function that lifts the original space into the embedding space. Given the embedding space descriptiveness, the platoon dynamics can be expressed as a linear dynamical system founded by the Koopman theory. Based on that, the routine of linear dynamical system analysis can be conducted on the learned traffic linear dynamics in the embedding space. By that, the physical interpretability and analyzability of model-based methods with the heightened precision inherent in data-driven approaches can be synergized. Comparative experiments have been conducted with existing modeling approaches, which suggest our method’s superiority in accuracy. Additionally, a phase plane analysis is performed, further evidencing our approach’s effectiveness in replicating the complex dynamic patterns. Moreover, the proposed methodology is proven to feature the capability of analyzing the stability, attesting to the physical analyzability.
</p>

<div style="clear: both;"></div>
<hr/>

### [FollowGen: A Scaled Noise Conditional Diffusion Model for Car-Following Trajectory Prediction](https://arxiv.org/abs/2411.16747)  
<p>
  <img src="/images/FollowGen.png" alt="FollowGen diffusion model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  Vehicle trajectory prediction is crucial for advancing autonomous driving and advanced driver assistance systems (ADAS). Although deep learning-based approaches - especially those utilizing transformer-based and generative models - have markedly improved prediction accuracy by capturing complex, non-linear patterns in vehicle dynamics and traffic interactions, they frequently overlook detailed car-following behaviors and the inter-vehicle interactions critical for real-world driving applications, particularly in fully autonomous or mixed traffic scenarios. To address the issue, this study introduces a scaled noise conditional diffusion model for car-following trajectory prediction, which integrates detailed inter-vehicular interactions and car-following dynamics into a generative framework, improving both the accuracy and plausibility of predicted trajectories. The model utilizes a novel pipeline to capture historical vehicle dynamics by scaling noise with encoded historical features within the diffusion process. Particularly, it employs a cross-attention-based transformer architecture to model intricate inter-vehicle dependencies, effectively guiding the denoising process and enhancing prediction accuracy. Experimental results on diverse real-world driving scenarios demonstrate the state-of-the-art performance and robustness of the proposed method.
</p>

<div style="clear: both;"></div>
<hr/>

### [Physical enhanced residual learning (PERL) framework for vehicle trajectory prediction](https://www.sciencedirect.com/science/article/pii/S277242472500006X)  
<p>
  <img src="/images/PERL.png" alt="PERL framework"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
While physics models for predicting system states can reveal fundamental insights owing to their parsimonious structure, they may not always yield the most accurate predictions, particularly for complex systems. As an alternative, neural network (NN) models usually yield more accurate predictions; however, they lack interpretable physical insights. To articulate the advantages of both physics and NN models while circumventing their limitations, this study proposes a physics-enhanced residual learning (PERL) framework that adjusts a physics model prediction with a corrective residual predicted from a residual learning NN model. The integration of the physics model preserves interpretability and tremendously reduces the amount of training data compared with pure NN models. We apply PERL to a vehicle trajectory prediction problem with real-world trajectory data of both a human-driven vehicle (HV) and an autonomous vehicle (AV), using an adapted Newell car-following model as the physics model and four kinds of neural networks (Gated Recurrent Unit (GRU), Convolution long short-term memory (CLSTM), Variational Autoencoder (VAE), and the Informer model) as the residual learning model. We compare this PERL model with pure physics models, NN models, and other physics-informed neural network (PINN) models. The results reveal that PERL yields the best prediction when the training data are small. The PERL model converges quickly during training. Moreover, compared with the NN and PINN models, the PERL model requires fewer parameters to achieve similar predictive performance. A sensitivity analysis revealed that the PERL model consistently outperforms the physics models, NN models and PINN models with different physics and residual learning models given a small training dataset. Among these, the PERL model based on CLSTM achieved the most accurate predictions.
</p>

<div style="clear: both;"></div>
<hr/>

### 1.2  Interaction-aware two-dimensional (2D) trajectory prediction 
Accurate prediction of human-driven vehicle trajectories is essential for decision-making and control in CAVs. In dynamic and complex environments, vehicle behavior is influenced by its own historical actions and interactions with surrounding vehicles, which complicates the precise prediction of future longitudinal and lateral movements. We proposed the following methodologies to address the 2D trajectory prediction challenges.

### [Graph-Based Interaction-Aware Multimodal 2D Vehicle Trajectory Prediction Using Diffusion Graph Convolutional Networks](https://ieeexplore.ieee.org/abstract/document/10352973)  
<p>
  <img src="/images/Graph.png" alt="GIMTP with DGCN"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  Predicting vehicle trajectories is crucial to ensuring automated vehicle operation efficiency and safety, particularly on congested multi-lane highways. In such dynamic environments, a vehicle's motion is determined by its historical behaviors as well as interactions with surrounding vehicles. These intricate interactions arise from unpredictable motion patterns, leading to a wide range of driving behaviors that warrant in-depth investigation. This study presents the Graph-based Interaction-aware Multi-modal Trajectory Prediction (GIMTP) framework, designed to probabilistically predict future vehicle trajectories by effectively capturing these interactions. Within this framework, vehicles' motions are conceptualized as nodes in a time-varying graph, and the traffic interactions are represented by a dynamic adjacency matrix. To holistically capture both spatial and temporal dependencies embedded in this dynamic adjacency matrix, the methodology incorporates the Diffusion Graph Convolutional Network (DGCN), thereby providing a graph embedding of both historical states and future states. Furthermore, we employ a driving intention-specific feature fusion, enabling the adaptive integration of historical and future embeddings for enhanced intention recognition and trajectory prediction. This model gives two-dimensional predictions for each mode of longitudinal and lateral driving behaviors and offers probabilistic future paths with corresponding probabilities, addressing the challenges of complex vehicle interactions and multi-modality of driving behaviors. Validation using real-world trajectory datasets demonstrates the efficiency and potential.
</p>

<div style="clear: both;"></div>
<hr/>

### [Hypergraph-based Motion Generation with Multi-modal Interaction Relational Reasoning](https://arxiv.org/abs/2409.11676)  
<p>
  <img src="/images/Hypergraph.png" alt="RHINO hypergraph motion generation"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  The intricate nature of real-world driving environments, characterized by dynamic and diverse interactions among multiple vehicles and their possible future states, presents considerable challenges in accurately predicting the motion states of vehicles and handling the uncertainty inherent in the predictions. Addressing these challenges requires comprehensive modeling and reasoning to capture the implicit relations among vehicles and the corresponding diverse behaviors. This research introduces an integrated framework for autonomous vehicles (AVs) motion prediction to address these complexities, utilizing a novel <strong>R</strong>elational <strong>H</strong>ypergraph <strong>I</strong>nteraction-informed <strong>N</strong>eural m<strong>O</strong>tion generator (RHINO). RHINO leverages hypergraph-based relational reasoning by integrating a multi-scale hypergraph neural network to model group-wise interactions among multiple vehicles and their multi-modal driving behaviors, thereby enhancing motion prediction accuracy and reliability. Experimental validation using real-world datasets demonstrates the superior performance of this framework in improving predictive accuracy and fostering socially aware automated driving in dynamic traffic scenarios.
</p>

<div style="clear: both;"></div>
<hr/>

### [Goal-based Neural Physics Vehicle Trajectory Prediction Model](https://arxiv.org/pdf/2409.15182)  
<p>
  <img src="/images/Goal.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  Vehicle trajectory prediction plays a vital role in intelligent transportation systems and autonomous driving, as it significantly affects vehicle behavior planning and control, thereby influencing traffic safety and efficiency. Numerous studies have been conducted to predict short-term vehicle trajectories in the immediate future. However, long-term trajectory prediction remains a major challenge due to accumulated errors and uncertainties. Additionally, balancing accuracy with interpretability in the prediction is another challenging issue in predicting vehicle trajectory. To address these challenges, this paper proposes a <strong>G</strong>oal-based <strong>N</strong>eural <strong>P</strong>hysics Vehicle Trajectory Prediction Model (GNP). The GNP model simplifies vehicle trajectory prediction into a two-stage process: determining the vehicle's goal and then choosing the appropriate trajectory to reach this goal. The GNP model contains two sub-modules to achieve this process. The first sub-module employs a multi-head attention mechanism to accurately predict goals. The second sub-module integrates a deep learning model with a physics-based social force model to progressively predict the complete trajectory using the generated goals. The GNP demonstrates state-of-the-art long-term prediction accuracy compared to four baseline models. We provide interpretable visualization results to highlight the multi-modality and inherent nature of our neural physics framework. Additionally, ablation studies are performed to validate the effectiveness of our key designs. The source code for this work is available at: https://github.com/mcgrche/GNP--Goal-based-Neural-Physics-Vehicle-Trajectory-Prediction-Model.
</p>

<div style="clear: both;"></div>
<hr/>

### [Interaction Dataset of Autonomous Vehicles with Traffic Lights and Signs](https://arxiv.org/pdf/2501.12536)  
<p>
  <img src="/images/Interaction.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
This paper presents the development of a comprehensive dataset capturing interactions between Autonomous Vehicles (AVs) and traffic control devices, specifically traffic lights and stop signs. Derived from the Waymo Motion dataset, our work addresses a critical gap in the existing literature by providing real-world trajectory data on how AVs navigate these traffic control devices. We propose a methodology for identifying and extracting relevant interaction trajectory data from the Waymo Motion dataset, incorporating over 37,000 instances with traffic lights and 44,000 with stop signs. Our methodology includes defining rules to identify various interaction types, extracting trajectory data, and applying a wavelet-based denoising method to smooth the acceleration and speed profiles and eliminate anomalous values, thereby enhancing the trajectory quality. Quality assessment metrics indicate that trajectories obtained in this study have anomaly proportions in acceleration and jerk profiles reduced to near-zero levels across all interaction categories. By making this dataset publicly available, we aim to address the current gap in datasets containing AV interaction behaviors with traffic lights and signs. Based on the organized and published dataset, we can gain a more in-depth understanding of AVs' behavior when interacting with traffic lights and signs. This will facilitate research on AV integration into existing transportation infrastructures and networks, supporting the development of more accurate behavioral models and simulation tools.
</p>

<div style="clear: both;"></div>
<hr/>

### 1.3  Large Vision-Language Models (VLMs) enabled prediction and planning for autonomous driving
Motivated by the emergent reasoning capabilities of LLMs and VLMs, we also focus on the application of VLMs in enhancing prediction and planning for end-to-end (E2E) autonomous driving, leveraging their multimodal understanding to improve decision-making and safety. 

### [V2X-VLM: End-to-End V2X Cooperative Autonomous Driving Through Large Vision-Language Models](https://arxiv.org/pdf/2408.09251)  
<p>
 <img src="/images/V2X-VLM.png" alt="MPL model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
  <!-- TODO: 内容似乎与上文 MPL（ACC）段落重复，请确认是否需要替换为 V2X‑VLM 的正确摘要。 -->
Advancements in autonomous driving have increasingly focused on end-to-end (E2E) systems that manage the full spectrum of driving tasks, from environmental perception to vehicle navigation and control. This paper introduces V2X-VLM, an innovative E2E vehicle-infrastructure cooperative autonomous driving (VICAD) framework with Vehicle-to-Everything (V2X) systems and large vision-language models (VLMs). V2X-VLM is designed to enhance situational awareness, decision-making, and ultimate trajectory planning by integrating multimodel data from vehicle-mounted cameras, infrastructure sensors, and textual information. The contrastive learning method is further employed to complement VLM by refining feature discrimination, assisting the model to learn robust representations of the driving environment. Evaluations on the DAIR-V2X dataset show that V2X-VLM outperforms state-of-the-art cooperative autonomous driving methods, while additional tests on corner cases validate its robustness in real-world driving conditions.
</p>

<div style="clear: both;"></div>
<hr/>

  </section>

  <!-- 面板 2：CAV Control -->
  <section id="panel-cav-control" class="tab-panel" markdown="1">
  <a id="cav-control"></a>

### 2  Optimal control of CAVs in mixed traffic environments
To address the challenges posed by the stochastic nature of human-driven behaviors, the heterogeneity in traffic composition, and the partial observability characteristic of complex mixed traffic conditions involving both CAVs and HVs, optimizing CAV driving behavior from a systemic traffic flow perspective remains particularly difficult. In response to these challenges, we have conducted extensive research on decision-making control for CAVs in mixed traffic environments. By integrating the core principles of physics models, control theory, and traffic flow theory into a deep reinforcement learning (DRL) framework, I developed the physics-informed deep reinforcement learning (PIDRL) methodology, specifically designed for the intelligent control of CAVs and other ITS agents in mixed traffic scenarios. This generic methodology has proven versatile and effective in various applications, including CAV control and intelligent bus operations. It has been validated in improving key system-level performance metrics such as safety, efficiency, stability, and energy utilization.

### 2.1  Centralized multi-objective cooperative control for CAVs
A centralized multi-objective cooperative control strategy based on deep reinforcement learning is proposed to address the heterogeneity of mixed traffic flow.

### [Connected automated vehicle cooperative control with a deep reinforcement learning approach in a mixed traffic environment](https://www.sciencedirect.com/science/article/pii/S0968090X21004150)  
<p>
  <img src="/images/Central.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
This paper proposes a cooperative strategy of connected and automated vehicles (CAVs) longitudinal control for a mixed connected and automated traffic environment based on deep reinforcement learning (DRL) algorithm, which enhances the string stability of mixed traffic, car following efficiency, and energy efficiency. Since the sequences of mixed traffic are combinatory, to reduce the training dimension and alleviate communication burdens, we decomposed mixed traffic into multiple subsystems where each subsystem is comprised of human-driven vehicles (HDV) followed by cooperative CAVs. Based on that, a cooperative CAV control strategy is developed based on a deep reinforcement learning algorithm, enabling CAVs to learn the leading HDV’s characteristics and make longitudinal control decisions cooperatively to improve the performance of each subsystem locally and consequently enhance performance for the whole mixed traffic flow. For training, a distributed proximal policy optimization is applied to ensure the training convergence of the proposed DRL. To verify the effectiveness of the proposed method, simulated experiments are conducted, which shows the performance of our proposed model has a great generalization capability of dampening oscillations, fulfilling the car following and energy-saving tasks efficiently under different penetration rates and various leading HDVs behaviors.
</p>

<div style="clear: both;"></div>
<hr/>

### 2.2  Distributed CAV control strategy considering communication loss
In response to the partial observability of mixed traffic flow and the stochastic nature of HV behavior, we propose novel distributed control strategies for CAVs based on physics-informed DRL, offering a more practical implementation than centralized controllers. This work uniquely integrates traffic flow theory with consensus and equilibrium theories from control science within the DRL framework. Such integration enables a fusion of macroscopic traffic flow characteristics and multi-vehicle state data, effectively mitigating the stochastic nature of HDV behavior and reducing the propagation of traffic oscillations in mixed traffic flow. 

### [A deep reinforcement learning based distributed control strategy for connected automated vehicles in mixed traffic platoon](https://www.sciencedirect.com/science/article/pii/S0968090X23000086)  
<p>
  <img src="/images/DistributedMix.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
This paper proposes an innovative distributed longitudinal control strategy for connected automated vehicles (CAVs) in the mixed traffic environment of CAV and human-driven vehicles (HDVs), incorporating high-dimensional platoon information. For mixed traffic, the traditional CAV control method focuses on microscopic trajectory information, which may not be efficient in handling the HDV stochasticity (e.g., long reaction time; various driving styles) and mixed traffic heterogeneities. Different from traditional methods, our method, for the first time, characterizes consecutive HDVs as a whole (i.e., AHDV) to reduce the HDV stochasticity and utilize its macroscopic features to control the following CAVs. The new control strategy takes advantage of platoon information to anticipate the disturbances and traffic features induced downstream under mixed traffic scenarios and greatly outperforms the traditional methods. In particular, the control algorithm is based on deep reinforcement learning (DRL) to fulfill car-following control efficiency and further address the stochasticity for the aggregated car following behavior by embedding it in the training environment. To better utilize the macroscopic traffic features, a general platoon of mixed traffic is categorized as a CAV-HDVs-CAV pattern and described by corresponding DRL states. The macroscopic traffic flow properties are built upon the Newell car-following model to capture the characteristics of aggregated HDVs' joint behaviors. Simulated experiments are conducted to validate our proposed strategy. The results demonstrate that the proposed control method has outstanding performances in terms of oscillation dampening, eco-driving, and generalization capability.
</p>

<div style="clear: both;"></div>
<hr/>

### [A deep reinforcement learning-based distributed connected automated vehicle control under communication failure](https://onlinelibrary.wiley.com/doi/epdf/10.1111/mice.12825) 
<p>
  <img src="/images/Communications.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
This paper proposes a deep reinforcement learning (DRL)-based distributed lon-gitudinal control strategy for connected and automated vehicles (CAVs) under communication failure to stabilize traffic oscillations. Specifically, the signal-interference-plus-noise ratio-based vehicle-to-vehicle communication is incor-porated into the DRL training environment to reproduce the realistic commu-nication and time–space varying information flow topologies (IFTs). A dynamic information fusion mechanism is designed to smooth the high-jerk control sig-nal caused by the dynamic IFTs. Based on that, each CAV controlled by the DRL-based agent was developed to receive the real-time downstream CAVs’ state information and take longitudinal actions to achieve the equilibrium consen-sus in the multi-agent system. Simulated experiments are conducted to tune the communication adjustment mechanism and further validate the control perfor-mance, oscillation dampening performance and generalization capability of our proposed algorithm. </p>

<div style="clear: both;"></div>
<hr/>

### [Physics-informed deep reinforcement learning-based integrated two-dimensional car-following control strategy for connected automated vehicles](https://www.sciencedirect.com/science/article/pii/S0950705123002356) 
<p>
  <img src="/images/2DControl.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
Connected automated vehicles (CAVs) are broadly recognized as next-generation transformative transportation technologies having great potential to improve traffic safety, efficiency, and stability. Efficiently controlling CAVs on two-dimensional curvilinear roadways to follow preceding vehicles is denoted as the two-dimensional car-following process, which is highly critical; this process is challenging to implement owing to the complexity and varied nature of driving environments. This study proposes an innovative integrated two-dimensional control strategy for CAVs based on deep reinforcement learning (DRL), which efficiently regulates the two-dimensional car-following process of CAVs in terms of both stability-wise longitudinal control performance and accurate lateral path-tracking performance. Within the control framework, each CAV can receive the surrounding information from downstream vehicles and roadway geometry based on vehicle-to-everything (V2X) communication. To better utilize this information, we designed a physics-informed DRL state fusion approach and reward function, which efficiently embeds prior physics knowledge and borrows the merits of the equilibrium and consensus concepts from the control theory. Given the physics-informed information, the DRL-based controller outputs the integrated control instructions for both longitudinal and lateral control. For training, we constructed a roadway with a set of varying curvatures and embedded the ground-truth vehicle trajectory datasets to more effectively capture the realistic variations in the roadway geometry and driving environment. To facilitate value function approximation and enhance the policy iteration process in training, the distributed proximal policy optimization (DPPO) algorithm was applied, owing to its balanced performance. A series of simulated experiments were conducted to validate the controller’s lateral control accuracy and stability-wise oscillation dampening performance in diverse traffic scenarios, including extreme ones. </p>

<div style="clear: both;"></div>
<hr/>

### [A Predictive Deep Reinforcement Learning Based Connected Automated Vehicle Anticipatory Longitudinal Control in a Mixed Traffic Lane Change Condition](https://ieeexplore.ieee.org/abstract/document/10988662) 
<p>
  <img src="/images/LaneChange.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
Maintaining safety and efficiency for mixed traffic consisting of connected automated vehicles (CAVs) and human-driven vehicles (HDVs) is an arduous task due to the inherent HDVs’ stochasticity. Especially for longitudinal control, which is the basic function of vehicle automation, prevailing research primarily considers CAV’s car-following control merely the acceleration and deceleration of leading vehicles. However, this approach overlooks the potential disruptions caused by surrounding vehicles executing lane changes, which can significantly impact the control vehicle’s stability and overall safety. Hence, our study introduces a predictive deep reinforcement learning (DRL) longitudinal CAV controller. This innovative approach leverages prediction from a physics-informed neural network as well as the control capability of DRL to better anticipate and mitigate issues arising from lane-changing, enhancing the safety and efficiency of CAVs in such scenarios. Validated by the numerical simulations embedded with the real-world data, the results indicate that the proposed controller significantly enhances the safety and efficiency of CAVs in situations involving lane changes by other vehicles, showcasing its potential as a valuable tool in advancing CAV technology in mixed traffic. </p>

<div style="clear: both;"></div>
<hr/>

### 2.3  Distributed dynamics bus control for reducing bus bunching 
We further extended the generic physics-informed control approach to develop dynamic control systems for buses to effectively reduces deviations in timetables and bus spacing, thereby enhancing the overall efficiency and stability of the transit system.

### [A distributed deep reinforcement learning–based integrated dynamic bus control system in a connected environment](https://onlinelibrary.wiley.com/doi/full/10.1111/mice.12803) 
<p>
  <img src="/images/Bus.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
The bus bunching problem caused by the uncertain interstation travel time andpassenger demand rate is a critical issue that impairs transit efficiency. Most cur-rent bus control studies focus on single or combined strategies while ignoring thebus system’s real-time environmental information. This paper proposed a dis-tributed deep reinforcement learning (DRL)-based generic bus dynamic controlmethod to solve the bus bunching problem by maintaining the schedule adher-ence, headway regularity, and achieving the consensus in the multiagent system.This study built a bus system that utilizes the bus historical and traffic informa-tion by incorporating these characteristics into the environment. After that, a dis-tributed DRL-based bus dynamic control strategy is developed based on the bussystem, enabling each bus to adjust its motion by any generic method utilizingthe weighted downstream buses’ information. Regarding the training process, adistributed proximal policy optimization algorithm is adopted for improving theconverging performance. Simulated experiments are conducted to verify the con-trol performance, robustness, feasibility, resilience, and generalization capability,which shows that our strategy can significantly reduce the schedule and head-way deviations, prevent the accumulation of deviation downstream, and avoidbus bunching. 
</p>

<div style="clear: both;"></div>
<hr/>


### [A robust integrated multi-strategy bus control system via deep reinforcement learning](https://www.sciencedirect.com/science/article/pii/S0952197624001441) 
<p>
  <img src="/images/Bus2.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
An efficient urban bus control system has the potential to significantly reduce travel delays and streamline the allocation of transportation resources, thereby offering enhanced and user-friendly transit services to passengers. However, bus operation efficiency can be impacted by bus bunching, a problem originating from uncertain travel times between stops and time-varying passenger demand rates. This problem is notably exacerbated when the bus system operates along a signalized corridor in the face of unpredictable travel demand. To mitigate this challenge, we introduce a multi-strategy fusion approach for the longitudinal control of connected and automated buses. The approach is driven by a physics-informed deep reinforcement learning (DRL) algorithm and takes into account a variety of traffic conditions along urban signalized corridors. Taking advantage of connected and autonomous vehicle (CAV) technology, the proposed approach can leverage real-time information regarding bus operating conditions and road traffic environment. By integrating the aforementioned information into the DRL-based bus control framework, our designed physics-informed DRL state fusion approach and reward function efficiently embed prior physics and leverage the merits of equilibrium and consensus concepts from control theory. This integration enables the framework to learn and adapt multiple control strategies to effectively manage complex traffic conditions and fluctuating passenger demands. Three control variables, i.e., dwell time at stops, speed between stations, and signal priority, are formulated to minimize travel duration and ensure bus stability with the aim of avoiding bus bunching. We present simulation results to validate the effectiveness of the proposed approach, underlining its superior performance when subjected to sensitivity analysis, specifically considering factors such as traffic volume, desired speed, and traffic signal conditions. 
</p>

<div style="clear: both;"></div>
<hr/>

  </section>

  <!-- 面板 3：Traffic Management -->
  <section id="panel-management" class="tab-panel" markdown="1">
  <a id="traffic-management"></a>

### 3  Traffic management
In addition to the above-emerging technologies for microscopic CAV and ITS modeling, prediction, and control, my research extends to traffic management strategies for diverse regions, including urban, rural, and tribal areas. This work involves developing traffic control solutions for mixed road networks, recovering traffic flow data in large-scale urban systems, enhancing safety programs for tribal and rural regions, and travel data analysis.

### 3.1  Traffic control and network design strategies for mixed urban and expressway systems
Regarding urban traffic management, we have explored strategies for mitigating congestion in mixed road networks that combine expressways and arterial roads. By employing traffic models such as the multi-class cell transmission model (CTM) and the macroscopic fundamental diagram (MFD), we aim to enhance coordination between these interconnected systems. Additionally, we propose a cooperative flow‑control strategy for large‑scale urban networks that seamlessly links expressways and surface streets. 

### [The expressway network design problem for multiple urban subregions based on the macroscopic fundamental diagram](https://onlinelibrary.wiley.com/doi/full/10.1111/mice.13435) 
<p>
  <img src="/images/Expressway.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
With the advancement of urbanization, cities are constructing expressways to meet complex travel demands. However, traditional link-based road network design methods face challenges in addressing large-scale expressway network design problems. This study proposes an expressway network design method tailored for multi-subregion road networks. The method employs the macroscopic fundamental diagram to model arterial dynamics and the cell transmission model to capture expressway dynamics. A stochastic user equilibrium model is further established for route choice, and a decision model is developed to minimize total time spent. Simulations show that new expressways alleviate network congestion, with significant effects in the initial stages. Moreover, route guidance strategies and driver compliance also influence the schemes. 
</p>

<div style="clear: both;"></div>
<hr/>

### [A Cooperation Control for Multiple Urban Regions Traffic Flow Coupled With an Expressway Network](https://ieeexplore.ieee.org/abstract/document/11045413) 
<p>
  <img src="/images/Cooperation.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
As cities expand and long-distance travel demand increases, expressways are usually constructed to enhance regional connectivity. In the mixed road networks of urban roads and expressways, coordinating the distinct traffic dynamics of the two networks is a challenge. To address this challenge, we propose a cooperative flow control method for large-scale mixed networks. First, we develop an integrated traffic model that models urban regions using the macroscopic fundamental diagram (MFD) and expressways using the multi-class cell transmission model (CTM), achieving route tracking of vehicles throughout the entire mixed network. Next, a route choice model is developed to allocate new traffic demands within the mixed network. To coordinate traffic flow, a perimeter control (PC) is conducted to manage transfer flows between region boundaries, ramp metering (RM) to regulate flows entering expressways from urban regions, and variable speed limit (VSL) to control mainline speeds on expressways. We establish this cooperative flow control method within a model predictive control (MPC) framework. Case studies show that, based on the implementation of PC, the combined application of RM and VSL to the expressway system is more effective in reducing congestion and improving traffic efficiency in the mixed network than using RM and VSL independently. 
</p>

<div style="clear: both;"></div>
<hr/>

### 3.2  Traffic flow recovery for large-scale urban transportation network
To address the challenge of recovering accurate and high-resolution traffic flow data in large-scale urban transportation networks with limited sensor coverage, we developed the Analytical Optimized Recovery (AOR) framework to reconstruct comprehensive traffic flow patterns. 

### [Analytical Optimized Traffic Flow Recovery for Large-scale Urban Transportation Network](https://arxiv.org/abs/2409.03906) 
<p>
  <img src="/images/Analytical.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
The implementation of intelligent transportation systems (ITS) has enhanced data collection in urban transportation through advanced traffic sensing devices. However, the high costs associated with installation and maintenance result in sparse traffic data coverage. To obtain complete, accurate, and high-resolution network-wide traffic flow data, this study introduces the Analytical Optimized Recovery (AOR) approach that leverages abundant GPS speed data alongside sparse flow data to estimate traffic flow in large-scale urban networks. The method formulates a constrained optimization framework that utilizes a quadratic objective function with l2 norm regularization terms to address the traffic flow recovery problem effectively and incorporates a Lagrangian relaxation technique to maintain non-negativity constraints. The effectiveness of this approach was validated in a large urban network in Shenzhen's Futian District using the Simulation of Urban MObility (SUMO) platform. Analytical results indicate that the method achieves low estimation errors, affirming its suitability for comprehensive traffic analysis in urban settings with limited sensor deployment. 
</p>

<div style="clear: both;"></div>
<hr/>

### 3.3  Traffic safety analysis and improvement
In addition to my focus on urban traffic management, we also aim to address the pressing need for improved transportation safety programs in tribal lands, which typically experience higher crash rates and severities. My research concentrates on enhancing tribal crash reporting and data quality, which is essential for identifying high-risk locations and developing effective safety programs. 

### [How to Collect Tribal Crash Data Properly? Experience from a New Wisconsin Crash Reporting System](https://ascelibrary.org/doi/abs/10.1061/9780784484333.005) 
<p>
  <img src="/images/Tribal1.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
Developing effective transportation safety programs for tribal lands is important due to higher crash rates and crash severities in those areas. Correspondingly, a comprehensive tribal crash reporting and crash data quality are imperative to analyze and identify high crash locations and to develop and fund effective tribal safety programs. This study presents quantitative and spatial data analyses to validate the effectiveness of tribal crash data elements on the Wisconsin police crash report with respect to three attributes: location, jurisdiction, and law enforcement agency. The results indicate that these tribal attributes are coupled with other standard location attributes, which negatively affects data quality for further analysis. The findings recommend that adding an independent subfield in the national standard crash classification for tribal elements and adding a specific tribal road type to the roadway data elements would be more effective for tribal crash reporting and analysis, which facilitates further safety analysis regarding all roadway types within tribal lands. 
</p>

<div style="clear: both;"></div>
<hr/>

### [Developing a Conceptual Tribal Crash Safety Dashboard: Data-Driven Strategies for Identifying High-Risk Areas and Enhancing Tribal Safety Programs](https://arxiv.org/abs/2308.08177) 
<p>
  <img src="/images/Tribal2.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
Tribal lands in the United States have consistently exhibited higher crash rates and injury severities compared to other regions. To address this issue, effective data-driven safety analysis methods are essential for resource allocation and tribal safety program development. This study outlines the minimum data requirements and presents a generic tribal crash dashboard prototype to enable feasible and reproducible tribal crash analysis. The dashboard offers statistical performance measurement techniques, tracks tribal safety trends using various indicators, and updates in with incoming data, making it adaptable for any state. Specifically, the dashboard's capabilities are showcased using Wisconsin tribal crash data, locating high-risk tribal land areas while analyzing and comparing statewide crashes and tribal crashes based on severity. The results reveal that tribal land roads, particularly rural ones, are more dangerous than those in other Wisconsin areas. The dashboard also examines crash types to uncover the causes and insights behind Wisconsin tribal crashes. Demonstrating this dashboard concept reveals its potential to facilitate a more intuitive understanding of tribal crashes from a statistical standpoint, thereby enabling more effective applications of available data sources and the development of targeted safety countermeasures.
</p>

<div style="clear: both;"></div>
<hr/>

### 3.4  Travel data analysis
We also aim to address the challenge of extracting meaningful travel features from disorganized public transportation data by leveraging trajectory mining and inference to enhance bus services and improve the attractiveness of public transit.

### [Bus travel feature inference with small samples based on multi-clustering topic model over Internet of Things](https://www.sciencedirect.com/science/article/pii/S0167739X24004898) 
<p>
  <img src="/images/BusTravel.png" alt="GNP goal-based neural physics model"
       style="float:left; width:clamp(140px,38%,350px); height:auto; margin:0 16px 8px 0;" />
With the widespread application of Internet of Things (IoT) technology, there has been a shift from a broad-brush to a more refined approach in traffic optimization. An increasing amount of IoT data is being utilized in trajectory mining and inference, offering more precise characteristic information for optimizing public transportation. Services that optimize public transit based on inferred travel characteristics can enhance the appeal of public transport, increase its likelihood as a travel choice, alleviate traffic congestion, and reduce carbon emissions. However, the inherent complexities of disorganized and unstructured public transportation data pose significant challenges to extracting travel features. This study explores the enhancement of bus travel by integrating advanced technologies like positioning systems, IoT, and AI to infer features in public transportation data. It introduces the MK-LDA (MeanShift Kmeans Latent Dirichlet Allocation), a novel thematic modeling technique for deducing characteristics of public transit travel using limited travel trajectory data. The model employs a segmented inference methodology, initially leveraging the Mean-shift clustering algorithm to create POI seeds, followed by the P-K-means algorithm for discerning patterns in user travel behavior and extracting travel modalities. Additionally, a P-LDA (POI-Latent Dirichlet Allocation) inference algorithm is proposed to examine the interplay between travel characteristics and behaviors, specifically targeting attributes significantly correlated with public transit usage, including age, occupation, gender, activity levels, cost, safety, and personality traits. Empirical validation highlights the efficacy of this thematic modeling-based inference technique in identifying and predicting travel characteristics and patterns, boasting enhanced interpretability and outperforming conventional benchmarks.
</p>

<div style="clear: both;"></div>
<hr/>

  </section>
</div>

<script>
/* 根据 URL Hash (#behavior / #cav-control / #traffic-management) 激活对应 Tab */
(function() {
  const map = {
    "#behavior": "tab-behavior",
    "#cav-control": "tab-cav-control",
    "#traffic-management": "tab-management"
  };

  function activateFromHash() {
    const id = map[location.hash];
    if (id) {
      const radio = document.getElementById(id);
      if (radio) {
        radio.checked = true;
        const top = document.getElementById("tabs-top");
        if (top && top.scrollIntoView) top.scrollIntoView({behavior: "instant", block: "start"});
      }
    }
  }

  window.addEventListener("hashchange", activateFromHash);
  activateFromHash();
})();
</script>
