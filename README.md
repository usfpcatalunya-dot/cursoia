# Aprende IA en 10 Días · تعلَّم الذكاء الاصطناعي

Curso bilingüe (español / árabe) de 10 días con lecciones, glosario, 50 prompts y generador de prompts.
Es una página estática de un solo archivo (`index.html`): Vue 3 y Tailwind se cargan desde CDN, y el progreso del alumno se guarda en el navegador (`localStorage`).

## Publicar en Vercel

1. Sube este repositorio a GitHub (ya lo está).
2. En [vercel.com/new](https://vercel.com/new) elige **Import Git Repository** y selecciona `cursoia`.
3. Ajustes: **Framework Preset: Other**, sin *Build Command* ni *Output Directory*. Pulsa **Deploy**.

Cada `git push` a la rama principal se publica automáticamente.

Desde la terminal también funciona: `npx vercel --prod` en esta carpeta.

## Archivos

- `index.html`: toda la aplicación.
- `vercel.json`: URLs limpias y cabeceras de seguridad básicas.

## Mejora pendiente recomendada

Tailwind se carga con su CDN de desarrollo (*Play CDN*), que genera los estilos en el navegador de cada visitante. Funciona, pero es más lento y el propio Tailwind no lo recomienda para producción. Para sustituirlo, compila el CSS una vez con el CLI de Tailwind v3 y enlaza el archivo resultante en lugar del `<script>` del CDN.
