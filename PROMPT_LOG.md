# Bitácora de prompts - BarrePlan, Assignment 2

## Paso 1. Especificación
Qué hace: agrega un botón "Exportar a mi calendario" que genera un archivo .ics con todas las publicaciones de la semana que se ve en pantalla, cada una como evento de calendario con su título, plataforma, estado y copy, en la fecha y hora del post (media hora de duración; si no tiene hora, evento de todo el día).
Qué datos necesita: los posts que ya guarda el planner en localStorage (titulo, fecha, hora, copy, plataforma, estado) y las 7 fechas de la semana visible. No usa API ni clave.
Cómo se sabrá que funciona: creo un post de Instagram con fecha y hora y toco Exportar a mi calendario. Se descarga barreplan-semana-AAAA-MM-DD.ics, lo abro en Calendario del iPad y aparece un evento en esa fecha y hora con 30 minutos de duración y el título del post. Si la semana no tiene posts, la app avisa que no hay nada que exportar y no descarga archivo.

## Paso 2. Aceptar / rechazar / revisar
Fecha: 2026-11-02
Qué propuso la IA: que cada publicación con hora dure 30 minutos en el calendario, algo que yo no había definido.
Campo de mi especificación en juego: "Qué hace", la acción exacta del botón.
Mi decisión: Aceptar.
Por qué: me gusta que dure media hora, porque un post es algo corto y así en el calendario se ve como un recordatorio sin ocupar un bloque largo.

## Paso 3. Registro de validación
Input exacto: post con título "Post", fecha 2026-11-03, hora 22:45, plataforma Instagram, estado Borrador, copy "Post otoño". Toqué "Exportar a mi calendario" en aat-muckup-valeria.vercel.app, se descargó barreplan-semana-2026-11-02.ics y lo abrí en Calendario del iPad.

Output real: Instagram: Post / Tuesday, Nov 3, 2026 / 10:45PM – 11:15PM / Notes: Estado: Borrador, Post otoño

Veredicto: Aceptar. El evento salió el martes 3 de noviembre de 10:45 PM a 11:15 PM, o sea 30 minutos desde la hora del post como decía mi especificación, con el título "Instagram: Post" y en las notas el estado Borrador y el copy.

## Uso de IA
Herramienta: Claude.
Para qué: escribir el código de la función de exportar a calendario y el rediseño de la app.
Qué decidí o verifiqué yo: pedí yo el estilo y los colores de la app con una imagen de referencia, y probé yo la función en mi iPad: creé un post, exporté el archivo, lo abrí en Calendario y revisé el título, la fecha, la hora y las notas antes de dar el veredicto.

