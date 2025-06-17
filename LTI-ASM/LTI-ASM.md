1. Descripción breve del software LTI, valor añadido y ventajas competitivas
Descripción breve
LTI Applicant Tracking System (ATS) es una plataforma digital diseñada para optimizar y modernizar el proceso de selección de talento en empresas de cualquier tamaño. Permite a los equipos de recursos humanos y managers gestionar ofertas de empleo, candidatos y entrevistas desde un único entorno colaborativo, sencillo y eficiente.

Valor añadido
Centralización: Unifica todas las fases del proceso de selección (publicación de vacantes, gestión de candidatos, entrevistas y seguimiento) en una única plataforma accesible.

Colaboración mejorada: Facilita la interacción y el trabajo conjunto entre recruiters y managers, agilizando la toma de decisiones y reduciendo errores de comunicación.

Automatización de tareas: Reduce la carga administrativa mediante recordatorios, envíos automáticos y gestión integrada de entrevistas y notificaciones.

Asistencia inteligente: Incorpora funcionalidades de IA (como sugerencias de candidatos o scoring automático) para acelerar la criba y el análisis de perfiles.

Interfaz intuitiva: Su diseño responsive y orientado a la experiencia de usuario permite un onboarding rápido y la adopción ágil por parte de los equipos.

Integración con portales externos: Publicación automática de vacantes en portales de empleo y sincronización de calendarios para entrevistas.

Ventajas competitivas
Ventaja competitiva	Situación actual (competidores)	Propuesta LTI
Rapidez en contrataciones	Procesos lentos y manuales; cuellos de botella frecuentes	Contrataciones hasta un 40% más rápidas gracias a la eliminación de tareas manuales y la automatización del workflow
Colaboración en tiempo real	Comunicación fragmentada por email o herramientas externas	Paneles colaborativos y notificaciones en tiempo real, centralizando la información
Automatización y reducción de errores	Tareas repetitivas gestionadas manualmente; alta probabilidad de errores	Automatización de tareas repetitivas y gestión de notificaciones, minimizando los errores humanos
Adopción sencilla	Plataformas complejas, difícil curva de aprendizaje	Interfaz intuitiva y responsive, lista para usar sin necesidad de formación avanzada
Escalabilidad e integración	Dificultad para escalar o integrar nuevas herramientas	Arquitectura modular que facilita la integración y el crecimiento del sistema

2. Explicación de las funciones principales
2.1 Panel unificado de vacantes y candidatos
Vista Kanban/pipeline: cada candidatura aparece como tarjeta y se mueve por fases definidas, facilitando la priorización visual. 

Base de datos centralizada: toda la información (CV, notas, comunicaciones) queda en un único repositorio accesible por rol y permiso, evitando duplicidades. 

Indicadores en vivo: contadores de candidatos, embudo por etapa y alertas de bloqueos permiten intervenir antes de que el proceso se ralentice. 
tacitbase.com

2.2 Colaboración en tiempo real HR ↔ Managers
Comentarios y puntuaciones compartidas directamente en la tarjeta del candidato, sin correos ni hojas de cálculo. 

Notificaciones contextuales (móvil y web) para que managers aprueben o rechacen en segundos, mejorando la velocidad de decisión. 

Diseño “chat-first” que minimiza la curva de aprendizaje y eleva la adopción — principal talón de Aquiles de muchos ATS complejos. 

2.3 Automatización e IA plug-and-play
Filtrado automático por requisitos clave y detección de duplicados en segundos, acelerando el cribado inicial. 

Scoring inteligente que aprende del feedback conjunto HR-manager, reduciendo sesgos y elevando la calidad del match. 

Workflows preconfigurados (avisos, recordatorios, programación de entrevistas) que eliminan hasta un 40 % de tareas administrativas típicas. 

3. Diagrama Lean Canvas para entender el modelo de negocio.
| Dolor actual del mercado              | Solución de LTI                                      | Beneficio medible                          |
| ------------------------------------- | ---------------------------------------------------- | ------------------------------------------ |
| **Procesos lentos (39-55 días)**      | Flujo único HR + Manager + IA                        | Objetivo **≤ 20 días** por vacante         |
| **60 % de tiempo en tareas manuales** | Automatización preconfigurada                        | **-40 %** de carga administrativa          |
| **Baja adopción por UX compleja**     | Interfaz chat-first, onboarding < 24 h               | Arranque inmediato, sin TI                 |
| **Colaboración fragmentada**          | Comentarios y decisiones en vivo en la misma tarjeta | Visibilidad total y decisiones más rápidas |
| **Sesgos y mala calidad de *match***  | Modelos ML entrenados con feedback conjunto          | Mejora continua en calidad de contratación |

