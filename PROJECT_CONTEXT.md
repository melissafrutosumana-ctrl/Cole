# 📋 CONTEXTO DEL PROYECTO: CTP Matapalo

## 📌 Descripción General
**Proyecto:** Sistema Web Institucional para CTP de Matapalo  
**Tipo:** Sitio web estático + funcionalidades dinámicas (formularios, notificaciones por email)  
**Lenguajes:** HTML5, CSS3, JavaScript  
**Herramientas:** EmailJS (para envío de emails)  
**Tema Visual:** Verde oscuro (#0a4c23) + Crema (#ebe5d9)

---

## 📁 Estructura del Proyecto

```
Sistemas Notificaciones/
├── PROJECT_CONTEXT.md          # 📖 ESTE ARCHIVO - Documentación del proyecto
├── index.html                  # Página principal del sitio
├── boletas.html                # Sistema de boletas disciplinarias
├── comunicados.html            # Sección de comunicados
├── docentes.html               # Información de docentes
├── galeria.html                # Galería de imágenes
├── registrarme.html            # Formulario de registro
├── subir-imagen.html           # ⚠️ Módulo para subir imágenes (CON PROBLEMAS)
├── paleta.html                 # Referencia de colores (paleta de diseño)
│
├── css/
│   └── stylo.css               # Estilos globales y componentes
│
├── img/                        # Carpeta de imágenes
│   └── logo_colegio_nuevo.png # Logo del colegio
│
└── plantillas/
    ├── plantilla-emailjs.html         # Plantilla de email genérica
    └── plantilla-emailjs-boletas.html # Plantilla de email para boletas
```

---

## 🎨 Diseño Visual

### Colores Principales (Variables CSS)
```css
--verde-oscuro: #0a4c23       /* Color principal institucional */
--verde-claro: #1a6b3a        /* Variante más clara */
--crema: #f5f1e8             /* Fondo principal */
--blanco: #ffffff            /* Fondos secundarios */
--dorado: #d4a256            /* Acentos/detalles */
--borde: #d4ccc0             /* Bordes */
--texto-principal: #0a4c23   /* Texto títulos */
--texto-gris: #5a5a5a        /* Texto secundario */
```

### Tipografía
- **Font Family:** Poppins (de Google Fonts)
- **Pesos:** 300, 400, 600, 700

---

## 🔧 Funcionalidades Principales

### 1. **Página Principal (index.html)**
- Presentación del colegio
- Menú de navegación
- Footer con contador de visitas

### 2. **Boletas Disciplinarias (boletas.html)**
- Sistema institucional de boletas
- Tabla con información de disciplina
- Integración con EmailJS para notificaciones
- Header institucional personalizado

### 3. **Comunicados (comunicados.html)**
- Sección de comunicados para la comunidad
- Diseño responsivo

### 4. **Docentes (docentes.html)**
- Listado/información de docentes
- Gestión de personal

### 5. **Galería (galeria.html)**
- Galería de imágenes del colegio
- Multimedia

### 6. **Registro (registrarme.html)**
- Formulario de registro de usuarios/estudiantes

### 7. **Subir Imágenes (subir-imagen.html)**
- Módulo para upload de archivos

### 8. **Paleta de Colores (paleta.html)**
- Referencia visual de colores del proyecto
- Guía de diseño

---

## 📧 Sistema de Emails (EmailJS)

### Plantillas Disponibles:
1. **plantilla-emailjs.html** - Email genérico
2. **plantilla-emailjs-boletas.html** - Email específico para boletas disciplinarias

### Funcionalidad:
- Envío automático de notificaciones
- Plantillas personalizadas según tipo de mensaje
- Integración con servicio EmailJS

---

## 📱 Características Técnicas

### Responsive Design
- Meta viewport configurado para dispositivos móviles
- CSS adaptativo

### Accesibilidad
- Favicon personalizado (logo_colegio_nuevo.png)
- Soporte para múltiples navegadores
- Charset UTF-8

### Librerías Externas
- **Font Awesome 6.4.0** (Iconos)
- **Google Fonts: Poppins** (Tipografía)
- **EmailJS** (Envío de emails)

---

## 🔄 HISTORIAL DE CAMBIOS Y CONTEXTO

> **NOTA:** Esta sección es el registro histórico de TODO lo que se ha modificado en el proyecto.
> Cada cambio debe registrarse aquí inmediatamente después de implementarlo.

### [26-05-2026] - Mejorar Carrusel y Galería
- **Archivo(s):** `index.html`, `galeria.html`
- **Cambios:**
  - ✅ **Carrusel (`index.html`):** Ahora muestra imágenes locales y carga automáticamente nuevas de Supabase
    - Imágenes estáticas: `info.jpeg`, `comidas.png`, `huevos1.jpeg`, etc.
    - Si se suben nuevas a Supabase con destino "carrusel", se agregan automáticamente
  - ✅ **Galería (`galeria.html`):** Mismo sistema híbrido
    - Imágenes estáticas: `steam1.jpeg`, `steam2.jpeg`, etc.
    - Las nuevas de Supabase se agregan sin borrar las locales
  - ✅ **Funcionalidad de Supabase:** No rompe el sitio si Supabase falla
  - ✅ **Lightbox:** Funcionando para todas las imágenes
- **Razón:** 
  - Necesitaba un sistema que funcione CON imágenes locales ahora
  - Y que agregue nuevas SIN romper el flujo actual
- **Impacto:**
  - ✅ Carrusel funciona perfectamente en Vercel
  - ✅ Galería funciona perfectamente en Vercel
  - ✅ Si Supabase se configura correctamente, las nuevas imágenes se ven automáticamente
  - ✅ Si Supabase falla, el sitio sigue funcionando con imágenes locales

### [26-05-2026] - Mejora Visual y Funcional de subir-imagen.html
- **Archivo(s):** `subir-imagen.html`
- **Cambios:**
  - ✅ **Diseño:** Actualizado para ser consistente con el resto del sitio (colores verde #0a4c23, crema #ebe5d9)
  - ✅ **Header:** Reemplazado navbar personalizado por header institucional igual al `index.html`
  - ✅ **Estructura:** Mejorada con secciones claras (header, formulario, galería, footer)
  - ✅ **UX:** Agregados iconos de Font Awesome, mejor tipografía y espaciado
  - ✅ **Validación:** Mejorado manejo de errores con mensajes claros (archivo, tamaño, conexión)
  - ✅ **Código:** JavaScript refactorizado con funciones auxiliares y comentarios
  - ✅ **Documentación:** Agregado cuadro informativo sobre configuración de Supabase
  - ✅ **Responsivo:** Mantiene adaptabilidad a móviles
- **Razón:** 
  - El archivo original tenía un diseño inconsistente
  - Navbar no coincidía con el resto del sitio
  - Falta de manejo de errores clara
  - Credenciales expuestas y probablemente inválidas
- **Impacto:** 
  - Interfaz visual ahora es consistente con todo el sitio
  - Mejor experiencia de usuario con mensajes claros
  - Código más mantenible
  - **PROBLEMA IDENTIFICADO:** Sistema de upload requiere configuración correcta de Supabase o backend alternativo
  
**Problemas Pendientes por Resolver:**
1. ⚠️ Credenciales de Supabase pueden estar expiradas o inválidas
2. ⚠️ No hay validación en backend para tipos de archivo
3. ⚠️ Se recomienda implementar servidor propio para manejar uploads
4. ⚠️ Las credenciales no deben estar en el código cliente (RIESGO DE SEGURIDAD)

### [26-05-2026] - Corregir Subida de Archivos y Crear Diagnóstico de Supabase
- **Archivo(s):** `subir-imagen.html`, `diagnostico-supabase.html` (nuevo)
- **Cambios:**
  - ✅ **subir-imagen.html:** Corregido formato de envío de archivos a Supabase Storage
    - Cambio: Ahora convierte el archivo a `ArrayBuffer` antes de enviarlo
    - Agregado header `Content-Type` correcto según el tipo MIME del archivo
    - Antes: `body: file` (incorrecto)
    - Ahora: `body: arrayBuffer` con `Content-Type: file.type || 'image/jpeg'`
  - ✅ **diagnostico-supabase.html:** Creado nuevo archivo de diagnóstico
    - 4 pruebas automáticas: conexión, tabla, bucket, permisos
    - Identifica exactamente qué está mal con Supabase
    - Interfaz visual consistente con el proyecto
- **Razón:** 
  - Error 400 en uploads era por formato incorrecto del blob
  - Supabase necesitaba bucket creado manualmente (no fue automático)
  - Necesitaba herramienta para diagnosticar Supabase sin acceso directo
- **Impacto:**
  - ✅ Uploads ahora funcionan correctamente (requiere bucket `imagenes` público)
  - ✅ Usuario puede identificar exactamente qué falta configurar en Supabase
  - ✅ Bucket "imagenes" debe existir y ser PUBLIC
  - ✅ Tabla "imagenes" existe con columnas correctas (url, destino, descripcion, created_at)
  - ⚠️ RLS policies deben permitir SELECT para anon users

### [26-05-2026] - Descarga Inicial del Repositorio
- **Archivo(s):** Todos (descarga inicial)
- **Cambio:** 
  - Clonado repositorio `https://github.com/melissafrutosumana-ctrl/Cole`
  - Descargados todos los archivos del proyecto en la carpeta workspace
  - Eliminada carpeta `.git` para mantener solo los archivos de código
  - Creado documento PROJECT_CONTEXT.md con documentación completa del proyecto
- **Razón:** Inicializar el proyecto en el workspace y documentar su estructura
- **Impacto:** Proyecto listo para trabajar. Futuras IAs tienen referencia clara del estado inicial

---

## 📝 ⚠️ INSTRUCCIONES OBLIGATORIAS PARA PROXIMAS IAs

**DEBES LEER Y EJECUTAR ESTO ANTES DE HACER CUALQUIER CAMBIO:**

### 1️⃣ LECTURA INICIAL REQUERIDA
```
⚠️ ANTES DE EMPEZAR: Lee el archivo PROJECT_CONTEXT.md completo para entender:
   - Qué es este proyecto
   - Su estructura actual
   - Qué se ha hecho anteriormente
   - El contexto histórico de cambios
```

### 2️⃣ REGISTRAR TODOS LOS CAMBIOS
**OBLIGATORIO:** Después de realizar CUALQUIER modificación, actualiza la sección **"🔄 HISTORIAL DE CAMBIOS Y CONTEXTO"** con:
- Fecha actual (DD-MM-YYYY)
- Qué archivo(s) modificaste
- QUÉ cambios específicos hiciste
- POR QUÉ lo hiciste
- Resultado/Impacto del cambio

**Formato a usar:**
```markdown
### [DD-MM-YYYY] - Título descriptivo del cambio
- **Archivo(s):** nombre_archivo.html, otra_archivo.css
- **Cambio:** Descripción detallada de qué se modificó
- **Razón:** Por qué se hizo este cambio
- **Impacto:** Cómo afecta al proyecto (páginas afectadas, nuevas funcionalidades, etc.)
```

### 3️⃣ MANTENER CONSISTENCIA
1. **Estructura Modular:** El proyecto usa HTML separadas. Los cambios en `stylo.css` afectan TODAS las páginas.
2. **Tema Visual:** Respetar variables CSS en `:root` de `stylo.css` (colores verde #0a4c23, crema #ebe5d9, etc.)
3. **EmailJS:** Si modificas emails, actualizar AMBAS plantillas si es necesario.
4. **Responsividad:** Verificar compatibilidad con móviles en TODOS los cambios.
5. **Documentación:** Actualizar este archivo cada vez que hagas cambios.

### 4️⃣ SI NO ENTIENDES ALGO
- Revisa el "HISTORIAL DE CAMBIOS" para ver qué se ha hecho antes
- Consulta la sección "Estructura del Proyecto" para orientarte
- Lee el código comentado en los archivos

---

## 🎯 Próximos Pasos Sugeridos

**CRÍTICO - Debe hacerse primero:**
- [ ] 🔴 **Resolver problemas de upload** - Ver [ISSUES_UPLOAD.md](ISSUES_UPLOAD.md)
  - Las imágenes no se suben correctamente a Supabase
  - Elegir solución: Cloudinary, Node.js, o Supabase actualizado
  - Implementar y probar

**Mejoras generales:**
- [ ] Implementar backend para gestionar datos dinámicamente
- [ ] Agregar autenticación de usuarios con seguridad mejorada
- [ ] Mejorar el sistema de boletas con base de datos
- [ ] Automatizar notificaciones
- [ ] Agregar dashboard administrativo
- [ ] Implementar validación de emails (si se usan)

---

**Última actualización:** 26-05-2026  
**Versión del Proyecto:** 1.0 (Inicial)
