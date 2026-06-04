# Configuración Formspree para ITO LabAgent

## ⚠️ PASO OBLIGATORIO: Crear cuenta Formspree

**El formulario NO funcionará hasta que completes este paso:**

### 1. Crear cuenta gratuita

1. Ve a **https://formspree.io**
2. Click en **"Sign Up Free"**
3. Regístrate con **itolabagent@gmail.com**
4. Verifica tu email

### 2. Crear formulario

1. Una vez dentro, click en **"+ New Form"**
2. Nombre: **"ITO LabAgent Contact"**
3. Email de destino: **itolabagent@gmail.com**
4. Click **"Create Form"**

### 3. Obtener tu Form ID

Después de crear el formulario verás algo como:

```
Your form endpoint:
https://formspree.io/f/mwpezzzz
```

El código al final (`mwpezzzz`) es tu **FORM_ID**

### 4. Actualizar el HTML

En el archivo `index.html`, línea ~773, cambia:

**ANTES:**
```html
<form id="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

**DESPUÉS:**
```html
<form id="contact-form" action="https://formspree.io/f/TU_FORM_ID_REAL" method="POST">
```

Reemplaza `TU_FORM_ID_REAL` por el ID que obtuviste en el paso 3.

### 5. Hacer commit y push

```bash
cd ~/ito-web
git add index.html
git commit -m "fix(form): añadir Form ID de Formspree"
git push origin main
```

---

## ✅ Verificar que funciona

1. Ve a https://www.itolabagent.org
2. Click en "Start automating →"
3. Rellena el formulario
4. Enviar
5. Deberías recibir un email en **itolabagent@gmail.com**

---

## 📊 Plan gratuito Formspree

- ✅ **50 envíos/mes** gratis
- ✅ Sin marca de agua
- ✅ Anti-spam incluido
- ✅ Notificaciones email

Si necesitas más, el plan Pro cuesta $10/mes (1,000 envíos).

---

**¿Necesitas ayuda?** Dímelo y te guío paso a paso 🚀
