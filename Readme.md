# Repositorio para la evaluación del pipeline DevOps utilizando la metodología **GitFlow**.

---

## 1. Justificación de la Estrategia de Ramificación (IE1)
Para este proyecto se seleccionó el modelo **GitFlow** en lugar de alternativas como *GitHub Flow* o *Trunk-Based Development*, debido a las siguientes ventajas en entornos colaborativos y de producción:
* **Separación de Entornos:** Permite mantener una rama estable (`main`) exclusiva para código en producción y una rama de integración continua (`develop`) donde convergen las nuevas funcionalidades.
* **Trazabilidad y Control:** El uso de ramas temporales (`feature/` y `hotfix/`) aísla el desarrollo de nuevas características y la corrección de errores críticos, evitando corromper la línea base de producción.
* **Preparación para CI/CD:** Facilita la automatización de pruebas y despliegues al estructurar claramente qué ramas deben disparar un pipeline de integración.

---

## 2. Guía de Buenas Prácticas y Convenciones (IE5)

### A. Naming de Ramas (Branch Naming)
Se establece la siguiente nomenclatura estándar para mantener el orden en el control de versiones:
* `main`: Rama principal que contiene el código estable y listo para producción.
* `develop`: Rama de integración para las nuevas funcionalidades desarrolladas por el equipo.
* `feature/<nombre-descriptivo>`: Utilizada para el desarrollo de nuevas características del microservicio (ej. `feature/agregar-microservicio`).
* `hotfix/<nombre-descriptivo>`: Utilizada exclusivamente para solucionar errores críticos detectados en producción de forma urgente (ej. `hotfix/correccion-urgente`).

### B. Convención de Mensajes de Commit
Se utiliza el estándar de **Conventional Commits** para asegurar la legibilidad del historial:
* `feat:` Para agregar una nueva funcionalidad o módulo (ej. `feat: agrego archivos del microservicio de predicccion`).
* `fix:` Para correcciones de errores o bugs en producción (ej. `fix: correccion de error critico en produccion`).
* `docs:` Para cambios o mejoras en la documentación y archivos README (ej. `docs: agrego README con metodologia y convenciones`).

### C. Estructura de Carpetas del Proyecto
```text
DevOps-Angel/
├── .github/              # Configuración de automatizaciones y flujos de trabajo
├── notebooks/            # Cuadernos Jupyter con el modelo de machine learning
│   └── Plant_Village.ipynb
├── .gitignore            # Archivos ignorados por Git
└── README.md             # Documentación técnica del repositorio
```

## 3. Trazabilidad del Desarrollo
A continuación se documenta el flujo de trabajo ejecutado paso a paso en el control de versiones: 

* **1. Clonación e inicialización:**
  Cloné el repositorio desde GitHub a mi computador para establecer la base de trabajo local. Luego creé y subí la rama `develop` para separar el código en desarrollo de la versión estable de producción (`main`).

* **2. Incorporación del microservicio (Rama Feature):**
  Creé la rama `feature/agregar-microservicio` para trabajar de manera aislada. Ahí subí los archivos del modelo de predicción, asegurando que la rama principal se mantuviera limpia mientras agregaba los componentes nuevos.

* **3. Integración mediante Pull Request:**
  Abrí un Pull Request hacia la rama `develop` para revisar visualmente los cambios antes de hacer el merge y comprobar que no existieran conflictos en el código.

* **4. Corrección de emergencia (Rama Hotfix):**
  Para solucionar un inconveniente de forma urgente, creé una rama `hotfix/correccion-urgente` a partir de `main`. Tras aplicar la corrección, realicé el doble Pull Request exigido por GitFlow para actualizar tanto producción como desarrollo.

