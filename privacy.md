---
layout: default
title: Política de Privacidad
---

[← Volver al inicio](./)

# Política de Privacidad de SBT BOT

**Última actualización: 25 de noviembre de 2026**

## 1. Introducción

SBT BOT es un bot de Discord que ofrece funciones de entretenimiento y
juegos para comunidades, incluyendo una economía virtual, colección de
cartas, misiones, rankings, casino virtual, Loldle y otras actividades.

Esta Política de Privacidad explica qué información utiliza SBT BOT,
cómo la almacena, para qué la utiliza, en qué circunstancias puede
compartirla y cómo puedes solicitar su eliminación.

El responsable del tratamiento de los datos relacionados con SBT BOT es
el equipo de desarrollo de SBT BOT, que se puede contactar en sbtdevbot@gmail.com.

**Contacto:** <sbtdevbot@gmail.com>

Al utilizar SBT BOT, puedes consultar tus opciones de privacidad
mediante los comandos disponibles. Esta política no limita los derechos
que te reconozca la legislación aplicable.

## 2. Información que recopilamos y almacenamos

SBT BOT utiliza información relacionada con el funcionamiento de sus
características.

### 2.1. Identificadores

Al utilizar el bot, se almacenan:

-   Tu Discord User ID, que permite asociar tus actividades con tu
    cuenta.
-   El ID del servidor de Discord donde utilizas el bot.
-   El ID de determinados canales, cuando es necesario para funciones
    como los avisos de temporada.

Estos identificadores permiten separar los datos de cada comunidad y
reconocer los registros correspondientes a cada usuario.

Además, por cada servidor se guarda si la función de resúmenes con IA
está activada y en qué modo funciona.

### 2.2. Datos de juego

Dependiendo de las funciones que utilices, SBT BOT puede almacenar:

-   Saldo de SBT Points.
-   Cartas obtenidas y fechas de adquisición.
-   Wishlist y búsquedas realizadas dentro de ella.
-   Progreso de misiones.
-   Progreso y participación en el pase.
-   Progreso de la torre.
-   Actividad y resultados del casino virtual.
-   Participación, intentos y victorias en Loldle.
-   Estadísticas y contadores necesarios para el funcionamiento de los
    juegos.
-   La experiencia (XP) ganada por mensajes durante el día (solo el
    número).
-   Tu preferencia sobre los resúmenes (`!resumen incluirme` o
    `!resumen excluirme`), solo si la indicaste.

Las búsquedas de la wishlist y las respuestas que escribes en Loldle se
almacenan porque forman parte de las funcionalidades que utilizas
voluntariamente.

### 2.3. Información que no almacenamos en nuestra base de datos

SBT BOT no almacena de forma persistente:

-   El contenido general de tus mensajes de Discord.
-   Tu nombre de usuario.
-   Tu avatar.
-   Tu dirección de correo electrónico de Discord.
-   Tu dirección IP.
-   Tu ubicación geográfica.

El bot puede consultar nombres de usuario y avatares a través de Discord
para mostrarlos en determinadas respuestas, pero no los conserva como
registros propios en su base de datos.

Tampoco se recopilan datos de tarjetas bancarias ni se realizan pagos a
través del bot.

## 3. Lectura de mensajes y permisos de Discord

SBT BOT utiliza el permiso **Message Content Intent** de Discord para
determinadas funcionalidades.

Esto permite:

-   Reconocer comandos escritos por los usuarios.
-   Contar mensajes para calcular la XP diaria.
-   Detectar actividad necesaria para hacer aparecer cofres.
-   Leer los mensajes recientes del canal cuando alguien solicita
    expresamente un resumen con `!resumen` (con o sin IA).

El contenido general de los mensajes no se almacena en la base de datos
del bot.

Para la experiencia diaria, se conserva únicamente la cantidad de XP
ganada por el usuario ese día.

Los mensajes utilizados para generar resúmenes con IA se procesan
temporalmente en la memoria del bot y no se guardan en su base de datos.

## 4. Inteligencia artificial y resúmenes

