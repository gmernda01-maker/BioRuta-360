# BioRuta 360

### Sistema de monitoreo y gestión inteligente de rutas logísticas

BioRuta 360 es una solución desarrollada para digitalizar, monitorear y analizar recorridos logísticos mediante **geolocalización GPS**, gestión de paradas, seguimiento de transportes y herramientas de control administrativo.

El proyecto integra una aplicación móvil para operación en ruta con un panel administrativo orientado al seguimiento, trazabilidad y análisis de recorridos.

---

## 🎯 Objetivo del proyecto

El objetivo principal de BioRuta 360 es transformar el seguimiento tradicional de transportes en un proceso digital, trazable y centralizado.

La plataforma permite conocer el estado de una ruta, registrar eventos durante el recorrido y disponer de información histórica para análisis operativo y mejora continua.

---

## 🚚 Funcionalidades principales

### Aplicación móvil

* Inicio y finalización de recorridos.
* Identificación de rutas asignadas.
* Registro de salida y llegada.
* Seguimiento mediante geolocalización GPS.
* Control de paradas programadas.
* Registro de observaciones durante el recorrido.
* Acceso mediante identificación y código QR.
* Registro de eventos operativos.
* Botón de alerta para situaciones excepcionales.
* Sincronización de información con una base de datos central.

### Panel administrativo

* Visualización de transportes activos.
* Seguimiento de recorridos sobre mapa.
* Posición geográfica de los vehículos.
* Estado de cada recorrido.
* Consulta de rutas y paradas.
* Visualización de información histórica.
* Filtros de búsqueda.
* Generación y consulta de reportes.
* Información meteorológica asociada al recorrido.
* Detección de vehículos detenidos durante períodos prolongados.
* Herramientas de control y análisis operativo.

---

## 🗺️ Gestión de rutas

Cada recorrido puede contener múltiples puntos o paradas previamente definidos.

El sistema permite analizar:

* punto de origen;
* destino;
* paradas intermedias;
* posición actual;
* avance del recorrido;
* cumplimiento de puntos programados;
* tiempos registrados;
* estado general de la ruta.

La información obtenida puede posteriormente utilizarse para análisis de cumplimiento, tiempos de recorrido y eficiencia logística.

---

## 📍 Geolocalización

BioRuta 360 utiliza información GPS para registrar y representar la ubicación de los transportes.

Esto permite construir una visión operativa del recorrido y facilitar el seguimiento desde el panel administrativo.

La arquitectura fue diseñada además para evolucionar hacia mecanismos de **geocercas**, detección automática de llegada a puntos y generación de eventos basados en ubicación.

---

## 📊 Trazabilidad

Uno de los objetivos principales del proyecto es conservar evidencia digital del recorrido.

Entre los datos gestionados se encuentran:

* recorrido;
* transporte;
* fecha;
* horario;
* posición;
* paradas;
* eventos;
* observaciones;
* estados;
* registros históricos.

Esta información permite reconstruir posteriormente el comportamiento de una ruta.

---

## 🧠 Arquitectura general

```text
┌─────────────────────────┐
│      Aplicación móvil   │
│    React Native / Expo  │
└────────────┬────────────┘
             │
             │ API / sincronización
             ▼
┌─────────────────────────┐
│        Supabase         │
│                        │
│  Base de datos         │
│  Autenticación         │
│  Servicios backend     │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│   Panel Administrativo │
│                        │
│  Mapas                 │
│  Rutas                 │
│  Historial             │
│  Reportes              │
│  Alertas               │
└─────────────────────────┘
```

---

## 🛠️ Tecnologías utilizadas

* React Native
* Expo
* Supabase
* Base de datos PostgreSQL
* Geolocalización GPS
* APIs
* Mapas interactivos
* Aplicación móvil Android
* Panel administrativo web
* Generación de reportes
* Arquitectura cliente-servidor

---

## 📱 Aplicación móvil

