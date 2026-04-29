# 📘 Sistema de Monitoreo de Contaminación en Cuerpos de Agua Basado en una Red Inalámbrica de Sensores y Visión Artificial

![Estado](https://img.shields.io/badge/Estado-En%20Proceso-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

### 🎓 Tesis de Ingeniería Telemática  
**Instituto Politécnico Nacional**  
**Unidad Profesional Interdisciplinaria en Ingeniería y Tecnologías Avanzadas (UPIITA)**  

---

# 🧠 Descripción del Proyecto

Este repositorio contiene el **código fuente en LaTeX** de la tesis titulada:

> *Sistema de monitoreo de contaminación en cuerpos de agua basado en una red inalámbrica de sensores y visión artificial.*

El proyecto propone el **diseño e implementación de un sistema automatizado de monitoreo ambiental** para cuerpos de agua, basado en una **Red Inalámbrica de Sensores (WSN)** combinada con **técnicas de visión artificial**.

El sistema permite medir parámetros fundamentales de **calidad del agua**, entre ellos:

* pH
* Oxígeno disuelto (OD)
* Temperatura
* Turbidez
* Conductividad eléctrica

Adicionalmente, la plataforma incorpora **visión artificial** para la **detección de residuos sólidos flotantes** en la superficie del agua.

Los datos capturados por los sensores y el sistema de visión son transmitidos a una **central de procesamiento**, donde se analizan y se visualizan mediante una **plataforma web de monitoreo**, permitiendo:

* monitoreo ambiental continuo
* detección temprana de eventos de contaminación
* apoyo en la toma de decisiones para la gestión ambiental

---

## 👥 Autores

- **Oscar Alfredo Dompablo Celaya**  
- **Itzel López Ramírez**

### 🧑‍🏫 Asesores
- **Dra. Iclia Villordo Jiménez**  
- **Dr. Luz Noé Oliva Moreno**

---

## 📄 Documento de la Tesis

La versión compilada de la tesis puede descargarse desde los **Releases del repositorio**.

👉 **Descargar PDF:**  
https://github.com/AlfredoDompablo/Proyecto-terminal/releases/tag/v43

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

# ⚙️ Cómo Compilar el Documento

El método recomendado para compilar el proyecto es utilizando **Visual Studio Code** con la extensión **LaTeX Workshop**, ya que automatiza todo el proceso de compilación.

---

## Requisitos de Software

Instalar los siguientes programas:

### 1️⃣ Distribución LaTeX

Instalar **MiKTeX**

https://miktex.org

Durante la instalación habilitar la opción:

> Install missing packages on-the-fly

---

### 2️⃣ Intérprete de Perl

La herramienta `latexmk` requiere **Perl** para ejecutar correctamente el proceso de compilación.

Para Windows se recomienda:

https://strawberryperl.com

---

### 3️⃣ Visual Studio Code

https://code.visualstudio.com

---

### 4️⃣ Extensión LaTeX Workshop

Instalar la extensión **LaTeX Workshop** desde el marketplace de extensiones de VS Code.

---

# 🧾 Proceso de Compilación

> ⚠️ Si solo deseas leer la tesis, puedes descargar directamente el PDF desde la sección **Releases** del repositorio.

### 1️⃣ Clonar el repositorio

Primero descarga el repositorio en tu equipo utilizando **Git**:

```bash
git clone https://github.com/AlfredoDompablo/Proyecto-terminal
````
Después entra a la carpeta del proyecto:

```bash
cd Proyecto-terminal
```
---
### 2️⃣ Abrir el proyecto en Visual Studio Code

Abre la carpeta del proyecto en **Visual Studio Code**.

También puedes hacerlo desde la terminal:

```bash
code .
```

---

### 3️⃣ Abrir el archivo principal

Dentro del proyecto, abre el archivo principal de la tesis:

```
main.tex
```

---

### 4️⃣ Compilar el documento

Guarda el archivo (`Ctrl + S`) o ejecuta el comando de compilación:

```
Ctrl + Alt + B
```

La extensión **LaTeX Workshop** ejecutará automáticamente todas las pasadas necesarias para resolver:

* referencias cruzadas
* bibliografía
* tabla de contenido

---

### 5️⃣ Visualizar el PDF

Para ver el resultado, abre la **vista previa del PDF** desde el icono de previsualización en el editor.


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

### 🌱 Guía de Colaboración

Para mantener un historial de cambios limpio y consistente, hemos creado una [guía de colaboración con buenas prácticas y comandos de Git](./CONTRIBUTING.md).

---

## 📜 Licencia

Este proyecto está licenciado bajo la [MIT License](https://opensource.org/licenses/MIT).

Puedes modificar, usar y distribuir este material dando el debido crédito.

---

# ✒️ Cómo Citar

Si este trabajo resulta útil para tu investigación, por favor considera citarlo.

```bibtex
@mastersthesis{DompabloLopez2025,
  author    = {Dompablo Celaya, Oscar Alfredo and López Ramírez, Itzel},
  title     = {Sistema de Monitoreo de Contaminación en Cuerpos de Agua Basado en una Red Inalámbrica de Sensores y Visión Artificial},
  school    = {Instituto Politécnico Nacional (UPIITA)},
  year      = {2025},
  address   = {Ciudad de México, México},
  type      = {Tesis de Ingeniería Telemática}
}
