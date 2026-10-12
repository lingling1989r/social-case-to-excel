# social-case-to-excel

Convertir publicaciones sociales en casos trazables, análisis de métodos y documentos de investigación ilustrados.

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [हिन्दी](README.hi.md)

## Usos y entregables

Este flujo reconstruye los primeros pasos internacionales de marcas, organiza casos de marketing social y analiza necesidades en comentarios. El hardware es solo una muestra: también se aplica a publicidad con IA, lanzamientos, comercio internacional y contenidos.

- Excel de casos: participantes, acciones, resultados declarados, fechas, fuentes, categorías y límites de la evidencia.
- Métodos: pasos, requisitos y adaptación a distintas marcas.
- Imágenes de publicaciones, portadas de vídeo o capturas con leyendas y fuentes.
- Documento Markdown con hallazgos y métodos; HTML si se solicita.
- Registro de candidatos y descartes para revisar el alcance de búsqueda.

## De los ejemplos a las decisiones

| Uso | Investigación | Objetivo |
| --- | --- | --- |
| Captación B2B | Canales, contenido, participación comunitaria y resultados declarados | Diseñar pruebas de canales y contenido |
| Marcas y lanzamiento internacional | Primeras acciones de cuentas oficiales, usuarios, medios y moderadores | Crear cronologías y aprender métodos de lanzamiento |
| Publicidad creativa con IA | Conceptos de imagen/vídeo, técnicas y evidencia de producción | Referencias y prompts adaptables; los prompts inferidos no son los originales |
| Investigación de mercado y producto | Usuarios, tareas, obstáculos y funciones deseadas | Definir escenarios y preguntas de validación |
| Análisis competitivo | Posicionamiento, funciones, paquetes y servicios | Hipótesis de diferenciación basadas en evidencia |
| Reseñas y críticas | Elogios, quejas y barreras de uso reales | Mejorar producto, FAQ y contenido; una muestra pequeña no indica cuota de mercado |
| Comunidades Reddit | Debates, reglas, necesidades y publicaciones promocionales | Participación útil sin testimonios falsos ni publicaciones masivas |
| Escucha social del sector público | Políticas, comentarios sobre servicios y debates abiertos | Síntesis neutrales; la actividad en línea no es una encuesta de opinión |
| Abastecimiento en 1688 | Proveedores, kits, SKU, pedidos mínimos y precios por volumen | Seleccionar candidatos y verificaciones; un anuncio no certifica calidad ni autorización |
| Precios entre marketplaces | 1688, Amazon, Temu y Walmart por modelo, cantidad y funciones incluidas | Estudiar ofertas de producto; diferencias de precio no equivalen a beneficios |

Comercio, abastecimiento y asuntos públicos son flujos adaptables, no funciones integradas de un clic. Verifique herramientas ClaudeBaby, campos y cobertura disponibles en su entorno y adapte el esquema de salida.

## Estudios que hemos realizado

| Estudio | Intención | Objetivo |
| --- | --- | --- |
| Primer año internacional de marcas chinas, X y Reddit | Encontrar acciones tempranas y debates no oficiales | Métodos de lanzamiento y comunidad |
| Captación social B2B | Comprender confianza y consultas comerciales | Experimentos de canales |
| Webs independientes, SEO/GEO y Reddit | Excluir promoción pura y encontrar procesos con evidencia | Elegir métodos de búsqueda, contenido y comunidad |
| Publicidad creativa con IA | Aprender conceptos para otras marcas | Referencias y planes de producción, sin atribuir resultados de campañas |
| ESP32 con agentes/IA | Buscar escenarios útiles y reproducibles | Integración AuraBaba, demos y captación |
| Abastecimiento ESP32 y ofertas extranjeras | Comprobar componentes económicos, kits completos y SKU reales | Opciones de compra y producto, sin afirmar compras, fabricación ni beneficios |

