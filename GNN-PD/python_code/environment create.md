# Create GNN environment
Here is a clean setup from scratch. I recommend using Miniconda/Anaconda if you are on a cluster, because it avoids many Python path problems.

PyTorch should be installed first, then PyTorch Geometric. PyTorch’s official installer recommends choosing the command based on OS, package manager, Python, and CUDA/CPU setting; PyTorch Geometric also recommends using a virtual environment and says current PyG can be installed with only PyTorch required for basic usage.

## Option 1: Conda environment — recommended
1. Create a new environment
2. conda create -n gnn_pd python=3.10 -y
3. conda activate gnn_pd

Check:

python --version

You should see something like:

Python 3.10.x

2. Install PyTorch
For CPU only

Use this if you are running on a laptop or a cluster node without GPU:

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
For GPU

First check CUDA/GPU availability on the cluster:

nvidia-smi

Then install the PyTorch version matching your CUDA setup. For many current systems with CUDA 12.6, this is commonly:

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126

After installing, verify:

python -c "import torch; print(torch.__version__); print(torch.cuda.is_available()); print(torch.version.cuda)"

Expected output for GPU should include:

True

For CPU-only, torch.cuda.is_available() will show:

False

That is okay.

3. Install PyTorch Geometric and other packages
pip install torch_geometric
pip install pandas numpy scikit-learn matplotlib

For the simple GCN code I gave you, this should be enough. PyTorch Geometric states that from PyG 2.3 onward, basic PyG usage does not require external libraries beyond PyTorch.

4. Verify installation

Run:

python -c "import torch; import torch_geometric; import pandas; import sklearn; print('All good')"

Then test GCNConv:

python -c "from torch_geometric.nn import GCNConv; print('GCNConv imported successfully')"

If both work, your environment is ready.

5. Put your files in one folder

Create a project folder:

mkdir gnn_pd_project
cd gnn_pd_project

Put these two files inside:

gnn_pd_project/
│
├── PD_vs_healthy.csv
└── gnn_pd_classification.py

Your script should contain:

CSV_PATH = "PD_vs_healthy.csv"

Then run:

python gnn_pd_classification.py
If you are using a remote cluster

Many clusters use csh or tcsh, not bash. In your earlier cluster issue, source venv/bin/activate gave:

Badly placed ()'s

That usually means you are not using bash.

For Conda, use:

conda activate gnn_pd

If Conda does not work directly, try:

source ~/.bashrc
conda activate gnn_pd

or on some clusters:

module load anaconda
conda activate gnn_pd

Then run:

python gnn_pd_classification.py

## Option 2: Python venv environment

Use this if you do not want Conda.

Linux/macOS/bash
python3 -m venv gnn_pd_env
source gnn_pd_env/bin/activate
python -m pip install --upgrade pip

Then install packages:

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install torch_geometric
pip install pandas numpy scikit-learn matplotlib

Run:

python gnn_pd_classification.py
If your shell is csh/tcsh

Use:

python3 -m venv gnn_pd_env
source gnn_pd_env/bin/activate.csh
python -m pip install --upgrade pip

Then install the same packages.

Recommended requirements.txt

Create a file named:

requirements.txt

Add:

pandas
numpy
scikit-learn
matplotlib
torch_geometric

Do not put torch in this file unless you are sure whether you need CPU or GPU. Install PyTorch separately first.

Then:

pip install -r requirements.txt
Quick final test script

Create test_env.py:

import torch
import torch_geometric
from torch_geometric.nn import GCNConv
import pandas as pd
import sklearn

print("PyTorch version:", torch.__version__)
print("CUDA available:", torch.cuda.is_available())
print("CUDA version used by PyTorch:", torch.version.cuda)
print("PyTorch Geometric imported successfully")
print("GCNConv imported successfully")

Run:

python test_env.py

If this runs without error, you are ready to run the GNN classification code.

My recommendation for you

Use this exact version first:

conda create -n gnn_pd python=3.10 -y
conda activate gnn_pd

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install torch_geometric pandas numpy scikit-learn matplotlib

python -c "from torch_geometric.nn import GCNConv; print('ready')"
python gnn_pd_classification.py

Start with CPU first to confirm the code works. After that, move to GPU if the dataset is large.
