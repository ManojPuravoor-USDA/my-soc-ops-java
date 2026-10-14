<div align="center">

# Soc Ops

### Turn a room full of introductions into a game everyone can join.

**Social Bingo for in-person mixers** — meet people, uncover the stories behind the squares, and be the first to make a line.

[Get started](#get-playing) · [Explore the lab](#build-it-with-the-lab) · [Español](README.es.md) · [Português (BR)](README.pt_BR.md)

</div>

---

## A better icebreaker

Soc Ops is a lightweight social-bingo game designed for the moments when people are together in the same room. Every board is filled with conversation prompts, so players have a natural reason to introduce themselves, compare experiences, and find common ground.

> **The goal:** find someone who matches each prompt, mark the square, and get five in a row.

| Made for mixers | Ready to play | Built to learn |
| :--- | :--- | :--- |
| Bring energy to team offsites, community events, and workshops. | Start a fresh 5 × 5 board in seconds—no account or setup for players. | Follow the accompanying lab to explore modern, agent-assisted development. |

## How a round works

1. **Start a board** and scan the prompts.
2. **Meet people** who match a square and learn their story.
3. **Mark your matches** as you go.
4. **Make a line of five**—across, down, or diagonally—to call **BINGO!**

## Get playing

### What you need

- [Java 21 JDK](https://adoptium.net/) or later
- The included Maven Wrapper—no separate Maven installation required

### Run locally

```bash
cd socops
./mvnw spring-boot:run
```

Then open [http://localhost:8080](http://localhost:8080), start a game, and get the conversation moving.

### Verify your build

```bash
cd socops
./mvnw test
./mvnw clean package
```

## Built for a smooth room experience

- **Fresh boards:** generate a new mix of prompts whenever a game begins.
- **Simple interaction:** tap a tile when you find a match.
- **Instant feedback:** the game recognizes winning rows, columns, and diagonals.
- **Resilient play:** your current board is preserved in the browser while you play.

Soc Ops is a [Spring Boot](https://spring.io/projects/spring-boot) application with a [Thymeleaf](https://www.thymeleaf.org/) interface, built on Java 21.

## Build it with the lab

This repository is also a hands-on guide to building Soc Ops with GitHub Copilot. Work through the lab at your own pace:

| Part | What you will explore |
| :--- | :--- |
| [**00**](workshop/00-overview.md) | Project overview and checklist |
| [**01**](workshop/01-setup.md) | Setup and context engineering |
| [**02**](workshop/02-design.md) | Design-first frontend development |
| [**03**](workshop/03-quiz-master.md) | A custom Quiz Master |
| [**04**](workshop/04-multi-agent.md) | Multi-agent development |

**[Open the complete Lab Guide →](workshop/GUIDE.md)**

---

Built for better conversations, one square at a time.
