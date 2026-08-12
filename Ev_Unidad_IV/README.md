# Prueba Práctica — Unidad IV — Ingeniería de Requisitos (ISR-401)

**Estudiante:** Sánchez Centeno Roselyn Andreina
**Curso:** 4to Software "A"
**Caso:** Sistema de Gestión de Pedidos

## Estructura del repositorio
├── main.tex # Archivo principal LaTeX (actividades P1–P8; alcance de esta entrega)
├── main.pdf # PDF compilado del desarrollo (resultado final)
├── caratula.tex # Carátula para subir al LMS (SGA)
├── caratula.pdf # Carátula compilada, con URL del repo y capturas del cuestionario
├── README.md # Este archivo
├── figuras/ # Imágenes de los diagramas UML dibujados a mano (P2)
│ ├── p1_diagrama_clases.png # (referencia; el diagrama final de P1 se generó en TikZ dentro de main.tex)
│ ├── p2_diagrama_actividades.png
│ ├── p2b_diagrama_actividades_continuacion.png
│ └── p3_diagrama_estados.png # (referencia; el diagrama final de P3 se generó en TikZ dentro de main.tex)
└── capturas/ # Capturas del cuestionario del SGA (usadas en caratula.tex)
├── resumen_cuestionario.png
└── evaluacion_intento.png
> Los diagramas de clases (P1) y de máquina de estados (P3), así como el fragmento corregido
> de P4, se generaron directamente en TikZ dentro de `main.tex` (opción explícitamente permitida
> por el enunciado), por lo que no dependen de las imágenes PNG para compilar. El diagrama de
> actividades (P2) se mantiene como imagen escaneada a mano.

> Este proyecto no usa archivo `referencias.bib` porque no se citan fuentes bibliográficas
> dentro del desarrollo (P1–P8); las referencias normativas se mencionan directamente en el
> texto del enunciado.

## Requisitos previos

- Distribución LaTeX con `pdflatex` (por ejemplo, TeX Live 2023 o superior, o MiKTeX).
- Paquetes utilizados (todos incluidos en una instalación `texlive-full`; con `texlive-latex-extra`
  más `texlive-pictures` también alcanza):
  `babel` (spanish, con opción `provide=*` por compatibilidad con TeX Live 2023+), `inputenc`,
  `fontenc`, `geometry`, `graphicx`, `booktabs`, `longtable`, `array`, `xcolor`, `enumitem`,
  `hyperref`, `fancyhdr`, `titlesec`, `amssymb`, `placeins`, `float`, `tikz` (con las librerías
  `shapes.multipart`, `shapes.geometric`, `positioning`, `arrows.meta`, `calc`, `fit`, `backgrounds`).

## Instrucciones de compilación

1. Clonar el repositorio:
```bash
   git clone https://github.com/Roselyn15/Ev_Practica_Unidad_IV_RS.git
   cd Ev_Practica_Unidad_IV_RS
```

2. Compilar el documento principal (desarrollo P1–P8) con `pdflatex` (se ejecuta dos veces
   para que se resuelvan correctamente las referencias internas):
```bash
   pdflatex main.tex
   pdflatex main.tex
```
   El PDF resultante se genera como `main.pdf` en la raíz del repositorio.

3. Compilar la carátula para el LMS:
```bash
   pdflatex caratula.tex
   pdflatex caratula.tex
```
   El PDF resultante se genera como `caratula.pdf`.

### Alternativa (recomendada): `latexmk`

```bash
latexmk -pdf main.tex
latexmk -pdf caratula.tex
```

`latexmk` detecta automáticamente cuántas pasadas de `pdflatex` son necesarias.

## Archivos principales

- **`main.tex`** — archivo principal del desarrollo de las actividades prácticas P1 a P8.
  Incluye directamente las imágenes ubicadas en `figuras/` mediante `\includegraphics`, por lo
  que la carpeta `figuras/` debe conservarse en la misma ruta relativa al momento de compilar.
- **`caratula.tex`** — carátula independiente y breve, con los datos de identificación, la URL
  de este repositorio en una sola línea, y las capturas del resumen y de la evaluación del
  cuestionario rendido en el SGA (tomadas de `capturas/`). Este es el PDF que se sube al LMS.

## Nota sobre la carátula subida al SGA

El PDF de carátula que se sube al LMS (SGA) es un documento separado y breve que contiene los
datos de identificación del estudiante, la URL de este repositorio en una sola línea, y las
capturas del resumen y de la evaluación del cuestionario rendido en el SGA. El desarrollo
completo de las actividades prácticas (P1–P8) se encuentra en este repositorio, en
`main.tex` / `main.pdf`.
