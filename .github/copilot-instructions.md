# Soc Ops Workspace Instructions

## Project overview

Soc Ops is a Spring Boot 3.4 application for playing social bingo at in-person mixers. The application serves a Thymeleaf game page and exposes a small REST endpoint that generates fresh bingo boards.

The Java project lives in `/socops`. The repository root also contains workshop material and the static documentation site deployed to GitHub Pages.

## Development environment

- Use Java 21. The project is configured with `<java.version>21</java.version>`.
- Use the Maven Wrapper from `/socops`; do not require a system Maven installation.
- The development server listens on port `8080`.
- The dev container is already configured with Java 21, Maven dependency resolution, and port forwarding for `8080`.

## Common commands

Run commands from `/socops`:

```bash
./mvnw spring-boot:run
./mvnw clean package
./mvnw test
```

If multiple JDKs are installed, set `JAVA_HOME` to a Java 21 installation before invoking Maven.

## Source layout

- `src/main/java/com/socops/model`: immutable domain records and enums.
- `src/main/java/com/socops/data`: application prompt data.
- `src/main/java/com/socops/service`: pure game logic, especially board creation, tile selection, and winning-streak detection.
- `src/main/java/com/socops/web`: Spring MVC controllers and REST endpoints.
- `src/main/resources/templates`: Thymeleaf HTML templates.
- `src/main/resources/static`: CSS, images, and other browser assets.
- `src/test/java`: JUnit 5 tests for game logic.

## Implementation conventions

- Keep game rules in `BoardAssembler` or closely related service classes rather than in controllers or templates.
- Prefer immutable Java records and return defensive copies when transforming boards.
- Keep controllers thin: map HTTP requests to service operations and return view names or response data.
- Preserve the existing public endpoint contracts, including `/` and `/api/bingo/fresh-board`.
- Add or update focused JUnit tests when changing board generation, tile flipping, or victory detection.
- Use the existing Spring Boot dependencies and Maven configuration; avoid adding libraries unless the change genuinely requires one.

## Frontend conventions

- The main UI is `src/main/resources/templates/game.html`; its client-side game engine mirrors the Java board logic.
- Keep JavaScript behavior and `BoardAssembler` behavior synchronized when changing game rules.
- Compose the custom utility classes defined in `src/main/resources/static/css/app.css` instead of introducing an external CSS framework.
- Follow `.github/instructions/css-utilities.instructions.md` for utility usage and `.github/instructions/frontend-design.instructions.md` for visual design work.
- Preserve accessible button labels, `aria-pressed` state, and keyboard-friendly interactions when changing the board UI.

## Validation

Before submitting changes:

1. Run `./mvnw test`.
2. Run `./mvnw clean package`.
3. For UI changes, run `./mvnw spring-boot:run` and verify the lobby and game flow at `http://localhost:8080/`.

Do not commit generated Maven output such as `target/`.
