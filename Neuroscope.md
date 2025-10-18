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

---

## Future Directions (Not in the Paper)

### 1. Make NeuroScope Better
- Try to make it work **faster** and analyze models while they are running.  
- Combine it with other signals like **power usage** or **timing patterns** to understand models more deeply.  
- Test it with **special input data** to reveal more details about hidden layers.  
- Use newer AI methods like **graph networks** or **transformers** to guess the structure more accurately.

### 2. Use It on New Kinds of Models
- Apply it to **Vision Transformers (ViTs)** and **attention-based networks**.  
- Test it on **small language models** that can run on phones or edge devices.  
- Try using it for **graph-based** or **brain-inspired models** in the future.

### 3. Run It on More Hardware
- Make it work on **FPGAs**, **mobile AI chips**, and **tiny microcontrollers**.  
- Support newer chip types like **RISC-V**, which are becoming popular for edge computing.

### 4. Build Better Protection
- Keep models safe by running them inside **secure hardware areas** (like ARM TrustZone).  
- **Change or update models often** so attackers can’t use stolen ones.  
- Add **hidden watermarks** or **security checks** to detect copied models.

### 5. Create Useful Tools
- Turn NeuroScope into a **testing tool** for checking if AI models are safe.  
- Use it in **security training** to help teams learn how attacks work and how to defend.  
- Use it for **verifying ownership** of AI models (to prove who made them).


---

## Personal Reflection
I found this paper very interesting because it shows how **model privacy** can be compromised even on local devices. It’s a good reminder that protecting AI models requires not just encryption, but also runtime protection.

---
