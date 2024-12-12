# Wath RL IA play mario bros

<div>
  <img src="https://github.com/jorgecasase/github-repos-img/blob/main/img/python.png" alt="python" height="100"/>
</div>

Este proyecto permite replicar el juego de Mario controlado por una IA en tiempo real en Windows. 
 
## Requisitos 
Pasos necesarios para correr un modelo de RL pre-entrenado con interfaz gráfica para verlo jugar. Funciona para Windows nativo, no funciona en Colab. 

## Entrenamiento y Modelos 
Puedes entrenar el modelo o cargarlo desde GitHub: 
- [Notebook para entrenar](https://github.com/pedroconcejero/deep_learning_2024/blob/main/mario_RL_pytorch_tutorial_400_episodes_save_every_1e4.ipynb)
- [Modelo entrenado](https://github.com/pedroconcejero/deep_learning_2024/blob/main/mario_net_8.chkpt)
- O en este mismo repositorio hay un modelo con 40000 episodios que termina el nivel: [trained_mario.chkpt](https://github.com/jorgecasase/mariobrosplay-windows-gym-RL/blob/main/trained_mario.chkpt)

## Instalación

### Miniconda
Descarga Miniconda para el entorno virtual desde [aquí](https://www.anaconda.com/download/). 

Durante la instalación, asegúrate de añadirlo al PATH. 

### Visual Studio Build Tools 
Descarga e instala Visual Studio Build Tools para C++ desde [aquí](https://visualstudio.microsoft.com/es/visual-cpp-build-tools/). 

Marca la casilla de "Desarrollar para escritorio en C++" e instala (esto puede tardar un rato). 

### Crear el Entorno Virtual 
Crea el entorno virtual con el archivo `environment.yml`: 
```bash conda env create -f environment.yml```

### Instalar Rust y Jupyter 
Instala Rustup para usar Jupyter (instalación estándar) desde [aquí](https://rustup.rs/)

reinicia el cmd y ejecuta: 
```bash conda activate mario```
```bash pip install matplotlib```
```bash pip install scikit-image```
```bash pip install jupyter```

### Crear un kernel para jupyter
```bash pip install ipykernel```
```bash python -m ipykernel install --user --name=mario --display-name "Python (mario)"```

### Abrir jupyter notebook
abre jupyter con 
```bash jupyter notebook```
y selecciona el kernel de mario Python (mario) creado

## Cargar Modelo y Ejecutar 
Abre `play.ipynb`, pon la ruta de tu modelo `.chkpt` en esta celda: ```python checkpoint = Path(trained_mario.chkpt)```

Ejecuta todo el notebook. Ahora se abrirá una ventana donde podrás ver la interfaz gráfica del juego y los entrenamientos de la IA.

¡Disfruta viendo a la IA jugar a Mario en tiempo real!