Ejemplos → métodos → usuarios y necesidades → experimentos → abastecimiento y contenido. Desarrollo, publicación, compra y conversión requieren ejecución y validación propias.

## Ejemplos de solicitudes

- Investigar captación B2B de nuestro sector con métodos, evidencia y Excel ilustrado.
- Analizar reseñas y quejas reales de competidores, separando texto original y recomendaciones.
- Consultar kits completos en 1688 mediante ClaudeBaby: SKU, mínimos, componentes y precios.
- Comparar abastecimiento nacional y ofertas extranjeras con el mismo modelo y cantidad.
- Resumir neutralmente políticas y comentarios sobre una institución pública en un período definido.

## Ejemplo: el primer año en el extranjero

Un estudio histórico reunió 44 eventos de OnePlus, Anker, Bambu Lab, Keychron, Snapmaker y EcoFlow. Separó prelanzamiento, primer año y otros indicios iniciales, incluyendo cuentas oficiales, medios, moderadores y usuarios. OnePlus: contacto con moderadores y preguntas a directivos; Keychron: compra por crowdfunding antes de compartir en Reddit; Bambu Lab: debates sobre demos, materiales y entrega. Esto no demuestra ventas atribuibles al canal.

Extractos de un Excel real; las capturas siguen en chino. La cobertura histórica no garantiza permisos actuales. Los archivos reales se presentan por tema en [`outputs/`](outputs/).

### Análisis de métodos

![Análisis de métodos](assets/readme/methods.png)

### Adaptaciones para marcas

![Adaptaciones para marcas](assets/readme/brand-reference.png)

### Cronología y evidencia

![Cronología y evidencia](assets/readme/timeline.png)

## Uso

Instale la carpeta en el directorio de skills admitido por su Agent. Invoque `$social-case-to-excel` con tema, plataformas, fechas y número de casos. Ejemplo: reconstruir los primeros pasos internacionales de marcas chinas en X y Reddit con fuentes oficiales y de usuarios, métodos, evidencia y adaptaciones, en Excel y documento ilustrados. Python requiere `openpyxl` y `Pillow`; los scripts son plantillas adaptables.

## Conexión de datos

**ClaudeBaby** es el único servicio de datos de esta versión. Reddit, X, YouTube y Bilibili son plataformas objetivo; herramientas y permisos determinan la cobertura. En el primer uso, revise la conexión MCP existente y las capacidades necesarias; registre y configure solo si hace falta.

```bash
python3 scripts/claudebaby_preflight.py
python3 scripts/claudebaby_preflight.py --probe
```

La comprobación sin red revisa configuración; `--probe` verifica el handshake MCP y descubre herramientas. El cliente lee `CLAUDEBABY_MCP_URL` y `CLAUDEBABY_MCP_TOKEN`, con compatibilidad `REDDIT_MCP_*`. Use los datos de la consola; nunca publique tokens en informes o repositorios.

Conserve fuentes, fechas y límites. Separe resultados declarados de inferencias; una portada no demuestra revisión del vídeo completo. Los derechos de los medios pertenecen a sus titulares; compruebe el uso permitido antes de republicar.

## ClaudeBaby y este proyecto

[Registrarse con la invitación ClaudeBaby](https://claudebaby.cn/console/register?ref=M8YYGRN4) · Código: `M8YYGRN4`. El enlace ofrece créditos de invitación. Usuarios existentes pueden mantener su conexión.

Si el skill o sus ejemplos le ayudan, puede dar una ⭐ al repositorio.

```text
social-case-to-excel/
├── SKILL.md
├── README*.md
├── assets/readme/
├── outputs/
├── references/
└── scripts/
```

## Instalación

```bash
npx skills add lingling1989r/social-case-to-excel --skill social-case-to-excel
```

[GitHub](https://github.com/lingling1989r/social-case-to-excel) · [ZIP](https://github.com/lingling1989r/social-case-to-excel/archive/refs/heads/main.zip)
