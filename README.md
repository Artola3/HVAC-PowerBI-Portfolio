# HVAC-PowerBI-Portfolio
Proyecto de análisis de datos del sector HVAC

# 🏭 HVAC Service 360º: Business Intelligence Dashboard

## 📊 Contexto del Proyecto
Este proyecto simula el ecosistema de datos de una empresa de servicios industriales (HVAC) que gestiona **2.000 órdenes de trabajo** anuales.

El objetivo fue transformar tablas desconectadas en un sistema centralizado para responder preguntas de **Rentabilidad, Productividad Técnica y Operaciones**.

## 💡 Hallazgos Reales (Data Storytelling)
El análisis reveló insights estratégicos para la dirección:

1.  **Finanzas:** El **Aire Acondicionado** representa el mayor coste en garantías (>83k€), desviándose del presupuesto esperado.
2.  **Talento:** Se detectó una brecha de formación en el técnico **T08**, cuya tasa de resolución a la primera (FTF) es del 61%, afectando la rentabilidad del equipo.
3.  **Operaciones:** **Cornellà** concentra el 23% de la carga de trabajo, saturando las rutas actuales.

---

## 📸 Recorrido Visual por el Dashboard

A continuación se detalla cada tablero del informe, explicando la lógica de negocio y las visualizaciones clave.

### 1. Control Financiero (Financial Overview)
Monitorización del **Ahorro Interanual (YoY)** y control presupuestario.
* **KPIs:** Ahorro total vs Año Anterior.
* **Visual:** Gráfico de columnas apiladas para estacionalidad de costes.
![Panel Financiero](Screenshots/01_Financial.png)

### 2. Matriz de Rendimiento Técnico (HR & Performance)
Evaluación objetiva del personal cruzando **Volumen de Trabajo** vs. **Calidad**.
* **Visual Clave:** Scatter Plot (Gráfico de Dispersión). Los técnicos en el cuadrante inferior izquierdo (Baja calidad/Bajo volumen) requieren intervención inmediata.
![Panel Tecnicos](Screenshots/02_Tecnicos.png)

### 3. Análisis de Causa Raíz (Decomposition Tree)
Uso de Inteligencia Artificial para desglosar métricas complejas.
* **Funcionalidad:** Este árbol permite entender *por qué* sube el ticket medio, desglosando el gasto por **Zona -> Máquina -> Tipo de Avería**.
* **Insight:** Permite llegar al "origen del problema" en 3 clics.
![Arbol de Descomposicion](Screenshots/03_Arbol_Descomposicion.png)

### 4. Tablero de Eficiencia Operativa
Auditoría de costes unitarios y desviaciones.
* **Visual Clave:** Semáforos de desviación.
* **Lógica:** Muestra en rojo cualquier tipología de máquina cuyo **Ticket Medio** haya subido respecto al año anterior, alertando de inflación de costes de repuestos.
![Eficiencia](Screenshots/04_Eficiencia.png)

### 5. Mapa de Distribución Geográfica
Optimización de rutas y zonas de servicio.
* **Visual:** Mapa de burbujas por volumen de intervenciones.
* **Insight:** Visualización clara de la saturación en la zona del Baix Llobregat (Cornellà).
![Mapa Operativo](Screenshots/05_Mapa.png)

---

## 🛠️ Stack Tecnológico
* **Herramienta:** Microsoft Power BI
* **Lenguaje:** DAX Avanzado (Time Intelligence, SelectedValue, Ranking).
* **Modelado:** Esquema de Estrella (Star Schema).
* **Transformación:** Power Query para limpieza de datos brutos.

---
*Proyecto desarrollado por **David Artola** como parte de mi portafolio profesional de Análisis de Datos.*
*Datos simulados para fines demostrativos.*
