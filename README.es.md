<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎲 Soc Ops

### Bingo Social para Encuentros Presenciales

**Encuentra a alguien que…** coincida con una pregunta. Márcala. Consigue 5 en línea. Rompe el hielo — con estilo.

[![Demo en Vivo](https://img.shields.io/badge/🎮_Demo_en_Vivo-Jugar_Ahora-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Guía del Lab](https://img.shields.io/badge/📚_Guía_del_Lab-Leer_Ahora-16a34a?style=for-the-badge)](workshop/es/GUIDE.md)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.4.2-6db33f?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-21-f89820?style=for-the-badge&logo=openjdk&logoColor=white)](https://adoptium.net/)

</div>

---

## ✨ ¿Qué es esto?

Soc Ops es una **aplicación web de Bingo Social en vivo** construida con Spring Boot y Thymeleaf. Impulsa sesiones de rompehielos en eventos presenciales — cada jugador recibe un tablero único y aleatorio 5×5 con preguntas de conversación. Encuentra a las personas que coincidan, márcalas y grita **¡BINGO!**

Es también el **proyecto práctico del GitHub Copilot Agent Lab** — un taller donde usas las funciones de agentes de VS Code, agentes personalizados y flujos de trabajo multi-agente para construir y extender una aplicación real.

---

## 🚀 Características

| Característica | Descripción |
|----------------|-------------|
| 🎲 **Tableros aleatorios** | Cada jugador recibe una cuadrícula de preguntas única y mezclada |
| ✅ **Celda central libre** | Bingo clásico con casilla libre en la posición 12 |
| 🏆 **Detección de victoria** | Filas, columnas y diagonales verificadas en tiempo real |
| 🔄 **Nuevo tablero** | Un clic reinicia y mezcla para un nuevo juego |
| 📱 **Diseño responsivo** | El diseño adaptable funciona en teléfonos y tablets |
| 🌐 **Despliegue automático** | Los pushes a `main` se despliegan a GitHub Pages automáticamente |

---

## 📚 Guía del Lab

Recorre el lab en cuatro partes:

| Parte | Título | Qué harás |
|-------|--------|-----------|
| [**00**](workshop/es/00-overview.md) | Descripción General y Lista de Verificación | Oriéntate y verifica los requisitos previos |
| [**01**](workshop/es/01-setup.md) | Configuración e Ingeniería de Contexto | Genera instrucciones del workspace con agentes |
| [**02**](workshop/es/02-design.md) | Desarrollo Frontend Orientado al Diseño | Rediseño completo de la UI usando el Modo de Planificación |
| [**03**](workshop/es/03-quiz-master.md) | Quiz Master Personalizado | Genera un conjunto de preguntas temáticas con un agente personalizado |
| [**04**](workshop/es/04-multi-agent.md) | Desarrollo Multi-Agente | Construye nuevas funcionalidades con flujos TDD multi-agente |

> 📝 Las guías del lab también están disponibles en la carpeta [`workshop/es/`](workshop/es/) para lectura sin conexión.

---

## 🛠️ Primeros Pasos

### Requisitos Previos

- [Java 21 JDK](https://adoptium.net/) o superior
- [Apache Maven 3.9+](https://maven.apache.org/) (o usa el Maven Wrapper incluido)

### Ejecutar localmente

```bash
cd socops
./mvnw spring-boot:run
```

Luego abre **http://localhost:8080** en tu navegador.

### Compilar

```bash
cd socops
./mvnw clean package
```

### Pruebas

```bash
cd socops
./mvnw test
```

---

## 🏗️ Estructura del Proyecto

```
socops/
├── src/main/java/com/socops/
│   ├── web/          # Controladores y endpoints REST
│   ├── service/      # BoardAssembler — lógica del juego y detección de victoria
│   ├── model/        # Records inmutables (BingoCell, etc.)
│   └── data/         # Catálogo de IcebreakerPrompts
└── src/main/resources/
    ├── templates/    # Plantillas HTML Thymeleaf
    └── static/css/   # Clases CSS utilitarias personalizadas
```

---

<div align="center">

Se despliega automáticamente a GitHub Pages con cada push a `main`.

Hecho con ☕ Java, 🌿 Spring Boot y muchos rompehielos.

</div>
