# Historial de cambios

Todos los cambios importantes de la app se documentan aquí.

---

## [1.3.0] - 2025

### Agregado
- Integración con Firebase Firestore para sincronización en tiempo real
- Login con Google mediante Firebase Authentication
- Sincronización automática entre dispositivos
- Barra de estado de conexión con Firebase
- Spinner de carga mientras se obtienen datos

### Cambiado
- Datos migrados de localStorage a Firebase Firestore
- Botón de limpieza ahora elimina datos directamente en Firebase

---

## [1.2.0] - 2025

### Agregado
- Selección individual de gastos recurrentes al aplicar (modal con checkboxes)
- Botones "Seleccionar todos" y "Deseleccionar todos"
- Total en tiempo real al seleccionar recurrentes
- Toast de confirmación al aplicar recurrentes
- Formato COP mejorado con símbolo $ y separador de miles colombiano

### Cambiado
- Presentación de valores monetarios con simbología COP en toda la app
- Diseño general mejorado con tipografía del sistema

---

## [1.1.0] - 2025

### Agregado
- Fechas de pago inteligentes por quincena en cada pestaña
- Ajuste automático de fecha de pago si cae en fin de semana o festivo colombiano
- Saldo sobrante encadenado automáticamente entre quincenas
- Botón de limpieza de datos con tres niveles (quincena / año / todo)
- Banner informativo del sobrante anterior
- Contador de días restantes para el pago
- Exportación a Excel (.xlsx) con hojas de Gastos, Ingresos, Recurrentes y Resumen

### Cambiado
- Navegación por año con flechas
- Diseño de pestañas con fecha de pago visible

---

## [1.0.0] - 2025

### Inicial
- Control de gastos por quincena (Q1 y Q2 por cada mes)
- 24 pestañas de navegación (12 meses × 2 quincenas)
- Registro de ingresos y gastos con categorías
- Gastos recurrentes con aplicación automática
- Gráfico de dona por categoría
- Gráfico de barras de evolución anual
- Modo oscuro automático
- Almacenamiento en localStorage
