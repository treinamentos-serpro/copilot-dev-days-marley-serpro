<!-- l10n-sync: source-file="README.md" -->
# Soc Ops · Social Bingo

> Un poco de estructura para mejores conversaciones.

Soc Ops es un juego de bingo ligero para encuentros presenciales. Encuentra a alguien que coincida con una pregunta, marca la casilla y mantén la conversación hasta completar cinco en línea.

📚 **[Ver Guía del Lab](workshop/es/GUIDE.md)**

---

## La idea

- **Conoce gente:** las preguntas convierten las presentaciones en invitaciones.
- **Juega en grupo:** el tablero está pensado para una sala compartida, no para una clasificación.
- **Aprende construyendo:** el workshop recorre la app, el diseño y el flujo con agentes.

## Workshop

| Parte | Enfoque |
| --- | --- |
| [00](workshop/es/00-overview.md) | Descripción general y checklist |
| [01](workshop/es/01-setup.md) | Configuración e ingeniería de contexto |
| [02](workshop/es/02-design.md) | Frontend orientado al diseño |
| [03](workshop/es/03-quiz-master.md) | Quiz master personalizado |
| [04](workshop/es/04-multi-agent.md) | Desarrollo multiagente |

Todos los capítulos también están disponibles en la carpeta [`workshop/es/`](workshop/es/) para leer sin conexión.

---

## Ejecútalo localmente

Necesitas [Java 21](https://adoptium.net/) o superior. El Maven Wrapper incluido se encarga del resto.

```bash
cd socops
./mvnw spring-boot:run
```

Abre `http://localhost:8080/` y empieza una partida.

## Comprueba tus cambios

```bash
cd socops
./mvnw clean package
./mvnw test
```

El proyecto se despliega automáticamente en GitHub Pages cuando se hace push a `main`.