El proyecto evolucionó desde un primer prototipo web hacia una aplicación móvil desarrollada con **React Native y Expo**.

La aplicación permite trabajar directamente desde el dispositivo del operador durante el recorrido.

Entre sus responsabilidades se encuentran:

```text
Operador
   │
   ▼
Inicio de ruta
   │
   ▼
Seguimiento GPS
   │
   ▼
Registro de paradas
   │
   ▼
Eventos / observaciones
   │
   ▼
Finalización
   │
   ▼
Historial
```

---

## 🖥️ Monitor administrativo

El panel administrativo fue diseñado para centralizar la información generada por los transportes.

Permite disponer de una vista operativa donde cada transporte puede ser analizado individualmente.

Entre los elementos disponibles se encuentran:

* transporte;
* ruta asignada;
* estado;
* posición;
* recorrido;
* paradas;
* historial;
* tiempos;
* alertas;
* información contextual.

---

## 📈 Evolución del proyecto

BioRuta 360 fue desarrollado de manera incremental.

### Primera etapa

Prototipo desarrollado utilizando tecnologías web orientado a validar:

* registro de rutas;
* geolocalización;
* seguimiento;
* panel administrativo;
* generación de información histórica.

### Segunda etapa

Migración del concepto hacia una arquitectura móvil utilizando:

* React Native;
* Expo;
* Supabase;
* aplicación Android;
* backend centralizado;
* panel administrativo independiente.

Esta evolución permitió separar mejor las responsabilidades del sistema y preparar la plataforma para una utilización más escalable.

---

## 📦 Estado actual

El proyecto cuenta con una versión funcional de aplicación móvil y panel administrativo.

Actualmente la plataforma permite trabajar con múltiples rutas y puntos logísticos previamente configurados.

El desarrollo continúa incorporando mejoras relacionadas con:

* geocercas;
* automatización de eventos de llegada y salida;
* mayor detalle histórico;
* análisis de tiempos;
* optimización de recorridos;
* generación avanzada de reportes.

---

## 🔐 Seguridad y privacidad

BioRuta 360 fue concebido para manejar información operativa y datos de geolocalización.

Por este motivo, este repositorio funciona principalmente como **documentación técnica y portfolio del proyecto**.

El código fuente completo, credenciales, información de infraestructura, coordenadas operativas y datos internos no se publican en este repositorio.

---

## 🧩 Principios de desarrollo

Durante el desarrollo se aplicaron conceptos relacionados con:

* separación de responsabilidades;
* arquitectura modular;
* persistencia de datos;
* trazabilidad;
* validación de información;
* manejo de estados;
* diseño orientado a procesos;
* control de errores;
* evolución incremental;
* integración entre sistemas.

---

## 🚀 Roadmap

Entre las mejoras previstas se encuentran:

* geocercas automáticas;
* detección automática de llegada y salida;
* eventos asociados a cada parada;
* análisis avanzado de tiempos de permanencia;
* historial descargable;
* optimización de rutas;
* indicadores de cumplimiento;
* nuevas herramientas de análisis logístico.

---

## 👨‍💻 Rol en el proyecto

Proyecto diseñado y desarrollado integralmente, incluyendo:

* análisis del problema;
* relevamiento del proceso;
* diseño funcional;
* arquitectura;
* modelado de datos;
* desarrollo de aplicación móvil;
* desarrollo del panel administrativo;
* integración con servicios backend;
* geolocalización;
* pruebas;
* evolución funcional del producto.

El proyecto combina conocimientos de **logística, desarrollo de software, automatización de procesos y análisis de información**.

---

## 📌 Sobre el repositorio

Este repositorio contiene documentación pública del proyecto.

Determinados componentes del sistema no se incluyen debido a que corresponden a información operativa, credenciales, configuraciones internas y datos que no deben exponerse públicamente.

---

**BioRuta 360 — Digitalización, trazabilidad y análisis aplicado a operaciones logísticas.**