4. Descripción de los 3 casos de uso principales, con el diagrama asociado a cada uno:
4.1 Crear y publicar vacante
Elemento	Detalle
Actor primario	HR Manager
Objetivo	Registrar una nueva vacante y publicarla en portales externos.
Escenario principal	

HR Manager accede al panel de LTI.

Completa título, requisitos y salario.

Selecciona portales de empleo.

Confirma y publica.

El sistema envía la oferta a los portales y la refleja en el pipeline interno.
Postcondición | Vacante visible en LTI y en los portales seleccionados.
%%{init: {'theme':'base'}}%%
flowchart TD
    HR[HR Manager] -->|Accede y crea vacante| LTI[(LTI ATS)]
    LTI -->|Publica oferta| JB[Portales de empleo]
    LTI -->|Actualiza pipeline interno| PIPE[Pipeline interno]

4.2 Evaluar candidato en colaboración HR + Manager
Elemento	Detalle
Actores primarios	HR Manager, Hiring Manager
Objetivo	Revisar, puntuar y tomar decisión sobre un candidato.
Escenario principal	

HR Manager abre la tarjeta del candidato.

Revisa CV y añade nota.

Hiring Manager recibe notificación.

Hiring Manager puntúa y comenta.

Ambos marcan “Avanzar” o “Rechazar”.
Postcondición | El candidato avanza a la siguiente fase o es descartado; registro trazable de la decisión.
%%{init: {'theme':'base'}}%%
flowchart TD
    HR[HR Manager] -->|Revisa candidato y comenta| LTI[(LTI ATS)]
    HM[Hiring Manager] -->|Puntúa y comenta| LTI
    LTI -->|Notifica decisión| PIPE[Actualiza fase de candidato]
    PIPE -->|Candidato avanza o es descartado| LTI

4.3 Programar entrevista y decisión de contratación
Elemento	Detalle
Actores primarios	HR Manager, Candidato
Objetivo	Coordinar fecha de entrevista y registrar la decisión final.
Escenario principal	

HR Manager selecciona “Programar entrevista”.

El sistema propone franjas basadas en disponibilidad.

Candidato confirma franja vía portal o correo.

Tras la entrevista, HR Manager registra feedback.

HR Manager marca “Contratar” y el sistema genera oferta.
Postcondición | Oferta enviada al candidato; vacante marcada como cubierta.
%%{init: {'theme':'base'}}%%
flowchart TD
    HR[HR Manager] -->|Programa entrevista| LTI[(LTI ATS)]
    LTI -->|Propone franjas| Candidato
    Candidato -->|Confirma franja| LTI
    LTI -->|Gestiona entrevista y recoge feedback| HR
    HR -->|Marca 'Contratar'| LTI
    LTI -->|Envía oferta y marca vacante cubierta| Candidato

5. Modelo de datos que cubra entidades, atributos (nombre y tipo) y relaciones.
Entities and Attributes (in English, for MVP)
| Entity          | Attribute       | Type     | Description                                                               |
| --------------- | --------------- | -------- | ------------------------------------------------------------------------- |
| **User**        | id              | int      | Primary key                                                               |
|                 | name            | string   | Full name                                                                 |
|                 | email           | string   | Unique email address                                                      |
|                 | role            | enum     | 'HR', 'Manager'                                                           |
|                 | created\_at     | datetime | Creation timestamp                                                        |
|                 | modified\_at    | datetime | Last modification timestamp                                               |
| **Candidate**   | id              | int      | Primary key                                                               |
|                 | name            | string   | Full name                                                                 |
|                 | email           | string   | Unique email address                                                      |
|                 | cv\_url         | string   | Link to CV or resume (URL)                                                |
|                 | created\_at     | datetime | Creation timestamp                                                        |
|                 | modified\_at    | datetime | Last modification timestamp                                               |
| **Job**         | id              | int      | Primary key                                                               |
|                 | title           | string   | Job title                                                                 |
|                 | description     | string   | Short description                                                         |
|                 | location        | string   | Location                                                                  |
|                 | status          | enum     | 'open', 'closed', 'draft'                                                 |
|                 | responsible\_id | int      | FK to User (HR/Manager responsible)                                       |
|                 | created\_at     | datetime | Creation timestamp                                                        |
|                 | modified\_at    | datetime | Last modification timestamp                                               |
| **Application** | id              | int      | Primary key                                                               |
|                 | candidate\_id   | int      | FK to Candidate                                                           |
|                 | job\_id         | int      | FK to Job                                                                 |
|                 | status          | enum     | 'applied', 'interviewing', 'discarded', 'offered', 'declined', 'accepted' |
|                 | created\_at     | datetime | Application timestamp                                                     |
|                 | modified\_at    | datetime | Last modification timestamp                                               |
| **Interview**   | id              | int      | Primary key                                                               |
|                 | application\_id | int      | FK to Application                                                         |
|                 | interviewer\_id | int      | FK to User (HR/Manager interviewer)                                       |
|                 | scheduled\_at   | datetime | Date/time of interview                                                    |
|                 | feedback        | string   | (Optional) Summary feedback                                               |
|                 | created\_at     | datetime | Creation timestamp                                                        |
|                 | modified\_at    | datetime | Last modification timestamp                                               |


