# 🔧 Excel-Based Automated Drawing Process Program

## 🌟 Project Overview

This project aims to develop an automated system for Excel-based drawing process calculations. It addresses the challenges of manual computation and multi-sheet Excel management by offering a consistent, accurate, and efficient solution for field use.

### 🗓️ Project Information

- **Project Name**: Excel-Based Automation Program Development  
- **Duration**: May – June 2025  
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
![Single Feasible 1](<img width="2244" height="1001" alt="image" src="https://github.com/user-attachments/assets/42e6e39c-5c73-4fc6-bcd3-1d95dd53f670"/>)  
![Single Feasible 2](https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_2.png?raw=true)

### ❌ Single Calculation (Not Feasible)
![Single Not Feasible 1](https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_3.png?raw=true)  
![Single Not Feasible 2](https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_4.png?raw=true)

### 📊 Area Reduction Rate Analysis
![Reduction Analysis 1](https://github.com/yourusername/your-repo-name/blob/main/screenshot_reduction_analysis_1.png?raw=true)  
![Reduction Analysis 2](https://github.com/yourusername/your-repo-name/blob/main/screenshot_reduction_analysis_2.png?raw=true)

### 🗃️ Batch Processing
![Batch 1](https://github.com/yourusername/your-repo-name/blob/main/screenshot_batch_processing_1.png?raw=true)  
![Batch 2](https://github.com/yourusername/your-repo-name/blob/main/screenshot_batch_processing_2.png?raw=true)

---

> _"Beyond being a simple calculation tool, this project improves real-world workflow and takes a step forward in the digital transformation of manufacturing."_

---

## 👨‍💻 Author

**JuHyeong Kim**  
*System Developer*  
GitHub: [github.com/kjh46](https://github.com/kjh46)
