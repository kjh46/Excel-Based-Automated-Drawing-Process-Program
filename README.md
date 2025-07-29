# 🔧 Excel-Based Automated Drawing Process Program

## 🌟 Project Overview
This project aims to develop an automated program for Excel-based drawing process calculations. The goal is to reduce human errors and the burden on field workers caused by manual processes and multi-sheet Excel handling, while ensuring consistency and accuracy of calculation results.

### 🗓️ Project Information
* **Project Name**: Excel-Based Automation Program Development
* [cite_start]**Duration**: May ~ June 2025 [cite: 9, 10]
* [cite_start]**Job Role**: IT Development [cite: 12, 13]
* [cite_start]**Participating Company**: RHINOX [cite: 15, 16]
* [cite_start]**Team Leader**: Kim Yun-yeol [cite: 2]
* [cite_start]**Team Members**: Kim Ju-hyeong, Kim Hyeon-jung, Jeong Hyeok [cite: 3]

## ✨ Key Features
[cite_start]This program automates core calculations for the drawing process and provides various analysis functions[cite: 28, 29].

### ⚙️ Core Calculation Functions
* [cite_start]**6 Input Variables**: K (Plasticity Modulus), n (Work Hardening Exponent), μ (Friction Coefficient), d₀ (Initial Bar Diameter), d (Final Bar Diameter), α (Die Semi-Angle) [cite: 30]
* [cite_start]**Automatic Calculation**: f₁, f₂, Q₁, εf, kfm, km automatically calculated [cite: 31]
    * [cite_start]$f_1 = \pi \times d_0^2 / 4$ (Initial bar cross-sectional area) [cite: 123]
    * [cite_start]$f_2 = \pi \times d^2 / 4$ (Final bar cross-sectional area) [cite: 123]
    * [cite_start]$Q_1 = \pi \times (d_0^2 - d^2) / (4 \times \sin(\alpha))$ (Effective cross-sectional area) [cite: 99]
    * [cite_start]$\epsilon_f = \ln(f_1 / f_2)$ (True strain) [cite: 156]
    * [cite_start]$k_{fm} = K \times (\epsilon_f)^n / (1 + n)$ (Average yield strength of material) [cite: 165, 167, 179]
    * [cite_start]$k_m = k_{fm} / (1 + ((F + Q_1 \mu) / (2 \times f_2)))$ (Average deformation resistance) [cite: 180, 181]
* [cite_start]**Load Analysis**: ZN (Pure Deformation Force), ZR (Frictional Resistance Force), ZS (Internal Shear Force) calculated [cite: 32]
    * [cite_start]$Z_N = k_m \times (f_1 - f_2)$ [cite: 184]
    * [cite_start]$Z_R = Q_1 \times \mu \times k_m$ [cite: 185]
    * [cite_start]$Z_S = 0.77 \times f_2 \times k_{fm} \times (\pi/180 \times \alpha)$ [cite: 186]
* [cite_start]**Final Judgment**: Z (Total Drawing Force), σ (Drawing Stress) and process feasibility judgment [cite: 33]
    * [cite_start]$Z = Z_N + Z_R + Z_S$ [cite: 194]
    * [cite_start]$\sigma = Z / f_2$ [cite: 195]
    * [cite_start]Feasibility: If $\sigma < k_m$, then 'Usable'; if $\sigma > k_m$, then 'Not Usable' [cite: 198, 199, 200, 201, 202, 203, 204]

### 💻 Main Feature Composition
* [cite_start]**Single Calculation**: Detailed calculation for individual conditions [cite: 35]
* [cite_start]**Area Reduction Rate Analysis**: Processability evaluation by 5% to 40% reduction rates, with graph visualization [cite: 36]
* [cite_start]**Batch Processing**: Large-volume calculation via CSV/Excel files [cite: 37]

## [cite_start]🚀 Technology Stack [cite: 39]
* [cite_start]**Python 3.10**: Main development language [cite: 40]
* [cite_start]**Streamlit**: Web application framework [cite: 41]
* [cite_start]**NumPy, Pandas**: Numerical calculation and data processing [cite: 42]
* [cite_start]**Matplotlib**: Data visualization [cite: 43]
* [cite_start]**Virtual Environment (venv)**: Dependency management [cite: 44]

