# Guía de uso — Control de Gastos Quincenales

## Primeros pasos

### 1. Acceder a la app

Abre en cualquier navegador:

```
https://abecorrea2290-collab.github.io/gastos-quincenales
```

Haz clic en **"Continuar con Google"** e inicia sesión con tu cuenta.

### 2. Navegar entre quincenas

- La barra de pestañas muestra los 24 períodos del año (Ene Q1, Ene Q2, Feb Q1…)
- Cada pestaña muestra la **fecha de pago** ajustada a días hábiles
- Usa las flechas **← →** para cambiar de año

---

## Registrar ingresos

1. En la sección **"Ingreso de la Quincena"** ingresa tu salario o ingreso base
2. Haz clic en **Guardar**
3. Si hay sobrante de la quincena anterior, aparece sumado automáticamente en **"Total disponible"**

---

## Registrar gastos

1. En la sección **"Agregar Gasto"** completa:
   - **Descripción** — nombre del gasto (ej: Arriendo, Mercado, Netflix)
   - **Valor** — monto en pesos colombianos
   - **Categoría** — elige entre las 11 categorías disponibles
   - **Fecha** — día en que se realizó el gasto
2. Activa **"Guardar como recurrente"** si es un pago que se repite cada quincena
3. Haz clic en **Agregar**

El gasto se guarda inmediatamente en Firebase y aparece en la tabla de movimientos.

---

## Gastos recurrentes

Los pagos fijos (arriendo, servicios, cuotas) se pueden guardar como recurrentes y aplicar rápidamente:

1. Al agregar un gasto, activa el toggle **"Guardar como recurrente"**
2. En quincenas siguientes, haz clic en **"Seleccionar y aplicar →"**
3. Se abre un panel con todos tus recurrentes — **selecciona solo los que aplican** a esta quincena
4. Haz clic en **"Aplicar seleccionados"**

> Ejemplo: el arriendo solo se paga en Q1, pero el teléfono se paga en Q2. Puedes seleccionar solo lo que corresponde.

---

## Saldo encadenado

La app calcula automáticamente el sobrante de cada quincena y lo transfiere a la siguiente:

```
Quincena anterior:
  Disponible:  $ 2.500.000
  Gastos:    - $ 1.800.000
  Sobrante:  = $   700.000  ← pasa automáticamente a la siguiente

Quincena actual:
  Ingreso base:     $ 2.500.000
  + Sobrante ant.:  $   700.000
  = Total disp.:    $ 3.200.000
```

---

## Tarjetas resumen

| Tarjeta | Descripción |
|---|---|
| Ingreso base | Lo que ingresaste manualmente |
| Total disponible | Ingreso + sobrante anterior |
| Total gastos | Suma de todos los movimientos |
| Saldo | Total disponible − Total gastos |
| % Gastado | Porcentaje del disponible que llevas gastado |

La barra de progreso cambia de color: 🟢 normal · 🟠 alerta (>65%) · 🔴 crítico (>85%)

---

## Exportar a Excel

Haz clic en **📤 Excel** en la barra superior para descargar un archivo `.xlsx` con:

- Hoja **Gastos** — todos los movimientos del año
- Hoja **Ingresos** — ingresos y sobrantes por quincena
- Hoja **Recurrentes** — lista de pagos fijos
- Hoja **Resumen Anual** — tabla consolidada del año

Guarda este archivo en OneDrive / Google Drive como respaldo adicional.

---

## Limpiar datos

El botón 🗑 en la barra superior ofrece tres niveles:

- **Limpiar esta quincena** — borra solo el período actual
- **Limpiar el año** — borra todos los períodos del año seleccionado
- **Limpiar TODO** — elimina todos tus datos de Firebase (irreversible)

---

## Sincronización entre dispositivos

La app funciona en cualquier dispositivo con la misma URL. Los datos se sincronizan automáticamente a través de Firebase:

1. Registra un gasto en el PC
2. Abre la misma URL en el celular
3. El gasto aparece en segundos

La barra de estado muestra:
- 🟢 **Sincronizado** — datos actualizados
- 🟡 **Guardando…** — escribiendo en Firebase
- 🔴 **Error de conexión** — sin internet
