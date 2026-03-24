Opioid Prescription Data Science Project
Overview

This project analyzes opioid prescription patterns using datasets such as Medicare Part D data, U.S. Census data, and other socioeconomic indicators (education, income, unemployment, etc.).

The project is notebook-driven, with all analysis, visualization, and modeling performed in Jupyter Notebooks.

Setup Instructions
1. Clone the Repository
git clone <your-repo-url>
cd THE-INTERVENTION-TASK-FORCE
2. Set Up Virtual Environment
python -m venv venv

Activate it:

Mac/Linux:

source venv/bin/activate

Windows:

venv\Scripts\activate
3. Install Dependencies
pip install -r requirements.txt
4. Configure Environment Variables

Create a .env file in the root directory:

CENSUS_API_KEY=your_api_key_here

This is required for accessing Census data.

5. Set Up Jupyter Kernel (Required)

We use ipykernel so the virtual environment works inside Jupyter notebooks.

Run:

pip install ipykernel
python -m ipykernel install --user --name=opioid-project --display-name "Python (opioid-project)"

Then open Jupyter and select the correct kernel:

Kernel → Change Kernel → Python (opioid-project)
6. Launch Jupyter Notebook
jupyter notebook

Open the notebooks/ folder and start working.

Best Practices
Always activate the virtual environment before working
Use the correct Jupyter kernel (Python (opioid-project))
Do not commit the .env file
Keep notebooks focused and well-documented with markdown cells
Save processed data back into the data/ folder when needed
