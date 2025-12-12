# Fluffusion for Zed

Fluffusion es un fork ligero del tema original de Catppuccin que aplica una paleta unica inspirada en "Fluffusion" y prioriza la legibilidad de Python con keywords y clases en negrita, comentarios/docstrings en cursiva y strings/numeros bien contrastados.

## Paleta & enfoque de sintaxis

- **Fondos & superficies** - editor: `#0e1024`, paneles: `#1a1e3d`.
- **Texto** - principal `#f2f4ff`, atenuado `#9aa0c9`.
- **Tokens semanticos** - keywords y operadores en `#1e9bff` (font-weight 700), clases/tipos en `#ff6dbd` (font-weight 700), funciones en `#66c8ff`, strings en `#4ce4a5`, numeros en `#ffe066`.
- **Comentarios/docstrings** - `#9aa0c9` (cursiva) en el tema dark, `#6c7297` (cursiva) en el light.
- **Estados** - exito `#4ce4a5`, advertencia `#ffe066`, error `#ff4f79`.
- **Cursor/seleccion** - cursor `#1e9bff`, seleccion `rgba(30,155,255,0.25)`.

## Instalacion

### 1. Desde este repositorio (modo desarrollo)
1. Abre Zed y ejecuta `zed: install dev extension`, luego selecciona la carpeta del repositorio.
2. Ejecuta `zed: reload extensions` si los temas no aparecen inmediatamente.
3. Abre la paleta de comandos, ejecuta `theme selector: toggle` y elige "Fluffusion Dark" o "Fluffusion Light Minimal".

### 2. Copia manual
1. Crea la carpeta `themes/` dentro de tu archivo de configuracion de Zed (`~/.config/zed/` en Linux/macOS o `%APPDATA%/zed/` en Windows).
2. Copia `themes/fluffusion.json` a esa carpeta.
3. Reinicia Zed y selecciona el tema deseado con `theme selector: toggle`.

## Optimizacion para Python

El tema utiliza:
- **Keywords (`def`, `class`, `import`, operadores...) en negrita** para distinguir bloques de control y declaraciones.
- **Clases/tipos** con color rosa `#ff6dbd` y font-weight 700 para sentirse mas estructuradas.
- **Funciones y llamadas** en azul cielo `#66c8ff` para seguir la cadena de ejecucion.
- **Strings/docstrings** verdes `#4ce4a5` y cursivas cuando el parser los marca como documentacion.
- **Numeros literales** en amarillo brillante `#ffe066`.
- **Comentarios y docstrings** en cursiva con tono de texto atenuado, lo que mejora el escaneo en bloques grandes.

Estos acentos tambien se replican en el tema light minimal para mantener consistencia visual.

## Activacion automatica (opcional)

Agrega este fragmento a tu `zed.json` (o el archivo de configuracion que uses) para fijar el tema sin pasar por el selector:

```json
{
  "ui.theme": "Fluffusion Dark"
}
```

Puedes cambiar el valor por `Fluffusion Light Minimal` si prefieres el modo claro.

## Desarrollo

- Modifica directamente `themes/fluffusion.json`.
- Usa `zed: install dev extension` para probar los cambios sin publicar.
- Despues de editar, ejecuta `zed: reload extensions` y vuelve a activar el tema desde `theme selector: toggle`.
- Si necesitas un `.zip` para publicar, empaqueta el contenido del repositorio (incluyendo `themes/fluffusion.json` y `extension.toml`) y subelo como actualizacion.

## Licencia

Este proyecto sigue la licencia MIT original. Consulta `LICENSE` para mas detalles.
