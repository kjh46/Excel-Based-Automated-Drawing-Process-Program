# 🔧 Excel-Based Automated Drawing Process Program

## 🌟 Project Overview

This project aims to develop an automated system for Excel-based drawing process calculations. It addresses the challenges of manual computation and multi-sheet Excel management by offering a consistent, accurate, and efficient solution for field use.

### 🗓️ Project Information

- **Project Name**: Excel-Based Automation Program Development  
- **Duration**: May – July 2025  
- **Job Role**: IT Development  
- **Participating Company**: RHINOX  
- **Team Leader**: Kim Yun-yeol  
- **Team Members**: Kim Ju-hyeong, Kim Hyeon-jung, Jeong Hyeok  

---

## ✨ Key Features

### ⚙️ Core Calculation Functions

The system performs automated calculations essential for the drawing process:

- **6 Input Variables**:
  - `K` – Plasticity Modulus  
  - `n` – Work Hardening Exponent  
  - `μ` – Friction Coefficient  
  - `d₀` – Initial Bar Diameter  
  - `d` – Final Bar Diameter  
  - `α` – Die Semi-Angle  

- **Automatic Calculations**:
  - $f_1 = \pi \cdot d_0^2 / 4$ (Initial area)  
  - $f_2 = \pi \cdot d^2 / 4$ (Final area)  
  - $Q_1 = \pi (d_0^2 - d^2) / (4 \sin(\alpha))$ (Effective area)  
  - $\epsilon_f = \ln(f_1 / f_2)$ (True strain)  
  - $k_{fm} = K \cdot \epsilon_f^n / (1 + n)$ (Average yield strength)  
  - $k_m = k_{fm} / \left[1 + \dfrac{F + Q_1 \mu}{2 f_2}\right]$ (Mean deformation resistance)  

- **Load Analysis**:
  - $Z_N = k_m (f_1 - f_2)$ – Pure Deformation Force  
  - $Z_R = Q_1 \cdot \mu \cdot k_m$ – Frictional Resistance  
  - $Z_S = 0.77 \cdot f_2 \cdot k_{fm} \cdot \left(\dfrac{\pi}{180} \cdot \alpha\right)$ – Internal Shear Force  

- **Final Judgement**:
  - $Z = Z_N + Z_R + Z_S$ – Total Drawing Force  
  - $\sigma = Z / f_2$ – Drawing Stress  
  - **Feasibility Rule**: If $\sigma < k_m$, then *Usable*; otherwise, *Not Usable*

---

### 💻 Functional Modules

- **Single Calculation**  
  Compute all results for a single input condition.

- **Cross-Section Reduction Analysis**  
  Simulate processability for 5% to 40% reduction rates with graphical visualization.

- **Batch Processing**  
  Perform calculations for multiple cases using CSV/Excel input.

---

## 🚀 Technology Stack

- **Python 3.10** – Main development language  
- **Streamlit** – Web application framework  
- **NumPy, Pandas** – Numerical and data processing  
- **Matplotlib** – Data visualization  
- **venv** – Virtual environment for dependency isolation  

---

## 📦 Program Structure
```
ProjectFolder/
├── venv/ # Virtual environment
├── app_extended.py # Main Streamlit app
├── launch_app.bat # One-click launch file
├── README.txt # Basic usage and installation guide

```
---

## 💡 Key Challenges & Solutions

| Challenge                     | Solution                                                                 |
|------------------------------|--------------------------------------------------------------------------|
| Complex installation process | Bundled virtual environment for seamless offline deployment             |
| User accessibility           | One-click launch via `.bat` file with step-by-step user manual          |
| Offline environment support  | All dependencies included for server-free local execution               |

---

## 📈 Expected Benefits & Future Directions

### 🏢 Internal Utilization

- Ready-to-use by production engineering departments  
- Enhances quality control reliability  

### 💰 Business Impact

- Reduces error-related production losses  
- Boosts operational efficiency and productivity  

### 🔭 Future Expansion

- Support for other forming processes (e.g., extrusion, forging)  
- Cloud-based web version  
- AI-powered optimization and recommendation system  
- IoT integration for real-time data feedback  

---

## 📝 Installation & Execution

### 1. Install Python 3.10.x

- Download from: [Python 3.10.9](https://www.python.org/downloads/release/python-3109/)  
- During installation:
  - ✅ Check **"Add Python to PATH"**  
  - ✅ Check **"Install for all users"** (if available)  

### 2. Prepare Project Files

- Extract the provided ZIP file  
- Place the folder under: `C:\DrawingClean`  
  (Modify `cd` path in `launch_app.bat` if different)

### 3. Launch the Application

- Double-click `launch_app.bat`  
- A browser will open automatically with the app interface

---

## 🖼️ Screenshots

### ✅ Single Calculation (Feasible)
[Single Feasible 1]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/42e6e39c-5c73-4fc6-bcd3-1d95dd53f670"/>  
[Single Feasible 2]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/fcba9f5e-e621-4689-af63-8218967f8973" />



### ❌ Single Calculation (Not Feasible)
[Single Not Feasible 1]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/aee3fe36-07db-41f6-90ee-b06dc20f6537" />
[Single Not Feasible 2]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/ee41006d-1698-4815-90e0-0df46bdac8bc" />


### 📊 Area Reduction Rate Analysis
[Reduction Analysis 1]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/d2f553e2-167b-4bc3-9c7e-3ac3bccd1a77" />
[Reduction Analysis 2]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/277d1b58-a71e-4bc7-acc0-397d1911f705" />


### 🗃️ Batch Processing
[Batch 1]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/3272c869-169a-4cd0-9c51-da5750421a53" />
[Batch 2]<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/50a8bb71-a821-4421-9b7a-b1b9cc0ba0f7" />


---

> _"Beyond being a simple calculation tool, this project improves real-world workflow and takes a step forward in the digital transformation of manufacturing."_

---
## 📥 Download

You can download the full project package (including the preconfigured virtual environment) from Google Drive:

**[🔗 Download from Google Drive](https://drive.google.com/file/d/1VRnLgbvvQUp7RHEvrWBOkLRiYrKHc7y8/view?usp=sharing)**

> ⚠️ Note: The download includes a preconfigured Python virtual environment.  
> After downloading and extracting, place the folder in `C:\DrawingClean` and simply double-click `launch_app.bat` to run the program.  
> No additional installation is required.
---
## 👨‍💻 Team
**Yunyeol Kim**  
*Team Leader*

**JuHyeong Kim**  
*System Developer*  

**Hyeon-jung Kim**  
*Front developer*

**Hyuk Jeong**  
*backend developer*
