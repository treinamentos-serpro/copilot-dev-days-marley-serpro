<!-- l10n-sync: source-file="README.md" -->
# Soc Ops · Social Bingo

> Um pouco de estrutura para conversas melhores.

O Soc Ops é um jogo de bingo leve para encontros presenciais. Encontre alguém que combine com uma pergunta, marque a casa e mantenha a conversa fluindo até completar cinco em linha.

📚 **[Ver Guia do Lab](workshop/pt_BR/GUIDE.md)**

---

## A ideia

- **Conheça pessoas:** as perguntas transformam apresentações em convites.
- **Jogue em grupo:** o tabuleiro foi feito para uma sala compartilhada, não para um ranking.
- **Aprenda construindo:** o workshop passa pelo app, pelo design e pelo fluxo com agentes.

## Workshop

| Parte | Foco |
| --- | --- |
| [00](workshop/pt_BR/00-overview.md) | Visão geral e checklist |
| [01](workshop/pt_BR/01-setup.md) | Configuração e engenharia de contexto |
| [02](workshop/pt_BR/02-design.md) | Frontend orientado a design |
| [03](workshop/pt_BR/03-quiz-master.md) | Quiz master personalizado |
| [04](workshop/pt_BR/04-multi-agent.md) | Desenvolvimento multiagente |

Todos os capítulos também estão na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## Execute localmente

É necessário ter [Java 21](https://adoptium.net/) ou superior. O Maven Wrapper incluído cuida do restante.

```bash
cd socops
./mvnw spring-boot:run
```

Abra `http://localhost:8080/` e comece uma rodada.

## Verifique suas alterações

```bash
cd socops
./mvnw clean package
./mvnw test
```

O projeto é publicado automaticamente no GitHub Pages quando há push para `main`.
