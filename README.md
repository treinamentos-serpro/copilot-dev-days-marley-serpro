🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

<div align="center">

# 🎲 Soc Ops

### Social Bingo for In-Person Mixers

**Find someone who…** matches a prompt. Mark it off. Get 5 in a row. Break the ice — beautifully.

[![Live Demo](https://img.shields.io/badge/🎮_Live_Demo-Play_Now-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Lab Guide](https://img.shields.io/badge/📚_Lab_Guide-Read_Now-16a34a?style=for-the-badge)](workshop/GUIDE.md)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.4.2-6db33f?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-21-f89820?style=for-the-badge&logo=openjdk&logoColor=white)](https://adoptium.net/)

</div>

---

## ✨ What Is This?

Soc Ops is a **live Social Bingo web app** built with Spring Boot and Thymeleaf. It powers icebreaker sessions at in-person events — each player gets a unique randomized 5×5 board of conversation prompts. Find the people who match, mark them off, and shout **BINGO!**

It's also the **hands-on project for the GitHub Copilot Agent Lab** — a workshop where you use VS Code agent features, custom agents, and multi-agent workflows to build and extend a real application.

---

## 🚀 Features

| Feature | Description |
|---------|-------------|
| 🎲 **Random boards** | Every player gets a unique shuffled prompt grid |
| ✅ **Free center cell** | Classic bingo with a free square at position 12 |
| 🏆 **Win detection** | Rows, columns, and both diagonals checked in real-time |
| 🔄 **Fresh board** | One click resets and reshuffles for a new game |
| 📱 **Mobile-friendly** | Responsive layout works on phones and tablets |
| 🌐 **Auto-deploy** | Pushes to `main` deploy to GitHub Pages automatically |

---

## 📚 Lab Guide

Work through the lab in four parts:

| Part | Title | What You'll Do |
|------|-------|----------------|
| [**00**](workshop/00-overview.md) | Overview & Checklist | Orient yourself and check prerequisites |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering | Generate workspace instructions with agents |
| [**02**](workshop/02-design.md) | Design-First Frontend | Full UI redesign using Plan Mode |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | Generate a themed prompt set with a custom agent |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development | Build new features with TDD multi-agent workflows |

> 📝 All lab guides are available in the [`workshop/`](workshop/) folder for offline reading.

---

## 🛠️ Getting Started

### Prerequisites

- [Java 21 JDK](https://adoptium.net/) or higher
- [Apache Maven 3.9+](https://maven.apache.org/) (or use the included Maven Wrapper)

### Run locally

```bash
cd socops
./mvnw spring-boot:run
```

Then open **http://localhost:8080** in your browser.

### Build

```bash
cd socops
./mvnw clean package
```

### Test

```bash
cd socops
./mvnw test
```

---

## 🏗️ Project Structure

```
socops/
├── src/main/java/com/socops/
│   ├── web/          # Controllers & REST endpoints
│   ├── service/      # BoardAssembler — game logic & win detection
│   ├── model/        # Immutable records (BingoCell, etc.)
│   └── data/         # IcebreakerPrompts catalog
└── src/main/resources/
    ├── templates/    # Thymeleaf HTML templates
    └── static/css/   # Custom CSS utility classes
```

---

<div align="center">

Deploys automatically to GitHub Pages on push to `main`.

Made with ☕ Java, 🌿 Spring Boot, and a lot of icebreakers.

</div>
