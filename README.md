
# Proyecto de Clasificación de Cáncer

Este repositorio contiene el código fuente del proyecto de clasificación de imágenes dermatológicas con técnicas de Deep Learning, integrando datos tabulares y visuales para mejorar la precisión en la predicción de distintos tipos de cáncer de piel.

## Descripción del Proyecto

Se implementaron dos estrategias de entrenamiento utilizando modelos de aprendizaje profundo con entrada dual (multimodal), combinando:

- Imágenes de lesiones cutáneas (transformadas en mapas de calor mediante técnicas de visualización)
- Datos tabulares asociados (edad, zona de la lesión, sexo)

Las arquitecturas desarrolladas fueron:

1. **CNN desde cero (CNN + Tabular)**: Modelo convolucional entrenado desde el inicio junto con entrada tabular densa.
2. **Transfer Learning (EfficientNet) + Fine Tuning**: Modelo preentrenado con pesos de `ImageNet`, ajustado con datos clínicos (tabulares), y luego fine-tuned con una tasa de aprendizaje reducida para mejorar resultados.

El enfoque principal es la detección automática de cáncer de piel a partir del conjunto de datos **HAM10000**, combinando procesamiento de imágenes y metadatos clínicos para potenciar la capacidad predictiva.

##  Estructura del Proyecto

```
.
├── DataFrames_Resultantes/        # Resultados intermedios 
├── Imagenes_Calor/                # Imágenes transformadas (en compilado .zip)
├── IMG_AUG/                       # Aumentos de datos (ignorados)
├── Modelos/                       # Modelos entrenados (.keras) (ignorados)
├── HAM10000_metadata.csv          # Metadatos originales (fuente HAM10000 KAGLE)
└── Proyecto_ML.ipynb              # Notebook principal de entrenamiento
```

## Requisitos

- Python ≥ 3.8
- TensorFlow / Keras
- Pandas, NumPy, Matplotlib

## Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu_usuario/Modelo_ML.git
   cd Modelo_ML
   ```

2. Crea un entorno virtual e instala dependencias:
   ```bash
   python -m venv venv
   ```

3. Ejecuta el notebook:
   ```bash
   jupyter notebook Proyecto_ML.ipynb
   ```
