# Regresión lineal multiple

[**➔ Ver en Google Colab**](https://colab.research.google.com/github/AndrewP05/Regresion_lineal_multiple/blob/main/RegresionLineal.ipynb)

## Objetivos

### General

1. Evaluar la capacidad de un modelo de regresión lineal múltiple para explicar y predecir los ingresos de las personas a partir de sus características demográficas y de patrimonio (edad y número de automóviles).

### Especificos

1. Estimar los coeficientes de regresión para edad y número de automóviles, y determinar su significancia estadística (p-valores e intervalos de confianza).
2. Calcular y analizar el R² (y R² ajustado) para valorar qué proporción de la variabilidad de los ingresos es explicada por las variables predictoras, y comparar diferentes especificaciones si se incorporasen nuevas variables.
3. Corroborar, mediante análisis de residuos (histograma, Q–Q plot, gráfico residuos vs. predichos) y pruebas formales, que se cumplen los supuestos de normalidad, homoscedasticidad e independencia de los errores, garantizando la validez de las inferencias.

## Distribución de los residuos
<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/55f4e276-685b-4d9b-b81b-b818673408b3" />

## Grafico de Quantiles para ver la distribucion de los residuos
<img width="600" height="455" alt="image" src="https://github.com/user-attachments/assets/db4d29b2-d292-4464-b422-ea6c29bdf49a" />

Resultados de la regresión lineal múltiple:
Intercept: 20396.84
Coeficiente para age: 1049.42
Coeficiente para num_cars: 3644.02

## Grafico de dispersion entre valores reales y predichos
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/0c81b454-9e0b-4597-9056-936a1635a66b" />

## Creamos unos ingresos que se relacionen y agregamos algo de dispersion
<img width="741" height="770" alt="image" src="https://github.com/user-attachments/assets/669fd1e3-5997-4475-b368-8f7428202659" />

## Grafico de calor de correlacion entre variables
<img width="506" height="374" alt="image" src="https://github.com/user-attachments/assets/f94c9d41-a456-4662-8e04-efdc78c17b8d" />

## Hallazgos

*   Hay una correlación positiva fuerte entre la edad y los ingresos, ya que a maoyor edad mayores suelen ser los ingresos
*   El 72.8 % de la variabilidad de los ingresos se explica combinando edad y número de autos.
*   El dispersograma “Real vs. Predicho” (y el gráfico residuos vs. predichos) no muestra un patrón evidente de abanico, lo que sugiere varianza de errores razonablemente constante.

## Recomendaciones

*   Incluir nuevas variables (educación, experiencia laboral, ubicación geográfica) para mejorar aún más el poder predictivo.
*   Evaluar interacciones (por ejemplo, si el efecto de la edad cambia según el número de autos).
*   Monitorear outliers extremos en los residuos y considerar transformaciones o modelos robustos si aparecen casos atípicos muy influyentes.

## Conclusiones

*   En conjunto, el modelo de regresión lineal múltiple conformado por edad y número de automóviles explica de manera sólida (R² ≈ 0.73) gran parte de la variabilidad en los ingresos, con ambos predictores resultando estadísticamente significativos. La edad emerge como el factor más determinante cada año adicional añade en promedio unos 1 049 al ingreso mientras que cada coche extra aporta cerca de 3 644 pero con mayor dispersión. Los residuos cumplen los supuestos de normalidad, homoscedasticidad e independencia, lo que valida la fiabilidad de los intervalos de confianza y p-valores obtenidos. Así, este modelo ofrece una base clara para cuantificar y predecir ingresos a partir de simples indicadores demográficos, aunque su poder explicativo podría reforzarse incorporando variables adicionales (educación, experiencia, ubicación) o explorando interacciones más complejas.
