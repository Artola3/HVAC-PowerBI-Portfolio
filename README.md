# 🏭 HVAC Service 360º: Business Intelligence Dashboard

## 📊 Contexto del Proyecto
Este proyecto simula el ecosistema de datos de una empresa de servicios industriales (HVAC) que gestiona **2.000 órdenes de trabajo** anuales. 

El objetivo principal fue transformar tablas desconectadas (Excel/CSV) en un sistema centralizado de inteligencia de negocios para responder preguntas críticas de **Rentabilidad, Productividad Técnica y Operaciones**.

## 💡 Hallazgos Reales (Data Storytelling)
Al analizar los datos, el dashboard reveló insights que permitieron tomar decisiones estratégicas inmediatas:

### 1. 💰 Finanzas: El coste oculto del "Aire Acondicionado"
Mientras que la atención operativa se centraba en las Calderas, el análisis financiero destapó que el **Aire Acondicionado** es el verdadero devorador de presupuesto en garantías, acumulando **más de 83.000€ en costes**, con un ticket medio superior a los **560€ por visita**.
* **Acción:** Se ha propuesto una revisión de proveedores de piezas de AA para reducir el coste medio en un 10%.

### 2. 🛠 Técnicos: Detección de necesidades de formación
El dashboard de Recursos Humanos utiliza una métrica personalizada de **First Time Fix (FTF)** basada en el análisis de texto de las observaciones.
* **Insight:** Se identificó que el técnico **T08 (Sergio Paredes)** tiene una tasa de resolución a la primera del **61%** (muy por debajo de la media del equipo).
* **Acción:** Programa de capacitación específico para T08, evitando su despido y mejorando su eficiencia.

### 3. 📍 Operaciones: Saturación en Cornellà
El mapa interactivo mostró que **Cornellà** concentra el **23% de toda la carga de trabajo** (466 intervenciones), superando a capitales más grandes como Barcelona.
* **Acción:** Reasignación de zonas de los técnicos de Badalona para cubrir la demanda excesiva en el Baix Llobregat.

---

## 🛠️ Stack Tecnológico & Diseño
* **Herramienta:** Microsoft Power BI
* **Modelado:** Esquema de Estrella (Star Schema) con tabla `CalendarBridge` para Time Intelligence.
* **DAX Avanzado:**
    * Cálculo de *Working Days* para productividad real.
    * *Text Mining* en columnas no estructuradas (`SEARCH`) para detectar "Revisitas".
* **UX/UI:** Diseño basado en navegación por paneles con fondos personalizados.

---

## 📸 Recorrido Visual por el Dashboard

### 1. Control Financiero (Financial Overview)
Monitorización del **Ahorro Interanual (YoY)** y control presupuestario.
* **KPIs:** Ahorro total vs Año Anterior.
* **Visual:** Gráfico de columnas apiladas para estacionalidad de costes.

![Panel Financiero](01_Financial.png)

### 2. Matriz de Rendimiento Técnico (HR & Performance)
Evaluación objetiva del personal cruzando **Volumen de Trabajo** vs. **Calidad**.
* **Visual Clave:** Scatter Plot (Gráfico de Dispersión). Los técnicos en el cuadrante inferior izquierdo (Baja calidad/Bajo volumen) requieren intervención inmediata.

![Panel Tecnicos](02_Tecnicos.png)

### 3. Análisis de Causa Raíz (Decomposition Tree)
Uso de Inteligencia Artificial para desglosar métricas complejas.
* **Funcionalidad:** Este árbol permite entender *por qué* sube el ticket medio, desglosando el gasto por **Zona -> Máquina -> Tipo de Avería**.
* **Insight:** Permite llegar al "origen del problema" en 3 clics.

![Arbol de Descomposicion](03_Arbol_Descomposicion.png)

### 4. Tablero de Eficiencia Operativa
Auditoría de costes unitarios y desviaciones.
* **Visual Clave:** Semáforos de desviación.
* **Lógica:** Muestra en rojo cualquier tipología de máquina cuyo **Ticket Medio** haya subido respecto al año anterior, alertando de inflación de costes de repuestos.

![Eficiencia](04_Eficiencia.png)

### 5. Mapa de Distribución Geográfica
Optimización de rutas y zonas de servicio.
* **Visual:** Mapa de burbujas por volumen de intervenciones.
* **Insight:** Visualización clara de la saturación en la zona del Baix Llobregat (Cornellà).

![Mapa Operativo](05_Mapa.png)

---
*Proyecto desarrollado por **David Artola** como parte de mi portafolio profesional de Análisis de Datos.*
*Datos origen: Simulados para demostración.*
