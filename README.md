# Machine Learning for Cosmological Fields

These hands-on sessions use CAMELS simulation fields and Lyα-forest spectra to build intuition for scientific machine learning. You will visualize three-dimensional cosmological data, generate mock spectra, reconstruct physical fields with analytic and neural methods, train a multi-task U-Net, create a tomographic map from sparse sightlines, and explore probabilistic reconstruction with a conditional denoising diffusion model (DDPM).

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

### 4. Open the notebooks

You can use any application that supports Jupyter notebooks. **Visual Studio Code is a convenient choice for beginners** because it combines the notebooks, files, terminal, and plots in one window:

1. Install [Visual Studio Code](https://code.visualstudio.com/).
2. Install the **Python** and **Jupyter** extensions from its Extensions panel.
3. Open this repository in VS Code and select a `.ipynb` file from the `Hands-On` folder.
4. Click the kernel name near the top-right of the notebook and choose **Python (camels-hands-on)**.

If you prefer a browser-based interface, activate the environment, enter the `Hands-On` directory, and start JupyterLab:

```bash
conda activate camels-hands-on
cd Hands-On
jupyter lab
```

Other notebook applications are also fine as long as they let you select the **Python (camels-hands-on)** kernel. Run cells in order with **Shift+Enter**; some calculations may take a little while to finish.

The notebooks expect the course data in `Hands-On/Sims/CMD_z=2_grid128`. If that folder is missing, obtain the dataset from the course instructor and place the supplied `.npy` files there before running the notebooks.

Run `Lya_forest_neural_vs_FGPA_improved.ipynb` before `Lya_forest_conditional_DDPM_inversion.ipynb`. The first notebook saves its trained U-Net, which the DDPM exercise loads for sightline and summary-statistic comparisons without retraining it.

If you started JupyterLab, stop it by returning to the terminal and pressing **Ctrl+C**. To leave the Conda environment, run `conda deactivate`.
