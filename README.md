# 💰 Control de Gastos Quincenales

> App web personal para controlar ingresos y gastos por quincena, con sincronización en tiempo real usando Firebase y acceso desde cualquier dispositivo.

[![Firebase](https://img.shields.io/badge/Firebase-Firestore-orange?logo=firebase)](https://firebase.google.com)
[![GitHub Pages](https://img.shields.io/badge/Hosting-GitHub%20Pages-black?logo=github)](https://pages.github.com)
[![Colombia](https://img.shields.io/badge/Moneda-COP%20%24-yellow)](https://es.wikipedia.org/wiki/Peso_colombiano)
[![Licencia](https://img.shields.io/badge/Uso-Personal-green)](#)

---

## ✨ Características

- 📅 **24 quincenas por año** — Q1 (1–15) y Q2 (16–fin de mes) por cada mes
- 📆 **Fechas de pago inteligentes** — ajusta automáticamente si el día cae en fin de semana o festivo colombiano
- 💸 **Saldo encadenado** — el sobrante de cada quincena pasa automáticamente a la siguiente
- 🔁 **Gastos recurrentes** — guarda pagos fijos y selecciona cuáles aplicar en cada quincena
- 📊 **Gráficos** — distribución por categoría y evolución anual
- 💵 **Formato COP** — valores en pesos colombianos con separador de miles
- ☁️ **Sincronización Firebase** — los datos se guardan en la nube en tiempo real
- 🔐 **Login con Google** — acceso seguro, solo tú ves tus datos
- 📤 **Exportar Excel** — respaldo en `.xlsx` en cualquier momento
- 🌙 **Modo oscuro** — se adapta automáticamente al sistema

---

## 🚀 Acceso

La app está disponible en:

**🔗 [https://abecorrea2290-collab.github.io/gastos-quincenales](https://abecorrea2290-collab.github.io/gastos-quincenales)**

Inicia sesión con tu cuenta de Google. Los datos se sincronizan automáticamente en todos tus dispositivos.

---

## 🛠️ Tecnologías

| Tecnología | Uso |
|---|---|
| HTML / CSS / JavaScript | App completa en un solo archivo |
| [Firebase Firestore](https://firebase.google.com/docs/firestore) | Base de datos en tiempo real |
| [Firebase Authentication](https://firebase.google.com/docs/auth) | Login con Google |
| [Chart.js](https://www.chartjs.org) | Gráficos de distribución y evolución |
| [SheetJS (xlsx)](https://sheetjs.com) | Exportación a Excel |
| [GitHub Pages](https://pages.github.com) | Hosting gratuito |

---

## 📱 Compatibilidad

Funciona en cualquier navegador moderno:

- ✅ Chrome (PC, Android)
- ✅ Safari (iPhone, iPad, Mac)
- ✅ Firefox
- ✅ Edge

---

## 🔐 Privacidad y seguridad

- Los datos se almacenan en **Firebase Firestore** bajo tu UID de Google
- Las **reglas de seguridad** garantizan que solo el usuario autenticado accede a sus propios datos
- El código fuente es público pero los **datos son completamente privados**
- Ningún tercero puede leer ni modificar tu información

---

## 📂 Estructura del proyecto

```
gastos-quincenales/
├── index.html          # App completa (HTML + CSS + JS + Firebase)
└── README.md           # Este archivo
```

---

## 🗂️ Categorías disponibles

`Vivienda` · `Alimentación` · `Transporte` · `Salud` · `Educación` · `Entretenimiento` · `Ropa` · `Servicios` · `Deudas` · `Ahorro` · `Otros`

---

## 📅 Lógica de fechas de pago

| Quincena | Fecha normal | Ajuste |
|---|---|---|
| Q1 | Día 15 de cada mes | Si cae sábado, domingo o festivo → día hábil anterior |
| Q2 | Último día del mes (el 31 se paga el 30) | Si cae sábado, domingo o festivo → día hábil anterior |

Los festivos colombianos están precargados en la app.

---

## 👤 Autor

**Abraham Correa**  
Ingeniero · Medellín, Colombia

---

*Desarrollado con asistencia de Claude (Anthropic) · 2025*
