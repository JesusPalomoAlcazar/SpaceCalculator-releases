# Space Calculator

Aplicación de escritorio para Windows que calcula cuánto espacio ocupan los archivos adjuntos de tus espacios de **Confluence**.

Se conecta con tu cuenta de Atlassian, recorre los espacios a los que tienes acceso y suma el tamaño de los adjuntos de cada página. Así ves de un vistazo qué espacios y qué páginas consumen más almacenamiento.

> Space Calculator **solo lee** información. No modifica, mueve ni borra nada en Confluence.

## Descarga

Descarga la última versión desde **[Releases](../../releases/latest)**:

1. Descarga `SpaceCalculator.exe`.
2. Ejecuta.

No necesita instalación.

## Requisitos

| Requisito | Detalle |
|---|---|
| Sistema operativo | Windows 10 u 11 (64 bits) |
| Componentes | [.NET 10 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/10.0). Windows ofrece instalarlo la primera vez si falta |
| Cuenta | Una cuenta de Atlassian con acceso a los espacios que quieres analizar |
| Credencial | Un [API token de Atlassian](https://id.atlassian.com/manage-profile/security/api-tokens) |

## Funciones

- **Resumen**: total de espacios, tamaño total utilizado, espacio que más consume y páginas analizadas.
- **Detalle por espacio**: páginas ordenadas de mayor a menor tamaño, con el porcentaje que ocupa cada una dentro de su espacio.
- **Búsqueda** por nombre de espacio o título de página.
- **Filtro** para ocultar las páginas sin adjuntos.
- **Expandir y colapsar** los espacios para comparar tamaños rápidamente.
- **Avisos de actualización**: al abrirse, la aplicación comprueba si hay una versión nueva en esta página.

## Primeros pasos

1. Abre la aplicación y pulsa **Configuración**.
2. Introduce:
   - tu **correo** de Atlassian,
   - el **dominio** de tu Confluence, por ejemplo `https://empresa.atlassian.net/wiki`,
   - tu **API token**.
3. Pulsa **Comprobar conectividad** para probar la conexión y después **Guardar Cambios**.
4. En la ventana principal, pulsa **Calcular**.

## Privacidad y seguridad

- Las credenciales se guardan **solo en tu equipo**, en `%APPDATA%\SpaceCalculator\settings.json`.
- El token se guarda **cifrado** con tu usuario de Windows (DPAPI): otro usuario del equipo no puede leerlo.
- La aplicación solo se comunica con tu Confluence y con GitHub, para comprobar si hay versiones nuevas.

## Limitaciones conocidas

- En cada consulta se leen como máximo 200 espacios, 200 páginas por espacio y 200 adjuntos por página. En sitios más grandes, los totales pueden ser menores que los reales.
- Solo se analiza lo que tu cuenta puede ver en Confluence.

## Versiones

| Versión | Novedades |
|---|---|
| 1.0.0 | Primera versión: cálculo por espacio y página, búsqueda, filtros, configuración con token cifrado y aviso de actualizaciones |

## Autor

Desarrollado por **Jesús Palomo**: [jesuspalomoalcazar.github.io](https://jesuspalomoalcazar.github.io/)
