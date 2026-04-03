# Política de seguridad

## Arquitectura de seguridad

Esta app implementa dos capas de protección para los datos del usuario:

### Capa 1 — Autenticación (Firebase Auth)

- El acceso a la app requiere inicio de sesión con una cuenta de Google
- Firebase Authentication gestiona los tokens de sesión
- Sin una sesión activa válida, no es posible leer ni escribir datos

### Capa 2 — Reglas de Firestore

Los datos de cada usuario se almacenan bajo la ruta:

```
/usuarios/{userId}/...
```

Las reglas de seguridad garantizan que **solo el propietario autenticado** puede acceder a sus datos:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /usuarios/{userId}/{document=**} {
      allow read, write: if request.auth != null
                         && request.auth.uid == userId;
    }
    match /{document=**} {
      allow read, write: if false;
    }
  }
}
```

## Datos almacenados

La app guarda en Firebase únicamente:

- Ingresos por quincena
- Lista de gastos (descripción, valor, categoría, fecha)
- Gastos recurrentes configurados

No se almacena ningún dato sensible como contraseñas, documentos de identidad o información bancaria.

## Código fuente público

El repositorio es público (requerido por GitHub Pages gratuito). Esto significa que cualquier persona puede ver el código de la app, pero **no puede acceder a los datos** de ningún usuario gracias a las reglas de Firestore.

## Reporte de vulnerabilidades

Si encuentras algún problema de seguridad, por favor abre un Issue en este repositorio.
