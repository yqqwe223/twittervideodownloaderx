# 🐦 Herramienta de Análisis de Videos de X.com

> Una herramienta ligera, rápida y multifuncional para extraer contenido de video de X (anteriormente Twitter)

[🌐 Demostración en línea](https://twittervideodownloaderx.com/sp) • [📝 Guía de uso](#-guía-de-uso) • [❓ Preguntas frecuentes](#-preguntas-frecuentes)

---

## 📋 Descripción del proyecto

Este proyecto es una herramienta de análisis de video basada en web que permite extraer de forma segura recursos de video de publicaciones públicas en X.com (anteriormente Twitter), ofreciendo opciones de conversión y descarga en múltiples formatos. No requiere instalación de software adicional ni registro de cuenta: úsala directamente desde tu navegador.

> ⚠️ **Aviso importante**: Esta herramienta está diseñada exclusivamente para aprendizaje personal, investigación técnica y uso dentro de límites razonables. Por favor, cumple con el [Acuerdo para Desarrolladores de la Plataforma X](https://developer.twitter.com/en/developer-terms/agreement) y las leyes de derechos de autor de cada país. Queda estrictamente prohibido su uso con fines que infrinjan los derechos de terceros.

---

## ✨ Funciones principales

- 🔗 **Análisis de enlaces**: Compatible con URLs estándar de publicaciones de X.com; detección automática de videos y GIFs animados
- 📥 **Exportación en múltiples formatos**:
  - Video MP4 con calidad original
  - Extracción de audio → Formato MP3
  - Fragmento de video → Conversión a GIF animado
- 🌍 **Interfaz multilingüe**: Soporte para español, inglés, chino, japonés, coreano y hasta 16 idiomas en total
- 📱 **Compatibilidad multiplataforma**: Funciona perfectamente en Chrome / Firefox / Safari / Edge; experiencia optimizada para móviles y tablets
- 🔒 **Privacidad priorizada**: Sin registro de cuenta, sin recolección de datos personales; proceso de análisis completamente anónimo
- ⚡ **Procesamiento ultrarrápido**: Análisis completado en promedio en menos de 5 segundos; soporte para solicitudes simultáneas

---

## 🚀 Inicio rápido

### Uso en línea (recomendado)
1. Accede a [https://twittervideodownloaderx.com/sp](https://twittervideodownloaderx.com/sp)
2. Copia el enlace de la publicación objetivo (ejemplo: `https://x.com/user/status/123456789`)
3. Pega el enlace en el campo de entrada → Haz clic en el botón 「Analizar」
4. Selecciona el formato deseado → Guarda el archivo siguiendo las indicaciones del navegador

### Implementación local (para desarrolladores)
```bash
# Clonar el repositorio
git clone https://github.com/your-repo/x-video-parser.git

# Instalar dependencias
cd x-video-parser && npm install

# Configurar variables de entorno (opcional)
cp .env.example .env

# Iniciar servidor de desarrollo
npm run dev
```

> 💡 Nota: Este proyecto utiliza una arquitectura basada en Node.js + Express. Consulta la documentación detallada de implementación en `/docs/DEPLOY.md`

---

## 🛠 Stack tecnológico

| Módulo | Tecnologías utilizadas |
|--------|------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Procesamiento de video | ffmpeg.wasm (conversión ligera en frontend) |
| Proxy de reenvío | Cloudflare Workers / Middleware personalizado |
| Internacionalización | vue-i18n + Paquetes de idioma JSON |

---

## 📚 Guía de uso

### Flujo de operación básico
```
1. Obtener el enlace de la publicación
   └─ Abre la publicación objetivo en X.com → Copia la URL desde la barra de direcciones del navegador

2. Enviar solicitud de análisis
   └─ Pega el enlace en el campo de entrada de la herramienta → Haz clic en 「Descargar video」

3. Seleccionar formato de salida
   ├─ 🎬 Descargar como MP4: Guardar con calidad original
   ├─ 🎵 Convertir a MP3: Extraer pista de audio
   └─ 🎞 Convertir a GIF: Generar animación corta (recomendado: ≤15 segundos)

4. Guardar el archivo
   └─ El recurso se abrirá en una nueva pestaña → Clic derecho/menú → 「Guardar como」
```

### Consejos para uso en dispositivos móviles
- iOS Safari: Botón Compartir → 「Guardar en Archivos」
- Android Chrome: Mantener presionado el video → 「Descargar video」
- Si el video se reproduce automáticamente: Haz clic en `⋮` en la esquina superior derecha del reproductor → Selecciona 「Descargar」

---

## ❓ Preguntas frecuentes

**P: ¿Dónde se guardan los archivos descargados?**  
R: Los archivos se guardan en la carpeta de descargas configurada en tu navegador. Puedes verificar o cambiar esta ruta en la configuración del navegador.

**P: ¿Puedo analizar cuentas privadas o contenido restringido?**  
R: No. Esta herramienta solo funciona con publicaciones configuradas como públicas y respeta los ajustes de acceso del contenido original.

**P: ¿Se reduce la calidad de imagen o audio tras la conversión?**  
R: El formato MP4 mantiene la calidad original. El formato MP3 utiliza codificación estándar de 128 kbps. El formato GIF optimiza la tasa de fotogramas según la duración para equilibrar tamaño de archivo y fluidez.

**P: ¿Se almacena el historial de descargas o caché?**  
R: No. Todos los recursos se transmiten directamente al dispositivo del usuario a través de un proxy temporal; el servidor no almacena ninguna solicitud ni archivo multimedia.

**P: ¿Qué hago si el análisis falla?**  
R: Verifica: ① Que el enlace sea de una publicación pública válida ② Que tu conexión a internet sea estable ③ Intenta con otro navegador. Si el problema persiste, no dudes en reportarlo mediante un Issue.

---

## ⚖️ Cumplimiento normativo y Descargo de responsabilidad

- Esta herramienta **no elude ni vulnera medidas de protección técnica** de ninguna plataforma; únicamente obtiene metadatos a través de interfaces públicas
- El usuario es responsable de verificar que su uso cumpla con la legislación local y los términos de servicio de la plataforma
- Casos de uso recomendados: Archivo personal, demostraciones educativas, material de referencia para creación de contenido... siempre dentro del marco del uso justo (Fair Use)
- Si detectas contenido que pueda infringir derechos, por favor contacta al canal oficial de [X a través de este formulario de reporte de derechos de autor](https://help.twitter.com/forms/dmca)

---

## 🤝 Guía de contribución

¡Agradecemos tus Pull Requests y reportes de Issues! Antes de contribuir, por favor revisa:
- [Estándares de código](/CONTRIBUTING.md)
- [Guía de traducción multilingüe](/locales/README.md)
- [Requisitos de seguridad y cumplimiento](/SECURITY.md)

---

## 📄 Licencia

Este proyecto se publica bajo la [Licencia MIT](/LICENSE). Puede utilizarse gratuitamente con fines educativos y de investigación. Para uso comercial, por favor verifica cuidadosamente el cumplimiento de las normativas legales aplicables.

---

> 🌟 Si esta herramienta te ha sido útil, ¡por favor ✨dale una Estrella (Star)! Tu apoyo es la mayor motivación para que sigamos manteniendo y mejorando este proyecto~

*Última actualización: Mayo 2026 | Versión: v2.1.0*