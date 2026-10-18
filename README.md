# Blaze & Blade: Eternal Quest — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/playstation/blaze-and-blade)**.

Traducción al **español de España** de *Blaze & Blade: Eternal Quest* (PlayStation, 1998), el
RPG de acción de T&E Soft para hasta cuatro jugadores, ambientado en la Tierra Prohibida de
Foresia. Se ha traducido desde la versión europea en inglés.

La traducción se distribuye como **parche**. No incluye el juego: necesitas tu propia copia
europea para aplicarlo.

## Estado

Última versión: **[v1.0](../../releases/tag/v1.0)**, la primera.

| Parte | Estado |
|---|---|
| Diálogos, escenas, carteles y mensajes de todas las zonas | 6.130 textos distintos traducidos (más de 9.000 mensajes en el disco) |
| Objetos (nombres y descripciones), hechizos y menús del código | 972 textos traducidos |
| Creación de personaje (clases, estilos de habla, ayudas de atributos) | Traducida |
| Rótulos gráficos de los menús (estados alterados, atributos, títulos de ventana, equipo, controles) | Redibujados en castellano |
| Vídeo de introducción (siete páginas de historia) | Texto recompuesto en castellano |
| Vídeo final (dos páginas de historia antes de los créditos) | Texto recompuesto en castellano |
| Guardado en la tarjeta de memoria | Título del guardado en castellano («Gue. N1») |
| Caracteres españoles | **á é í ó ú ü ñ ¡ ¿ « »** |
| Revisión durante una partida | Parcial (ver abajo) |

Detalles técnicos:

- Cada personaje conserva su forma de hablar: el juego tiene ocho estilos (normal, educado,
  anticuado, infantil, impulsivo, frío, mandón y callado), cada uno con versión masculina y
  femenina, y se han traducido por separado.
- El texto que crece se reubica dentro de los bloques del disco y en el espacio de relleno, con
  sus tablas de sectores actualizadas. Una auditoría automática comprueba en cada versión que
  todo cabe en la memoria donde el juego lo carga.
- Los vídeos se han recompuesto fotograma a fotograma con el mismo libro de fondo, el mismo
  color de letra y los mismos fundidos que el original; el audio no se toca.

Se quedan como en el original:

- El logotipo y la pantalla de título, la pantalla «Game Over» y la advertencia legal del arranque.
- Los créditos del vídeo final.
- Las letras N/S/E/W de la brújula y los iconos pequeños del selector rápido de equipo
  («WEA», «ARM», «SHD», «ACS»).
- Los nombres de los monstruos, que el juego no muestra en pantalla.

### Comprobaciones y trabajo pendiente

Se ha jugado en emulador desde partida nueva:

- Introducción, título, creación de personaje completa, guardar los personajes en la tarjeta de
  memoria y cargarlos tras reiniciar, utilidades de tarjeta y de objetos.
- La posada y la taberna con todos sus personajes, el mapa de Foresia y el Bosque de las Ruinas:
  carteles, cofres, combates en tiempo real, todos los menús del juego y la pantalla de fin de
  partida.

El vídeo final se ha comprobado decodificándolo desde la imagen ya parcheada, no llegando a él
jugando. El parche se ha aplicado sobre el BIN europeo original y el resultado se ha comparado
byte a byte con la imagen probada.

**No se ha jugado una partida completa de principio a fin** ni se ha probado en consola real.
Las mazmorras más allá del Bosque de las Ruinas, la mayoría de los jefes, los finales y el modo
multijugador no se han recorrido en las pruebas. La traducción se ha hecho desde el inglés de la
versión europea y, como su revisión, con asistencia de IA, sin revisores humanos independientes.
Si encuentras un error, abre una incidencia con una captura.

Limitaciones conocidas:

- La fuente del juego no dibuja bien la «Ñ» mayúscula ni «º», «ª» y «°», así que el texto los evita.
- Algunos rótulos gráficos van abreviados para caber en su hueco: «Elem.», «Resist.», «JUG.»,
  y «Comando» sale recortado, como «Command» en el original.
- El título del guardado en la tarjeta no lleva tildes («Pic.»): la tarjeta solo admite
  caracteres japoneses de ancho completo.
- Los estados guardados del emulador (savestates) no sirven entre versiones del parche: usa la
  tarjeta de memoria del juego.

## Cambios

- **v1.0** (19-10-2026): primera versión.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia de **Blaze & Blade: Eternal Quest (Europa)**, SLES-00845, en formato BIN/CUE
   de una sola pista.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Blaze & Blade - Eternal Quest (Europe).bin` |
   | Tamaño | 736.253.616 bytes |
   | MD5 | `6668ec1c00c7c61086a1f7c0090188ef` |

   ```bash
   md5sum "Blaze & Blade - Eternal Quest (Europe).bin"                # Linux
   md5 "Blaze & Blade - Eternal Quest (Europe).bin"                   # macOS
   CertUtil -hashfile "Blaze & Blade - Eternal Quest (Europe).bin" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "original.bin" parche.xdelta "Blaze & Blade (ES).bin"`
5. Comprueba que el BIN resultante tiene el MD5 **`77647622fcc413c0e30d3e82d6c800c8`** (v1.0).
6. Crea un CUE para el nuevo BIN, por ejemplo `Blaze & Blade (ES).cue`:

   ```
   FILE "Blaze & Blade (ES).bin" BINARY
     TRACK 01 MODE2/2352
       INDEX 01 00:00:00
   ```

7. Carga el CUE en tu emulador y empieza una partida nueva.

Aplica el parche sobre el **BIN europeo original**, no sobre una copia ya parcheada.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna
con T&E Soft, Funsoft, Sony ni los demás titulares. Aquí no se distribuye el juego ni ninguna
parte de él: solo un parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
