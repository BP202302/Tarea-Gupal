# PRIMERA ENTREGA — PROYECTO "GASOYA"

**Asignatura:** Diseño de la plataforma WEB
**Temática:** Combustibles (Precios, Ubicaciones, Horarios, Ofertas)
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
        "GASOYA — Plataforma web de consulta de precios
         de combustible, ubicaciones de gasolineras,
         horarios y ofertas en línea."

                 TEMÁTICA: COMBUSTIBLES

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

> *Completar datos personales antes de exportar a PDF.*

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

Diseñar e implementar una plataforma web denominada **GASOYA**, basada en HTML, CSS y posteriormente en **Java Spring Boot + MySQL**, que permita a los conductores y ciudadanos consultar en tiempo real los precios de combustible, ubicar gasolineras cercanas, conocer sus horarios y acceder a ofertas y promociones, de manera clara, organizada y accesible desde cualquier dispositivo.

### 3.2 Objetivos Específicos

1. Definir la estructura de almacenamiento más idónea para la información de gasolineras, tipos de combustible, precios, horarios y ofertas mediante una base de datos relacional MySQL.
2. Diseñar una interfaz gráfica intuitiva y responsive que permita al usuario encontrar la información de combustible que necesita en el menor número de clics posible.
3. Organizar la información mediante un **mapa de sitio** y **wireframes** que sirvan de base al desarrollo dinámico con Java Spring Boot en la entrega final.
4. Implementar la estructura HTML5, CSS3 y carpetas de imágenes que conformarán el sitio estático base.
5. Justificar la utilidad social, ambiental y económica del proyecto, y planificar las fases de desarrollo hasta la entrega final.

---

## 4. DEFINICIÓN DEL PROYECTO

**GASOYA** es una plataforma web orientada al sector de **combustibles y gasolineras**. Centraliza en un solo sitio la información que los conductores necesitan antes y durante el reabastecimiento de su vehículo:

- Consultar **precios actualizados** de gasolina extra, súper y diésel por gasolinera y zona.
- Localizar **gasolineras cercanas** con mapa interactivo, distancia y calificación de usuarios.
- Revisar **horarios de atención** de cada estación de servicio.
- Acceder a **ofertas y promociones** vigentes (descuentos, puntos de fidelidad, combos de servicio).

### 4.1 Público objetivo

- Conductores de vehículos particulares que buscan el mejor precio de combustible antes de tanquear.
- Transportistas y flotas empresariales que necesitan optimizar costos de combustible.
- Ciudadanos en general que requieren saber si una gasolinera está abierta o tiene algún producto disponible.

### 4.2 Alcance de la Primera Entrega

- Diseño del mapa de sitio y wireframes.
- Sitio web **estático** en HTML5 + CSS3 con todas las páginas navegables.
- Estructura organizada de imágenes y hojas de estilo.
- Documentación de justificación y planificación.

La parte dinámica (formularios funcionales con Java Spring Boot, base de datos MySQL, autenticación, geolocalización y publicación en hosting) corresponde a la **Entrega Final**.

---

## 5. ORGANIZACIÓN DE LA INFORMACIÓN

### 5.1 Mapa del sitio web

```
                              ┌─────────────────────┐
                              │       INICIO        │
                              │   (index.html)      │
                              └──────────┬──────────┘
                                         │
   ┌─────────────┬──────────────┬────────┼────────┬──────────────┬────────────┐
   │             │              │        │        │              │            │
┌──▼────────┐ ┌──▼──────────┐ ┌─▼──────┐ ┌─▼────┐ ┌─▼────────┐ ┌─▼────────┐ ┌─▼────────┐
│ Gasolineras│ │  Precios   │ │Horarios│ │Ofertas│ │Calculadora│ │Contacto  │ │Acerca de │
│(Ubicaciones│ │            │ │        │ │       │ │           │ │          │ │          │
└──┬─────────┘ └──┬─────────┘ └────────┘ └──┬───┘ └───────────┘ └──────────┘ └──────────┘
   │              │                          │
   │        ┌─────▼──────┐             ┌─────▼──────┐
   │        │ Histórico  │             │  Cupones   │
   │        │ de precios │             │            │
   │        └────────────┘             └────────────┘
   │
┌──▼──────────┐
│  Detalle de │
│ gasolinera  │
│(mapa+serv.) │
└─────────────┘

      ┌──────── Zona de Usuario (transversal) ────────────┐
      │  • Iniciar sesión   • Registro   • Mi cuenta      │
      │  • Gasolineras favoritas   • Alertas de precio    │
      └───────────────────────────────────────────────────┘
```

### 5.2 Secciones principales

