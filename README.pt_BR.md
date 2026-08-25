<!-- l10n-sync: source-file="README.md" -->

<div align="center">

# 🎲 Soc Ops

### Bingo Social para Encontros Presenciais

**Encontre alguém que…** corresponda a uma pergunta. Marque. Faça 5 em linha. Quebre o gelo — com estilo.

[![Demo ao Vivo](https://img.shields.io/badge/🎮_Demo_ao_Vivo-Jogar_Agora-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Guia do Lab](https://img.shields.io/badge/📚_Guia_do_Lab-Ler_Agora-16a34a?style=for-the-badge)](workshop/pt_BR/GUIDE.md)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.4.2-6db33f?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-21-f89820?style=for-the-badge&logo=openjdk&logoColor=white)](https://adoptium.net/)

</div>

---

## ✨ O que é isso?

Soc Ops é um **aplicativo web de Social Bingo ao vivo** construído com Spring Boot e Thymeleaf. Ele alimenta sessões de quebra-gelo em eventos presenciais — cada jogador recebe um tabuleiro único e aleatório 5×5 com perguntas de conversa. Encontre as pessoas que correspondem, marque e grite **BINGO!**

É também o **projeto prático do GitHub Copilot Agent Lab** — um workshop onde você usa recursos de agentes do VS Code, agentes personalizados e fluxos de trabalho multi-agente para construir e estender uma aplicação real.

---

## 🚀 Funcionalidades

| Funcionalidade | Descrição |
|----------------|-----------|
| 🎲 **Tabuleiros aleatórios** | Cada jogador recebe uma grade de perguntas única e embaralhada |
| ✅ **Célula central livre** | Bingo clássico com casa livre na posição 12 |
| 🏆 **Detecção de vitória** | Linhas, colunas e diagonais verificadas em tempo real |
| 🔄 **Novo tabuleiro** | Um clique redefine e embaralha para um novo jogo |
| 📱 **Responsivo** | Layout adaptável funciona em celulares e tablets |
| 🌐 **Deploy automático** | Pushes para `main` fazem deploy no GitHub Pages automaticamente |

---

## 📚 Guia do Lab

Percorra o lab em quatro partes:

| Parte | Título | O que você vai fazer |
|-------|--------|----------------------|
| [**00**](workshop/pt_BR/00-overview.md) | Visão Geral & Lista Rápida | Oriente-se e verifique os pré-requisitos |
| [**01**](workshop/pt_BR/01-setup.md) | Configuração & Engenharia de Contexto | Gere instruções de workspace com agentes |
| [**02**](workshop/pt_BR/02-design.md) | Frontend Design-First | Redesign completo da UI usando o Modo de Planejamento |
| [**03**](workshop/pt_BR/03-quiz-master.md) | Quiz Master Personalizado | Gere um conjunto de perguntas temáticas com um agente personalizado |
| [**04**](workshop/pt_BR/04-multi-agent.md) | Desenvolvimento Multi-Agente | Construa novas funcionalidades com fluxos TDD multi-agente |

> 📝 Os guias do lab também estão disponíveis na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## 🛠️ Começando

### Pré-requisitos

- [Java 21 JDK](https://adoptium.net/) ou superior
- [Apache Maven 3.9+](https://maven.apache.org/) (ou use o Maven Wrapper incluído)

### Executar localmente

```bash
cd socops
./mvnw spring-boot:run
```

Depois abra **http://localhost:8080** no seu navegador.

### Build

```bash
cd socops
./mvnw clean package
```

### Testes

```bash
cd socops
./mvnw test
```

---

## 🏗️ Estrutura do Projeto

```
socops/
├── src/main/java/com/socops/
│   ├── web/          # Controllers e endpoints REST
│   ├── service/      # BoardAssembler — lógica do jogo e detecção de vitória
│   ├── model/        # Records imutáveis (BingoCell, etc.)
│   └── data/         # Catálogo de IcebreakerPrompts
└── src/main/resources/
    ├── templates/    # Templates HTML Thymeleaf
    └── static/css/   # Classes CSS utilitárias personalizadas
```

---

<div align="center">

O deploy é feito automaticamente no GitHub Pages ao fazer push para `main`.

Feito com ☕ Java, 🌿 Spring Boot e muitos quebra-gelos.

</div>
