# PRIMERA ENTREGA — PROYECTO "SABORYA"

**Asignatura:** Diseño de la plataforma WEB
**Temática:** Comidas (Pedidos, Ofertas, Reservas, Listado de restaurantes, Compras en línea)
**Modalidad:** Trabajo grupal (máximo 3 estudiantes)
**Tipo de entrega:** Primera entrega

---

## 1. PORTADA

```
══════════════════════════════════════════════════════════════════
                    UNIVERSIDAD / INSTITUCIÓN
                Facultad de Ingeniería en Sistemas

                   ASIGNATURA:
              DISEÑO DE LA PLATAFORMA WEB

                  PROYECTO INTEGRADOR:
        "SABORYA — Plataforma web de pedidos de comida
         en línea, ofertas, reservas y listado
         de restaurantes."

                    TEMÁTICA: COMIDAS

                    PRIMERA ENTREGA

                INTEGRANTES DEL GRUPO:
            • Integrante 1 — Líder de grupo
            • Integrante 2
            • Integrante 3

                  DOCENTE: __________
                  PARALELO: __________
                  PERIODO ACADÉMICO: __________

                       AÑO 2026
══════════════════════════════════════════════════════════════════
```

> *Nota: completar los datos personales antes de imprimir o exportar el documento a PDF.*

---

## 2. ÍNDICE

| # | Sección | Página |
|---|---------|--------|
| 1 | Portada | 1 |
| 2 | Índice | 2 |
| 3 | Objetivos del proyecto | 3 |
| 4 | Definición del proyecto | 4 |
| 5 | Organización de la información — Mapa del sitio | 5 |
| 6 | Interfaz gráfica — Diseño de alambre (wireframes) | 6 |
| 7 | Creación del sitio HTML | 7 |
| 8 | Estructura de imágenes | 8 |
| 9 | Estructura del CSS | 9 |
| 10 | Justificación del proyecto | 10 |
| 11 | Planificación del proyecto | 11 |

---

## 3. OBJETIVOS DEL PROYECTO

### 3.1 Objetivo General

Diseñar e implementar una plataforma web denominada **SABORYA**, basada en HTML, CSS y posteriormente en **Java Spring Boot + MySQL**, que permita a los usuarios consultar restaurantes, realizar pedidos en línea, reservar mesas y aprovechar ofertas, de manera clara, organizada y accesible desde cualquier dispositivo.

### 3.2 Objetivos Específicos

1. Definir la estructura de almacenamiento más idónea para la información de restaurantes, productos, pedidos, reservas y usuarios mediante una base de datos relacional MySQL.
2. Diseñar una interfaz gráfica amigable e intuitiva que facilite la navegación del usuario final (cliente del restaurante) en cualquier dispositivo.
3. Organizar la información mediante un **mapa de sitio** y **wireframes** que sirvan de base al desarrollo posterior con Java Spring Boot.
4. Implementar la estructura HTML, CSS e imágenes que servirán como base para el sitio dinámico de la segunda entrega.
5. Justificar la utilidad social y comercial del proyecto, así como planificar las fases de desarrollo hasta la entrega final.

---

## 4. DEFINICIÓN DEL PROYECTO

**SABORYA** es una plataforma web orientada al sector de **comidas y restaurantes**. La plataforma centraliza en un solo sitio los servicios que típicamente ofrecen las cadenas y restaurantes independientes, permitiendo que el usuario:

- Consulte un **listado de restaurantes** afiliados, con su carta, horario, ubicación y calificación.
- Realice **pedidos en línea** (delivery o retiro en local) seleccionando platos individuales o combos.
- Acceda a **ofertas y promociones** vigentes por restaurante o por categoría.
- Realice **reservas de mesa** indicando fecha, hora y número de personas.
- Efectúe **compras en línea** pagando con distintos métodos (tarjeta, transferencia, pago en local).

### 4.1 Público objetivo

- Personas entre 18 y 55 años con acceso a internet, que buscan ahorrar tiempo al pedir comida o reservar.
- Empleados de oficina, estudiantes universitarios y familias.
- Restaurantes pequeños y medianos que necesitan visibilidad digital sin contratar un desarrollo a la medida.

### 4.2 Alcance

Para la **Primera Entrega** el proyecto comprende:

