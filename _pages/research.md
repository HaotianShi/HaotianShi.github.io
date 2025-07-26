---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

The rapid advancement of communication, vehicle automation technologies, and artificial intelligence (AI) is transforming intelligent transportation systems (ITS), offering opportunities to enhance safety, efficiency, and energy. Motivated by these developments, my research focuses on 1) interactive driving behavior modeling and prediction, 2) optimal control of connected and automated vehicles (CAVs) in mixed traffic environments, and 3) traffic management for urban, rural, and tribal regions. My research philosophy hinges on addressing challenges in these areas by integrating traditional analytical methods, such as physics-based modeling, control theory, and traffic flow theory, with emerging technologies like machine learning (ML) and foundation models (FMs)/large language models (LLMs). In line with my research philosophy, I have developed generic and interpretable methodological frameworks and computational models to analyze and improve transportation system performance in terms of mobility, safety, stability, and energy consumption. These models are validated through field implementations using Level 3 CAVs.

## Major Research Areas <br>
Over the years, I have investigated the following three broad areas of research: 1) interactive driving behavior modeling and prediction, 2) optimal control of connected and automated vehicles (CAV) in mixed traffic environments, and 3) traffic management for urban, rural, and tribal regions. A selection of my papers is provided in the reference section for further reading. 

### 1 Interactive driving behavior modeling and prediction
With the integration of Autonomous Vehicles (AVs) and CAVs, the dynamics of mixed traffic flows have shifted significantly compared to traditional traffic conditions. In mixed traffic, human-driven vehicle (HV) behaviors exhibit greater variability and uncertainty, particularly in longitudinal car-following and lateral maneuvers. These factors heighten traffic safety risks and complicate the decision-making processes of AVs. To address these challenges, we have developed novel modeling and prediction methodologies for both AVs and HVs, focusing on longitudinal and lateral driving behaviors. These methodologies leverage approaches including physics-based models, machine learning (ML), physics-informed machine learning (PIML), and foundation models (FMs)/large language models (LLMs).

### 1.1  Multi-scale car-following and traffic dynamics modeling methodologies for HVs and AVs
In a mixed traffic environment, it is crucial to model and accurately calibrate car-following behaviors of both HVs and AVs. This provides critical information about the driving characteristics of surrounding vehicles for CAVs to optimize their decision-making processes. However, current car-following models based on either physics or ML often struggle to accurately capture the uncertainty in driving behaviors and typically overlook the influence of macroscopic traffic flow (traffic dynamics) on individual driving behaviors. In this regard, We have developed models using both physics-based approaches and ML techniques. 

### [Generative adversarial network for car following trajectory generation and anomaly detection](https://www.tandfonline.com/doi/abs/10.1080/15472450.2023.2301691)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/gan.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Car-following trajectory generation and anomaly detection are critical functions in the sensing module of an automated vehicle. However, developing models that capture realistic trajectory data distribution and detect anomalous driving behaviors could be challenging. This paper proposes ‘TrajGAN’, an unsupervised learning approach based on the Generative Adversarial Network (GAN) to exploit vehicle car following trajectory data for generation and anomaly detection. The proposed TrajGAN consists of two modules, an encoder-decoder Long Short-Term Memory (LSTM)-based generator and an LSTM-multilayer perceptron (MLP) based discriminator, whose former component is used to generate vehicular car following trajectories and the latter one is for trajectory anomaly detection. By letting these two modules game with each other in training, we can simultaneously achieve robust trajectory generators and anomaly detectors. Trained with the Next Generation Simulation (NGSIM) dataset, TrajGAN can generate realistic trajectories with a similar distribution of training data and identify a manifold of anomalous trajectories based on an anomaly scoring scheme. Simulation results indicate that the proposed approach is efficient in reproducing artificial trajectories and identifying anomalous driving behaviors.</p>
  </div>
</div>

---

