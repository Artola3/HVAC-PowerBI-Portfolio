# 🏭 HVAC Service 360º: Business Intelligence Dashboard

## 📊 Contexto del Proyecto
Este proyecto simula el ecosistema de datos de una empresa de servicios industriales (HVAC) que gestiona **2.000 órdenes de trabajo** anuales. 

El objetivo principal fue transformar tablas  (Excel) en un sistema centralizado de inteligencia de negocios para responder preguntas críticas de **Rentabilidad, Productividad Técnica y Operaciones**.

## 💡 Hallazgos Reales (Data Storytelling)
Al analizar los datos, el dashboard reveló insights que permitieron tomar decisiones estratégicas inmediatas:

### 1. 💰 Finanzas: El coste oculto del "Aire Acondicionado"

Se ha detectado que el vigente año se ha gastado mas en garantía sobre la unidad de negocio del "aire acondicionado" vs el año anterior. Sin embargo es el "Fan coil" el tipo de equipo que nos genera mas gasto promedio por intervención (con el dashboard de Eficiencia terminamos por determinar que es donde más piezas promedio en garantia se aplican).
También identificamos a través de la gráficas podemos identificar las estacionalidades en el gasto y el ahorro vs el año anterior.

### 2. 🛠 Técnicos: Detección de necesidades de formación
El dashboard de Recursos Humanos utiliza una métrica personalizada de **First Time Fix (FTF)** basada en el análisis de texto de las observaciones.
* **Insight:** Se identificó que el técnico **T08 (Sergio Paredes)** tiene una tasa de resolución a la primera del **53'85%** (muy por debajo de la media del equipo).
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

<img width="1400" height="794" alt="01_Financial" src="https://github.com/user-attachments/assets/2fe86a20-6559-4727-a5cc-8de6fffc3dc8" />


### 2. Matriz de Rendimiento Técnico (HR & Performance)
Evaluación objetiva del personal cruzando **Volumen de Trabajo** vs. **Calidad**.
* **Visual Clave:** Nos permite analizar los ratios de resolución en la primera intervención por técnico, esto se traslada a una atención mas eficiente y por ende repercute en la satisfacción del cliente.

<img width="1390" height="792" alt="02_Tecnicos" src="https://github.com/user-attachments/assets/f12804f7-7980-4d76-9c10-41ab6d00581d" />


### 3. Análisis de Causa Raíz (Decomposition Tree)
Uso de Inteligencia Artificial para desglosar métricas complejas.
* **Funcionalidad:** Este árbol permite ver el número de intervenciones por técnico, cuáles son los tipos de equipo que mas ha atendido y que piezas ha aplicado en cada asistencia por equipo.
* **Insight:** Permite tener una trazabilidad de las piezas que mas fallan.

<img width="1132" height="784" alt="03_Arbol_Descomposicion" src="https://github.com/user-attachments/assets/54c26268-de30-4637-bf87-e524b13a6457" />


### 4. Tablero de Eficiencia Operativa
Auditoría de costes unitarios y desviaciones.
* **Visual Clave:** Semáforos de desviación.
* **Lógica:** Muestra donde se aplican mas piezas promedio en garantia, así como identificar estacionalidad en los acuerdos de atención (SLA's), también podemos ver que técnicos requieren revisión en este apartado.

<img width="1415" height="797" alt="04_Eficiencia" src="https://github.com/user-attachments/assets/c501d040-11d8-4b93-98e3-7dc8f9f458ac" />


### 5. Mapa de Distribución Geográfica
Optimización de rutas y zonas de servicio.
* **Visual:** Mapa de burbujas por volumen de intervenciones.
* **Insight:** Visualización clara de la saturación en la zona del Baix Llobregat (Cornellà).


<img width="1389" height="785" alt="05_Mapa" src="https://github.com/user-attachments/assets/256c3d34-42bb-4b4e-801a-d2a551349c81" />

---
*Proyecto desarrollado por **David Artola** como parte de mi portafolio profesional de Análisis de Datos.*
*Datos origen: Simulados para demostración.*
