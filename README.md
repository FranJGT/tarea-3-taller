# Proyecto de Taller de Machine Learning - Actividad 2

Este proyecto implementa un agente que aprende a navegar en un entorno con obstáculos utilizando el algoritmo **Policy Gradient (REINFORCE)**.

## Descripción general

El sistema entrena a un agente para que:

1. Salga desde la posición inicial (0,0).
2. Evite las celdas clasificadas como “hoyos” (obstáculos).
3. Alcance la meta principal para finalizar el episodio con éxito.
4. Opcionalmente recoja un objeto intermedio para obtener una recompensa adicional.

## Ejecución del proyecto

### Opción 1: Ejecución local

1. Verificar que Python esté instalado.
2. Instalar las dependencias mediante el siguiente comando:

   ```bash
   pip install -r requirements.txt
   ```
3. Abrir el notebook:

   ```bash
   jupyter notebook notebooks/Actividad2.ipynb
   ```
4. En Jupyter Notebook, ejecutar todas las celdas desde el menú **Cell → Run All**.

La ejecución mostrará el proceso de entrenamiento, una animación del recorrido del agente y mapas de calor que ilustran la frecuencia de visita por celda.

### Opción 2: Google Colab

1. Subir el archivo `notebooks/Actividad2.ipynb` a Google Drive.
2. Abrirlo con Google Colab.
3. Ejecutar todas las celdas.

## Estructura del Informe (4 Fases)

### 1. Inteligencia

La métrica principal corresponde a **maximizar la recompensa total acumulada** durante un episodio. Se trabaja con un entorno de 9x9 celdas que define posiciones iniciales, metas, objetos y obstáculos, permitiendo evaluar el desempeño del comportamiento aprendido.

### 2. Proceso Empresarial

El objetivo estratégico consiste en mostrar cómo un método de aprendizaje por refuerzo permite resolver un problema de navegación autónoma en un entorno definido, optimizando decisiones sin necesidad de reglas programadas de forma explícita.

### 3. Tecnología

El método utilizado corresponde a **Policy Gradient (REINFORCE)**. Este procedimiento ajusta una política probabilística en función de los retornos obtenidos. Acciones que conducen a mejores resultados incrementan su probabilidad de selección futura.

### 4. Proceso de Cambio

La implementación se desarrolla en **Python**, utilizando **NumPy** para operaciones numéricas. En el diseño del sistema se consideró el riesgo de que el agente adopte comportamientos no deseados, como recorridos repetitivos; esto se mitigó mediante ajustes en la asignación de recompensas.

## Archivos relevantes

* `notebooks/Actividad2.ipynb`: Contiene la implementación principal.
* `requirements.txt`: Lista de dependencias necesarias para la ejecución.
