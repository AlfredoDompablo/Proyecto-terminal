# 🌱 Guía de Colaboración y Uso de Git

Para mantener un historial limpio y ordenado en el repositorio de la tesis, es importante seguir las siguientes prácticas y utilizar los comandos de Git de manera consistente.

---

## 🏁 Primeros Pasos: Clonar el Repositorio

Este es el primer y único paso que necesitas para descargar el proyecto a tu computadora por primera vez.

* #### `git clone <URL-del-repositorio>`
    **¿Qué hace?** Crea una copia local completa del repositorio remoto.
    **¿Cómo se usa?**
    1.  Ve a la página principal del repositorio en GitHub.
    2.  Haz clic en el botón verde que dice **`< > Code`**.
    3.  Copia la URL que aparece (se recomienda usar HTTPS).
    4.  Abre una terminal en la carpeta donde quieras descargar el proyecto y ejecuta el comando:
        ```bash
        git clone [https://github.com/tu-usuario/nombre-del-repositorio.git](https://github.com/tu-usuario/nombre-del-repositorio.git)
        ```


---

## 🚀 Flujo de Trabajo Diario

Este es el ciclo de trabajo que usarás el 90% del tiempo para guardar y subir tus cambios.

1.  #### `git pull`
    **¿Qué hace?** Descarga los cambios del repositorio remoto (GitHub) y los fusiona con tu rama actual. Es una combinación de `git fetch` (descargar) + `git merge` (fusionar).
    **Truco:** Acostúmbrate a hacer `git pull` antes de empezar a trabajar para asegurarte de tener la versión más reciente.
---
* #### `git clone <URL-del-repositorio>`
    **¿Qué hace?** Crea una copia local de un repositorio remoto existente. Solo lo usas la primera vez que descargas un proyecto en una nueva computadora.
---

2.  #### `git status`
    **¿Qué hace?** Te da un resumen del estado de tu repositorio. Te dice qué archivos han sido modificados (`M`), cuáles son nuevos (`??`) y cuáles están listos para el próximo commit.
    **Truco:** Úsalo *siempre* antes de `add` y `commit` para estar seguro de lo que vas a guardar.

3.  #### `git add <archivo>` o `git add .`
    **¿Qué hace?** Prepara tus cambios para ser guardados (los añade al "Staging Area"). `git add .` añade todos los archivos modificados y nuevos.
    **Truco:** Para crear commits más lógicos y pequeños, añade archivos de uno en uno: `git add Documento/3-Propuesta.tex`.

4.  #### `git commit -m "Tu mensaje descriptivo"`
    **¿Qué hace?** Guarda permanentemente los cambios que preparaste con `git add` en el historial del proyecto.
    **Truco para el mensaje:** Usa el "modo imperativo". En lugar de "Agregué la sección de...", escribe "**Agrega** la sección de...". Es un estándar y hace el historial más fácil de leer.
    * ✅ **Bien:** `git commit -m "Corrige error de tipeo en la introducción"`
    * ❌ **Mal:** `git commit -m "cambios"`

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

* #### `git reset <archivo>`
    **¿Qué hace?** Saca un archivo del "área de preparación". Si hiciste `git add` a un archivo por error, este comando lo "des-añade".

* #### `git checkout -- <archivo>`
    **⚠️⚠️¡CUIDADO!⚠️⚠️** Este comando **descarta todos los cambios no guardados** en un archivo, devolviéndolo a su estado del último commit. No hay vuelta atrás para esos cambios.

* #### `git commit --amend`
    **¿Qué hace?** Te permite modificar el último commit. Es perfecto si te equivocaste en el mensaje o si olvidaste añadir un archivo.
    **Flujo de trabajo:**
    1.  `git add archivo-olvidado.tex` (Añades el archivo que faltaba).
    2.  `git commit --amend --no-edit` (Añade el archivo al commit anterior sin cambiar el mensaje).

