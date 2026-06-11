# Saliency Spoofing in Deep Neuro-Classifiers: Exposing and Eradicating the Clever Hans Illusion in MRI Diagnostics

This repository contains the code and experiments for evaluating saliency map quality and pseudo-mask generation in deep neural networks trained on neuroimaging data (e.g., MRI scans). 

The primary notebook utilizes `timm` for EfficientNet architectures and PyTorch Grad-CAM to extract and visualize feature maps for model interpretability and quality assessment (QC).

## Project Structure

* `notebooks/`: Contains the main experimental Jupyter Notebooks.
* `data/`: Directory for the MRI datasets (e.g., Nickparvar dataset). *Note: Data is not tracked by Git.*
* `models/`: Directory for saved PyTorch model checkpoints (`.pth`).
* `outputs/`: Directory where generated QC figures (like `Fig6_PseudoMask_QC.pdf`) are saved.

## Installation

It is recommended to use a virtual environment (like `venv` or `conda`) to manage your dependencies.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/saliency-spoofing.git](https://github.com/yourusername/saliency-spoofing.git)
   cd saliency-spoofing
   ```
2. Create and activate a virtual environment:

```Bash
python -m venv venv

# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

```
3. Install the dependencies:
```
Bash
pip install -r requirements.txt
```
4.Usage

Download Data: Place your MRI datasets inside the data/ directory. Ensure your dataset loaders in the notebook point to this path.

Model Weights: If you have pre-trained seed models, place them in the models/ directory (e.g., models/EfficientNet-B0_Nick_SeedModel_std_best.pth).

5.Run Notebook:
```
Bash
jupyter lab
```

Navigate to notebooks/saliency-spoofing-in-deep-neuro-classifiers.ipynb to execute the pipeline. Generated figures will be saved to the outputs/ folder.