- Diseño de la estructura de información (mapa de sitio).
- Wireframes (diseño de alambre) de las pantallas principales.
- Sitio web **estático** en HTML5 + CSS3 con todas las páginas navegables.
- Estructura organizada de imágenes y hojas de estilo.
- Documentación de justificación y planificación.

La parte dinámica (formularios funcionales, Java Spring Boot, MySQL, autenticación, manual de uso y publicación en hosting) corresponde a la **Entrega Final**.

---

## 5. ORGANIZACIÓN DE LA INFORMACIÓN

### 5.1 Mapa del sitio web

```
                              ┌─────────────────────┐
                              │       INICIO        │
                              │   (index.html)      │
                              └──────────┬──────────┘
                                         │
   ┌─────────────┬──────────────┬────────┼────────┬──────────────┬──────────────┐
   │             │              │        │        │              │              │
┌──▼───┐   ┌─────▼──────┐  ┌────▼────┐ ┌─▼────┐ ┌─▼────────┐ ┌───▼──────┐ ┌─────▼─────┐
│Restau│   │   Menú /   │  │ Ofertas │ │Pedido│ │ Reservas │ │ Compras  │ │  Contacto │
│rantes│   │  Productos │  │         │ │      │ │          │ │ en línea │ │           │
└──┬───┘   └─────┬──────┘  └────┬────┘ └──┬───┘ └────┬─────┘ └────┬─────┘ └───────────┘
   │             │              │         │          │            │
   │       ┌─────▼──────┐       │   ┌─────▼──────┐   │      ┌─────▼──────┐
   │       │  Detalle   │       │   │  Carrito   │   │      │  Checkout  │
   │       │   plato    │       │   │            │   │      │   /Pago    │
   │       └────────────┘       │   └─────┬──────┘   │      └────────────┘
   │                            │         │          │
┌──▼──────────┐                 │   ┌─────▼──────┐   │
│  Detalle de │                 │   │ Confirmac. │   │
│ restaurante │                 │   │  pedido    │   │
└─────────────┘                 │   └────────────┘   │
                                │                    │
                                │              ┌─────▼──────┐
                                │              │ Confirmac. │
                                │              │  reserva   │
                                │              └────────────┘
                                │
                          ┌─────▼─────┐
                          │  Cupones  │
                          └───────────┘

      ┌──────── Zona de Usuario (transversal) ────────┐
      │   • Iniciar sesión   • Registro   • Mi cuenta │
      │   • Mis pedidos      • Mis reservas           │
      └────────────────────────────────────────────────┘
```

### 5.2 Secciones principales del sitio

| Sección | Descripción funcional |
|---------|----------------------|
| **Inicio** | Página de bienvenida con banner, restaurantes destacados, categorías y ofertas del día. |
| **Restaurantes** | Listado filtrable por categoría, ubicación y calificación. |
| **Menú / Productos** | Catálogo de platos con buscador, filtros, fotos y precios. |
| **Ofertas** | Promociones vigentes, cupones, combos y descuentos. |
| **Pedidos** | Carrito de compras, cantidades, dirección de envío. |
| **Reservas** | Formulario de reserva con fecha, hora y cantidad de personas. |
| **Compras en línea** | Checkout con datos del cliente y método de pago. |
| **Contacto** | Datos de la empresa, formulario y mapa. |
| **Mi cuenta** | Acceso a historial de pedidos y reservas (segunda entrega). |

---

## 6. INTERFAZ GRÁFICA — DISEÑO DE ALAMBRE (WIREFRAMES)

Los wireframes de baja fidelidad se encuentran en formato SVG dentro de la carpeta `wireframes/` del repositorio:

| Wireframe | Archivo |
|-----------|---------|
| Página de Inicio | `wireframes/wf-01-inicio.svg` |
| Listado de Restaurantes | `wireframes/wf-02-restaurantes.svg` |
| Menú / Productos | `wireframes/wf-03-menu.svg` |
| Reservas | `wireframes/wf-04-reservas.svg` |
| Pedido / Carrito | `wireframes/wf-05-pedido.svg` |

### 6.1 Descripción visual (Inicio)

