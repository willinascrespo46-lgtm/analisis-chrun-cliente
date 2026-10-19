# 📊 Análisis de Retención y Churn de Clientes en MySQL

## 🎯 Objetivo del Proyecto
Identificar el porcentaje de inactividad de los clientes (Churn) en una plataforma de suscripciones, evaluando el impacto económico en los ingresos mensuales de la empresa para tomar decisiones estratégicas de fidelización.

---

## 🛠️ Herramientas Utilizadas
- **Base de Datos:** MySQL
- **Funciones Clave:** `DATEDIFF`, `IF`, `SUM`, `COUNT`, `AVG`, `ROUND`, `GROUP BY`, `INNER JOIN`
- **Dashboard / Visualización:** Looker Studio / Google Sheets

---

## 💻 Script de Base de Datos y Consultas

### 1. Creación de la Estructura de Datos
```sql
CREATE DATABASE IF NOT EXISTS club_clientes;
USE club_clientes;

CREATE TABLE IF NOT EXISTS clientes (
    id_cliente INT PRIMARY KEY,
    nombre VARCHAR(50),
    categoria_plan VARCHAR(20),
    monto_mensual DECIMAL(10,2),
    fecha_registro DATE,
    fecha_ultima_compra DATE,
    metodo_pago VARCHAR(20)
);
