# Tarea-Gupal — Proyecto SABORYA

Proyecto académico de la asignatura **Diseño de la plataforma WEB**.

**Temática:** Comidas (Pedidos, Ofertas, Reservas, Listado de restaurantes, Compras en línea).
**Nombre del proyecto:** SABORYA — plataforma web para realizar pedidos de comida en línea, reservar mesas y aprovechar ofertas de restaurantes afiliados.

---

## Estado de las entregas

| Entrega | Estado |
|---------|--------|
| **Primera Entrega (puntos 1–11)** | ✅ Completada |
| Entrega Final (puntos 12–19 + extras) | ⏳ Pendiente |

---

## Estructura del repositorio

```
.
├── README.md                       Este archivo
├── docs/
│   └── ENTREGA-1.md                Documento completo de la Primera Entrega
├── site/                           Sitio web estático (HTML + CSS)
│   ├── index.html                  Página de inicio
│   ├── css/
│   │   ├── base.css                Reset, variables, tipografía
│   │   ├── layout.css              Header, footer, grids, contenedores
│   │   ├── components.css          Botones, tarjetas, formularios, badges
│   │   └── pages.css               Estilos específicos por página
│   ├── img/                        Recursos gráficos organizados por tipo
│   │   ├── logo/
│   │   ├── banners/
│   │   ├── platos/
│   │   ├── restaurantes/
│   │   └── iconos/
│   └── pages/                      Resto de páginas del sitio
│       ├── restaurantes.html
│       ├── menu.html
│       ├── ofertas.html
│       ├── reservas.html
│       ├── pedido.html
│       ├── compras.html
│       └── contacto.html
└── wireframes/                     Diseño de alambre (SVG)
    ├── wf-01-inicio.svg
    ├── wf-02-restaurantes.svg
    ├── wf-03-menu.svg
    ├── wf-04-reservas.svg
    └── wf-05-pedido.svg
```

---

## IDE utilizado

El proyecto se desarrolla en **Apache NetBeans 8.2** y es compatible con versiones posteriores. Está configurado como **proyecto HTML5/JS** (carpeta `nbproject/`).

Para abrirlo:

1. Abrir NetBeans 8.2 → **File → Open Project...** (NO "Open File").
2. Navegar hasta la carpeta `Tarea-Gupal/` — debe aparecer el ícono naranja de proyecto HTML5.
3. Seleccionarla y pulsar **Open Project**.
4. Una vez cargado el proyecto se mostrará en el panel "Projects" con el nombre **SABORYA**.
5. Para ejecutar: clic derecho sobre el proyecto → **Run** (lanzará `index.html` en el navegador integrado de Chrome).
6. Git está integrado vía **Team → Git** dentro de NetBeans.

> Si NetBeans 8.2 no muestra el navegador integrado de Chrome, instalá la extensión "NetBeans Connector" en Chrome, o cambiá el navegador en **Properties → Run → Browser**.

---

## ¿Cómo visualizar el sitio?

Abre `site/index.html` directamente en tu navegador (o desde NetBeans con "Run File"), o sirve la carpeta con cualquier servidor estático:

```bash
# Opción 1: Python
cd site && python3 -m http.server 8080

# Opción 2: Node (si tienes 'serve' instalado)
npx serve site
```

Luego abre `http://localhost:8080` en el navegador.

---

## Contenido cubierto en la Primera Entrega

1. Portada
2. Índice
3. Objetivos del proyecto
4. Definición del proyecto
5. Organización de la información — Mapa del sitio
6. Interfaz gráfica — Wireframes
7. Creación del sitio HTML
8. Estructura de imágenes
9. Estructura del CSS
10. Justificación del proyecto
11. Planificación del proyecto

El detalle completo se encuentra en [`docs/ENTREGA-1.md`](docs/ENTREGA-1.md).
