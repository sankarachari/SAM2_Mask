# 1. Create and activate a clean environment
python3 -m venv sam2_env
source sam2_env/bin/activate  # Windows: sam2_env\Scripts\activate

# 2. Install PyTorch with GPU support
pip3 install torch torchvision --index-url https://pytorch.org

# 3. Clone and install the official SAM 2 package
git clone https://github.com
cd segment-anything-2
pip install -e .

# 4. Install standard dependencies for data handling and rendering
pip install opencv-python matplotlib numpy

# 5. Download model weights (Base model used in examples below)
mkdir -p checkpoints
cd checkpoints
curl -L -O https://fbaipublicfiles.com
cd ..