SBT BOT dispone de una función opcional de resúmenes mediante
inteligencia artificial, utilizando la API de Claude de Anthropic.

Esta función se encuentra **desactivada por defecto en cada servidor**.

Para utilizarla:

1.  Un administrador del servidor debe habilitar la función.
2.  El servidor debe establecer el modo de consentimiento o exclusión.
3.  Cada solicitud de resumen requiere una confirmación expresa mediante
    una reacción de confirmación.
4.  Si no se confirma la operación, no se realiza ninguna solicitud a
    Anthropic.

### 4.1. Información enviada a Anthropic

Cuando se confirma una solicitud, el bot puede enviar hasta 500 mensajes
del canal donde se usó el comando, junto con la hora de cada mensaje.

Antes del envío, el bot aplica medidas para reducir la información
identificable:

-   Sustituye los nombres de los participantes por seudónimos como
    «Persona 1» o «Persona 2».
-   Elimina menciones.
-   Elimina identificadores de Discord.
-   Elimina enlaces.
-   Elimina direcciones de correo electrónico.

**Estas medidas constituyen seudonimización, no anonimización
completa.**

El texto de los mensajes puede contener nombres, referencias,
situaciones u otros datos que permitan identificar a una persona,
incluso después de aplicar estos filtros.

Por ese motivo, no debes asumir que el contenido enviado a Anthropic es
completamente anónimo.

Anthropic procesa la información conforme a sus propias condiciones y
políticas. SBT BOT no controla los plazos de conservación que Anthropic
aplique a dicha información.

### 4.2. Modos de consentimiento

La función admite dos modalidades:

**Modo consentimiento:** solamente se incluyen mensajes de usuarios que
hayan aceptado expresamente mediante `!resumen incluirme`.

**Modo exclusión:** se incluyen los mensajes de los usuarios que no
hayan solicitado su exclusión mediante `!resumen excluirme`.

La exclusión individual se respeta en ambos modos. Los mensajes de una
persona excluida no se incluyen en ningún resumen, tampoco en los que
solo muestran estadísticas, y no se puede pedir un resumen de lo que
dijo esa persona.

### 4.3. Control individual

Puedes utilizar:

-   `!resumen incluirme`: autoriza la inclusión de tus mensajes en los
    resúmenes con IA, cuando corresponda.
-   `!resumen excluirme`: excluye tus mensajes de todos los resúmenes,
    con o sin IA.

La exclusión se mantiene incluso si posteriormente eliminas tus datos de
juego. En cambio, al eliminar tus datos se retira tu autorización de
`!resumen incluirme`, y tendrías que darla de nuevo si quieres volver a
participar.

El bot no almacena en su base de datos los mensajes enviados a Anthropic
ni las respuestas generadas por la IA.

## 5. Servicios externos

SBT BOT utiliza determinados servicios externos para funcionar.

### Discord

Es la plataforma sobre la que funciona el bot. Discord procesa los
mensajes, las reacciones, los perfiles y demás información necesaria
para prestar sus propios servicios. SBT BOT también consulta información
de Discord para reconocer usuarios y mostrar resultados.