```
┌────────────────────────────────────────────────────────────────┐
│ LOGO SABORYA   [Inicio] [Restaurantes] [Menú] [Ofertas] [...]  │  ← Header
│                                  [ 🔍 Buscar... ] [Iniciar S.] │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│              ████  BANNER PRINCIPAL  ████                      │
│              "Pide tu comida favorita en minutos"              │
│                       [ Pedir ahora ]                          │
│                                                                │
├────────────────────────────────────────────────────────────────┤
│  Categorías:  🍕 Pizza  🍔 Burgers  🍣 Sushi  🥗 Saludable     │
├────────────────────────────────────────────────────────────────┤
│  Restaurantes destacados                                       │
│  ┌──────┐  ┌──────┐  ┌──────┐  ┌──────┐                        │
│  │ IMG  │  │ IMG  │  │ IMG  │  │ IMG  │                        │
│  │ Nom. │  │ Nom. │  │ Nom. │  │ Nom. │                        │
│  └──────┘  └──────┘  └──────┘  └──────┘                        │
├────────────────────────────────────────────────────────────────┤
│  Ofertas del día                                               │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                        │
│  │ 2x1 PIZZA│ │ -30% SUSHI│ │ COMBO 5$│                        │
│  └──────────┘ └──────────┘ └──────────┘                        │
├────────────────────────────────────────────────────────────────┤
│ Footer:  Sobre nosotros | Contacto | Términos | Redes sociales │
└────────────────────────────────────────────────────────────────┘
```

---

## 7. CREACIÓN DEL SITIO HTML

Se desarrolló la estructura HTML5 estática con las siguientes páginas, todas enlazadas entre sí siguiendo el mapa de sitio:

```
site/
├── index.html                  ← Página de inicio
└── pages/
    ├── restaurantes.html       ← Listado de restaurantes
    ├── menu.html               ← Catálogo de platos
    ├── ofertas.html            ← Ofertas y promociones
    ├── pedido.html             ← Carrito / pedido
    ├── reservas.html           ← Formulario de reserva
    ├── compras.html            ← Compra en línea / checkout
    └── contacto.html           ← Contacto
```

### 7.1 Principios aplicados

