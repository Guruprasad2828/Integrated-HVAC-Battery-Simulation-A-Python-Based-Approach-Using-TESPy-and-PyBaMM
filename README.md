# Integrated-HVAC-Battery-Simulation-A-Python-Based-Approach-Using-TESPy-and-PyBaMM
I developed a fully open-source simulation framework by integrating two advanced Python libraries — TESPy for modeling a basic automotive HVAC system, and PyBaMM for detailed electrochemical battery simulation.

The goal was to analyze the dynamic interaction between cabin cooling demands and battery behavior in electric vehicles, while maintaining a defined cabin temperature. Unlike traditional tools that rely on static load assumptions or simplified battery models, this framework uses real-time compressor power output from TESPy as a dynamic input into PyBaMM, allowing precise tracking of State of Charge (SoC), Open Circuit Voltage (OCV), and other key battery parameters.

This approach supports greater flexibility, insight, and transparency—especially beneficial in early-stage design and system analysis


 # Key Takeaways:

1) ##### Open-Source Frameworks for Cost Saving
Leveraging TESPy and PyBaMM removes the dependency on proprietary tools like GT ISE, GT POST, and Simscape, eliminating license costs and enabling scalable simulation for budget-conscious R&D teams.

2) ##### Simulation Time Efficiency
Simulations run relatively fast compared to commercial software, although time depends on model complexity. For simpler HVAC-battery couplings, performance is quite responsive.

3) ##### Enhanced Parameter Tracking & System Insight
The framework enables full visibility into system performance, allowing users to track compressor power, cabin temperature, SoC, OCV, and other library-documented variables—greatly enhancing optimization and diagnostic potential.

4) ##### Complex HVAC Modeling with TESPy
TESPy supports detailed HVAC modeling and even engine thermodynamics, making it applicable not just to EVs but also to ICE-based vehicle systems.

5) ##### PID Tuning for Refrigerant Mass Flow Rate
PID control logic must be properly tuned to regulate refrigerant mass flow and ensure stable temperature maintenance—customizable for different thermal environments.

6) ##### Integration of Standalone Models
Both TESPy and PyBaMM are modular; the user must carefully build the integration loop. Since TESPy is highly sensitive to parameter constraints, loop stability requires attention to avoid solver failures.

7) ##### Battery Model Comparison Challenges
Resistance curves or voltage responses from PyBaMM may not match GT-Suite or Simscape directly due to solver differences, making cross-tool comparisons unreliable without calibration.

# Assumptions:

 Both the TESPy and PyBaMM models developed are relatively simple; however, each library offers strong potential for modeling more complex systems. Integrating the two standalone models is challenging, as it can result in under- or over-constraining the overall system. 
