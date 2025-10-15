# 🌱 Guía de Colaboración y Uso de Git

Para mantener un historial limpio y ordenado en el repositorio de la tesis, es importante seguir las siguientes prácticas y utilizar los comandos de Git de manera consistente.

---

## 🏁 Primeros Pasos: Clonar el Repositorio

Este es el primer y único paso que necesitas para descargar el proyecto a tu computadora por primera vez.

* #### `git clone <URL-del-repositorio>`
    **¿Qué hace?** Crea una copia local completa del repositorio remoto.
    **¿Cómo se usa?**
    1. Ve a la página principal del repositorio en GitHub.
    2. Haz clic en el botón verde que dice **`< > Code`**.
    3. Copia la URL que aparece (se recomienda usar HTTPS).
    4. Abre una terminal en la carpeta donde quieras descargar el proyecto y ejecuta el comando:
        ```bash
        git clone [https://github.com/tu-usuario/nombre-del-repositorio.git](https://github.com/tu-usuario/nombre-del-repositorio.git)
        ```


---

## 🚀 Flujo de Trabajo Diario

Este es el ciclo de trabajo que usarás el 90% del tiempo para guardar y subir tus cambios.

1.  #### `git pull`
    **¿Qué hace?** Descarga los cambios del repositorio remoto (GitHub) y los fusiona con tu rama actual. Es una combinación de `git fetch` (descargar) + `git merge` (fusionar).
    **Truco:** Acostúmbrate a hacer `git pull` antes de empezar a trabajar para asegurarte de tener la versión más reciente.

2.  #### `git status`
    **¿Qué hace?** Te da un resumen del estado de tu repositorio. Te dice qué archivos han sido modificados (`M`), cuáles son nuevos (`??`) y cuáles están listos para el próximo commit.
    **Truco:** Úsalo *siempre* antes de `add` y `commit` para estar seguro de lo que vas a guardar.

3.  #### `git add <archivo>` o `git add .`
    **¿Qué hace?** Prepara tus cambios para ser guardados (los añade al "Staging Area"). `git add .` añade todos los archivos modificados y nuevos.
    **Truco:** Para crear commits más lógicos y pequeños, añade archivos de uno en uno: `git add Documento/3-Propuesta.tex`.