### [Bi-scale car-following model calibration based on corridor-level trajectory](https://www.sciencedirect.com/science/article/abs/pii/S1366554524000887)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/BiScale.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>The precise estimation of macroscopic traffic parameters, such as travel time and fuel consumption, is essential for the optimization of traffic management systems. Despite its importance, the comprehensive acquisition of vehicle trajectory data for the calculation of these macroscopic measures presents a challenge. To bridge this gap, this study aims to calibrate car-following models capable of predicting both microscopic measures and macroscopic measures. We conduct a numerical analysis to trace the cumulative process of model prediction errors across various measurements, and our findings indicate that macroscopic measures encapsulate the accumulation of model errors. By incorporating macroscopic measures into vehicle model calibration, we can mitigate the impact of noise on microscopic data measurements. We compare three car-following model calibration methods: MiC (using microscopic measurements), MaC (using macroscopic measurements), and BiC (using both microscopic and macroscopic measurements)—utilizing real-world trajectory data. The BiC method emerges as the most successful in reconstructing vehicle trajectories and accurately estimating travel time and fuel consumption, whereas the MiC method leads to overfitting and inaccurate macro-measurement predictions. This study underscores the importance of bi-scale calibration for precise traffic and energy consumption predictions, laying the groundwork for future research aimed at enhancing traffic management strategies.</p>
  </div>
</div>

---

### [Development, Calibration, and validation of a Novel nonlinear Car-Following Model: Multivariate piecewise linear approach for adaptive cruise control vehicles](https://www.sciencedirect.com/science/article/pii/S1366554525000729)  
<p>
  <img src="/images/MPL.png" alt="MPL model"
       style="float:left; width:clamp(140px,28%,300px); height:auto; margin:0 16px 8px 0;" />
  As advanced driver-assistance systems (ADAS) are more widely implemented—particularly the adaptive cruise control (ACC) system in car-following behavior—accurate modeling of ACC vehicles’ behavior is needed. Currently, each vehicle manufacturer develops its ACC systems with unique controllers, creating “black boxes” that are not openly accessible for analysis. In addition, the vehicle dynamics that use sensor and dynamics systems introduce complicated inherent nonlinearity in ACC-equipped vehicles’ behaviors (hereinafter referred to as ACC vehicles). Given the complex inherent nonlinearity of ACC systems, traditional vehicle behavior modeling methods have to trade off between modeling accuracy and interpretability. To address these challenges, this study introduces an innovative multivariate piecewise linear (MPL) car-following modeling methodology to emulate any ACC system from observational data. The MPL modeling methodology allows for several empirical quantifications of the unknown design parameters of the different ACC systems as they are manifested in the vehicles’ driving behavior. This approach distinguishes itself from traditional piecewise linear models by incorporating multiple breakpoints. These breakpoints serve to capture the inherent nonlinearity of ACC vehicle dynamics across a range of linear functions. Simultaneously, these breakpoints are empirically derived from actual trajectory data, thereby enhancing modeling accuracy. A case study illustrates four calibrated MPL models based on a large-scale field automated vehicle experiment dataset. Compared to other models, the MPL models show sufficient accuracy and interpretability. This robust and transparent modeling methodology may serve as an analytical tool for future transportation planning.
</p>

<div style="clear: both;"></div>
<hr/>
---

### [Physically Analyzable AI-Based Nonlinear Platoon Dynamics Modeling During Traffic Oscillation: A Koopman Approach](https://ieeexplore.ieee.org/abstract/document/10954270)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/Koopman.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Given the complexity and nonlinearity inherent in traffic dynamics within vehicular platoons, there exists a critical need for a modeling methodology with high accuracy while concurrently achieving physical analyzability. Currently, there are two predominant approaches: the physics model-based approach and the Artificial Intelligence (AI)–based approach. Knowing the facts that the physical-based model usually lacks sufficient modeling accuracy and potential function mismatches and the pure-AI-based method lacks analyzability, this paper innovatively proposes an AI-based Koopman approach to model the unknown nonlinear platoon dynamics harnessing the power of AI and simultaneously maintaining physical analyzability, with a particular focus on periods of traffic oscillation. Specifically, this research first employs a deep learning framework to generate the embedding function that lifts the original space into the embedding space. Given the embedding space descriptiveness, the platoon dynamics can be expressed as a linear dynamical system founded by the Koopman theory. Based on that, the routine of linear dynamical system analysis can be conducted on the learned traffic linear dynamics in the embedding space. By that, the physical interpretability and analyzability of model-based methods with the heightened precision inherent in data-driven approaches can be synergized. Comparative experiments have been conducted with existing modeling approaches, which suggest our method’s superiority in accuracy. Additionally, a phase plane analysis is performed, further evidencing our approach’s effectiveness in replicating the complex dynamic patterns. Moreover, the proposed methodology is proven to feature the capability of analyzing the stability, attesting to the physical analyzability.</p>
  </div>
