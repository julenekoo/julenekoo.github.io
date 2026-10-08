# Escaparate del portfolio

La web publica que presenta los doce proyectos. Se sirve con GitHub Pages en
https://julenekoo.github.io

**Este repositorio es el unico publico.** Los doce repositorios de codigo son
privados; aqui solo hay el HTML del escaparate, las capturas y los textos. Por
eso Pages funciona sin plan de pago: Pages gratuito solo sirve repositorios
publicos, asi que el escaparate vive aparte y el codigo se queda privado.

## Que hay dentro

| | |
|---|---|
| `index.html` | El escaparate entero: HTML y CSS en un fichero, sin dependencias |
| `img/` | Capturas de los juegos, sacadas de los arneses de prueba de cada proyecto |
| `_serve.ps1` | Servidor local para verlo antes de publicar: `powershell -ExecutionPolicy Bypass -File _serve.ps1` y abrir http://localhost:8769 |

## Las cifras, y COMO se cuentan

Al dia 2026-10-08: **753.547 lineas de codigo, 7.599 comprobaciones
verificadas, 472 commits de historial y 446 con co-autoria de IA declarada.**

Ese mismo dia entraron los dos ultimos proyectos, que llevaban mucho codigo y
ningun control de versiones: **Asistente del local** (el gestor para bares,
200.812 lineas) y **Residy** (el gestor de habitaciones, 176.664). De diez
proyectos a doce, y de 376.071 lineas a 753.547.

La primera vez, en septiembre, estas cifras se midieron y no se estimo ninguna,
pero **la regla no quedo escrita**, y al volver a medir en octubre no se pudo
repetir: en el commit donde el escaparate decia que Veta Serena tenia 196
commits, sus `.gd` versionados dan 78.768 lineas y el sitio publicaba 79.986.
La diferencia es que entonces se conto el **arbol de trabajo**, con ficheros sin
commitear, y eso no se puede reproducir despues. Asi que la regla queda aqui.

**Lineas de codigo.** Las lineas de los ficheros **versionados en `HEAD`** de
cada repositorio:

- los seis juegos de Godot: los `.gd`;
- los cuatro proyectos web: los `.html`, `.css` y `.js`;
- Residy: los `.kt` del movil y del servidor, mas el `.js`, `.html` y `.css` del
  panel web;
- Asistente del local: los `.ts`, `.tsx`, `.js` y `.mjs`.

No cuentan los assets, ni las escenas `.tscn`, ni la configuracion, ni los
documentos en Markdown —que en algunos proyectos son miles de lineas y no son
codigo—, ni nada que `.gitignore` excluya. Que sean los ficheros versionados y
no los del disco es lo que hace la cifra repetible: cualquiera con el
repositorio saca el mismo numero.

La regla se comprobo contra las cifras viejas en los tres proyectos que no
habian cambiado desde septiembre, y da exacto: CovetBorn 24.927, FUSE 3.070 y
el prototipo de Just One More Door 2.327.

**Y una copia duplicada estuvo a punto de inflar la cifra otra vez.** El
Asistente del local guarda en `fotos-desarrollo/` dos copias enteras de su
propio arbol —`antes-ronda-2` y `antes-ronda-3`—, asi que contar sus `.ts` a lo
bruto daba **441.791** lineas en vez de 200.812: el proyecto contado tres veces,
240.979 lineas de duplicado. Es el mismo error que el worktree de CovetBorn-sim
en septiembre, con otro traje. Las copias no cuentan.

**Comprobaciones.** La suma de la ultima bateria **ejecutada** de los tres
juegos que tienen arnes:

| Proyecto | Comprobaciones | De donde sale |
|---|---|---|
| Veta Serena | 3.815 | bateria ejecutada, anotada y fechada en su `README.md` |
| We Need Millions | 2.492 | la suite al cerrar su ultima sesion, en `ESTADO-PROYECTO.md` |
| La ciudad en una maleta | 1.292 | ejecutadas las 12 suites el 2026-10-08, todas verdes |

Los otros tres juegos **no tienen arnes** y sus README lo dicen en la primera
pantalla; los cuatro proyectos web tampoco.

Las dos aplicaciones de gestion **si tienen pruebas y no entran en esta suma**:
Residy tiene 231 ficheros de prueba con 1.261 metodos marcados con la anotacion de prueba, contados sobre el
codigo, y el Asistente del local 193 ficheros mas una tanda en navegador que su
documentacion deja medida en «40 de 40, sin errores en la consola». Ninguna de
las dos publica todavia un total consolidado de UNA ejecucion, y sumar un
recuento de ficheros a una cifra de comprobaciones ejecutadas seria mezclar dos
cosas distintas. Cuando alguna lo publique, entra en la tabla.

Ninguna cifra de la tabla de arriba es un
recuento sobre el codigo: hasta septiembre las 1.554 de Veta Serena lo eran, y
dejaron de serlo cuando su arnes aprendio a informar del resultado mientras
corre.

**Un aviso que el sitio tambien da:** el arnes de We Need Millions **no corre
sin pantalla**. Lanzado en modo `--headless` imprime comprobaciones correctas
pero cuatro fallan, y las cuatro por nodos visuales que sin render no existen
(sprites, botones, `global_position`). Su cifra es la que el proyecto mide con
pantalla, no una verificada aqui.

**Commits y co-autoria.** `git rev-list --count HEAD` por repositorio, y los que
llevan el remolque `Co-Authored-By` en el mensaje. Los 26 sin co-autoria son los
mas viejos de Veta Serena, de antes de que la costumbre empezara.

**Si cambian los proyectos, hay que volver a medir antes de tocar el numero.** Un
escaparate que presume de medir no puede llevar una cifra inflada ni una heredada.

## Capturas

Las capturas de `img/` salen de los arneses de prueba de los propios juegos,
no de una sesion de juego a mano. Veta Serena, Just One More Door y CovetBorn
todavia no tienen captura en el escaparate.
