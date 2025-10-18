# NeuroScope: Reverse Engineering Deep Neural Network on Edge Devices using Dynamic Analysis
**Conference:** USENIX Security 2025 

**Link:** [Paper PDF](https://www.usenix.org/system/files/usenixsecurity25-wu-ruoyu.pdf)
---

## Summary

This paper presents **NeuroScope**, a framework that can **reverse engineer deep neural networks** running on edge devices.  
It uses **dynamic analysis** — meaning it observes the program while it’s running — to capture inputs and outputs of neural network operators (like convolution, pooling, etc.).  

Then it uses machine learning models to **reconstruct the architecture** of the network, including layer types, order, and parameters.  

The motivation is that edge devices often store valuable AI models locally, and attackers could steal them to learn proprietary architectures or data. NeuroScope shows that this is a realistic threat even without direct model access.

**Key points:**
- Works on compiled binaries of DNNs (no source code needed).  
- Supports multiple architectures and frameworks.  
- Demonstrates successful recovery on various hardware.  
- Highlights how current model protection mechanisms are weak.