</div>

---


### [FollowGen: A Scaled Noise Conditional Diffusion Model for Car-Following Trajectory Prediction](https://arxiv.org/abs/2411.16747)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/FollowGen.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Vehicle trajectory prediction is crucial for advancing autonomous driving and advanced driver assistance systems (ADAS). Although deep learning-based approaches - especially those utilizing transformer-based and generative models - have markedly improved prediction accuracy by capturing complex, non-linear patterns in vehicle dynamics and traffic interactions, they frequently overlook detailed car-following behaviors and the inter-vehicle interactions critical for real-world driving applications, particularly in fully autonomous or mixed traffic scenarios. To address the issue, this study introduces a scaled noise conditional diffusion model for car-following trajectory prediction, which integrates detailed inter-vehicular interactions and car-following dynamics into a generative framework, improving both the accuracy and plausibility of predicted trajectories. The model utilizes a novel pipeline to capture historical vehicle dynamics by scaling noise with encoded historical features within the diffusion process. Particularly, it employs a cross-attention-based transformer architecture to model intricate inter-vehicle dependencies, effectively guiding the denoising process and enhancing prediction accuracy. Experimental results on diverse real-world driving scenarios demonstrate the state-of-the-art performance and robustness of the proposed method.</p>
  </div>
</div>

---


### [Physical enhanced residual learning (PERL) framework for vehicle trajectory prediction](https://www.sciencedirect.com/science/article/pii/S277242472500006X)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/PERL.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Vehicle trajectory prediction is crucial for advancing autonomous driving and advanced driver assistance systems (ADAS). Although deep learning-based approaches - especially those utilizing transformer-based and generative models - have markedly improved prediction accuracy by capturing complex, non-linear patterns in vehicle dynamics and traffic interactions, they frequently overlook detailed car-following behaviors and the inter-vehicle interactions critical for real-world driving applications, particularly in fully autonomous or mixed traffic scenarios. To address the issue, this study introduces a scaled noise conditional diffusion model for car-following trajectory prediction, which integrates detailed inter-vehicular interactions and car-following dynamics into a generative framework, improving both the accuracy and plausibility of predicted trajectories. The model utilizes a novel pipeline to capture historical vehicle dynamics by scaling noise with encoded historical features within the diffusion process. Particularly, it employs a cross-attention-based transformer architecture to model intricate inter-vehicle dependencies, effectively guiding the denoising process and enhancing prediction accuracy. Experimental results on diverse real-world driving scenarios demonstrate the state-of-the-art performance and robustness of the proposed method.</p>
  </div>
</div>

---

### 1.2  Interaction-aware two-dimensional (2D) trajectory prediction 
Accurate prediction of human-driven vehicle trajectories is essential for decision-making and control in CAVs. In dynamic and complex environments, vehicle behavior is influenced by its own historical actions and interactions with surrounding vehicles, which complicates the precise prediction of future longitudinal and lateral movements. We proposed the following methodologies to address the 2D trajectory prediction challenges.