- HTML5 **semántico** (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- Compatibilidad **responsive** mediante `<meta name="viewport">`.
- Codificación UTF-8 para soportar correctamente acentos y caracteres especiales.
- Estructura repetida (header / footer) para facilitar la conversión posterior a plantillas Thymeleaf en la entrega final.

---

## 8. ESTRUCTURA DE IMÁGENES

```
site/img/
├── logo/         ← Logotipo principal y variaciones
│   └── README.txt
├── banners/      ← Imágenes grandes para hero / portada
│   └── README.txt
├── platos/       ← Fotografías de platos del catálogo
│   └── README.txt
├── restaurantes/ ← Portadas y logos de cada restaurante
│   └── README.txt
└── iconos/       ← Íconos de categorías, redes sociales, UI
    └── README.txt
```

### 8.1 Convenciones de nombrado

| Tipo | Patrón | Ejemplo |
|------|--------|---------|
| Logo | `logo-<variante>.svg` | `logo-principal.svg` |
| Banner | `banner-<seccion>-<n>.jpg` | `banner-inicio-1.jpg` |
| Plato | `plato-<categoria>-<n>.jpg` | `plato-pizza-01.jpg` |
| Restaurante | `rest-<slug>.jpg` | `rest-pizzeria-luna.jpg` |
| Ícono | `ico-<accion>.svg` | `ico-carrito.svg` |

Se prefieren formatos **SVG** para logos e íconos (escalables) y **JPG/WebP** comprimidos para fotografías.

---

## 9. ESTRUCTURA DEL CSS

```
site/css/
├── base.css         ← Reset, variables, tipografía
├── layout.css       ← Header, footer, grid, contenedores
├── components.css   ← Botones, tarjetas, formularios
└── pages.css        ← Estilos específicos por página
```

### 9.1 Metodología

Se aplica una metodología tipo **BEM ligero** y **variables CSS** (`:root`) para colores y tipografías, lo que permite mantener una identidad visual consistente y facilita los ajustes posteriores.

### 9.2 Paleta de colores

| Rol | Variable | Color |
|------|----------|-------|
| Primario | `--color-primary` | `#E63946` (rojo apetitoso) |
| Secundario | `--color-secondary` | `#F1A208` (mostaza) |
| Fondo claro | `--color-bg` | `#FFF8F0` |
| Texto | `--color-text` | `#1D1D1D` |
| Acento | `--color-accent` | `#2A9D8F` |

---

## 10. JUSTIFICACIÓN DEL PROYECTO

En la actualidad, el consumo de comida a través de plataformas digitales ha crecido de forma sostenida. Sin embargo, **muchos restaurantes pequeños y medianos no cuentan con presencia digital propia** y dependen totalmente de aplicaciones de terceros que cobran comisiones elevadas.

**SABORYA** se justifica desde tres dimensiones:

### 10.1 Dimensión social

- Facilita a personas con poca disponibilidad de tiempo (trabajadores, estudiantes, adultos mayores) el acceso a alimentos preparados sin necesidad de desplazarse.
- Permite a usuarios con limitaciones de movilidad realizar pedidos y reservas desde casa.

### 10.2 Dimensión tecnológica

- Aplica buenas prácticas de **diseño web responsive** y **arquitectura cliente-servidor** con Java Spring Boot y MySQL en la siguiente fase.
- Pone en práctica los conocimientos de **HTML, CSS, modelado entidad-relación, formularios y conexión a base de datos** vistos en la asignatura.

### 10.3 Dimensión económica

- Brinda a restaurantes locales una vitrina digital de bajo costo.
- Centraliza pedidos, reservas y ofertas, reduciendo errores manuales y mejorando la experiencia del cliente.

---

## 11. PLANIFICACIÓN DEL PROYECTO

### 11.1 Cronograma general

| Fase | Actividad | Duración | Entrega |
|------|-----------|----------|---------|
| 1 | Definición de tema y alcance | 1 semana | Entrega 1 |
| 2 | Mapa de sitio y wireframes | 1 semana | Entrega 1 |
| 3 | Maquetación HTML + CSS estática | 2 semanas | Entrega 1 |
| 4 | Justificación, planificación, documentación | 1 semana | Entrega 1 |
| 5 | Diseño de base de datos (MER) | 1 semana | Entrega Final |
| 6 | Desarrollo Spring Boot + MySQL | 3 semanas | Entrega Final |
| 7 | Formularios dinámicos y validaciones | 1 semana | Entrega Final |
| 8 | Pruebas y ajustes | 1 semana | Entrega Final |
| 9 | Manual de uso y conclusiones | 0.5 semanas | Entrega Final |
| 10 | Publicación en hosting y GitHub | 0.5 semanas | Entrega Final |

### 11.2 Distribución de roles del grupo

| Rol | Responsable | Funciones |
|-----|-------------|-----------|
| Líder de proyecto | Integrante 1 | Coordinación, documentación, evaluaciones |
| Desarrollo Front-End | Integrante 2 | HTML, CSS, wireframes, imágenes |
| Desarrollo Back-End | Integrante 3 | Java Spring Boot, MySQL, modelo entidad-relación |

### 11.3 Recursos / Herramientas

- **IDE principal:** **Apache NetBeans** (utilizado para todo el desarrollo del proyecto, tanto la maquetación HTML/CSS como el back-end Java Spring Boot de la entrega final).
- **Maquetación:** HTML5, CSS3 (editados desde NetBeans).
- **Back-End (entrega final):** Java 17, Spring Boot, Thymeleaf, ejecutado y depurado desde NetBeans.
- **Base de Datos:** MySQL 8 (servidor local).
- **Versionamiento:** Git + GitHub (repositorio `bp202302/tarea-gupal`), integrado en NetBeans mediante su soporte Git nativo.
- **Diseño de wireframes:** SVG.

### 11.4 Porcentaje de avance — Primera Entrega

| Componente | Avance |
|------------|--------|
| Documentación (puntos 1–6, 10, 11) | 100 % |
| Sitio HTML estático | 100 % |
| Estructura de imágenes | 100 % |
| Estructura de CSS | 100 % |
| Wireframes | 100 % |
| Base de datos (MER) | 0 % (Entrega final) |
| Lógica Spring Boot | 0 % (Entrega final) |
| **AVANCE TOTAL DEL PROYECTO** | **≈ 55 %** |

### 11.5 Autoevaluación, evaluación al líder y entre integrantes

Estas matrices se entregarán **firmadas por cada integrante** junto al documento individual el día de la evaluación, conforme lo solicita la guía:

- Autoevaluación (1 por integrante).
- Evaluación al líder de grupo.
- Evaluación entre integrantes.

---

*Fin de la Primera Entrega.*
