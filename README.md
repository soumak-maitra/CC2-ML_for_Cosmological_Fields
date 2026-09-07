# Machine Learning for Cosmological Fields

These hands-on sessions use CAMELS simulation fields and Lyα-forest spectra to build intuition for scientific machine learning. You will visualize three-dimensional cosmological data, generate mock spectra, reconstruct physical fields with analytic and neural methods, train a multi-task U-Net, and create a tomographic map from sparse sightlines.

## Beginner-friendly setup

### 1. Install Conda

Install [Miniconda](https://docs.conda.io/projects/miniconda/en/latest/) if `conda` is not already available. Close and reopen your terminal after installation, then check it with:

```bash
conda --version
```

### 2. Create the course environment

Open a terminal in this repository and run:

```bash
cd Hands-On
conda env create -f environment.yml
conda activate camels-hands-on
```

You only need to create the environment once. For later sessions, use `conda activate camels-hands-on`.

### 3. Register the notebook kernel

With the environment active, run:

```bash
python -m ipykernel install --user --name camels-hands-on --display-name "Python (camels-hands-on)"
```

### 4. Start JupyterLab

From the `Hands-On` directory, run:

```bash
jupyter lab
```

Open the notebook for the current session. If Jupyter asks for a kernel, choose **Python (camels-hands-on)**. Run cells in order with **Shift+Enter**; some calculations may take a little while to finish.

The notebooks expect the course data in `Hands-On/Sims/CMD_z=2_grid128`. If that folder is missing, obtain the dataset from the course instructor and place the supplied `.npy` files there before running the notebooks.

To stop JupyterLab, return to the terminal and press **Ctrl+C**. To leave the Conda environment, run `conda deactivate`.
