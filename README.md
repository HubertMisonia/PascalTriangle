# PascalTriangle \LaTeX{} Package

**PascalTriangle** is a \LaTeX{} package that provides a simple and highly customizable way to generate and visualize Pascal's triangle using TikZ. It supports both rectangular and hexagonal layouts, modular coloring patterns, and factorial display.

> 📦 Repository: [https://github.com/HubertMisonia/PascalTriangle](https://github.com/HubertMisonia/PascalTriangle)

---

## 🚀 Installation

You can install `PascalTriangle.sty` by downloading it directly into your project folder (no move needed):

### MacOS / Linux (using `curl` or `wget`)

```sh
curl -O https://raw.githubusercontent.com/HubertMisonia/PascalTriangle/main/PascalTriangle.sty
```

or

```sh
wget https://raw.githubusercontent.com/HubertMisonia/PascalTriangle/main/PascalTriangle.sty
```

### Windows (PowerShell)

```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/HubertMisonia/PascalTriangle/main/PascalTriangle.sty" -OutFile "PascalTriangle.sty"
```

Then, in your `.tex` file:

```latex
\usepackage{PascalTriangle}
```

---

## ✨ Features

* Draw Pascal’s triangle in rectangular or hexagonal form
* Highlight divisibility patterns using modular arithmetic
* Show factorial formulas for each binomial coefficient
* Fully configurable style: radius, margin, font size, etc.

---

## 📐 Options

All options are passed to the `\PascalTriangle` command as key-value pairs:

| Option        | Type    | Description                                                                |
| ------------- | ------- | -------------------------------------------------------------------------- |
| `rows`        | integer | Number of rows to render (default: 6)                                      |
| `radius`      | float   | Size of each hexagon or rectangle (default: 1.0)                           |
| `fontSize`    | float   | Text scaling factor (default: 0.7)                                         |
| `margin`      | float   | Inner spacing inside shapes (default: 0)                                   |
| `nodeType`    | string  | `hex` or `rect` (default: `hex`)                                           |
| `pattern`     | string  | `none` or `divisibility` (default: `none`)                                 |
| `divisor`     | integer | Used when `pattern=divisibility` to color entries divisible by this number |
| `showFormula` | boolean | `true` or `false` — whether to show binomial formula below each value      |

> ⚠️ **Note:** To avoid parsing errors, all options must be written on the **same line**. Do not use line breaks or trailing commas.

---

## 📊 Usage Examples

### Basic Hexagonal Triangle

```latex
\PascalTriangle
```

### Rectangular Triangle

```latex
\PascalTriangle[rows=6, nodeType=rect, radius=0.8, margin=0.08, fontSize=0.7]
```

### Divisibility by 3 (Hexagonal with Formula)

```latex
\PascalTriangle[pattern=divisibility, divisor=3, radius=0.9, margin=0.04, fontSize=0.7, showFormula=true]
```

### Multiple Divisibility Visualizations

```latex
\PascalTriangle[rows=13, pattern=divisibility, divisor=5, radius=0.5, margin=0.03, fontSize=0.7]
```

---

## 📄 License

This project is currently **not under any license**. Please contact [Hubert Misonia](https://github.com/HubertMisonia) before using it for commercial or redistribution purposes.

---

## 👨🏾‍💻 Author

**Hubert Misonia** — [@HubertMisonia on GitHub](https://github.com/HubertMisonia)
