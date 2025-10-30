# 📘 Sistema de Monitoreo de Contaminación en Cuerpos de Agua Basado en una Red Inalámbrica de Sensores y Visión Artificial

![Estado](https://img.shields.io/badge/Estado-En%20Proceso-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

### 🎓 Tesis de Ingeniería Telemática  
**Instituto Politécnico Nacional**  
**Unidad Profesional Interdisciplinaria en Ingeniería y Tecnologías Avanzadas (UPIITA)**  

---

## 🧠 Descripción del Proyecto

Este repositorio contiene el código fuente en **LaTeX** correspondiente a la tesis titulada:  
> *Sistema de monitoreo de contaminación en cuerpos de agua basado en una red inalámbrica de sensores y visión artificial.*

El documento describe el desarrollo de un sistema automatizado para monitorear parámetros de calidad del agua en cuerpos lóticos mediante una **red inalámbrica de sensores distribuida (WSN)**, capaz de medir **pH, oxigenación, temperatura, turbidez y conductividad**.  
Además, el sistema integra **visión artificial** para la detección de **residuos sólidos flotantes** en la superficie.  
Los datos recolectados se envían a una **central de procesamiento**, donde se analizan y visualizan mediante una **interfaz web**, proporcionando información útil para la **gestión ambiental y respuesta ante emergencias**.

---

## 👥 Autores

- **Oscar Alfredo Dompablo Celaya**  
- **Itzel López Ramírez**

### 🧑‍🏫 Asesores
- **Dra. Iclia Villordo Jiménez**  
- **Dr. Luz Noé Oliva Moreno**

---

## 📁 Estructura del Repositorio

```

.
├── .github/
│   └── workflows/
│       └── latex.yml      \# Workflow para compilar el PDF automáticamente
├── Documento/             \# Carpeta principal del contenido de la tesis
│   ├── Imagenes/          \# Subcarpeta para las figuras y diagramas
│   ├── Tablas/            \# Subcarpeta para tablas complejas o datos
│   ├── 1-Introduccion.tex \# Archivo .tex para el Capítulo 1
│   └── ...                \# Y así sucesivamente con los demás capítulos
├── bst/                   \# Estilos para la bibliografía (ej. IEEEtran.bst)
├── STY/                   \# Macros y estilos personalizados (ej. EPN.sty)
├── main.tex               \# 📄 Documento principal que une todas las partes
├── Bibliografia.bib       \# 📚 Base de datos de referencias en formato BibTeX
├── IPN.png, UPIITA.png    \# 🖼️ Logos para la portada o encabezados
├── .gitignore             \# Archivos a ignorar por Git
├── CONTRIBUTING.md        \# 🌱 Guía de colaboración y uso de Git
├── LICENSE                \# 📜 Licencia del proyecto (MIT)
├── latexmkrc              \# ⚙️ Configuración para la herramienta latexmk
└── README.md              \# ⏪ Este archivo

```

---

## ⚙️ Cómo Compilar el Documento

El método recomendado para compilar el proyecto es usando **Visual Studio Code** con la extensión **LaTeX Workshop**, ya que automatiza todo el proceso.

### Requisitos de Software

1.  **MiKTeX:** Descarga e instala la distribución de LaTeX desde [miktex.org](https://miktex.org/). Durante la instalación, asegúrate de seleccionar la opción que permite instalar paquetes faltantes "al vuelo" (on-the-fly).
2.  **Perl:** La extensión LaTeX Workshop utiliza `latexmk` para una compilación robusta, lo cual requiere un intérprete de Perl. Para Windows, la opción recomendada es **[Strawberry Perl](https://strawberryperl.com/)**.
3.  **Visual Studio Code:** Descarga e instala el editor desde [code.visualstudio.com](https://code.visualstudio.com/).
4.  **Extensión LaTeX Workshop:** Dentro de VS Code, ve a la pestaña de `Extensiones` (Ctrl+Shift+X), busca `LaTeX Workshop` y haz clic en Instalar.

### Proceso de Compilación

Una vez que tengas todo instalado:

1.  Abre la carpeta del proyecto en VS Code.
2.  Abre el archivo principal `main.tex`.
3.  Guarda el archivo (`Ctrl+S`) o usa el atajo para compilar (`Ctrl+Alt+B`). LaTeX Workshop detectará los cambios y ejecutará automáticamente todas las pasadas de compilación necesarias para resolver las referencias y la bibliografía.
4.  Para ver el PDF resultante, haz clic en el icono de **previsualización** (una lupa sobre un documento) que aparece en la esquina superior derecha del editor.

---

## 🧱 Archivos importantes

| Archivo / Carpeta  | Descripción                                                      |
| ------------------ | ---------------------------------------------------------------- |
| `main.tex`         | Documento principal que incluye todos los capítulos.             |
| `Documento/`       | Carpeta con los capítulos y anexos del trabajo.                  |
| `Bibliografia.bib` | Base de datos BibTeX con las referencias bibliográficas.         |
| `bst/`             | Archivos de estilo para las referencias.                         |
| `STY/`             | Archivos de estilo personalizados (propios o de la institución). |
| `.gitignore`       | Define qué archivos no deben subirse al repositorio.             |
---
## 🧰 Buenas prácticas

- Realiza **commits pequeños y descriptivos**:  
  ```bash
  git commit -m "Agrego sección de metodología experimental"
 -  Usa ramas para grandes modificaciones (revision-final, nuevo-capitulo, etc.)
 - No subas archivos generados (.pdf, .aux, .log, etc.)
 - Compila antes de hacer push para asegurarte que el documento no tiene errores.

---

> 🪶 "La tesis no se termina, se entrega." 😅
---

### 🌱 Guía de Colaboración

Para mantener un historial de cambios limpio y consistente, hemos creado una [guía de colaboración con buenas prácticas y comandos de Git](./CONTRIBUTING.md).

---

## 📜 Licencia

Este proyecto está licenciado bajo la [MIT License](https://opensource.org/licenses/MIT).

Puedes modificar, usar y distribuir este material dando el debido crédito.

---

## ✒️ Cómo Citar

Si encuentras este trabajo útil para tu investigación, por favor considera citarlo. Puedes usar la siguiente entrada en formato BibTeX.

```bibtex
@mastersthesis{DompabloLopez2025,
  author    = {Dompablo Celaya, Oscar Alfredo and L\'{o}pez Ram\'{i}rez, Itzel},
  title     = {Sistema de Monitoreo de Contaminaci\'{o}n en Cuerpos de Agua Basado en una Red Inal\'{a}mbrica de Sensores y Visi\'{o}n Artificial},
  school    = {Instituto Polit\'{e}cnico Nacional (UPIITA)},
  year      = {2025}, 
  address   = {Ciudad de M\'{e}xico, M\'{e}xico},
  type      = {Tesis de Ingenier\'{i}a Telem\'{a}tica}
}