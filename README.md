## Capítulo VI: Product Implementation, Validation & Deployment 

### 6.1. Software Configuration Management 

Esta sección presenta las decisiones y convenciones adoptadas por el equipo para asegurar la consistencia técnica en la implementación del sistema, desde el desarrollo hasta el despliegue.

### 6.1.1. Software Development Environment Configuration

Esta sección detalla las herramientas y tecnologías que el equipo utilizará para colaborar eficazmente en el desarrollo, pruebas y despliegue de los productos digitales que componen la solución. Se especifica su propósito y la ruta de acceso correspondiente.

#### **Requirements Management**

**Trello:** Herramienta para gestionar proyectos bajo metodologías ágiles. Permite la planificación, seguimiento y priorización de tareas, así como la asignación de responsables durante cada sprint.  
**Ruta de referencia:** [https://trello.com/es](https://trello.com/es)

#### **User Experience Design (UX/UI)**

**Figma:** Plataforma colaborativa de diseño digital. En este proyecto se utilizará para crear prototipos de alta fidelidad, mockups y wireflows tanto para la aplicación móvil como para la web.  
**Ruta de referencia:** [https://www.figma.com/login](https://www.figma.com/login)

#### **Software Testing**

**Gherkin + Cucumber:** Lenguaje estructurado y herramienta que permiten definir criterios de aceptación, pruebas de integración y pruebas de aceptación automatizadas en formato legible. Su aplicación será en el backend desarrollado con Spring Boot.  
**Ruta de referencia:** [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/)

#### **Software Development**

**Android Studio:** IDE oficial para el desarrollo de aplicaciones móviles Android. Se utilizará para la primera versión de la aplicación nativa desarrollada en Kotlin.  
**Ruta de referencia:** [https://developer.android.com/studio](https://developer.android.com/studio)

**Kotlin:** Lenguaje de programación moderno, interoperable con Java y orientado al desarrollo Android.  
**Ruta de referencia:** [https://kotlinlang.org/](https://kotlinlang.org/)

**Flutter** _(planificado en siguientes entregas)_: Framework UI de código abierto para desarrollar aplicaciones nativas multiplataforma desde una sola base de código.  
**Ruta de referencia:** [https://flutter.dev/](https://flutter.dev/)

**HTML5:** Lenguaje de marcado para la estructura de contenido en la Landing Page.  
**Ruta de referencia:** [https://www.w3schools.com/html/html5_syntax.asp](https://www.w3schools.com/html/html5_syntax.asp)

**CSS:** Lenguaje de estilos usado para definir la presentación visual del contenido web en la Landing Page.  
**Ruta de referencia:** [https://developer.mozilla.org/es/docs/Web/CSS](https://developer.mozilla.org/es/docs/Web/CSS)

**JavaScript:** Lenguaje de programación para la interactividad de la Landing Page.  
**Ruta de referencia:** [https://developer.mozilla.org/es/docs/Web/JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)

**Java + Spring Boot:** Lenguaje y framework utilizados para desarrollar los servicios RESTful del backend.  
**Ruta de referencia Java:** [https://dev.java](https://dev.java)  
**Ruta de referencia Spring Boot:** [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)

**IntelliJ IDEA Ultimate:** Entorno de desarrollo integrado utilizado para construir y mantener el backend en Java con Spring Boot.  
**Ruta de referencia:** [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/)

#### **Software Deployment**

**Git:** Sistema de control de versiones que permite gestionar los cambios del código fuente y facilitar el trabajo colaborativo.  
**Ruta de referencia:** [https://git-scm.com/](https://git-scm.com/)

#### **Software Documentation and Project Management**

**GitHub:** Plataforma de gestión de repositorios donde se almacenará el código fuente y documentación del proyecto. También se usará para la revisión de cambios y gestión de issues.  
**Ruta de referencia:** [https://github.com/](https://github.com/)

### 6.1.2. Source Code Management 

Esta sección describe la organización del código fuente, el control de versiones y las convenciones de trabajo colaborativo que el equipo utilizará mediante GitHub. Se detallan las prácticas asociadas al uso de GitFlow y estándares para los nombres de ramas, versiones y mensajes de commit.

#### **Repositorio principal**

El equipo utilizará GitHub como sistema de gestión de versiones. La organización del proyecto se encuentra bajo el siguiente espacio:

- **Organización GitHub:**  
    [https://github.com/G3-UPC-CC238-346-ParkingNow](https://github.com/G3-UPC-CC238-346-ParkingNow)
    
- **Landing Page:** 
    
- **Web Services:** 
    
- **Mobile Application:**
    

#### **Modelo de Ramas: GitFlow**

El equipo implementará el modelo de desarrollo basado en **GitFlow**, propuesto por Vincent Driessen. Este flujo de trabajo permite mantener un control ordenado y colaborativo del proyecto mediante ramas específicas para cada tipo de tarea.

**Ramas principales:**

- `main`: Contendrá el código de producción estable.
    
- `develop`: Contendrá las últimas funcionalidades en desarrollo integradas, previo a su paso a producción.
    

**Ramas auxiliares:**

- `feature/*`: Ramas para el desarrollo de nuevas funcionalidades. Se deben nombrar con prefijo claro y descriptivo.  
    _Ejemplo:_ `feature/login-screen`, `feature/rent-request-api`
    
- `release/*`: Ramas para preparar versiones de producción. Se crearán a partir de `develop` y se nombrarán con la versión.  
    _Ejemplo:_ `release/1.0.0`, `release/2.1.0`
    
- `hotfix/*`: Ramas para corregir errores críticos directamente desde `main`.  
    _Ejemplo:_ `hotfix/fix-payment-validation`, `hotfix/1.0.1`
    
![GitFlow](/Assets/chapter-6/chapter6-gitflow.png)

#### **Semantic Versioning**

El equipo aplicará **Semantic Versioning 2.0.0** para el nombrado de versiones, usando el siguiente esquema:

`MAJOR.MINOR.PATCH`

- `MAJOR`: Cambios incompatibles con versiones anteriores.
    
- `MINOR`: Nuevas funcionalidades compatibles con versiones previas.
    
- `PATCH`: Corrección de errores sin afectar la compatibilidad.
    

_Ejemplo de versión:_ `1.2.0`, `2.0.1`

Referencias: [https://semver.org/](https://semver.org/)

#### **Conventional Commits**

Para los mensajes de commit, se seguirá el estándar **Conventional Commits**, con el fin de mantener un historial claro y automatizable.

**Ejemplos de prefijos válidos:**

- `feat`: Para nuevas funcionalidades.
    
- `fix`: Para corrección de errores.
    
- `docs`: Para cambios en documentación.
    
- `style`: Cambios de formato o estilo (sin cambios de lógica).
    
- `refactor`: Reestructuración del código sin cambiar funcionalidad.
    
- `test`: Agregado/modificación de pruebas.
    
- `chore`: Tareas de mantenimiento (builds, dependencias, etc.).
    

_Ejemplo de commit:_  
`feat: add rental request flow for university students`

Referencias: [https://www.conventionalcommits.org/](https://www.conventionalcommits.org/)

### 6.1.3. Source Code Style Guide & Conventions

Esta sección detalla las guías de estilo y convenciones de codificación que seguirá el equipo para asegurar la legibilidad, coherencia y mantenibilidad del código fuente en todos los lenguajes usados. Se adoptan estándares reconocidos y nomenclatura en inglés para todos los elementos del código.

#### HTML & CSS

- Se aplicarán las guías del **Google HTML/CSS Style Guide**.
    
- Nombres de clases en CSS en **kebab-case**.
    
- Uso semántico de etiquetas HTML5.
    
- Separación clara entre estructura (HTML) y estilo (CSS).
    
- Ruta de referencia: [https://google.github.io/styleguide/htmlcssguide.html](https://google.github.io/styleguide/htmlcssguide.html)
    

#### JavaScript

- Se sigue el estándar **Airbnb JavaScript Style Guide**.
    
- Uso de **camelCase** para variables y funciones.
    
- Constantes en **UPPER_SNAKE_CASE**.
    
- Ruta de referencia: [https://github.com/airbnb/javascript](https://github.com/airbnb/javascript)
    

#### TypeScript

- Se sigue el **Google TypeScript Style Guide**.
    
- Uso de **interfaces** y tipado explícito.
    
- Archivos con una sola clase o componente.
    
- Ruta de referencia: https://google.github.io/styleguide/tsguide.html
    

#### Java (Backend con Spring Boot y DDD)

- Se aplica el **Google Java Style Guide**.
    
- Clases, métodos y atributos en inglés, utilizando **camelCase** y **PascalCase** según corresponda.
    
- El backend aplica **Domain-Driven Design (DDD)**, por lo tanto:
    
    - Las entidades y agregados seguirán principios de encapsulación y responsabilidad única.
        
    - No se utilizarán DTOs ni controladores típicos de un enfoque MVC.
        
- Se prioriza la separación de responsabilidades entre capas del dominio, aplicación e infraestructura.
    
- Ruta de referencia: https://google.github.io/styleguide/javaguide.html
    

#### Kotlin (Android)

- Se utiliza el **Kotlin Coding Conventions** oficial.
    
- Uso de **camelCase** para nombres de variables y funciones.
    
- Propiedades inmutables (`val`) por defecto.
    
- Nombres claros, concisos y en inglés.
    
- Ruta de referencia: https://kotlinlang.org/docs/coding-conventions.html
    

#### Gherkin

- Se sigue el estándar **Gherkin Conventions for Readable Specifications**.
    
- Escenarios escritos en inglés con formato: `Given`, `When`, `Then`.
    
- Archivos `.feature` organizados por funcionalidad principal.
    
- Ruta de referencia: [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/)

### 6.1.4. Software Deployment Configuration 


