# Instrucciones personalizadas para Copilot - Canarias con Mozambique

Este es el sitio web de la ONG "Canarias con Mozambique", una organización humanitaria con 25 años de experiencia trabajando en proyectos de solidaridad internacional en Mozambique.

## Tecnologías y herramientas

Usamos Hugo como generador de sitios estáticos con el tema "wishfund-hugo". Cuando generes código o sugieras cambios, ten en cuenta estas tecnologías:

- Hugo v0.150.0 o superior
- Tema: wishfund-hugo
- Bootstrap CSS para componentes responsivos
- Markdown para contenido con front matter YAML
- JavaScript vanilla (sin frameworks)

## Idioma y localización

El sitio está completamente en español (España). El contenido debe:

- Usar español como idioma principal
- Configurar fechas en formato español
- Usar terminología apropiada para ONGs y trabajo humanitario
- Dirigirse a audiencia española/canaria interesada en cooperación internacional

## Estructura del contenido

El contenido se organiza en estas secciones principales:

- `/blog/` - Artículos sobre actividades, reconocimientos y noticias
- `/causes/` - Proyectos y causas que apoyamos
- `/event/` - Eventos y actividades organizadas
- `/about/` - Información sobre la organización
- `/volunteer/` - Información para voluntarios
- `/donation/` - Página de donaciones
- `/contact/` - Información de contacto

## Categorías y etiquetado

Para artículos de blog, usa estas categorías existentes:

- "Medios" - Para cobertura mediática y reconocimientos
- "Agua" - Proyectos relacionados con agua potable
- "Educación" - Proyectos educativos
- "Salud" - Proyectos de salud
- "Alimentación" - Seguridad alimentaria
- "Vivienda" - Vivienda y refugio

Tags comunes: "mozambique", "canarias", "agüimes", "voluntariado", "cooperación", "solidaridad", años como "2025", "2024".

## Gestión de imágenes

Las imágenes se almacenan en `static/images/` con esta estructura:

- `static/images/blog/XXX/` - donde XXX es el número del artículo
- Usar HTML con clases Bootstrap para control responsivo: `class="img-fluid rounded mb-3"`
- Optimizar imágenes para web antes de subirlas
- Usar nombres descriptivos para las imágenes

## Estilo de escritura

El tono debe ser:

- Profesional pero cercano y humano
- Inspirador y motivador para la acción solidaria
- Respetuoso hacia la cultura mozambiqueña
- Enfocado en el impacto positivo y la transparencia
- Inclusivo y accesible

## Desarrollo y deployment

Usa estos comandos para el flujo de trabajo:

- `hugo server` para desarrollo local
- Git con commits descriptivos separando bug fixes de nuevas funcionalidades
- El sitio se despliega automáticamente desde la rama main

## SEO y metadatos

Todos los artículos y páginas deben incluir:

- Títulos optimizados para SEO (máx. 60 caracteres)
- Descripciones meta (máx. 160 caracteres)
- Imágenes principales para redes sociales
- Fechas en formato ISO 8601
- Tags y categorías relevantes
