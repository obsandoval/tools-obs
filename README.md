# ToolsObs

Panel de herramientas personales con diseño dark y glass morphism.

## Herramientas

### 01 — Menú Semanal
Planificador de comidas para la semana. Genera menús aleatorios a partir de un catálogo de platillos (`platillos.json`) y permite editar cada comida manualmente. Exporta a PDF o copia el menú como texto plano.

### 02 — Calculadora de Cervezas
Compara dos ofertas de cerveza y determina cuál tiene mejor precio por litro. Muestra una tabla comparativa con volumen total, precio por unidad, costo por 100 ml y precio por litro. Incluye gráfico de barras e historial de comparaciones.

### 03 — Radio YSUCA 91.7 FM
Reproductor de radio en vivo con diseño vintage. Conecta al stream de YSUCA (Citrus3). Incluye visualizador de barras, indicador de sintonía (magic eye), perilla de encendido y control de volumen.

## Stack

- HTML5 + CSS3 vanilla + JavaScript vanilla
- [Chart.js](https://www.chartjs.org/) — gráfico de barras en la calculadora
- [jsPDF](https://github.com/parallax/jsPDF) — exportación PDF del menú
- [Google Fonts](https://fonts.google.com/) — Inter, Special Elite, VT323
- [Material Icons Round](https://fonts.google.com/icons) — iconografía

## Estructura

```
tools-obs-main/
├── index.html           # Panel principal (bento grid)
├── menu_semanal.html    # Planificador de comidas
├── beer-calc.html       # Calculadora de cervezas
├── radio.html           # Reproductor YSUCA 91.7 FM
├── platillos.json       # Catálogo de platillos
└── css/
    ├── index.css
    ├── menu_semanal.css
    ├── beer-calc.css
    └── radio.css
```

## Uso local

Requiere un servidor web local para que `menu_semanal.html` pueda cargar `platillos.json` (los navegadores bloquean `fetch()` con el protocolo `file://`).

```bash
# Python
python3 -m http.server 8080

# Node (npx)
npx serve .
```

Luego abre `http://localhost:8080` en el navegador.

---

Hecho por Ob Sandoval
