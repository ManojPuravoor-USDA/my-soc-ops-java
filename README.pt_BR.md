<!-- l10n-sync: source-file="README.md" -->
<div align="center">

# Soc Ops

### Transforme uma sala cheia de apresentações em um jogo que todos podem curtir.

**Social Bingo para encontros presenciais** — conheça pessoas, descubra as histórias por trás das casas e seja a primeira pessoa a completar uma linha.

[Comece](#comece-a-jogar) · [Explore o lab](#crie-com-o-lab) · [English](README.md) · [Español](README.es.md)

</div>

---

## Um quebra-gelo melhor

Soc Ops é um jogo leve de bingo social feito para os momentos em que as pessoas estão juntas na mesma sala. Cada cartela é preenchida com perguntas para conversa, dando aos jogadores um motivo natural para se apresentar, compartilhar experiências e encontrar pontos em comum.

> **O objetivo:** encontre alguém que corresponda a cada pergunta, marque a casa e faça cinco em linha.

| Feito para encontros | Pronto para jogar | Feito para aprender |
| :--- | :--- | :--- |
| Dê energia a reuniões de equipe, eventos comunitários e workshops. | Comece uma nova cartela de 5 × 5 em segundos; os jogadores não precisam de conta ou configuração. | Siga o lab que acompanha o projeto para explorar o desenvolvimento moderno assistido por agentes. |

## Como funciona uma rodada

1. **Comece uma cartela** e examine as perguntas.
2. **Conheça pessoas** que correspondam a uma casa e ouça a história delas.
3. **Marque suas correspondências** enquanto joga.
4. **Complete uma linha de cinco** —na horizontal, vertical ou diagonal— para gritar **BINGO!**

## Comece a jogar

### O que você precisa

- [Java 21 JDK](https://adoptium.net/) ou posterior
- O Maven Wrapper incluído; não é necessário instalar o Maven separadamente

### Execute localmente

```bash
cd socops
./mvnw spring-boot:run
```

Depois, abra [http://localhost:8080](http://localhost:8080), comece um jogo e inicie a conversa.

### Verifique o build

```bash
cd socops
./mvnw test
./mvnw clean package
```

## Criado para uma experiência tranquila na sala

- **Cartelas novas:** gere uma combinação de perguntas a cada novo jogo.
- **Interação simples:** toque em uma casa quando encontrar uma correspondência.
- **Resposta imediata:** o jogo reconhece linhas vencedoras horizontais, verticais e diagonais.
- **Jogo resiliente:** a cartela atual é preservada no navegador enquanto você joga.

Soc Ops é uma aplicação [Spring Boot](https://spring.io/projects/spring-boot) com uma interface [Thymeleaf](https://www.thymeleaf.org/), criada com Java 21.

## Crie com o lab

Este repositório também é um guia prático para criar Soc Ops com o GitHub Copilot. Siga o lab no seu ritmo:

| Parte | O que você explorará |
| :--- | :--- |
| [**00**](workshop/pt_BR/00-overview.md) | Visão geral e lista de verificação |
| [**01**](workshop/pt_BR/01-setup.md) | Configuração e engenharia de contexto |
| [**02**](workshop/pt_BR/02-design.md) | Desenvolvimento frontend orientado ao design |
| [**03**](workshop/pt_BR/03-quiz-master.md) | Um Quiz Master personalizado |
| [**04**](workshop/pt_BR/04-multi-agent.md) | Desenvolvimento multiagente |

**[Abra o Guia completo do Lab →](workshop/pt_BR/GUIDE.md)**

---

Criado para conversas melhores, uma casa de cada vez.