| Sección | Descripción funcional |
|---------|----------------------|
| **Inicio** | Banner, buscador de gasolineras por zona, precios del día, noticias de combustible. |
| **Gasolineras** | Listado filtrable por marca, tipo de combustible, servicio y zona. |
| **Precios** | Tabla comparativa de precios: Extra, Súper, Diésel, Gas Natural. |
| **Horarios** | Consulta de horarios por estación; filtro de gasolineras abiertas ahora. |
| **Ofertas** | Promociones vigentes, cupones de descuento y programas de fidelidad. |
| **Calculadora** | Calcula el costo de llenar el tanque según el precio actual. |
| **Contacto** | Datos de la empresa, formulario y mapa. |

---

## 6. INTERFAZ GRÁFICA — DISEÑO DE ALAMBRE (WIREFRAMES)

Los wireframes de baja fidelidad se encuentran en formato SVG en la carpeta `wireframes/`:

| Wireframe | Archivo |
|-----------|---------|
| Página de Inicio | `wireframes/wf-01-inicio.svg` |
| Gasolineras / Ubicaciones | `wireframes/wf-02-gasolineras.svg` |
| Precios | `wireframes/wf-03-precios.svg` |
| Horarios | `wireframes/wf-04-horarios.svg` |
| Ofertas | `wireframes/wf-05-ofertas.svg` |

### 6.1 Descripción visual (Inicio)

```
┌──────────────────────────────────────────────────────────────────┐
│ ⛽ GASOYA   [Inicio][Gasolineras][Precios][Horarios][Ofertas][…] │  ← Header
│                        [ 🔍 Buscar gasolinera o ciudad… ]        │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│           ████  BANNER — "¿A cuánto está la gasolina?"  ████     │
│                   [ Consultar precios ]  [ Encontrar gasolinera ]│
│                                                                  │
├──────────────────────────────────────────────────────────────────┤
│  Precios del día:  Extra $X.XX | Súper $X.XX | Diésel $X.XX     │
├──────────────────────────────────────────────────────────────────┤
│  Gasolineras destacadas (mejor precio / más cercanas)            │
│  ┌──────┐  ┌──────┐  ┌──────┐  ┌──────┐                          │
│  │ IMG  │  │ IMG  │  │ IMG  │  │ IMG  │                          │
│  │ Nom. │  │ Nom. │  │ Nom. │  │ Nom. │                          │
│  └──────┘  └──────┘  └──────┘  └──────┘                          │
├──────────────────────────────────────────────────────────────────┤
│  Ofertas del día                                                 │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐                        │
│  │ -$0.05/gal│ │ 2x lavado│ │ Puntos x2│                        │
│  └──────────┘  └──────────┘  └──────────┘                        │
├──────────────────────────────────────────────────────────────────┤
│ Footer:  Sobre nosotros | Contacto | Términos | Redes sociales   │
└──────────────────────────────────────────────────────────────────┘
```

---

## 7. CREACIÓN DEL SITIO HTML

Estructura de páginas HTML5 estáticas, todas enlazadas entre sí:

```
site/
├── index.html                  ← Página de inicio
└── pages/
    ├── gasolineras.html        ← Listado y ubicaciones de gasolineras
    ├── precios.html            ← Tabla comparativa de precios
    ├── horarios.html           ← Horarios de atención
    ├── ofertas.html            ← Ofertas y promociones
    ├── calculadora.html        ← Calculadora de costo de tanqueo
    └── contacto.html           ← Contacto
```

### 7.1 Principios aplicados

