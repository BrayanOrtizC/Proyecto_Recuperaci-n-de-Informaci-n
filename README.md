# Proyecto_Recuperaci-n-de-Informaci-n
Integrantes: Brayan Ortiz - Fabián Simbaña
Link video de demostración: https://youtu.be/VQ3yQS9M2_o

Motor de Búsqueda de Recuperación de Información (Cranfield Dataset)

Este repositorio contiene la implementación de un **Sistema de Recuperación de Información (SRI)** desarrollado en Python. El sistema está diseñado para indexar y recuperar documentos científicos sobre **Aerodinámica e Ingeniería Aeronáutica** (Colección Cranfield), comparando el desempeño de tres modelos clásicos: **Jaccard**, **TF-IDF** y **BM25**.

Descripción del Proyecto

El objetivo principal es evaluar cómo diferentes modelos de recuperación manejan vocabulario técnico especializado. El sistema incluye un pipeline de preprocesamiento personalizado que conserva terminología de ingeniería (ej: *steady-flow*) y elimina "ruido académico" para mejorar la precisión.

Requisitos e Instalación

El proyecto está desarrollado en Kaggle y el corpus está alojado en Kaggle por lo que la forma de importación del corpus de está desarrollada en ese ambiente, por cual:
- Es necesario agregar en el Input de kaggle el siguiente Dataset: https://www.kaggle.com/datasets/hhhoang/cranfield-dataset

Luego se debe ejecutar todas las celdas secuencialmente.
En la última celda se encuentra ubicado el menú para el usuario.

El sistema presenta 5 opciones claras:
1. Consultar (Jaccard): Ejecuta una búsqueda utilizando el modelo de Similitud de Jaccard. Es útil para consultas rápidas donde solo importa la coincidencia exacta de términos (presencia/ausencia), funcionando como una línea base comparativa.
2. Consultar (TF-IDF): Activa el Modelo Vectorial con suavizado logarítmico. Esta opción pondera los términos de la consulta, dando prioridad a documentos que contienen palabras "raras" o específicas del dominio.
3. Consultar (BM25): Ejecuta el Modelo Probabilístico (Best Match 25). Esta es la opción recomendada, ya que utiliza los hiperparámetros calibrados ($k_1=1.8, b=0.9$) para ofrecer los resultados más precisos en el contexto de ingeniería aeronáutica.
4. Evaluar Sistema Completo: Ejecuta una batería de pruebas automatizada sobre las 225 consultas del dataset. Calcula y muestra las métricas de rendimiento global (MAP, Precision, Recall) para los tres modelos, permitiendo una comparación directa de su eficacia.
5. Salir: Finaliza la ejecución del programa de manera segura.
