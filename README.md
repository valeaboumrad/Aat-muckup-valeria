 de diseño vs. sugerencias del IS

1. Seguridad: qué llave va en la app

El IS me propuso usar solo la publishable key de Supabase en el index.html, dejar la secret key y la contraseña de la base de datos fuera del repo, y activar RLS en la tabla perfiles para que cada usuaria solo vea y edite su propia fila. Lo acepté tal cual. Entendí que la publishable key es pública por diseño y lo que realmente protege los datos son las políticas RLS, mientras que la secret key se salta RLS, así que si se sube a GitHub cualquiera puede leer todo.

2. Escalabilidad: dónde guardar los posts

El diagnóstico de la Sesión 22 mostró que los límites gratis de Vercel Hobby y Supabase Free me alcanzan hasta unos 5,000 usuarios, pero que mis posts viven solo en el localStorage de cada dispositivo y que Supabase Free pausa el proyecto tras 1 semana sin actividad. Revisé la propuesta: por ahora dejo los posts en localStorage y documento que mover los posts a Supabase es el siguiente paso, porque ese es mi cuello de botella real, no el costo.

3. Deployment: a qué rama subir

El agente de Claude Code propuso subir los cambios a una rama aparte. Lo rechacé y le pedí que subiera a main, porque Vercel despliega desde main y en una rama mi link de producción no se iba a actualizar.

Luego toca el botón verde "Commit changes..." arriba a la derecha. En el mensaje escribe "README: decisiones de diseño vs sugerencias del IS", deja marcado "Commit directly to the main branch" y toca "Commit changes".
