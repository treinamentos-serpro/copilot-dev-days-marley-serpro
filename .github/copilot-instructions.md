# Soc Ops Agent Instructions

## Mandatory Development Checklist

- [ ] Lint or equivalent static validation
- [ ] Build: `cd socops && ./mvnw clean package`
- [ ] Test: `cd socops && ./mvnw test`

## Project Snapshot

- Spring Boot social bingo app for in-person mixers.
- Code lives under `socops/` and targets Java 21 / Spring Boot 3.4.2.
- Start with [README.md](../README.md) and [workshop/GUIDE.md](../workshop/GUIDE.md); link instead of duplicating content.

## Key Commands

```bash
cd socops && ./mvnw test
cd socops && ./mvnw clean package
cd socops && ./mvnw spring-boot:run
```

The app listens on port `8080` by default.

## Code Map

- `src/main/java/com/socops/web/`: controller and REST endpoints
- `src/main/java/com/socops/service/BoardAssembler.java`: board assembly, toggling, and win detection
- `src/main/java/com/socops/model/`: immutable records and enums
- `src/main/java/com/socops/data/IcebreakerPrompts.java`: prompt catalog
- `src/main/resources/templates/game.html`: Thymeleaf UI
- `src/main/resources/static/css/app.css`: project CSS utilities
- `src/test/java/`: JUnit tests, with `BoardAssemblerTests` as the domain example

## Domain Rules

- Board is 5x5 with 25 cells; index 12 is always the free cell.
- `BoardAssembler` must not mutate inputs and should return new lists.
- Victory detection checks rows, columns, and both diagonals.
- Keep prompt data immutable and preserve existing `BingoCell` record/factory patterns.

## Change Guidance

- Keep controller logic in the web layer and game rules in `BoardAssembler`.
- Prefer narrow JUnit tests for board assembly, toggle behavior, and win detection.
- Preserve package names, record-based models, and static helper conventions unless the task explicitly requires a design change.
- For template or CSS work, read [frontend-design.instructions.md](instructions/frontend-design.instructions.md) and [css-utilities.instructions.md](instructions/css-utilities.instructions.md) first.
- Keep changes scoped and avoid generated/build output edits.

## Agent Workflow

1. Inspect the nearest owning controller, service, model, template, or test.
2. Make the smallest coherent change.
3. Complete the checklist above before finishing.
4. For UI work, verify the affected route at `http://localhost:8080/` when browser tooling is available.