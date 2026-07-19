# Creador de formas (plugin de NOPAL)

Editor vectorial paramétrico para [NOPAL](https://github.com/charlymigenes-ux/nopal):
rectángulos, círculos, polígonos y formas paramétricas con medidas exactas y
esquinas configurables, listas para enviar a la cola de láser/CNC o guardar
en la biblioteca.

## Instalación

Desde NOPAL → Configuración → Galería de plugins → Creador de formas →
Instalar. NOPAL clona este repo a `plugins/shape-creator/` y carga su
frontend automáticamente — no requiere pasos manuales.

## Desarrollo

Este plugin es **solo frontend** (sin componente de backend propio): usa
directamente los endpoints ya existentes de NOPAL core (subida a la
biblioteca, cola de láser/CNC), no expone `backend` en su manifest.

Estructura:
```
nopal-plugin.json      # manifest (versión, entry point de frontend)
frontend/
  shape-creator.js       # editor vectorial + integración con NOPAL
  shape-creator.css
```

No tiene tests propios de backend por no tener backend — la validación es
manual en el navegador (ver el flujo de instalación desde la Galería de
plugins de NOPAL).
