# Wath RL IA play mario bros

<div>
  <img src="https://github.com/jorgecasase/github-repos-img/blob/main/img/python.png" alt="python" height="100"/>
  <img src="https://github.com/jorgecasase/github-repos-img/blob/main/img/anaconda.png" alt="anaconda" height="100"/>
</div>

This project makes it possible to replicate the real-time AI-controlled Mario game on Windows. 
 
## Requirements 
Steps needed to run a pre-trained RL model with GUI to watch it play. Works for native Windows, does not work on Colab. 

## Training and Models 
You can train the model or upload it from GitHub: 
- [Notebook for training](https://github.com/pedroconcejero/deep_learning_2024/blob/main/mario_RL_pytorch_tutorial_400_episodes_save_every_1e4.ipynb)
- [Trained model](https://github.com/pedroconcejero/deep_learning_2024/blob/main/mario_net_8.chkpt)
- Or in this same repository there is a model with 40000 episodes that finishes the level: [trained_mario.chkpt](https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/trained_mario.chkpt)

## Installation

### Miniconda
Download Miniconda for the virtual environment from [here](https://www.anaconda.com/download/). 
<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/1.png" alt="conda" height="250"/>

During installation, be sure to add it to the PATH. 
<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/2.png" alt="condapath" height="250"/>

### Visual Studio Build Tools 
Download and install Visual Studio Build Tools for C++ from [here](https://visualstudio.microsoft.com/es/visual-cpp-build-tools/). 

Check the ‘Develop for desktop in C++’ box and install (this may take a while). 

<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/3.png" alt="vscpp" height="250"/>

### Create the Virtual Environment 
Create the virtual environment with the file `environment.yml`: 
```bash conda env create -f environment.yml```

<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/4.png" alt="condacreate" height="250"/>

### Install Rust and Jupyter 
Install Rustup to use Jupyter (standard installation) from [here](https://rustup.rs/)

<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/5.png" alt="rust" height="250"/>

restart cmd and run: 
```conda activate mario```

```pip install matplotlib```

```pip install scikit-image```

```pip install jupyter```

### Create a jupyter kernel
```pip install ipykernel```

```python -m ipykernel install --user --name=mario --display-name "Python (mario)"```

### Open jupyter notebook
open jupyter with 
```jupyter notebook```
and select the created mario Python kernel (mario)

<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/6.png" alt="kernel" height="250"/>

## Load Model and Run 
Open `play.ipynb`, put the route of your model `.chkpt` in this cell: ```checkpoint = Path(trained_mario.chkpt)```

<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/7.png" alt="celda" height="250"/>

Run the entire notebook. A window will now open where you can see the game's graphical interface and AI trainings.

Enjoy watching the AI play Mario in real time!

<img src="https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/img/8.png" alt="marioplay" height="250"/>