- HTML5 semántico (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- Diseño **responsive** con `<meta name="viewport">` para móviles y tablets.
- Codificación UTF-8.
- Estructura replicable a plantillas **Thymeleaf** para la entrega final con Spring Boot.

---

## 8. ESTRUCTURA DE IMÁGENES

```
site/img/
├── logo/         ← Logotipo principal de GASOYA
│   └── README.txt
├── banners/      ← Imágenes hero / cabecera de sección
│   └── README.txt
├── estaciones/   ← Fotos y logos de cada gasolinera
│   └── README.txt
├── mapas/        ← Capturas o recursos de mapas / íconos de pin
│   └── README.txt
└── iconos/       ← Íconos de tipos de combustible, servicios, UI
    └── README.txt
```

### 8.1 Convenciones de nombrado

| Tipo | Patrón | Ejemplo |
|------|--------|---------|
| Logo | `logo-<variante>.svg` | `logo-principal.svg` |
| Banner | `banner-<seccion>.jpg` | `banner-inicio.jpg` |
| Estación | `est-<slug>.jpg` | `est-petroecuador-norte.jpg` |
| Mapa | `mapa-<zona>.png` | `mapa-quito-norte.png` |
| Ícono | `ico-<nombre>.svg` | `ico-extra.svg`, `ico-diesel.svg` |

---

## 9. ESTRUCTURA DEL CSS

```
site/css/
├── base.css         ← Reset, variables CSS, tipografía
├── layout.css       ← Header, footer, grid, contenedores
├── components.css   ← Botones, tarjetas, tablas, formularios
└── pages.css        ← Estilos específicos por página
```

### 9.1 Paleta de colores

| Rol | Variable | Color |
|------|----------|-------|
| Primario | `--color-primary` | `#F77F00` (naranja energía) |
| Secundario | `--color-secondary` | `#1B2A41` (azul marino profundo) |
| Fondo claro | `--color-bg` | `#F4F6F9` |
| Texto | `--color-text` | `#1A1A1A` |
| Acento / éxito | `--color-accent` | `#2EC4B6` (verde-azul) |
| Peligro / extra | `--color-danger` | `#E63946` |

### 9.2 Metodología

Variables CSS en `:root`, nomenclatura tipo BEM ligero, diseño mobile-first con `@media (max-width: 720px)`.

---

## 10. JUSTIFICACIÓN DEL PROYECTO

### 10.1 Dimensión social

El precio del combustible afecta directamente el costo de vida de millones de familias y negocios. **GASOYA** democratiza el acceso a esta información: cualquier persona con un celular puede comparar precios antes de tanquear y tomar la mejor decisión sin depender de terceros ni datos desactualizados.

### 10.2 Dimensión económica

- Los conductores pueden ahorrar dinero al elegir la gasolinera con el mejor precio por galón.
- Las flotas de transporte y empresas logísticas pueden optimizar sus rutas y costos de combustible.
- Las gasolineras locales obtienen visibilidad digital sin necesidad de contratar desarrollo web propio.

### 10.3 Dimensión ambiental

Al optimizar rutas hacia gasolineras cercanas y abiertas, se reduce el consumo innecesario de combustible buscando una estación, contribuyendo a menor emisión de gases contaminantes.

### 10.4 Dimensión tecnológica

El proyecto aplica buenas prácticas de diseño web responsive, arquitectura MVC con Java Spring Boot, modelo entidad-relación en MySQL, y versionamiento con Git/GitHub, integrando los conocimientos del eje de la asignatura.

---

## 11. PLANIFICACIÓN DEL PROYECTO

### 11.1 Cronograma general

| Fase | Actividad | Duración | Entrega |
|------|-----------|----------|---------|
| 1 | Definición de tema y alcance | 1 semana | Entrega 1 |
| 2 | Mapa de sitio y wireframes | 1 semana | Entrega 1 |
| 3 | Maquetación HTML + CSS estática | 2 semanas | Entrega 1 |
| 4 | Justificación, planificación y documentación | 1 semana | Entrega 1 |
| 5 | Diseño de base de datos (MER) | 1 semana | Entrega Final |
| 6 | Desarrollo Spring Boot + MySQL | 3 semanas | Entrega Final |
| 7 | Formularios dinámicos y validaciones | 1 semana | Entrega Final |
| 8 | Pruebas y ajustes | 1 semana | Entrega Final |
| 9 | Manual de uso y conclusiones | 0.5 semanas | Entrega Final |
| 10 | Publicación en hosting y GitHub | 0.5 semanas | Entrega Final |

### 11.2 Distribución de roles

| Rol | Responsable | Funciones |
|-----|-------------|-----------|
| Líder de proyecto | Integrante 1 | Coordinación, documentación, evaluaciones |
| Desarrollo Front-End | Integrante 2 | HTML, CSS, wireframes, imágenes |
| Desarrollo Back-End | Integrante 3 | Java Spring Boot, MySQL, MER |

### 11.3 Herramientas

- **IDE:** Apache NetBeans 8.2 (Java 8).
- **Front-End:** HTML5, CSS3.
- **Back-End (entrega final):** Java 8, Spring Boot 2.7.x, Thymeleaf.
- **Base de Datos:** MySQL 8, diseñado desde NetBeans y MySQL Workbench.
- **Versionamiento:** Git + GitHub (`bp202302/tarea-gupal`), integrado en NetBeans vía Team → Git.
- **Wireframes:** SVG.

### 11.4 Porcentaje de avance — Primera Entrega

| Componente | Avance |
|------------|--------|
| Documentación (puntos 1–6, 10, 11) | 100 % |
| Sitio HTML estático (7 páginas) | 100 % |
| Estructura de imágenes | 100 % |
| Estructura CSS (4 archivos) | 100 % |
| Wireframes (5 pantallas) | 100 % |
| Modelo Entidad-Relación | 0 % (Entrega Final) |
| Lógica Spring Boot + MySQL | 0 % (Entrega Final) |
| **AVANCE TOTAL DEL PROYECTO** | **≈ 50 %** |

### 11.5 Autoevaluación y evaluaciones cruzadas

Se entregará firmado el día de la evaluación (una por integrante):

- Autoevaluación individual.
- Evaluación al líder de grupo.
- Evaluación entre integrantes.

---

*Fin de la Primera Entrega.*
