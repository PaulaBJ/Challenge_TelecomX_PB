# Análisis de Evasión de Clientes (Churn Analysis) - Telecom X

Este proyecto consiste en un análisis exploratorio de datos (EDA) para una empresa de telecomunicaciones ficticia (**Telecom X**). El objetivo principal es identificar patrones de comportamiento y factores determinantes que llevan a los clientes a abandonar la compañía (*Churn*), con el fin de proponer estrategias de retención basadas en datos.

## Descripción del Proyecto

El análisis se centra en procesar un conjunto de datos en formato JSON crudo, limpiarlo, normalizarlo y realizar visualizaciones estadísticas. Se busca responder preguntas clave como:
* ¿Qué perfil demográfico tiene mayor tendencia a cancelar el servicio?
* ¿Cómo influyen el tipo de contrato y el método de pago en la fidelización?
* ¿Existe una correlación entre el costo mensual y la fuga de clientes?

## Instalación y Requisitos

Para ejecutar este proyecto en tu máquina local, necesitas tener instalado **Python 3.x**.

### Dependencias
Las librerías utilizadas en este análisis son:
* `pandas` (Manipulación de datos)
* `matplotlib` y `seaborn` (Visualización de datos)
* `requests` (Extracción de datos vía API/HTTP)
* `IPython` (Visualización de Markdown en notebooks)

### Configuración del Entorno
Puedes instalar todas las dependencias necesarias ejecutando el siguiente comando en tu terminal:

```pip install pandas matplotlib seaborn requests```

Estructura del Proyecto
El proyecto está organizado de la siguiente manera:

├── TelecomX_Analisis.ipynb
└── README.md                 

⚙️ Uso y Ejecución
Clona este repositorio o descarga el archivo .ipynb.
Abre el archivo en Jupyter Notebook, VS Code o Google Colab.
Ejecuta las celdas en orden secuencial.
El flujo del código sigue estos pasos:
- Ingesta: Descarga automática del JSON desde el repositorio remoto usando requests.
- Normalización: Aplanado de datos anidados (json_normalize).
- Limpieza: Tratamiento de valores nulos, conversión de tipos (object a float) y renombrado de columnas.
- Análisis: Generación de gráficos Pastel, Barras, Boxplots y tablas cruzadas.

🛠️ Posibles Problemas y Soluciones
1. Advertencia de Pyarrow
Al importar Pandas, podrías ver un mensaje como:
DeprecationWarning: Pyarrow will become a required dependency...
Solución: Es solo una advertencia. Puedes ignorarla o instalar la librería para mejorar el rendimiento:
```pip install pyarrow```
Reinicia el kernel después de instalar.
2. Error de Conexión (Requests)
Si al ejecutar la celda de carga de datos obtienes un error de conexión, verifica tu conexión a internet, ya que el dataset se descarga en tiempo real desde GitHub. Asegúrate de que la URL en el código apunte a la versión raw del archivo JSON.

Desarrollado como parte del Challenge Data Science - LATAM.
