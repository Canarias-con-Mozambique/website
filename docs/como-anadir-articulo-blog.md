# 📝 Cómo añadir un nuevo artículo al blog

## 1. 📁 Crear el archivo del artículo

Los artículos del blog se encuentran en `content/blog/`. Para añadir un nuevo artículo:

1. Crea un nuevo archivo con el formato: `blog-post-X.md` (donde X es el siguiente número)
2. La estructura actual es:
   ```
   content/blog/
   ├── _index.md
   ├── blog-post-1.md
   ├── blog-post-2.md
   ├── ...
   └── blog-post-7.md  (último artículo)
   ```

## 2. 📋 Estructura del artículo

Cada artículo debe tener la siguiente estructura con **front matter** (metadatos) al inicio:

```markdown
---
title: "Título del artículo"
date: 2025-01-20T10:28:32+06:00
draft: false
description: "Descripción breve del artículo para SEO"
bgImage: "images/bg/bg-3.jpg"
image: "images/blog/XXX/imagen-principal.jpg"
categories:
  - "Categoría"
tags:
  - "etiqueta1"
  - "etiqueta2"
  - "etiqueta3"
type: "post"
---

## Contenido del artículo

Aquí va el contenido en formato Markdown...
```

## 3. 🏷️ Metadatos importantes

- **`title`**: Título que aparecerá en la web y SEO
- **`date`**: Fecha y hora de publicación (formato ISO 8601)
- **`draft`**: `false` para publicar, `true` para borrador
- **`description`**: Resumen para motores de búsqueda (máx. 160 caracteres)
- **`image`**: Imagen principal que aparece en listings y redes sociales
- **`categories`**: Categorías existentes: `"Medios"`, `"Water"`, etc.
- **`tags`**: Etiquetas descriptivas del contenido

## 4. 🖼️ Gestión de imágenes

### Estructura de carpetas

```
static/images/blog/
├── 001/
├── 002/
├── ...
└── XXX/  (carpeta del nuevo artículo)
    ├── imagen-principal.jpg
    ├── imagen-secundaria1.jpg
    └── imagen-secundaria2.jpg
```

### Usar imágenes en el artículo

**Imagen principal** (se configura en el front matter):

```markdown
image: "images/blog/XXX/imagen-principal.jpg"
```

**Imágenes en el contenido** (HTML responsivo recomendado):

```html
<div class="text-center mb-4">
  <img
    src="/images/blog/XXX/imagen.jpg"
    alt="Descripción de la imagen"
    class="img-fluid rounded"
    style="max-width: 80%;"
  />
  <p class="text-muted mt-2"><em>Pie de imagen descriptivo</em></p>
</div>
```

**Alternativa en Markdown** (menos control visual):

```markdown
![Descripción de la imagen](/images/blog/XXX/imagen.jpg)
```

## 5. 🎨 Categorías y tags existentes

### Categorías comunes

- `"Medios"` - Para cobertura mediática, entrevistas, reconocimientos
- `"Agua"` - Proyectos relacionados con agua potable
- `"Educación"` - Proyectos educativos
- `"Salud"` - Proyectos de salud

### Tags frecuentes

- Ubicación: `"mozambique"`, `"agüimes"`, `"canarias"`
- Tipo: `"premio"`, `"reconocimiento"`, `"proyecto"`, `"voluntariado"`
- Tema: `"agua"`, `"educación"`, `"salud"`, `"medios"`
- Año: `"2025"`, `"2024"`, etc.

## 6. 🔗 Enlaces y referencias

**Enlaces internos:**

```markdown
[texto del enlace](/causes)
[contáctanos](/contact)
[donaciones](/donation)
```

**Enlaces externos:**

```markdown
[La Provincia](https://www.laprovincia.es/...)
[YouTube](https://www.youtube.com/...)
```

## 7. ⚡ Previsualización y publicación

1. **Ejecutar el servidor local:**

   ```bash
   hugo server
   ```

2. **Previsualizar en:** <http://localhost:1313/blog/>

3. **Hacer commit y push:**

   ```bash
   git add content/blog/blog-post-X.md static/images/blog/XXX/
   git commit -m "Feat: Añadir nuevo artículo sobre [tema]"
   git push origin main
   ```

## 8. ✅ Lista de verificación

Antes de publicar, verifica:

- [ ] **Metadatos completos** en el front matter
- [ ] **Fecha correcta** en formato ISO
- [ ] **Imágenes optimizadas** y en la carpeta correcta
- [ ] **Enlaces funcionando** (internos y externos)
- [ ] **Ortografía y gramática** revisadas
- [ ] **Previsualización** en servidor local
- [ ] **Responsive** - se ve bien en móvil y desktop
- [ ] **SEO** - título y descripción optimizados

## 9. 🔧 Troubleshooting

**Problemas comunes:**

- **Imágenes no aparecen**: Verificar rutas en `static/images/blog/XXX/`
- **Fecha en inglés**: Configuración de idioma en `config.toml`
- **HTML no se renderiza**: Verificar `markup.goldmark.renderer.unsafe = true`
- **Artículo no aparece**: Verificar `draft: false`

---

## 📚 Ejemplo completo

Ver `content/blog/blog-post-7.md` (artículo sobre la Espiga de Oro) como referencia de estructura completa y buenas prácticas.
