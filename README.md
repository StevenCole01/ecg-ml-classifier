# Clasificación de arritmias cardíacas mediante aprendizaje automático usando señales ECG

* **Materia:** Aprendizaje Automático
* **Alumno:** Erick Steven Cole Jimenez

Este notebook implementa un flujo completo para clasificar latidos cardíacos usando la base de datos publica **MIT-BIH Arrhythmia Database**. El proyecto descarga o reutiliza registros ECG, segmenta latidos, extrae características numéricas y compara modelos clásicos de aprendizaje automático: KNN, SVM y Random Forest.

## Archivos principales

* `ECG_Arrhythmia_Classification.ipynb`: notebook principal del proyecto.
* `requirements.txt`: dependencias necesarias para ejecutar el notebook.

Al ejecutarse, el notebook puede crear o actualizar estas carpetas dentro de `Notebook`:

* `data/mitdb`: registros descargados de MIT-BIH Arrhythmia Database.
* `outputs`: resultados tabulares del experimento.
* `outputs/figures`: gráficas generadas durante el análisis.

También se guardan algunas imágenes principales en la carpeta `Notebook` para reutilizarlas fácilmente en la presentación o reporte.

## Instrucciones de ejecución

Abre una terminal en la carpeta del proyecto.

```bash
cd "ecg-ml-classifier"
```

### 1. Crear el entorno virtual

```bash
python3 -m venv .venv
```

### 2. Activar el entorno virtual

En macOS o Linux:

```bash
source .venv/bin/activate
```

En Windows:

```bash
.venv\Scripts\activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Seleccionar el entorno en el IDE

En VS Code, PyCharm o el IDE de tu elección selecciona el interprete de Python del entorno virtual.

En macOS o Linux:

```text
.venv/bin/python
```

En Windows:

```text
.venv\Scripts\python.exe
```

### 5. Opcional: registrar el kernel para Jupyter

Este paso solo es necesario si el entorno virtual no aparece en la lista de kernels disponibles.

```bash
python -m ipykernel install --user --name ecg-arrhythmia-ml --display-name "Python (ECG Arrhythmia ML)"
```

### 6. Abrir y ejecutar el notebook

Abre `ECG_Arrhythmia_Classification.ipynb` en tu IDE o en Jupyter.

Selecciona el kernel o interprete correspondiente al entorno virtual. Si registraste el kernel manualmente, aparecerá como:

```text
Python (ECG Arrhythmia ML)
```

Después ejecuta las celdas en orden desde el inicio. La primera ejecución puede descargar los registros de MIT-BIH desde PhysioNet; si los archivos ya están disponibles en `data/mitdb`, el notebook los reutilizara.

Al finalizar la ejecución, se generaran los resultados principales en:

* `outputs/model_comparison_results.csv`
* `outputs/figures/class_distribution_count.png`
* `outputs/figures/ecg_record_sample.png`
* `outputs/figures/example_beats_by_class.png`
* `outputs/figures/average_beat_by_class.png`
* `outputs/figures/rr_distribution_by_class.png`
* `outputs/figures/random_forest_confusion_matrix.png`
* `outputs/figures/random_forest_confusion_matrix_normalized.png`
