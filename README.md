🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# Soc Ops · Social Bingo

> A little structure for better conversations.

Soc Ops is a lightweight bingo game for in-person mixers. Find someone who matches a prompt, mark the square, and keep the conversation moving until you make five in a row.

**[Start with the lab guide →](workshop/GUIDE.md)**

---

## The idea

- **Meet people:** prompts turn introductions into invitations.
- **Play together:** the board is designed for a shared room, not a leaderboard.
- **Learn by building:** the workshop walks through the app, design, and agent workflow.

## Workshop

| Part | Focus |
| --- | --- |
| [00](workshop/00-overview.md) | Overview and checklist |
| [01](workshop/01-setup.md) | Setup and context engineering |
| [02](workshop/02-design.md) | Design-first frontend |
| [03](workshop/03-quiz-master.md) | Custom quiz master |
| [04](workshop/04-multi-agent.md) | Multi-agent development |

Every chapter is also available in the [`workshop/`](workshop/) folder for offline reading.

---

## Run it locally

Requires [Java 21](https://adoptium.net/) or higher. The included Maven Wrapper handles the rest.

```bash
cd socops
./mvnw spring-boot:run
```

Open `http://localhost:8080/` and start a round.

## Check your changes

```bash
cd socops
./mvnw clean package
./mvnw test
```

The project deploys automatically to GitHub Pages when changes are pushed to `main`.