## [cite_start]📦 Program Structure [cite: 45]
The project consists of the following files:
* [cite_start]`venv/`: Virtual environment folder [cite: 47]
* [cite_start]`app_extended.py`: Main application Python file [cite: 48]
* [cite_start]`launch_app.bat`: One-click execution batch file [cite: 49]
* [cite_start]`README.txt`: User manual (installation and execution guide) [cite: 50]

## [cite_start]💡 Key Challenges and Solutions [cite: 60]
* [cite_start]**Complex Environment Setup**: Simplified the complex installation process by distributing with a virtual environment included[cite: 61].
* [cite_start]**User Accessibility**: Provided a one-click execution system via a batch file (.bat) and a detailed manual to enhance user convenience[cite: 62].
* [cite_start]**Offline Execution**: Configured as a package including all dependencies for execution in a local environment without building a separate server[cite: 63].

## [cite_start]📈 Expected Effects and Future Directions [cite: 64]

### [cite_start]🏢 In-Company Utilization [cite: 65]
* [cite_start]Immediately usable by departments responsible for drawing processes[cite: 66].
* [cite_start]Contributes to improving quality control processes[cite: 67].

### [cite_start]💰 Business Expected Effects [cite: 68]
* [cite_start]Minimizes losses due to calculation errors[cite: 69].
* [cite_start]Increases productivity by improving work efficiency[cite: 70].

### [cite_start]🚀 Future Development Directions [cite: 71]
* [cite_start]Expansion to calculators for other processes (e.g., extrusion, forging)[cite: 72].
* [cite_start]Development of a web-based cloud version[cite: 73].
* [cite_start]AI-based optimal processing condition recommendation system[cite: 74].
* [cite_start]IoT-linked system[cite: 75].

## 📝 Installation and Execution Method

### 1. Install Python 3.10.x
* Download and install Python 3.10.x from the official website. (Anaconda installation is not recommended) [cite_start][cite: 206]
* [cite_start]**Be sure to check "Add Python to PATH"** during installation[cite: 206].
* [cite_start]If available, check the "Install for all users" option[cite: 206].
* [cite_start]Download link: [https://www.python.org/downloads/release/python-3109/](https://www.python.org/downloads/release/python-3109/) [cite: 206]

### 2. Prepare Project Files
* Extract the provided Zip file. [cite_start]Create a folder named `DrawingClean` under the `C:` drive and place the extracted files inside this folder[cite: 206]. (If you change the folder path, you need to modify the `cd` part of the path in the `launch_app.bat` file) [cite_start][cite: 206].

### 3. Run the Program
* [cite_start]Double-click the `launch_app.bat` file in the `DrawingClean` folder to run it[cite: 206].
* [cite_start]A command prompt window will appear, install the necessary libraries, and then automatically open a web browser to run the program[cite: 205].

## 🖼️ Screenshots

### Single Calculation Example (Feasible)
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_1.png?raw=true" alt="Single Calculation Example 1" width="700"/>
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_2.png?raw=true" alt="Single Calculation Example 2" width="700"/>

### Single Calculation Example (Not Feasible)
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_3.png?raw=true" alt="Single Calculation Example 3" width="700"/>
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_single_calc_4.png?raw=true" alt="Single Calculation Example 4" width="700"/>

### Area Reduction Rate Analysis
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_reduction_analysis_1.png?raw=true" alt="Area Reduction Rate Analysis 1" width="700"/>
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_reduction_analysis_2.png?raw=true" alt="Area Reduction Rate Analysis 2" width="700"/>

### Batch Processing
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_batch_processing_1.png?raw=true" alt="Batch Processing 1" width="700"/>
<img src="https://github.com/yourusername/your-repo-name/blob/main/screenshot_batch_processing_2.png?raw=true" alt="Batch Processing 2" width="700"/>

---

[cite_start]**"Beyond being a simple calculation tool, it seems to have enhanced the work efficiency of field workers and taken a step forward in the digital transformation of manufacturing."** [cite: 81]