4.  #### `git commit -m "Describe tu cambio aquí"`
    **¿Qué hace?** Guarda permanentemente los cambios que preparaste con `git add` en el historial del proyecto.
    **Truco para el mensaje:** Usa el "modo imperativo". En lugar de "Agregué la sección de...", escribe: "**Agrega** la sección de...". Es un estándar y hace el historial más fácil de leer.
    * ✅ **Buen mensaje:** `git commit -m "Agrega la sección de metodología al capítulo 3"`
    * ❌ **Mal mensaje:** `git commit -m "actualización"`

    > 💡 **Nota:** Para un historial profesional, seguimos un formato estándar. Consulta la [guía completa de formato para commits](#-guía-de-formato-para-commits) para ver todos los tipos y ejemplos.

5.  #### `git push`
    **¿Qué hace?** Sube tu commit (tus puntos de guardado) desde tu computadora local al repositorio remoto en GitHub para que todos los colaboradores puedan verlo.

---

## 🌿 Trabajando con Ramas (Branches)

Las ramas te permiten trabajar en nuevas ideas (como reescribir un capítulo) sin afectar la versión principal (`main`).

* #### `git branch <nombre-de-la-rama>`
    **¿Qué hace?** Crea una nueva rama.
    **Ejemplo:** `git branch revision-capitulo-2`

* #### `git checkout <nombre-de-la-rama>`
    **¿Qué hace?** Te mueves a la rama que especifiques.
    **Truco:** Crea y muévete a una nueva rama en un solo paso con `git checkout -b <nuevo-nombre-de-rama>`.

* #### `git merge <nombre-de-la-rama>`
    **¿Qué hace?** Fusiona los cambios de la rama especificada en tu rama actual.
    **Flujo de trabajo común:**
    1.  `git checkout main` (Vuelves a tu rama principal).
    2.  `git merge revision-capitulo-2` (Traes los cambios de la rama de revisión a la principal).

---

## ⏪ Historial y Cómo Deshacer Errores

Todos cometemos errores. Git es tu máquina del tiempo personal.

* #### `git log`
    **¿Qué hace?** Muestra el historial de commits, del más reciente al más antiguo.
    **Truco:** Usa `git log --oneline --graph` para una vista mucho más compacta y visual del historial y las ramas.

* #### `git log --oneline --graph --decorate --all`
    **¿Qué hace?** Te muestra una vista **compacta y visual** de todo el historial de commits. Es el mejor comando para entender cómo se han movido las ramas y quién ha hecho qué.
    * `--oneline`: Muestra cada commit en una sola línea.
    * `--graph`: Dibuja el árbol de ramas con caracteres ASCII.
    * `--decorate`: Muestra dónde están las ramas (ej. `HEAD -> main`, `origin/main`).
    * `--all`: Muestra los commits de todas las ramas, no solo la actual.

* #### `git reset <archivo>`
    **¿Qué hace?** Saca un archivo del "área de preparación". Si hiciste `git add` a un archivo por error, este comando lo "des-añade".

* #### `git checkout -- <archivo>`
    > **⚠️ ¡CUIDADO!** Este comando **descarta permanentemente** todos los cambios no guardados en un archivo, devolviéndolo a su estado del último commit. No hay vuelta atrás para esos cambios.


* #### `git commit --amend`
    **¿Qué hace?** Te permite modificar el último commit. Es perfecto si te equivocaste en el mensaje o si olvidaste añadir un archivo.
    **Flujo de trabajo:**
    1.  `git add archivo-olvidado.tex` (Añades el archivo que faltaba).
    2.  `git commit --amend --no-edit` (Añade el archivo al commit anterior sin cambiar el mensaje).

---

## 🎨 Guía de Formato para Commits

Para mantener un historial de Git limpio, legible y profesional, seguimos la especificación de **Commits Convencionales (Conventional Commits)**. Esto nos permite entender fácilmente el propósito de cada cambio y automatizar procesos en el futuro.

La estructura general de un commit es:

````
<tipo>(<alcance>): <descripción breve>

[cuerpo opcional con más detalles]

[pie de página opcional para breaking changes o issues]
````

---

### 🚀 Tipos de Commit Principales

Estos son los prefijos que debes usar para describir la naturaleza de tus cambios.

* ### **`feat`** (Feature - Característica)
    Se usa cuando añades una **nueva funcionalidad** al proyecto.
    * **Ejemplo:** `feat(capitulo4): Añade sección de análisis de resultados`

* ### **`fix`** (Fix - Corrección)
    Se usa cuando **corriges un error (bug)** en el código o en el documento.
    * **Ejemplo:** `fix(referencias): Corrige entrada de BibTeX para la norma APA`

* ### **`docs`** (Documentation - Documentación)
    Se usa para **cambios exclusivos en la documentación**, como el `README.md`, guías de contribución o comentarios.
    * **Ejemplo:** `docs(readme): Añade instrucciones de compilación`

* ### **`style`** (Style - Estilo)
    Se usa para cambios que **no afectan el significado del contenido**, solo el formato (espacios, sangrías, etc.).
    * **Ejemplo:** `style(main.tex): Ajusta espaciado entre párrafos`

* ### **`refactor`** (Refactor - Refactorización)
    Se usa cuando **reescribes o mejoras una parte del texto o código** sin cambiar su comportamiento externo ni añadir nuevas funcionalidades.
    * **Ejemplo:** `refactor(capitulo2): Reescribe el planteamiento del problema para mayor claridad`

* ### **`test`** (Test - Pruebas)
    Se usa para **añadir o corregir pruebas automatizadas**.
    * **Ejemplo:** `test(graficas): Agrega prueba para verificar la generación de gráficas`

* ### **`chore`** (Chore - Tarea)
    Se usa para **cambios en el proceso de construcción o herramientas auxiliares** que no tienen que ver con el contenido principal. Es el mantenimiento del repositorio.
    * **Ejemplo:** `chore(ci): Actualiza la versión de la acción de GitHub para compilar LaTeX`

* ### **`revert`** (Revert - Revertir)
    Se usa cuando **reviertes un commit anterior**. El mensaje debe empezar con `revert:`, seguido del encabezado del commit revertido.
    * **Ejemplo:** `revert: feat(capitulo4): Añade sección de análisis de resultados`

---

## 📝 Estructura Detallada y Buenas Prácticas

* #### **Alcance (Scope)**
    El `<alcance>` entre paréntesis es **opcional** y sirve para especificar la parte del proyecto que estás modificando (ej. `(readme)`, `(capitulo3)`, `(ci)`).

* #### **Descripción (Subject)**
    * **Usa el modo imperativo:** "Agrega", "Corrige", "Cambia".
    * No uses mayúscula inicial.
    * No pongas un punto final.
    * Mantenlo corto (idealmente < 50 caracteres).

* #### **Cuerpo (Body)**
    * **Opcional**, pero muy recomendado para commits complejos.
    * Explica el **qué y el porqué** del cambio.
    * Sepáralo de la descripción con una línea en blanco.

* #### **Pie de Página (Footer)**
    * **Opcional.** Se usa para referenciar `issues` de GitHub (`Closes #123`) o para marcar **Breaking Changes**.

---

### 🎨 Ejemplo Completo
```bash
# Un commit simple
fix(referencias): corrige el formato de la cita para 'Smith 2020'

# Un commit más completo
feat(capitulo5): agrega análisis estadístico de los resultados

Se implementa la prueba t de Student para comparar los resultados de los sensores A y B, validando la hipótesis de que el sensor B es más preciso.
````