Consulta la [Política de Privacidad de
Discord](https://discord.com/privacy/policy/).

### Anthropic (API de Claude)

Se utiliza exclusivamente para generar resúmenes cuando la IA está
habilitada y la solicitud ha sido confirmada.

Puede recibir hasta 500 mensajes, procesados previamente con seudónimos
y filtros de información identificable.

Consulta la [información legal y de privacidad de
Anthropic](https://www.anthropic.com/legal).

### AniList

Se utiliza para consultar información pública de personajes de anime.
SBT BOT realiza solicitudes de consulta utilizando números de página. No
envía identificadores personales de los jugadores para esta
funcionalidad.

Consulta los [términos de AniList](https://anilist.co/terms).

### Meraki Analytics y Riot Data Dragon

Se utilizan para obtener información pública de League of Legends,
incluyendo campeones, aspectos e imágenes. Estas consultas descargan
información pública y no requieren enviar datos personales de los
usuarios.

Consulta la [Política de Privacidad de Riot
Games](https://www.riotgames.com/en/privacy-notice).

Los servicios externos tienen sus propias políticas, condiciones y
prácticas de tratamiento de información. SBT BOT no controla sus
operaciones ni puede garantizar sus períodos de conservación.

## 6. Visibilidad de la información

Algunas funcionalidades muestran información de juego a otros miembros
del mismo servidor de Discord.

Esto incluye:

-   Rankings.
-   Harems.
-   Wishlists.
-   Inventarios.
-   Estadísticas y resultados de determinadas actividades.

Esta información se muestra dentro del servidor en el que se utiliza la
funcionalidad correspondiente.

SBT BOT no publica deliberadamente estos registros en sitios externos ni
los comparte públicamente fuera de Discord.

La visibilidad también depende de los permisos y configuraciones del
servidor.

## 7. Economía virtual

SBT Points, cartas y demás elementos de la economía de SBT BOT son
exclusivamente virtuales.

No tienen valor monetario, no pueden comprarse con dinero real y no
pueden canjearse por dinero, productos o servicios reales.

Las apuestas del casino utilizan únicamente moneda virtual.

SBT Points y cartas no constituyen dinero, instrumentos financieros,
activos de inversión ni derechos de cobro.

## 8. Conservación de los datos

Los datos de juego se conservan hasta que el usuario solicita su
eliminación o se realiza una operación de borrado autorizada.

| Información | Conservación |
| --- | --- |
| Saldos, cartas, misiones, pase, torre, casino, Loldle y wishlist | Hasta su eliminación |
| Preferencia sobre resúmenes y configuración de la IA del servidor | Hasta que se cambia o se elimina |
| XP diaria | Se sobrescribe diariamente |
| Contadores de tiradas, blackjack y torre | Se sobrescriben según su ventana temporal |
| Mensajes utilizados para resúmenes | No se almacenan en la base de datos |
| Tiempos de espera en memoria | Hasta que se reinicia el bot |
| Información enviada a Anthropic | Según las políticas de Anthropic |

### Copias de respaldo

Los datos eliminados de la base de datos principal pueden permanecer en
copias de respaldo anteriores hasta que dichas copias sean eliminadas.

Actualmente no se establece un plazo máximo verificable de conservación
de respaldos.

Por esta razón, SBT BOT no garantiza que una solicitud de eliminación
retire inmediatamente la información de todas las copias de respaldo
existentes.

## 9. Derechos de los usuarios y eliminación de datos

Puedes consultar y eliminar los datos asociados a tu cuenta mediante los
siguientes comandos.

### 9.1. Consultar tus datos

Utiliza:

`!misdatos`

El bot mostrará la información de juego que mantiene asociada a tu
cuenta dentro del servidor actual.

### 9.2. Eliminar tus datos

Utiliza:

`!borrarmisdatos`

El bot mostrará los datos que serán eliminados y solicitará dos
confirmaciones:

1.  Reaccionar con ✅.
2.  Escribir exactamente `BORRAR`.

El procedimiento debe completarse dentro de 60 segundos. Si no se
cumplen ambas confirmaciones, no se ejecutará el borrado.

Una vez confirmada la operación, los registros correspondientes se
eliminan de la base de datos mediante una transacción.

Al eliminar tus datos:

-   Tus cartas quedan disponibles para otros jugadores.
-   Tus SBT Points no se devuelven.
-   Se eliminan los registros de juego correspondientes.
-   Se retira tu autorización para los resúmenes con IA, si la habías
    dado. Tu exclusión de los resúmenes, si la pediste, se mantiene.
-   Tu participación en rankings y estadísticas deja de contabilizarse
    cuando corresponda.
-   Tus identificadores se retiran o sustituyen en los registros de
    Loldle para impedir que sigan atribuyéndose a tu cuenta.

**Importante:** si solicitas el borrado mientras participas en una
partida con apuesta o un duelo que todavía no ha terminado, el resultado
posterior puede volver a crear un registro asociado a tu cuenta. Para
evitarlo, solicita la eliminación una vez finalizadas las partidas
activas.

La eliminación de la base de datos principal no implica la eliminación
inmediata de copias de respaldo anteriores.

### 9.3. Eliminación por administradores

Los administradores de un servidor pueden solicitar la eliminación de
los datos de un usuario mediante:

`!borrardatos @usuario`

También pueden utilizar el identificador de Discord cuando corresponda.

Esta función dispone de restricciones de permisos, confirmaciones y
límites de uso para evitar eliminaciones indebidas.

### 9.4. Solicitudes por correo electrónico

También puedes solicitar la eliminación de tus datos escribiendo a:

**<sbtdevbot@gmail.com>**

La solicitud debe incluir:

-   Tu Discord User ID.
-   El ID del servidor correspondiente o la indicación «todos» si deseas
    solicitar la eliminación en todos los servidores.

Para evitar que alguien pida borrar los datos de otra persona, el
responsable confirmará que la solicitud viene del titular de la cuenta,
por ejemplo pidiéndote que escribas un mensaje directo desde esa misma
cuenta de Discord. Si puedes, usa directamente `!borrarmisdatos`, que no
requiere verificación adicional.

### 9.5. Exclusión de resúmenes con IA

Si únicamente deseas evitar que tus mensajes se utilicen en resúmenes,
puedes escribir:

`!resumen excluirme`

Esta decisión se mantiene aunque posteriormente elimines tus datos de
juego.

## 10. Seguridad de la información

SBT BOT utiliza medidas técnicas destinadas a reducir los riesgos de
acceso no autorizado y exposición de información.

Entre ellas:

-   Almacenamiento de credenciales fuera del código fuente, en archivos
    de configuración separados y excluidos del repositorio.
-   Evitar la impresión de credenciales y determinados datos
    identificables en la consola.
-   Operaciones de eliminación mediante transacciones de base de datos.
-   Confirmaciones explícitas para las operaciones de borrado.
-   Restricciones de permisos para las funciones administrativas.

Ningún sistema informático puede garantizar seguridad absoluta. Por
ello, no se garantiza la ausencia total de fallos, accesos no
autorizados o pérdida de información.

## 11. Sin publicidad, venta ni rastreo

SBT BOT no vende información personal, no utiliza los datos de juego
para publicidad, no incorpora sistemas propios de analítica de usuarios
y no implementa mecanismos propios de rastreo publicitario.

La información se utiliza para proporcionar las funcionalidades del bot.

Esta declaración se refiere a SBT BOT y no a las prácticas
independientes de Discord, los proveedores externos o la plataforma de
alojamiento de la documentación.

## 12. Edad mínima

SBT BOT no está dirigido a menores de 13 años, la edad mínima para usar
Discord. Si crees que el bot tiene datos de un menor de esa edad,
escribe al correo de contacto para eliminarlos.

## 13. Salida de un servidor y desinstalación

Salir de un servidor o retirar SBT BOT de una comunidad no provoca
automáticamente la eliminación de los datos almacenados.

Si deseas eliminar tu información, debes utilizar `!borrarmisdatos`,
solicitarlo a un administrador o escribir al correo de contacto.

## 14. Modificaciones de esta política

Esta Política de Privacidad puede actualizarse cuando cambien las
funcionalidades, los servicios externos o las prácticas de tratamiento
de información de SBT BOT.

Las modificaciones relevantes serán publicadas en esta misma página,
indicando la fecha de actualización.

## 15. Contacto

Para consultas, solicitudes de acceso, eliminación de información o
dudas relacionadas con esta política:

**Correo electrónico:** <sbtdevbot@gmail.com>

**Responsable:** Equipo de desarrollo de SBT BOT (sbtdevbot@gmail.com)

------------------------------------------------------------------------

SBT BOT es un proyecto independiente y no está afiliado, patrocinado ni
respaldado oficialmente por Discord, Anthropic, AniList o Riot Games.

[← Volver al inicio](./) · [Consultar los Términos y Condiciones](terms)