### [Graph-Based Interaction-Aware Multimodal 2D Vehicle Trajectory Prediction Using Diffusion Graph Convolutional Networks](https://ieeexplore.ieee.org/abstract/document/10352973)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/Graph.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Predicting vehicle trajectories is crucial to ensuring automated vehicle operation efficiency and safety, particularly on congested multi-lane highways. In such dynamic environments, a vehicle's motion is determined by its historical behaviors as well as interactions with surrounding vehicles. These intricate interactions arise from unpredictable motion patterns, leading to a wide range of driving behaviors that warrant in-depth investigation. This study presents the Graph-based Interaction-aware Multi-modal Trajectory Prediction (GIMTP) framework, designed to probabilistically predict future vehicle trajectories by effectively capturing these interactions. Within this framework, vehicles' motions are conceptualized as nodes in a time-varying graph, and the traffic interactions are represented by a dynamic adjacency matrix. To holistically capture both spatial and temporal dependencies embedded in this dynamic adjacency matrix, the methodology incorporates the Diffusion Graph Convolutional Network (DGCN), thereby providing a graph embedding of both historical states and future states. Furthermore, we employ a driving intention-specific feature fusion, enabling the adaptive integration of historical and future embeddings for enhanced intention recognition and trajectory prediction. This model gives two-dimensional predictions for each mode of longitudinal and lateral driving behaviors and offers probabilistic future paths with corresponding probabilities, addressing the challenges of complex vehicle interactions and multi-modality of driving behaviors. Validation using real-world trajectory datasets demonstrates the efficiency and potential.</p>
  </div>
</div>

---

### [Hypergraph-based Motion Generation with Multi-modal Interaction Relational Reasoning](https://arxiv.org/abs/2409.11676)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/Hypergraph.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>The intricate nature of real-world driving environments, characterized by dynamic and diverse interactions among multiple vehicles and their possible future states, presents considerable challenges in accurately predicting the motion states of vehicles and handling the uncertainty inherent in the predictions. Addressing these challenges requires comprehensive modeling and reasoning to capture the implicit relations among vehicles and the corresponding diverse behaviors. This research introduces an integrated framework for autonomous vehicles (AVs) motion prediction to address these complexities, utilizing a novel \textbf{R}elational \textbf{H}ypergraph \textbf{I}nteraction-informed \textbf{N}eural m\textbf{O}tion generator (\texttt{RHINO}). \texttt{RHINO} leverages hypergraph-based relational reasoning by integrating a multi-scale hypergraph neural network to model group-wise interactions among multiple vehicles and their multi-modal driving behaviors, thereby enhancing motion prediction accuracy and reliability. Experimental validation using real-world datasets demonstrates the superior performance of this framework in improving predictive accuracy and fostering socially aware automated driving in dynamic traffic scenarios.</p>
  </div>
</div>

---

### [Goal-based Neural Physics Vehicle Trajectory Prediction Model](https://arxiv.org/pdf/2409.15182)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/Goal.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Vehicle trajectory prediction plays a vital role in intelligent transportation systems and autonomous driving, as it significantly affects vehicle behavior planning and control, thereby influencing traffic safety and efficiency. Numerous studies have been conducted to predict short-term vehicle trajectories in the immediate future. However, long-term trajectory prediction remains a major challenge due to accumulated errors and uncertainties. Additionally, balancing accuracy with interpretability in the prediction is another challenging issue in predicting vehicle trajectory. To address these challenges, this paper proposes a \textbf{G}oal-based \textbf{N}eural \textbf{P}hysics Vehicle Trajectory Prediction Model (\textbf{GNP}). The GNP model simplifies vehicle trajectory prediction into a two-stage process: determining the vehicle's goal and then choosing the appropriate trajectory to reach this goal. The GNP model contains two sub-modules to achieve this process. The first sub-module employs a multi-head attention mechanism to accurately predict \textbf{goals}. The second sub-module integrates a deep learning model with a physics-based social force model to progressively predict the complete trajectory using the generated goals. The GNP demonstrates state-of-the-art long-term prediction accuracy compared to four baseline models. We provide interpretable visualization results to highlight the multi-modality and inherent nature of our neural physics framework. Additionally, ablation studies are performed to validate the effectiveness of our key designs. The source code for this work are available at: \url{https://github.com/mcgrche/GNP--Goal-based-Neural-Physics-Vehicle-Trajectory-Prediction-Model}.</p>
  </div>
