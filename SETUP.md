Local Setup Instructions (uv + Jupyter / VS Code)

Follow these setup instructions if you are running this notebook locally.
Running locally avoids notebook instability and allows proper inspection of agent behavior.

1. Prerequisites

Before starting, make sure you have:

Python 3.10+

uv
Install instructions: https://docs.astral.sh/uv/

If you are using VS Code :

* [Install the Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

* [Install the Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)

2. Clone the Repository
git clone https://github.com/tligorio/ai_workflow_rag_tutorial.git
cd ai_workflow_rag_tutorial

3. Create and Sync the Environment

Create the project-local `.venv` and install the exact versions recorded in
`uv.lock`, including Jupyter support:

uv sync --dev


You do not need to activate the environment when using `uv run`. If you prefer
to activate it, run:

source .venv/bin/activate


On Windows (PowerShell):

.venv\Scripts\activate


4. Register the Jupyter Kernel

Register the environment as a Jupyter kernel:

uv run python -m ipykernel install \
  --user \
  --name ai-workflow-rag \
  --display-name "Python (ai-workflow-rag)"

5. If using VS Code, select the Kernel:

Open AI_Workflow_with_RAG.ipynb

Click Select Kernel (top right)

Choose:

Python (ai-workflow-rag)


This ensures the notebook runs inside the correct environment.


6. Start the Notebook (Terminal Option)

If you are not using vscode, you may also start Jupyter from the terminal:

uv run jupyter notebook AI_Workflow_with_RAG.ipynb

The notebook's first installation cell is primarily for Google Colab. The uv
environment already contains those packages, so rerunning that cell locally is
optional.
