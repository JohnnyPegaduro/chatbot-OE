# Chatbot “Cambio de Contraseña” – Demo Web

Este proyecto demuestra un **chatbot Dialogflow** (Dialogflow Messenger) incrustado en una página web y documenta su uso para el Trabajo Integrador de **Organización Empresarial**.

---

## Contenido del repositorio

| Archivo | Descripción |
|---------|-------------|
| `index.html` | Página web con estilos rápidos, bloque de preguntas sugeridas y widget `<df-messenger>` |
| `diagrama_cambiar_contrasena_clean.png` | Diagrama BPMN del proceso “Cambio de contraseña” |
| `Plantilla_TP_Organizacion_Empresarial.docx` | Informe editable del TP |
| `Preguntas_Frecuentes_Chatbot.docx` | Tabla con las 5 FAQs y sus respuestas |
| `README.md` | Esta guía de uso |

---

## 1. Requisitos

| Herramienta | Uso |
|-------------|-----|
| **Visual Studio Code** | Editar / probar el proyecto |
| **Live Server** *(extensión VS Code)* | Levantar un servidor local con recarga automática |
| Navegador moderno | Testear el chatbot |

### Instalación rápida

1. Descarga e instala VS Code: <https://code.visualstudio.com/>  
2. Abre VS Code → **Extensiones** (Ctrl + Shift + X) → busca **“Live Server”** → **Install**.

---

## 2. Configurar tu agente Dialogflow

1. En la consola de Dialogflow ve a **Integrations → Dialogflow Messenger**.  
2. Activa **Enable Dialogflow Messenger**.  
3. Copia los valores mostrados en el snippet:

| Parámetro | Dónde verlo |
|-----------|------------|
| `project-id` | Settings → General → **Google Project ID** |
| `agent-id`   | Dentro del snippet `<df-messenger>` |

4. Edita `index.html` y reemplaza:

```html
<df-messenger
    project-id="TU_PROJECT_ID"
    agent-id="TU_AGENT_ID"
    language-code="es"
    chat-title="Asistente de Contraseña">
</df-messenger>
```

---

## 3. Probar en local con Live Server

```bash
# Abre la carpeta del proyecto en VS Code
code tp-chatbot/

# Haz clic derecho sobre index.html → "Open with Live Server"
# Se abrirá http://127.0.0.1:5500/index.html (el puerto puede variar)
```

- Verás el bloque de **Preguntas sugeridas** y el widget flotante.  
- Haz clic en la burbuja y prueba las frases de ejemplo.

---

## 4. Despliegue

| Servicio | Pasos |
|----------|-------|
| **GitHub Pages** | Sube el repo → Settings → Pages → Branch `main` |
| **Netlify / Vercel** | Arrastra la carpeta o conecta el repo y publica |
| **Hosting propio** | Sube `index.html` a cualquier servidor HTTPS |

---

## 5. Estructura de entrega

```
tp-chatbot/
├─ index.html
├─ diagrama_cambiar_contrasena_clean.png
├─ Plantilla_TP_Organizacion_Empresarial.docx
├─ Preguntas_Frecuentes_Chatbot.docx
└─ README.md
```

Incluye además el enlace al **video grupal** (YouTube oculto o Drive) dentro del informe.

---

## Créditos

- **Matías Ariel Deluca**  
- **Luciano Demián Contreras**  
- **Augusto M. Cúneo Brouwer de Koning**

Materia **Organización Empresarial** – Tecnicatura Universitaria en Programación.
