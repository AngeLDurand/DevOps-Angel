# Metodología de trabajo

Para este proyecto decidí utilizar Gitflow. Elegí esa forma de trabajar porque me ayuda a mantener el código ordenado y me acostumbra a trabajar como se hace en el mundo real.

Tener una rama main para el código que funciona bien y una rama develop para ir subiendo mis avances, me asegura de no romper el proyecto. Además crear ramas feature me permite enforcarme en desarrollar una sola cosa a la vez. Si algo se rompe y es urgente, se que puedo sacar un hotfix sin que se mezcle con otros desarrollos que tengo a medidas.


# Mis Convenciones de Trabajo

1. Nombres de las ramas:
* Para agregare nuevas cosas usaré: feature/agregar-login (ejemplo)
* Para arreglar errores urgentes usaré: hotflix/caida_base_de_datos (ejemplo)

2. Nombres de los commits: Usare mensajes cortos pero claros para saber que cambios hice en cada momento.
* feat: cuando agregue algo nuevo (ejemplo: feat: agrego formulario de contrato)
* fix: cuando solucione un error (ejemplo: arreglo el boton enviar).
* docs: Cuando solo modifique el README u otra documentacion.
  
3. Reglas para jntar el código (Merge):
* Para simular un entorno de trabajo real, evitare hacer merge directo a las ramas main o develop desde la terminal.
* Todo lo integrare creando Pull Requests (PR) en github. Así me obligo a hacer una ultima revisión visual de mi propio codigo antes de aceptarlo y juntarlo con lo principal.
**Nota:** Correcci�n cr�tica de emergencia aplicada.