</div>

---

### 1.3  Large Vision-Language Models (VLMs) enabled prediction and planning for autonomous driving
Motivated by the emergent reasoning capabilities of LLMs and VLMs, we also focus on the application of VLMs in enhancing prediction and planning for end-to-end (E2E) autonomous driving, leveraging their multimodal understanding to improve decision-making and safety. 

### [Goal-based Neural Physics Vehicle Trajectory Prediction Model](https://arxiv.org/pdf/2409.15182)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/Goal.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Vehicle trajectory prediction plays a vital role in intelligent transportation systems and autonomous driving, as it significantly affects vehicle behavior planning and control, thereby influencing traffic safety and efficiency. Numerous studies have been conducted to predict short-term vehicle trajectories in the immediate future. However, long-term trajectory prediction remains a major challenge due to accumulated errors and uncertainties. Additionally, balancing accuracy with interpretability in the prediction is another challenging issue in predicting vehicle trajectory. To address these challenges, this paper proposes a \textbf{G}oal-based \textbf{N}eural \textbf{P}hysics Vehicle Trajectory Prediction Model (\textbf{GNP}). The GNP model simplifies vehicle trajectory prediction into a two-stage process: determining the vehicle's goal and then choosing the appropriate trajectory to reach this goal. The GNP model contains two sub-modules to achieve this process. The first sub-module employs a multi-head attention mechanism to accurately predict \textbf{goals}. The second sub-module integrates a deep learning model with a physics-based social force model to progressively predict the complete trajectory using the generated goals. The GNP demonstrates state-of-the-art long-term prediction accuracy compared to four baseline models. We provide interpretable visualization results to highlight the multi-modality and inherent nature of our neural physics framework. Additionally, ablation studies are performed to validate the effectiveness of our key designs. The source code for this work are available at: \url{https://github.com/mcgrche/GNP--Goal-based-Neural-Physics-Vehicle-Trajectory-Prediction-Model}.</p>
  </div>
</div>

---

### [Goal-based Neural Physics Vehicle Trajectory Prediction Model](https://arxiv.org/pdf/2409.15182)  
<div style="display: flex; align-items: flex-start; margin-bottom: 15px;">
  <!-- Image Section with dynamic sizing -->
  <div style="flex: 0 0 auto; margin-right: 20px;">
    <img src="/images/Goal.png" style="max-width: 350px; height: auto;" />
  </div>
  <!-- Abstract Section -->
  <div style="flex: 1;">
    <p>Vehicle trajectory prediction plays a vital role in intelligent transportation systems and autonomous driving, as it significantly affects vehicle behavior planning and control, thereby influencing traffic safety and efficiency. Numerous studies have been conducted to predict short-term vehicle trajectories in the immediate future. However, long-term trajectory prediction remains a major challenge due to accumulated errors and uncertainties. Additionally, balancing accuracy with interpretability in the prediction is another challenging issue in predicting vehicle trajectory. To address these challenges, this paper proposes a \textbf{G}oal-based \textbf{N}eural \textbf{P}hysics Vehicle Trajectory Prediction Model (\textbf{GNP}). The GNP model simplifies vehicle trajectory prediction into a two-stage process: determining the vehicle's goal and then choosing the appropriate trajectory to reach this goal. The GNP model contains two sub-modules to achieve this process. The first sub-module employs a multi-head attention mechanism to accurately predict \textbf{goals}. The second sub-module integrates a deep learning model with a physics-based social force model to progressively predict the complete trajectory using the generated goals. The GNP demonstrates state-of-the-art long-term prediction accuracy compared to four baseline models. We provide interpretable visualization results to highlight the multi-modality and inherent nature of our neural physics framework. Additionally, ablation studies are performed to validate the effectiveness of our key designs. The source code for this work are available at: \url{https://github.com/mcgrche/GNP--Goal-based-Neural-Physics-Vehicle-Trajectory-Prediction-Model}.</p>
  </div>
