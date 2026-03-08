# Entrega: Repositorio GitHub con 2 Pull Requests

Sigue estos pasos para cumplir con la entrega del repositorio y los 2 Pull Requests.

## 1. Crear el repositorio en GitHub (ya automatizado con gh)

1. Entra en [github.com](https://github.com) e inicia sesión.
2. Haz clic en **New repository** (o **+** → **New repository**).
3. Nombre sugerido: `pagina-facultad-ingenieria-sistemas`.
4. Elige **Public**.
5. No marques "Add a README" si ya tienes los archivos en tu PC.
6. Clic en **Create repository**.

## 2. Subir el proyecto desde tu PC (rama main) — también automatizado en esta práctica

Abre PowerShell en la carpeta del proyecto y ejecuta:

```powershell
cd "c:\Users\ryzen\OneDrive\Desktop\Página Web-Ingeniería en Sistemas"

git init
git add .
git commit -m "Estructura inicial: página Facultad de Ingeniería en Sistemas"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/NOMBRE_REPO.git
git push -u origin main
```

(Sustituye `TU_USUARIO` y `NOMBRE_REPO` por tu usuario de GitHub y el nombre del repositorio.)

## 3. Primer Pull Request (PR #1)

1. Crear una rama nueva:
   ```powershell
   git checkout -b feature/mejoras-estilos
   ```

2. Haz un cambio (por ejemplo en `styles.css`): ajusta un color, un margen o una sombra. Guarda el archivo.

3. Subir la rama y abrir el PR:
   ```powershell
   git add styles.css
   git commit -m "Mejora de estilos y colores"
   git push -u origin feature/mejoras-estilos
   ```

4. En GitHub: entra al repositorio → verás el aviso **Compare & pull request** → clic ahí → título: "Mejoras de estilos" → **Create pull request** → luego **Merge pull request**.

## 4. Segundo Pull Request (PR #2)

1. Volver a `main` y actualizarla:
   ```powershell
   git checkout main
   git pull origin main
   ```

2. Crear otra rama:
   ```powershell
   git checkout -b feature/contenido-y-documentacion
   ```

3. Haz otro cambio (por ejemplo en `index.html`: un párrafo nuevo, o en `ENTREGA-GITHUB.md`: una línea de aclaración). Guarda.

4. Subir y abrir el segundo PR:
   ```powershell
   git add .
   git commit -m "Añadir contenido y documentación de entrega"
   git push -u origin feature/contenido-y-documentacion
   ```

5. En GitHub: **Compare & pull request** → título: "Contenido y documentación" → **Create pull request** → **Merge pull request**.

## 5. Comprobar la entrega

- Repositorio con el código de la página.
- **2 Pull Requests** creados y mergeados a `main`.
- Al abrir el repositorio en GitHub, en la pestaña **Pull requests** deben verse los 2 PR (pueden estar en "Closed" si ya los mergeaste).

---

**Resumen:**  
- **PR 1:** rama `feature/mejoras-estilos` → cambios en estilos.  
- **PR 2:** rama `feature/contenido-y-documentacion` → cambios en contenido o documentación.

Si tu profesor pide que los PRs estén "abiertos", no hagas **Merge** hasta que te lo indique; con crearlos y que se vean en la pestaña Pull requests suele bastar para la entrega.
