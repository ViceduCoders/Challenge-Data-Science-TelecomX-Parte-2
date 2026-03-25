# 📊 Análisis de Cancelación de Clientes (Churn) - Telecom X - Parte 2
#### Autor: Victor Asencio
Este proyecto desarrolla un modelo predictivo diseñado para identificar los factores críticos que provocan el abandono de clientes en una compañía de telecomunicaciones y propone estrategias accionables para mejorar la retención.

## 📊 Resumen del Proyecto

### 1. Preparación y Modelado de Datos
* **Curación:** Limpieza profunda eliminando identificadores sin poder predictivo (`CustomerID`) y variables con baja correlación según pruebas estadísticas (`Gender` y `PhoneService`).
* **Encoding:** Transformación de variables categóricas mediante **One-Hot Encoding** para compatibilidad con algoritmos matemáticos.
* **Balanceo de Clases:** Se corrigió el desbalanceo mediante el ajuste de pesos de clase en el algoritmo de Regresión Logística.
* **Evaluación de Modelos:** La **Regresión Logística Balanceada** resultó la más efectiva al lograr un **Recall del 79%**, minimizando los falsos negativos.

**Análisis de Desempeño:**
La evaluación mediante la Matriz de Confusión confirma una alta capacidad del modelo para detectar correctamente a los clientes que efectivamente cancelaron el servicio (clase 1), objetivo principal del negocio para permitir una intervención oportuna.

---

### 2. Factores Clave de Cancelación

1. **Análisis de Correlación:** A través del Mapa de Calor, se identificó una correlación positiva entre los cargos mensuales y la cancelación. Esto indica que la sensibilidad al precio influye significativamente en la decisión del cliente de abandonar el servicio.
2. **Impacto del Tipo de Contrato:** Identificado como el predictor más fuerte. Los clientes con contratos **mes a mes** tienen una tasa de fuga del **42.7%**, comparado con solo el **2.8%** en contratos de dos años. La duración del compromiso reduce drásticamente la volatilidad del cliente, validando la estabilidad contractual como estrategia de retención.
3. **Comportamiento del Gasto:** Se observa que los clientes que cancelan suelen tener cargos mensuales medianos más elevados, reforzando la idea de la competitividad por precio en el mercado de telecomunicaciones.

---

### 3. Jerarquía de Importancia y Estrategias

**Ranking de Importancia de Variables:**
Tras la influencia del tipo de contrato, la tenencia (`Tenure`) y los cargos mensuales se posicionan como los factores determinantes en el modelo de clasificación. Asimismo, la falta de servicios de valor agregado (seguridad y soporte) incrementa el riesgo de fuga.

#### **Estrategias de Retención Propuestas:**
1.  **Incentivos de Migración:** Campañas dirigidas a mover a clientes de contratos mensuales a planes de 1 o 2 años mediante beneficios exclusivos.
2.  **Paquetes de Valor Agregado:** Incluir servicios de seguridad y soporte técnico de forma gratuita para aumentar el costo de salida del cliente.
3.  **Optimización de Pagos:** Fomentar el cambio de cheque electrónico a **pago automático** para reducir fricciones mensuales y bajas administrativas.

## 📈 Conclusiones
El éxito en la retención de Telecom X depende de fomentar la estabilidad mediante **contratos de mayor duración** y asegurar el uso de **servicios de valor agregado**. El modelo implementado funciona como un sistema de alerta temprana proactivo para identificar clientes en riesgo antes de la decisión final de retiro.

## 🛠️ Tecnologías Utilizadas

* **Lenguajes:** Python 3.12
* **Librerías de Análisis de Datos:**
    * `Pandas`: Manipulación y limpieza de datos.
    * `NumPy`: Operaciones numéricas.
* **Visualización:**
    * `Matplotlib`: Gráficos base.
    * `Seaborn`: Visualizaciones estadísticas avanzadas.
* **Machine Learning (Scikit-Learn):**
    * `LogisticRegression`: Modelo lineal balanceado.
    * `RandomForestClassifier`: Modelo de ensamble basado en árboles.
    * `StandardScaler`: Normalización de datos.
    * `train_test_split`: División de conjuntos de datos.
* **Entornos:** Google Colab / Jupyter Notebooks

---






