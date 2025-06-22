# 🖥️ Ejecutar Chatbot “Cambio de Contraseña” en Local con Live Server

Esta guía explica **únicamente** cómo levantar la página `index.html` en tu PC usando **Visual Studio Code** y la extensión **Live Server**.  

---

## 1. Requisitos

| Herramienta | Descarga |
|-------------|----------|
| **Visual Studio Code** | <https://code.visualstudio.com/> |
| **Extensión Live Server** | Marketplace dentro de VS Code (gratuita) |
| Navegador moderno | Chrome, Edge, Firefox, etc. |

---

## 2. Preparar el proyecto

1. **Descarga o clona** este repositorio en tu equipo.  
2. Estructura mínima que debes ver:

```
tp-chatbot/
├─ index.html
└─ README.md   (este archivo)
```

3. Abre VS Code y selecciona **File → Open Folder…** → navega hasta `tp-chatbot/`.

---

## 3. Configurar el widget Dialogflow

Antes de lanzar Live Server debes poner los IDs correctos de tu agente:

1. En Dialogflow ve a **Integrations → Dialogflow Messenger** y activa *Enable*.  
2. Copia:

   | Valor | Ejemplo |
   |-------|---------|
   | `project-id` | `chatbot-gckr` |
   | `agent-id`   | `a4dcef57-a229-421d-bc51-9ba2a33de676` |

3. Abre `index.html` en VS Code.  
4. Reemplaza las marcas:

```html
<df-messenger
    project-id="TU_PROJECT_ID"
    agent-id="TU_AGENT_ID"
    language-code="es"
    chat-title="Asistente de Contraseña">
</df-messenger>
```

Guarda el archivo (Ctrl + S).

---

## 4. Lanzar Live Server

1. En la barra inferior de VS Code haz clic en **Go Live**  
   <br>*(o clic derecho sobre `index.html` → **Open with Live Server**).*  
2. VS Code abrirá una pestaña con una URL similar a:

```
http://127.0.0.1:5500/index.html
```

3. Verás:

- Título **Asistente de Cambio de Contraseña**  
- Bloque **Preguntas sugeridas**  
- Burbuja de chat (esquina inferior derecha).  

Haz clic en la burbuja para desplegar el chatbot y prueba las frases de ejemplo.

---

## 5. Problemas comunes

| Síntoma | Posible causa y solución |
|---------|-------------------------|
| El chat no aparece / ícono roto | Verifica `project-id` y `agent-id`. Confirma que el agente está *published* y Messenger *enabled*. |
| “Mixed content blocked” | Abre la página como `http://` (Live Server lo hace). Si subes a un hosting, usa HTTPS. |
| Extensiones bloquean scripts | Deshabilita AdBlock/PrivacyBadger o prueba en incógnito. |

---

## 6. Personalización rápida

- **Cambiar preguntas sugeridas**: edita la lista `<ul>` en `index.html`.  
- **Ancho/alto del chat**: ajusta `width` y `min-height` del selector `df-messenger` en la sección `<style>`.  
- **Colores y fuente**: modifica las reglas CSS en el bloque `<style>`.

---

## Créditos

Desarrollado por:

- Matías Ariel Deluca  
- Luciano Demián Contreras  
- Augusto M. Cúneo Brouwer de Koning  

Materia **Organización Empresarial** – Tecnicatura Universitaria en Programación (modalidad a distancia).

¡Disfruta probando el chatbot en tu entorno local!