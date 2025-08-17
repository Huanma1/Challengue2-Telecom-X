# Challengue2-Telecom-X
# Análisis y Predicción de Churn de Clientes en Telecomunicaciones

## 📝 Resumen del Proyecto

Este proyecto se enfoca en el análisis y la predicción de la **cancelación de clientes (Churn)** en una empresa de telecomunicaciones. El objetivo principal es identificar los factores clave que impulsan a los clientes a dejar el servicio y construir un modelo predictivo que pueda identificar a los clientes en riesgo de cancelación.

El análisis se basa en un conjunto de datos que incluye información demográfica, de servicios y de facturación de los clientes.

## 📊 Metodología

El proyecto siguió un flujo de trabajo estándar de ciencia de datos:

1.  **Análisis Exploratorio y Preprocesamiento de Datos:** Se realizó una limpieza exhaustiva de los datos, manejando valores nulos y convirtiendo variables categóricas a un formato numérico.
2.  **Manejo del Desbalance de Clases:** El dataset original presentaba un fuerte desbalance entre clientes que cancelan y los que no. Para abordar esto, se utilizó la técnica de **Undersampling** en el conjunto de entrenamiento, que balanceó las clases y mejoró significativamente el rendimiento del modelo.
3.  **Modelado Predictivo:** Se construyeron y evaluaron dos modelos: una **Regresión Logística** y un **Árbol de Decisión**.
4.  **Evaluación y Selección del Modelo:** El modelo de **Regresión Logística** demostró un desempeño superior, especialmente en la métrica de **`Recall`**, crucial para identificar a la mayor cantidad posible de clientes en riesgo.

## 📈 Factores Clave de la Cancelación (Basado en el Modelo)

El análisis de los coeficientes del modelo de Regresión Logística reveló que los siguientes factores son los más influyentes en la predicción de Churn, ordenados por su importancia:

* **Antigüedad del Cliente (`customer.tenure`):** El factor más crítico. La probabilidad de cancelación disminuye drásticamente a medida que el cliente se mantiene por más tiempo.
* **Tipo de Contrato (`account.Contract_...`):** Los clientes con contratos **mes a mes** tienen un riesgo de cancelación muy alto. Por el contrario, los contratos a **dos años** son un fuerte indicador de retención.
* **Servicio de Internet (`internet.InternetService_...`):** Los clientes con servicio de **fibra óptica** son más propensos a cancelar.
* **Gasto Total (`account.Charges.Total`):** El gasto total del cliente tiene una correlación positiva con la cancelación, lo que sugiere que los clientes con facturas altas podrían buscar alternativas más económicas.

## 🎯 Estrategias de Retención Propuestas

Basándonos en los hallazgos del modelo, se recomiendan las siguientes acciones estratégicas:

* **Enfoque en la Retención Temprana:** Implementar programas de bienvenida y seguimiento intensivo para los clientes durante sus primeros meses, ya que es el período de mayor riesgo de `Churn`.
* **Incentivos para Contratos a Largo Plazo:** Ofrecer descuentos y beneficios especiales para incentivar a los clientes con contratos mes a mes a cambiarse a contratos de uno o dos años.
* **Análisis del Servicio de Fibra Óptica:** Investigar las posibles causas de la alta tasa de `Churn` entre los clientes de fibra óptica, como problemas de rendimiento o alta competencia en el mercado.
