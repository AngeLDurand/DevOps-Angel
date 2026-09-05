# Repositorio para la evaluacion del pipeline DevOps utilizado en la metodologia.


# 1. Justificacion de la estrategia de ramificacion.
Para este proyecto decidi­ utilizar Gitflow. Elegi­ esa forma de trabajar porque me ayuda a mantener el codigo ordenado y me acostumbra a trabajar como se hace en el mundo real.

Tener una rama main para el codigo que funciona bien y una rama develop para ir subiendo mis avances, me asegura de no romper el proyecto. Ademas crear ramas feature me permite enforcarme en desarrollar una sola cosa a la vez. Si algo se rompe y es urgente, se que puedo sacar un hotfix sin que se mezcle con otros desarrollos que tengo a medidas.


## 2. Mis Convenciones de Trabajo

### a. Nombres de las ramas:
* Para agregare nuevas cosas usare: feature/agregar-login (ejemplo)
* Para arreglar errores urgentes usare: hotflix/caida_base_de_datos (ejemplo)

### b. Nombres de los commits: Usare mensajes cortos pero claros para saber que cambios hice en cada momento.
* feat: cuando agregue algo nuevo (ejemplo: feat: agrego formulario de contrato)
* fix: cuando solucione un error (ejemplo: arreglo el boton enviar).
* docs: Cuando solo modifique el README u otra documentacion.

### c. Estructura de carpetas del proyecto
DevOps-Angel/
├── .github/              # Configuración de automatizaciones y flujos de trabajo
├── notebooks/            # Cuadernos Jupyter con el modelo de machine learning
│   └── Plant_Village.ipynb
├── .gitignore            # Archivos ignorados por Git
└── README.md             # Documentación técnica del repositorio
  
## 3. Reglas para juntar el codigo (Merge):
* Para simular un entorno de trabajo real, evitare hacer merge directo a las ramas main o develop desde la terminal.
* Todo lo integrare creando Pull Requests (PR) en github. AsÃ­ me obligo a hacer una ultima revision visual de mi propio codigo antes de aceptarlo y juntarlo con lo principal.
