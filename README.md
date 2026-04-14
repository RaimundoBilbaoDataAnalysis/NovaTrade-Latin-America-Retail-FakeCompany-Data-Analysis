# NovaTrade-Latin-America-Retail-FakeCompany-Data-Analysis
Este proyecto consiste en el diseño y construcción de un ecosistema de datos de extremo a extremo (End-to-End) para una empresa ficticia de retail con base en Chile y operaciones en toda Latinoamérica.  -
- Database creada en Python (con ayuda de Gemini).


## Fase 1: Arquitectura y Generación de Datos (Python)

En esta primera etapa, se diseñó un modelo relacional robusto y se desarrolló un script en Python para generar una base de datos sintética pero con lógica de negocio real.

### 1. El Modelo de Datos (ERD)

El diseño se basa en un modelo relacional que conecta las ventas con la logística y el capital humano, permitiendo análisis de rentabilidad profunda.

### 2. Stack Tecnológico - Fase 1

- **Python 3**: Lenguaje principal.
- **Pandas**: Para la estructuración de tablas y manipulación de DataFrames.
- **Faker**: Para la generación de datos aleatorios realistas (nombres, correos, fechas).
- **VS Code**: Entorno de desarrollo.

### 3. Lógica de Negocio Implementada

Para que el análisis posterior sea valioso, se programaron las siguientes reglas en el script de generación:

- **Jerarquía de Precios**: Los productos tienen costos base lógicos (ej. Laptops > Smart Lamps) y un margen de ganancia de entre el 10% y 30%.
- **Geografía Latam**: Clientes y proveedores distribuidos en 8 países de Latinoamérica (Chile, México, Colombia, Argentina, Perú, Brasil, Uruguay, Ecuador).
- **Integridad Temporal**: Se garantizó que ninguna venta ocurra antes de la fecha de registro del cliente.
- **Logística Centralizada**: Los costos de envío se calculan basados en la distancia desde el Hub central (Chile) hacia el país de destino.
- **KPI de Calidad**: Se introdujo un 15% de retrasos aleatorios en las entregas para medir la eficiencia de los proveedores.

### **4. Entidades Generadas (CSVs)**
| **Tabla** | **Descripción** |
| --- | --- |
| `products.csv` | Catálogo de tecnología y hogar con costos y precios de venta. |
| `customers.csv` | Base de 1.000 clientes con segmentación y correos dinámicos. |
| `employees.csv` | Staff de ventas con cargos y salarios competitivos. |
| `logistics_provider.csv` | Empresas de transporte con tarifas por KM y tipo (Aéreo/Terrestre). |
| `sales.csv` | Cabecera de 5.000 transacciones con fecha y canal de venta. |
| `sales_details.csv` | Detalle de productos por venta, incluyendo descuentos estratégicos. |
| `shipping.csv` | Registro de envíos, fechas de entrega y costos logísticos totales. |
