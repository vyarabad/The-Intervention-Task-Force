# 💊 The Intervention Task Force — Opioid Prescription Data Science Project
 
> Analyzing West Virginia opioid prescribing trends using Medicare Part D data, socioeconomic indicators, and U.S. Census data.
 
---
 
## ⚙️ Setup Instructions
 
Follow these steps **in order** to get the project running on your machine.
 
### 1. Clone the Repository
 
```bash
git clone https://github.com/your-org/the-intervention-task-force.git
cd the-intervention-task-force
```
 
---
 
### 2. Create & Activate the Virtual Environment
 
> A virtual environment keeps project dependencies isolated from the rest of your computer.
 
**Create the environment** (only do this once):
```bash
python -m venv venv
```
 
**Activate it** every time you work on the project:
 
| Operating System | Command |
|---|---|
| macOS / Linux | `source venv/bin/activate` |
| Windows (Command Prompt) | `venv\Scripts\activate` |
| Windows (PowerShell) | `venv\Scripts\Activate.ps1` |
 
✅ You'll know it's active when you see `(venv)` at the start of your terminal line.
 
---
 
### 3. Install Dependencies
 
```bash
pip install -r requirements.txt
```
 
---
 
### 4. Set Up Your `.env` File
 
This project uses the **U.S. Census API** to pull socioeconomic data. You need a free API key.
 
**Get your Census API key:**
1. Go to [https://api.census.gov/data/key_signup.html](https://api.census.gov/data/key_signup.html)
2. Fill out the short form — your key will be emailed to you
 
**Create a `.env` file** in the root of the project:
```bash
touch .env
```
 
**Add your key inside the file:**
```
Census_API_Key=your_api_key_here
```
 
> ⚠️ **Never commit your `.env` file to GitHub.** It is already listed in `.gitignore` to keep your key safe.
 
---
 
### 5. Register the Virtual Environment as a Jupyter Kernel
 
> This step lets Jupyter notebooks use the `venv` Python environment (with all your installed packages) instead of your system Python.
 
```bash
pip install ipykernel
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```
 
---
 
### 6. Launch Jupyter
 
```bash
jupyter notebook
```
 
This will open Jupyter in your browser. Navigate to the `notebooks/` folder to get started.
 
**Make sure you're using the right kernel:**
- In any notebook, go to **Kernel → Change Kernel → Python (venv)**
 
## 🛠️ Troubleshooting
 
**`ModuleNotFoundError` inside a notebook?**
→ Make sure you selected the **Python (venv)** kernel (Kernel → Change Kernel).
 
**Census API returning errors?**
→ Double-check your `.env` file has no extra spaces: `Census_API_Key=abc123` ✅ not `Census_API_Key = abc123` ❌
 
**`jupyter` command not found?**
→ Make sure your virtual environment is activated (`source venv/bin/activate`) before running `jupyter notebook`.
 
**Kernel not showing up in Jupyter?**
→ Re-run the ipykernel install step:
```bash
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```
 
---
