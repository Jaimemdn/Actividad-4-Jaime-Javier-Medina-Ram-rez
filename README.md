# Actividad-4-Jaime-Javier-Medina-Ram-rez
Actividad 4 Jaime Javier Medina Ramírez
# Benchmarking de Clasificación de Sentimiento con Modelos Preentrenados (Hugging Face)

Este repositorio aloja el código fuente y el reporte técnico del prototipo de Inteligencia Artificial enfocado en la clasificación automatizada de opiniones de usuarios a través del análisis de sentimiento.

## 📊 Arquitectura del Ecosistema
La solución evalúa y explota los siguientes componentes esenciales de la infraestructura de **Hugging Face**:
* **Models Registry:** Descarga y mapeo de arquitecturas Transformer basadas en `BERT` y `DistilBERT`.
* **Datasets (Espejo de Respaldo):** Extracción automatizada del corpus de referencia `IMDb Movie Reviews` mediante canal estructurado en Pandas para garantizar la máxima reproducibilidad del sistema.

## ⚙️ Especificaciones de la Infraestructura de Pruebas
* **Procesamiento:** NVIDIA T4 GPU (Google Colab Compute Cloud).
* **Métricas Evaluadas:** Accuracy, Precision, Recall, F1-Score y Latencia del Sistema en milisegundos (ms).

## 📈 Resultados Obtenidos en el Benchmark

| Modelo (Hugging Face) | Accuracy | Precision | Recall | F1-Score | Latencia (ms) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| distilbert-base-uncased-finetuned-sst-2-english | 0.8500 | 0.9032 | 0.8000 | 0.8485 | 16.09 ms |
| textattack/bert-base-uncased-imdb | 0.9600 | 0.9709 | 0.9524 | 0.9615 | 27.04 ms |
| **lvwerra/distilbert-imdb (Recomendado)** | 0.9500 | 0.9703 | 0.9333 | 0.9515 | 12.60 ms |

## 🚀 Instrucciones para la Reproducción del Prototipo
1. Sube el archivo de extensión `.ipynb` adjunto en este repositorio a tu espacio de **Google Colab**.
2. Modifica el entorno hardware desde el menú superior: `Entorno de ejecución > Cambiar tipo de entorno de ejecución` y asegúrate de marcar **T4 GPU**.
3. Ejecuta secuencialmente de la Celda 1 a la Celda 6. Los resultados numéricos se imprimirán de manera dinámica en la consola de comandos.

## 📝 Conclusión del Proyecto
Las pruebas demuestran de forma contundente que los modelos basados en destilación de conocimiento (`DistilBERT`) especializados en el dominio de destino ofrecen un balance óptimo para entornos de producción, reduciendo los tiempos de ejecución a más de la mitad en comparación con redes completas (`BERT-Base`) a cambio de un impacto estadístico insignificante en las métricas predictivas.
