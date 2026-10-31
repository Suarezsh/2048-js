# 🔢 2048 JS

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Sin dependencias](https://img.shields.io/badge/Sin%20dependencias-3fb950?style=for-the-badge)
![License](https://img.shields.io/badge/Licencia-MIT-yellow?style=for-the-badge)

**El clásico juego de combinar números con animaciones fluidas.**  
Fusiona losetas del mismo valor hasta llegar al 2048 — y más allá.

**[▶ Ver demo en vivo](https://suarezsh.github.io/2048-js)**

</div>

---

## 🎯 ¿Qué es esto?

Una implementación completa del juego 2048 construida desde cero con HTML, CSS y JavaScript puro.  
Incluye animaciones suaves de deslizamiento y fusión, pantalla de pausa, puntaje máximo guardado localmente y soporte táctil.

Sin npm, sin frameworks, sin servidor — solo abre `index.html`.

---

## ✨ Características

- 🎯 **Tablero 4×4** clásico con lógica de deslizamiento y fusión correcta
- ✨ **Animaciones CSS** — losetas se deslizan y "rebotan" al fusionarse
- ⏸ **Pausa / Reanudar** — overlay con `P` o el botón
- 🏆 **Mejor puntaje** — guardado en `localStorage` entre sesiones
- 🎉 **Pantalla de victoria** — al alcanzar 2048, opción de seguir jugando
- 💀 **Pantalla de Game Over** — detecta cuando no hay movimientos posibles
- 🎨 **Colores por valor** — cada potencia de 2 tiene su propio color
- 📱 **Swipe táctil** — funciona en móvil deslizando en cualquier dirección
- ↺ **Reiniciar** — con el botón o la tecla `R`

---

## 🕹️ Controles

| Acción | Teclado | Touch |
|---|---|---|
| Mover tiles | `↑ ↓ ← →` o `WASD` | Deslizar en cualquier dirección |
| Pausar / Reanudar | `P` o botón | Botón |
| Nueva partida | `R` o botón | Botón |

---

## 🔢 Cómo funciona

Al presionar una dirección, **todos los tiles se deslizan** hacia ese lado:

```
Estado inicial     →  ArrowLeft  →  Resultado
 .  .  .  2            2  .  .  .
 .  2  .  2     →      4  .  .  .
 .  .  4  .            4  .  .  .
 2  .  2  .            4  .  .  .
```

**Reglas:**
1. Los tiles se deslizan lo más lejos posible en la dirección elegida.
2. Dos tiles del **mismo valor** que chocan se fusionan en uno de **valor doble**.
3. Cada tile fusionado solo puede volver a fusionarse en el siguiente turno.
4. Después de cada movimiento válido, aparece un nuevo tile (2 o 4).
5. El juego termina cuando no hay celdas vacías ni fusiones posibles.

---

## 🎨 Paleta de losetas

| Valor | Color |
|---|---|
| 2 | Azul oscuro |
| 4 | Violeta oscuro |
| 8 – 64 | Naranja → Rojo |
| 128 – 1024 | Dorado |
| **2048** | **Oro brillante** ✨ |
| 4096+ | Violeta / Rosa |

---

## 🖥️ Vista previa

```
┌────────────────────────────────────┐
│  2048          PUNTOS  MEJOR       │
│                  512    2048       │
├────────────────────────────────────┤
│  [↺ Nueva]    [⏸ Pausar]           │
├────────────────────────────────────┤
│   ·    ·    ·    ·                 │
│   ·    4    ·    ·                 │
│   ·    ·   16    8                 │
│   2    4    ·   32                 │
├────────────────────────────────────┤
│  ↑↓←→ / WASD  ·  P pausar  ·  R nueva │
└────────────────────────────────────┘
```

---

## 🚀 Uso

```bash
git clone https://github.com/Suarezsh/2048-js.git
cd 2048-js

# Abrir directo en el navegador
start index.html        # Windows
open  index.html        # macOS / Linux
```

---

## 📁 Estructura

```
2048-js/
└── index.html    ← Todo en un solo archivo (HTML + CSS + JS)
```

---

## 🛠️ Tecnologías

- **HTML5** — estructura del tablero con CSS Grid
- **CSS3** — transiciones de posición (`top`/`left`) para animaciones de movimiento, `@keyframes` para pop de aparición y fusión
- **JavaScript ES6+** — lógica del juego, motor de deslizamiento/fusión, gestión de estado
- **Google Fonts** — Space Grotesk
- **localStorage** — persistencia del puntaje máximo entre sesiones
- **Sin frameworks · Sin librerías · Sin npm**

---

## 📄 Licencia

MIT © [Suarezsh](https://github.com/Suarezsh)
