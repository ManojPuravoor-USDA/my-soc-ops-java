<!-- l10n-sync: source-file="README.md" -->
<div align="center">

# Soc Ops

### Convierte una sala llena de presentaciones en un juego al que todos pueden sumarse.

**Social Bingo para encuentros presenciales**: conoce gente, descubre las historias detrás de las casillas y sé la primera persona en completar una línea.

[Empezar](#empieza-a-jugar) · [Explora el lab](#créalo-con-el-lab) · [English](README.md) · [Português (BR)](README.pt_BR.md)

</div>

---

## Un mejor rompehielos

Soc Ops es un juego de bingo social ligero, diseñado para los momentos en que las personas están juntas en una misma sala. Cada tablero está lleno de preguntas para conversar, por lo que los jugadores tienen una razón natural para presentarse, compartir experiencias y encontrar puntos en común.

> **El objetivo:** encuentra a alguien que coincida con cada pregunta, marca la casilla y consigue cinco en línea.

| Hecho para encuentros | Listo para jugar | Hecho para aprender |
| :--- | :--- | :--- |
| Da energía a reuniones de equipo, eventos comunitarios y talleres. | Inicia un tablero nuevo de 5 × 5 en segundos; los jugadores no necesitan cuenta ni configuración. | Sigue el lab incluido para explorar el desarrollo moderno asistido por agentes. |

## Cómo funciona una ronda

1. **Inicia un tablero** y revisa las preguntas.
2. **Conoce personas** que coincidan con una casilla y escucha su historia.
3. **Marca tus coincidencias** mientras avanzas.
4. **Completa una línea de cinco** —horizontal, vertical o diagonal— para gritar **¡BINGO!**

## Empieza a jugar

### Lo que necesitas

- [Java 21 JDK](https://adoptium.net/) o posterior
- El Maven Wrapper incluido; no necesitas instalar Maven por separado

### Ejecuta localmente

```bash
cd socops
./mvnw spring-boot:run
```

Luego abre [http://localhost:8080](http://localhost:8080), inicia un juego y pon la conversación en marcha.

### Verifica la compilación

```bash
cd socops
./mvnw test
./mvnw clean package
```

## Creado para una experiencia fluida en la sala

- **Tableros nuevos:** genera una combinación nueva de preguntas al empezar cada juego.
- **Interacción sencilla:** toca una casilla cuando encuentres una coincidencia.
- **Respuesta inmediata:** el juego reconoce líneas ganadoras horizontales, verticales y diagonales.
- **Juego resistente:** el tablero actual se conserva en el navegador mientras juegas.

Soc Ops es una aplicación de [Spring Boot](https://spring.io/projects/spring-boot) con una interfaz [Thymeleaf](https://www.thymeleaf.org/), creada con Java 21.

## Créalo con el lab

Este repositorio también es una guía práctica para crear Soc Ops con GitHub Copilot. Avanza por el lab a tu ritmo:

| Parte | Lo que explorarás |
| :--- | :--- |
| [**00**](workshop/es/00-overview.md) | Descripción general y lista de verificación |
| [**01**](workshop/es/01-setup.md) | Configuración e ingeniería de contexto |
| [**02**](workshop/es/02-design.md) | Desarrollo frontend centrado en el diseño |
| [**03**](workshop/es/03-quiz-master.md) | Un Quiz Master personalizado |
| [**04**](workshop/es/04-multi-agent.md) | Desarrollo multiagente |

**[Abre la Guía completa del Lab →](workshop/es/GUIDE.md)**

---

Creado para tener mejores conversaciones, una casilla a la vez.