</div>

---

### 2  Optimal control of CAVs in mixed traffic environments
To address the challenges posed by the stochastic nature of human-driven behaviors, the heterogeneity in traffic composition, and the partial observability characteristic of complex mixed traffic conditions involving both CAVs and HVs, optimizing CAV driving behavior from a systemic traffic flow perspective remains particularly difficult. In response to these challenges, we have conducted extensive research on decision-making control for CAVs in mixed traffic environments. By integrating the core principles of physics models, control theory, and traffic flow theory into a deep reinforcement learning (DRL) framework, I developed the physics-informed deep reinforcement learning (PIDRL) methodology, specifically designed for the intelligent control of CAVs and other ITS agents in mixed traffic scenarios. This generic methodology has proven versatile and effective in various applications, including CAV control and intelligent bus operations. It has been validated in improving key system-level performance metrics such as safety, efficiency, stability, and energy utilization.

### 2.1  Centralized multi-objective cooperative control for CAVs
A [centralized multi-objective cooperative control strategy](https://www.sciencedirect.com/science/article/abs/pii/S0968090X21004150) based on deep reinforcement learning is proposed to address the heterogeneity of mixed traffic flow. This approach decomposes the mixed traffic flow into multiple subsystem types, accommodating any heterogeneous combination of traffic fleets. Within each subsystem, targeted multi-objective cooperative control regarding safety, energy, and stability is applied to CAVs, enabling local optimization of the mixed traffic flow. Compared to advanced MPC and linear/nonlinear control methods, the proposed CAV control model significantly improves system stability, energy, safety, and mobility.

### 2.2  Distributed CAV control strategy considering communication loss
In response to the partial observability of mixed traffic flow and the stochastic nature of HV behavior, we propose a novel [distributed control strategy for CAVs](https://www.sciencedirect.com/science/article/abs/pii/S0968090X23000086) based on physics-informed DRL, offering a more practical implementation than centralized controllers. This work uniquely integrates traffic flow theory with consensus and equilibrium theories from control science within the DRL framework. Such integration enables a fusion of macroscopic traffic flow characteristics and multi-vehicle state data, effectively mitigating the stochastic nature of HDV behavior and reducing the propagation of traffic oscillations in mixed traffic flow. Furthermore, the proposed strategy [addresses the issue of Vehicle-to-Vehicle (V2V) communication loss](https://onlinelibrary.wiley.com/doi/abs/10.1111/mice.12825) by introducing a dynamic information flow fusion method, which mitigates the impact of communication disruptions. As a result, the approach significantly enhances traffic flow stability, safety, and efficiency across a wide range of traffic scenarios, including emergency situations.

Additionally, I have extended this generic framework from one-dimensional longitudinal control to a [two-dimensional car-following control strategy](https://www.sciencedirect.com/science/article/abs/pii/S0950705123002356) and a [predictive lane-changing control framework](https://ieeexplore.ieee.org/abstract/document/10988662). Given the inherent randomness of dynamic traffic environments and the variability of two-dimensional road curvatures, the two-dimensional car-following control addresses both car-following and lane-keeping strategies within a curvilinear coordinate system. This approach decomposes driving behaviors into longitudinal "string" behaviors and lateral "local" behaviors, offering a refined control mechanism for complex traffic scenarios. Through V2X communication, this physics-informed learning-based CAV control framework integrates traffic flow data with road geometry, optimizing CAV driving behaviors. Following the model development and simulations, we validated their field implementation, focusing on Level 3 CAVs to validate their practical applications. Our proposed model is applied to the CAV validating the superior performances regarding traffic oscillation dampening, safety, and fuel efficiency. 
 
### 2.3  Distributed dynamics bus control for reducing bus bunching 
We further extended the generic physics-informed control approach to develop [dynamic control systems for buses](https://onlinelibrary.wiley.com/doi/abs/10.1111/mice.12803). To mitigate the issue of bus bunching, which arises from uncertain travel times and fluctuating passenger demand, we proposed a dynamic control strategy for buses based on deep reinforcement learning (DRL). This strategy incorporates both historical and real-time traffic data to optimize bus operations. By improving the accuracy of schedules and maintaining consistent intervals between buses, the [proposed method](https://www.sciencedirect.com/science/article/abs/pii/S0952197624001441) effectively reduces deviations in timetables and bus spacing, thereby enhancing the overall efficiency and stability of the transit system.

### 3  Traffic management for urban, rural, and tribal regions
In addition to the above-emerging technologies for microscopic CAV and ITS modeling, prediction, and control, my research extends to traffic management strategies for diverse regions, including urban, rural, and tribal areas. This work involves developing traffic control solutions for mixed road networks, recovering traffic flow data in large-scale urban systems, and enhancing safety programs for tribal and rural regions.

### 3.1  Traffic control and network design strategies for mixed urban and expressway systems
Regarding urban traffic management, we have explored [strategies for mitigating congestion in mixed road networks](https://onlinelibrary.wiley.com/doi/abs/10.1111/mice.13435) that combine expressways and arterial roads. By employing traffic models such as the multi-class cell transmission model (CTM) and the macroscopic fundamental diagram (MFD), we aim to enhance coordination between these interconnected systems. We developed an integrated approach using route guidance, perimeter control, and ramp metering within a model predictive control (MPC) framework, which has proven effective in reducing congestion by optimizing traffic flow across expressways and arterial networks. Additionally, we propose a [cooperative flow‑control strategy for large‑scale urban networks](https://ieeexplore.ieee.org/abstract/document/11045413/) that seamlessly links expressways and surface streets. The approach couples a multi‑class cell transmission model for expressways with an MFD‑based representation of urban regions, so vehicles can be tracked across the entire network. A demand‑responsive route‑choice module assigns new trips, while perimeter control balances region‑to‑region transfers and ramp metering tempers expressway inflows—all coordinated by model‑predictive control.

### 3.2  Traffic flow recovery for large-scale urban transportation network
To address the challenge of recovering accurate and high-resolution traffic flow data in large-scale urban transportation networks with limited sensor coverage, we developed the [Analytical Optimized Recovery (AOR) framework](https://arxiv.org/abs/2409.03906). This method leverages widely available GPS speed data combined with sparse traffic flow observations to reconstruct comprehensive traffic flow patterns. By formulating a constrained optimization problem with a quadratic objective function and using Lagrangian relaxation to enforce non-negativity constraints, the AOR framework effectively recovers traffic flow data. This approach is validated through simulations on calibrated Shenzhen's urban network using SUMO.

### 3.3  Traffic safety analysis and improvement in tribal and rural areas
In addition to my focus on urban traffic management, we also aim to address the pressing need for improved transportation safety programs in tribal lands, which typically experience higher crash rates and severities. My research concentrates on [enhancing tribal crash reporting and data quality](https://ascelibrary.org/doi/abs/10.1061/9780784484333.005), which is essential for identifying high-risk locations and developing effective safety programs. Using the Wisconsin police crash report, the study validates the effectiveness of specific tribal data elements, such as location, jurisdiction, and law enforcement agency. The findings reveal the necessity for establishing an independent subcategory in national crash classification systems for tribal data and creating a distinct tribal road type within roadway data elements to enhance data quality for safety analyses in tribal areas. Furthermore, we conducted a comprehensive [tribal crash analysis](https://arxiv.org/abs/2308.08177), utilizing a dashboard prototype for statistical performance measurement and monitoring of safety trends in tribal lands. This dashboard, demonstrated with Wisconsin tribal crash data, effectively identifies high-risk areas and compares tribal crashes with statewide data based on severity and type. The research highlights the importance of high-quality, spatially referenced crash data and proposes a reproducible, data-driven approach to enhance tribal safety programs.