Mermaid ER Diagram
erDiagram
    USER {
        int id PK
        string name
        string email
        enum role "HR or Manager"
        datetime created_at
        datetime modified_at
    }
    CANDIDATE {
        int id PK
        string name
        string email
        string cv_url
        datetime created_at
        datetime modified_at
    }
    JOB {
        int id PK
        string title
        string description
        string location
        enum status
        int responsible_id FK
        datetime created_at
        datetime modified_at
    }
    APPLICATION {
        int id PK
        int candidate_id FK
        int job_id FK
        enum status
        datetime created_at
        datetime modified_at
    }
    INTERVIEW {
        int id PK
        int application_id FK
        int interviewer_id FK
        datetime scheduled_at
        string feedback
        datetime created_at
        datetime modified_at
    }

    USER ||--o{ JOB : ""
    USER ||--o{ INTERVIEW : ""
    CANDIDATE ||--o{ APPLICATION : ""
    JOB ||--o{ APPLICATION : ""
    APPLICATION ||--o{ INTERVIEW : ""

6. Diseño del sistema a alto nivel (para LTI ATS MVP)
El sistema está compuesto por los siguientes componentes principales, cada uno con su stack tecnológico específico:

Aplicación web frontend (React):
Es la interfaz principal a la que acceden HR Managers, Managers y Candidatos. Permite crear y gestionar vacantes, inscribirse a ofertas, revisar candidatos, programar entrevistas y tomar decisiones de contratación. Todas las acciones se realizan a través de esta aplicación web, desarrollada con React.

Backend/API (Node.js + Express):
Es el componente central que gestiona toda la lógica de negocio, validación de datos y seguridad. Recibe las peticiones del frontend, las procesa, aplica las reglas de negocio y se comunica con la base de datos y servicios externos cuando es necesario. El backend está desarrollado en Node.js usando Express, y expone APIs RESTful que consume el frontend.

Base de datos (PostgreSQL):
Almacena todas las entidades clave: usuarios (con su rol), candidatos, vacantes, postulaciones y entrevistas. Cada entidad está modelada para soportar los casos de uso principales: creación y publicación de vacantes, evaluación de candidatos y programación de entrevistas. Se utiliza PostgreSQL como base de datos relacional.

Servicios externos (SendGrid, Google Calendar API):
Incluyen integraciones con sistemas de terceros como SendGrid para envío de emails (notificaciones, invitaciones), y Google Calendar API para agendar entrevistas. El backend gestiona estas integraciones mediante API estándar.

Despliegue (AWS):
Toda la infraestructura está desplegada en AWS.

El frontend se aloja en Amazon S3 y se sirve a través de Amazon CloudFront.

El backend se gestiona con AWS Elastic Beanstalk.

La base de datos utiliza Amazon RDS.

Actores:

HR Manager y Manager: Ambos pueden crear y gestionar vacantes, evaluar candidatos y participar en entrevistas, diferenciados por su rol asignado.

Candidato: Puede inscribirse a ofertas, ver el estado de sus aplicaciones y participar en entrevistas.

7. Explicación del diagrama C4 (Nivel 3 – Backend/API, MVP LTI)
El Backend/API de LTI está compuesto por los siguientes componentes principales:

API Controller Layer:
Es el punto de entrada a todo el backend. Gestiona las peticiones REST recibidas desde el frontend, valida y enruta cada solicitud al módulo correspondiente.

Authentication Service:
Encargado de la autenticación de usuarios y validación de roles, utilizando estándares modernos como JWT y Passport.

Job Management Module:
Maneja la lógica de negocio para la creación, actualización, publicación y cierre de vacantes de empleo.

Candidate Management Module:
Gestiona la información y el ciclo de vida de los candidatos en la plataforma.

Application Processing Module:
Orquesta el ciclo de vida de las postulaciones, desde que un candidato aplica hasta que se le rechaza, avanza o contrata.

Interview Scheduling Module:
Se encarga de la planificación y gestión de entrevistas, incluyendo la integración con servicios externos de calendario (por ejemplo, Google Calendar).

Notification Service:
Responsable del envío de notificaciones a los usuarios y la integración con servicios externos de correo electrónico (por ejemplo, SendGrid).

Persistence Layer (ORM/Repository):
Implementa el acceso y la persistencia de los datos principales en la base de datos PostgreSQL, desacoplando la lógica de negocio del almacenamiento.

Integraciones externas:

Email Service (SendGrid): Para el envío de notificaciones y comunicaciones.

Calendar API (Google Calendar): Para la sincronización y gestión de entrevistas.

Job Board: Para la publicación de vacantes en portales externos.

Base de datos:
Toda la información se almacena en una única base de datos relacional PostgreSQL.

Usuarios del sistema:
Los componentes interactúan indirectamente con los usuarios finales (HR Manager, Manager, Candidate) a través de la capa de controlador de API, asegurando validación, control de acceso y orquestación correcta de todas las operaciones.

Este diseño modular y desacoplado garantiza que cada parte del backend sea escalable, fácil de mantener y extensible para futuros desarrollos o integraciones.

Esquema DSL:
workspace "ATS Model" "C4 model for the Applicant Tracking System (ATS)" {
    
    model {
        // People
        user = person "Recruiter" "An HR user who uses the ATS to manage job postings and candidates."
        
        // Software System (Main product/system)
        lti = softwareSystem "LTI - Applicant Tracking System" "The main ATS application that manages job applications and the hiring process." {
            
            // Containers of the ATS
            backend = container "Backend/API" "Handles business logic and data for the ATS" "Node.js + Express" {
                // Components inside the Backend/API container
                api   = component "API Controller" "Handles incoming HTTP requests (exposes REST API endpoints)." "Express.js"
                logic = component "Business Logic" "Implements core hiring/application processing logic." "Node.js"
                repo  = component "Data Repository" "Provides data access and persistence operations." "Node.js"
            }
            frontend = container "Frontend/UI" "Allows users to interact with the ATS through a web application." "React" {
                // Components inside the Frontend/UI container
                appComponent   = component "App Component" "Root React component" "React"
                authModule     = component "Auth Module" "Handles login and user roles" "React/JS"
                jobView        = component "Job Management View" "UI for creating and listing jobs" "React/JS"
                candidateView  = component "Candidate Management View" "UI for candidate profiles" "React/JS"
                workflowView   = component "Application Workflow View" "UI for job application workflow" "React/JS"
                interviewView  = component "Interview Scheduler View" "UI for scheduling interviews" "React/JS"
                apiService     = component "API Service" "Handles communication with backend" "JS/Fetch/Axios"

                // Relationships between frontend components
                appComponent   -> authModule      "Uses"
                appComponent   -> jobView         "Uses"
                appComponent   -> candidateView   "Uses"
                appComponent   -> workflowView    "Uses"
                appComponent   -> interviewView   "Uses"
                jobView        -> apiService      "Calls"
                candidateView  -> apiService      "Calls"
                workflowView   -> apiService      "Calls"
                interviewView  -> apiService      "Calls"
                authModule     -> apiService      "Calls"
            }
            database = container "Database" "Stores persistent data for the ATS (e.g., jobs, applications, users)." "PostgreSQL"
        }
        
        // Relationships between containers
        user -> frontend "Uses the web application"
        frontend -> backend "Sends requests to the API"
        backend -> database "Reads from and writes to data store"
        
        // Internal component-level relationships within the Backend
        frontend -> api "Calls API endpoints" 
        api -> logic "Invokes business logic"
        logic -> repo "Uses for data persistence"
        repo -> database "Reads/writes data in"
    }
    
    views {
        systemContext lti {
            title "System Context Diagram"
            include *
            autolayout lr
        }
        container lti {
            title "Container Diagram"
            include *
            autolayout lr
        }
        component backend {
            title "Backend/API – Component Diagram"
            include *
            autolayout lr
        }
        component frontend {
            title "Frontend/UI – Component Diagram"
            include *
            autolayout lr
        }
        theme default
    }
}
