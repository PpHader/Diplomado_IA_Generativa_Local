# **PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA** 

Diplomado en Inteligencia Artificial Generativa 

**Institución:** Corporación Universitaria Comfacauca - Unicomfacauca 

#### **Programa / Asignatura: Opción de grado** 

Diplomado en Inteligencia Artificial Generativa] 

**Docentes:** 

#### **Integrantes:** 

- Hader Jose Vargas Mejia (Encargado del Backend) 

- Sergio Andres Quintero (Encargado del Frontend) 

**Fecha:** 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

## **TABLA DE CONTENIDO** 

## **Contenido** 

|1. Introducción...............................................................................................................................2|
|---|
|2. Planteamiento del Problema.....................................................................................................2|
|3. Justificación...............................................................................................................................3|
|4. Objetivos del Proyecto...............................................................................................................4|
|4.1 Objetivo general...................................................................................................................4|
|4.2 Objetivos específicos...........................................................................................................5|
|5. Usuarios y actores involucrados................................................................................................5|
|6. Alcance del proyecto................................................................................................................. 6|
|6.1 Alcance funcional.................................................................................................................6|
|6.2 Alcance técnico.................................................................................................................... 6|
|6.3 Alcance organizacional........................................................................................................7|
|6.4 Alcance de seguridad y privacidad......................................................................................7|
|7. Equipo de trabajo y roles...........................................................................................................7|
|8. Exclusiones y limitaciones.........................................................................................................7|
|9. Requisitos del sistema...............................................................................................................7|
|9.1 Requisitos funcionales.........................................................................................................7|
|9.2 Requisitos no funcionales..................................................................................................10|
|10. Criterios de Éxito................................................................................................................... 10|
|11. Matriz de riesgos NIST AI RMF.............................................................................................11|
|12. Propuesta Tecnológica de Alto Nivel.....................................................................................13|
|12.1 Flujo de datos y arquitectura RAG...................................................................................13|
|12.2 Modelo de lenguaje local.................................................................................................14|
|12.3 Despliegue e infraestructura híbrida................................................................................14|
|13. Conclusión............................................................................................................................. 15|



1 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

## **1. Introducción** 

La inteligencia artificial generativa ha adquirido una importancia creciente en diferentes áreas de la educación superior, especialmente en aquellas relacionadas con la consulta, organización y gestión de información. Sin embargo, la incorporación de modelos de lenguaje en contextos universitarios requiere mecanismos que permitan controlar las fuentes utilizadas, reducir la generación de información no sustentada y mantener la trazabilidad de las respuestas. 

En este contexto, el presente proyecto propone el diseño y desarrollo de un asistente conversacional académico institucional, orientado a facilitar la consulta de información oficial por parte de los estudiantes mediante una interfaz web integrada al portal institucional. El sistema utilizará el enfoque Retrieval-Augmented Generation (RAG), mediante el cual las consultas de los usuarios serán relacionadas semánticamente con información contenida en documentos institucionales autorizados antes de generar una respuesta. 

La solución se plantea mediante una arquitectura híbrida local-nube, cuya distribución de componentes será definida de acuerdo con criterios de seguridad, privacidad, disponibilidad, rendimiento y sensibilidad de la información. De esta manera, se busca establecer un esquema de procesamiento que permita mantener bajo control institucional aquellos datos y componentes que lo requieran, mientras que los servicios externos podrán utilizarse únicamente cuando sean compatibles con las políticas y condiciones de seguridad establecidas. 

El proyecto contempla el uso de tecnologías como React para la interfaz conversacional, Node.js con Express para los servicios backend, y PostgreSQL con pgvector para el almacenamiento y recuperación semántica de información. Para el procesamiento de lenguaje natural y la orquestación del patrón RAG, el sistema se apoyará en AnythingLLM y en un motor de inferencia local con Ollama (Gemma 3). Asimismo, se incorporarán mecanismos de citación de fuentes, control de acceso, trazabilidad, manejo de consultas sin evidencia suficiente y derivación hacia canales institucionales cuando la respuesta del sistema no sea suficiente. 

De esta manera, el proyecto busca desarrollar un prototipo funcional y evaluable que facilite el acceso a información académica institucional, reduzca la dependencia de fuentes no oficiales y permita estudiar la aplicación de técnicas de RAG bajo criterios de seguridad, privacidad y gobernanza de la inteligencia artificial. 

## **2. Planteamiento del Problema** 

La información académica, administrativa e institucional de las universidades suele encontrarse distribuida entre diferentes medios y documentos, como portales web, reglamentos, manuales, procedimientos, circulares, documentos internos y otros repositorios institucionales. Esta dispersión puede dificultar que los estudiantes localicen de manera rápida y sencilla información oficial relacionada con procesos académicos, requisitos, trámites, calendarios, reglamentos y preguntas frecuentes. 

Cuando la información requerida no se encuentra fácilmente o no existe un mecanismo centralizado de consulta, los estudiantes pueden recurrir a diferentes fuentes para resolver sus inquietudes, lo que puede generar confusión respecto a cuál información es oficial, vigente o 

2 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

aplicable a su situación. Esto también puede incrementar la necesidad de acudir a funcionarios o dependencias institucionales para resolver consultas que podrían ser atendidas mediante mecanismos de consulta automatizada. 

En este contexto, los asistentes conversacionales basados en modelos de inteligencia artificial generativa representan una alternativa para facilitar el acceso a la información institucional mediante lenguaje natural. Sin embargo, un asistente basado únicamente en un modelo generativo presenta riesgos importantes cuando se utiliza en un entorno académico. Entre estos se encuentran la generación de respuestas no sustentadas en información institucional, la utilización de información desactualizada, la ausencia de referencias que permitan verificar las respuestas y la posibilidad de revelar información que no debería estar disponible para determinados usuarios. 

Por esta razón, el desarrollo de un asistente conversacional académico requiere una arquitectura que permita controlar las fuentes de información utilizadas para generar las respuestas, recuperar contenido relevante de documentos institucionales autorizados y mantener trazabilidad sobre la información empleada. El enfoque Retrieval-Augmented Generation (RAG) permite abordar esta necesidad mediante la recuperación de información relevante desde una base documental antes de generar la respuesta del modelo. 

Adicionalmente, debido a que la solución puede involucrar información institucional que requiere diferentes niveles de protección, resulta necesario considerar una arquitectura que permita definir qué componentes y datos deben mantenerse bajo control institucional y cuáles pueden utilizar servicios externos. En este sentido, una arquitectura híbrida local-nube puede ser evaluada como alternativa para distribuir los componentes del sistema de acuerdo con criterios de seguridad, privacidad, disponibilidad y rendimiento. 

Por lo anterior, se plantea la necesidad de diseñar y desarrollar un asistente conversacional académico institucional que utilice RAG y una arquitectura híbrida, orientado a facilitar la consulta de información institucional autorizada, proporcionando respuestas fundamentadas en las fuentes recuperadas, referencias que permitan su verificación y mecanismos de advertencia o derivación hacia canales institucionales cuando no exista evidencia suficiente para responder. 

#### **Pregunta de investigación:** 

¿Cómo diseñar y desarrollar un asistente conversacional académico basado en RAG y una arquitectura híbrida local-nube que permita recuperar y utilizar información institucional autorizada de manera semántica, trazable y segura, mitigando los riesgos asociados a la generación de respuestas no sustentadas, la exposición de datos y la desactualización documental? 

## **3. Justificación** 

La dispersión de información académica e institucional dificulta que los estudiantes puedan acceder de manera rápida a contenidos oficiales relacionados con sus procesos, procedimientos, reglamentos y demás información de interés académico. Por esta razón, resulta pertinente desarrollar una herramienta que facilite la consulta de dicha información 

3 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

mediante lenguaje natural y que, al mismo tiempo, permita mantener un mayor control sobre las fuentes utilizadas para generar las respuestas. 

El desarrollo de un asistente conversacional basado en Retrieval-Augmented Generation (RAG) permite abordar esta necesidad mediante la recuperación de información relevante desde un conjunto de documentos institucionales autorizados antes de generar una respuesta. Este enfoque permite que las respuestas estén fundamentadas en contenido documental recuperado y que puedan incorporar referencias a las fuentes utilizadas, facilitando su posterior verificación por parte del usuario. 

Desde el punto de vista institucional, la propuesta puede contribuir a mejorar el acceso a la información académica y reducir la dependencia de fuentes no oficiales para resolver consultas frecuentes. Asimismo, la incorporación de mecanismos de advertencia y derivación hacia canales institucionales permitirá establecer límites al funcionamiento del asistente cuando la información disponible no sea suficiente para responder una consulta de manera adecuada. 

Desde la perspectiva tecnológica, el proyecto permitirá integrar diferentes componentes para construir un prototipo funcional de inteligencia artificial generativa. La solución contempla el uso de React para la interfaz conversacional, Node.js con Express para los servicios backend, y PostgreSQL con pgvector para almacenar y realizar la recuperación semántica de los fragmentos documentales. Además, se incorporará AnythingLLM y la ejecución local de modelos de lenguaje mediante Ollama (Gemma 3), garantizando el procesamiento privado y eficiente de la información. Esta integración permitirá abordar de manera práctica aspectos clave del desarrollo web, bases de datos vectoriales, orquestación de IA y generación aumentada por recuperación (RAG) en entornos locales. 

De igual manera, la incorporación de una arquitectura híbrida local-nube resulta pertinente debido a la necesidad de considerar diferentes niveles de sensibilidad de la información y las condiciones de procesamiento del sistema. Esta arquitectura permitirá evaluar qué componentes deben permanecer bajo control institucional y cuáles podrían utilizar servicios externos, teniendo en cuenta criterios de seguridad, privacidad, disponibilidad y rendimiento, en lugar de asumir que toda la información debe ser procesada en un único entorno. 

Finalmente, el proyecto tiene relevancia desde el punto de vista de la seguridad, privacidad y gobernanza de la inteligencia artificial, debido a que el asistente deberá contemplar mecanismos de control de acceso, trazabilidad, protección de información, gestión de fuentes autorizadas y tratamiento de consultas que se encuentren fuera de su alcance. Estos elementos permitirán que el prototipo no se limite a demostrar el funcionamiento de un chatbot, sino que también pueda ser evaluado bajo criterios técnicos y de gestión de riesgos asociados al uso de inteligencia artificial en un contexto institucional. 

## **4. Objetivos del Proyecto** 

### **4.1 Objetivo general** 

Diseñar un asistente conversacional académico basado en Retrieval-Augmented Generation (RAG) y una arquitectura híbrida local-nube, que permita a la comunidad estudiantil consultar 

4 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

información institucional autorizada de manera semántica, trazable y segura, considerando mecanismos de gobernanza de los datos y supervisión humana. 

### **4.2 Objetivos específicos** 

- Identificar las fuentes documentales institucionales autorizadas según su contenido, sensibilidad y vigencia. 

- Diseñar la arquitectura híbrida local-nube del sistema según criterios de seguridad, privacidad, disponibilidad y rendimiento. 

- Implementar la interfaz web y los servicios backend del asistente conversacional utilizando React, Node.js y Express. 

- Integrar un sistema RAG mediante AnythingLLM, PostgreSQL y pgvector para la recuperación semántica, acoplado a un motor local en Ollama (Gemma 3) para la inferencia de respuestas. 

- Evaluar el asistente mediante pruebas de recuperación, generación de respuestas, trazabilidad y seguridad. 

## **5. Usuarios y actores involucrados** 

|**Actor o usuario**||**Necesidad o**<br>**interés**|**Interacción c**<br>**sistema**|**on el**|**Nivel de acceso o**<br>**responsabilidad**|
|---|---|---|---|---|---|
|Consultar<br>información<br>académica,<br>reglamentos<br>procedimientos<br>manera rápida<br>precisa.|y<br>de<br>y|Interactúan con la<br>interfaz<br>conversacional web.|Usuario<br>Lectura<br>respuestas.|final.<br>de|Usuario<br>final.<br>Lectura<br>de<br>respuestas.|
|Personal<br>administrativo<br>académico||Responder<br>consultas frecuentes<br>y derivar casos<br>complejos.|El sistema<br>convertir la co<br>del usuario<br>embeddings<br>buscar en pgve|debe<br>nsulta<br>en<br>para<br>ctor.|Reciben alertas de<br>consultas<br>no<br>resueltas<br>o<br>escalamientos.|
|Dependencias<br>académicas<br>responsables||Mantener la vigencia<br>y exactitud de la<br>información<br>publicada.|El sistema<br>generar la resp<br>utilizando<br>exclusivamente<br>contexto<br>recuperado.|debe<br>uesta<br>el|Aprueban<br>documentos fuente y<br>revisan reportes de<br>obsolescencia.|



5 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 



<!-- Start of picture text -->
Actor o usuario Necesidad o  Interacción con el  Nivel de acceso o<br>interés sistema responsabilidad<br>Administradores del  Gestionar la  El sistema debe  Configuran<br>sistema plataforma,  mostrar el  parámetros,<br>usuarios, roles y  documento, sección  gestionan accesos y<br>configuración. o enlace de origen  monitorean el<br>de la respuesta. estado.<br>Área de tecnologías  Asegurar la  Despliegan,  Responsable de<br>de información disponibilidad,  monitorean y  infraestructura y<br>integración y  mantienen los  seguridad.<br>seguridad de la  componentes<br>infraestructura. locales y de nube.<br>Responsable de  Garantizar el  Revisan matrices de  Responsable de<br>protección de datos /  cumplimiento  riesgo, auditorías y  gobierno y riesgo.<br>Gobierno de IA normativo y la ética  políticas de<br>en el uso de la IA. retención.<br><!-- End of picture text -->

## **6. Alcance del proyecto** 

### **6.1 Alcance funcional** 

El sistema permitirá la consulta conversacional de documentos institucionales aprobados mediante búsqueda semántica. Recuperará fragmentos documentales relevantes y generará respuestas contextualizadas, visualizando las referencias, fuentes o enlaces institucionales cuando estén disponibles. En caso de no encontrar evidencia suficiente, el sistema emitirá una advertencia y facilitará el escalamiento a canales humanos. Incluirá un panel administrativo para la gestión, indexación y actualización de fuentes documentales, así como el registro de consultas, eventos y errores, respetando las políticas de protección de datos. 

### **6.2 Alcance técnico** 

La interfaz web se desarrollará en React, mientras que el backend y la API se construirán en Node.js con Express. Como entorno de desarrollo y asistencia en la codificación del producto se utilizará OpenCode. PostgreSQL actuará como base de datos relacional, extendido con pgvector para el almacenamiento de embeddings y búsquedas de similitud semántica. Para la orquestación del patrón RAG (Retrieval-Augmented Generation) y la recuperación del contenido institucional se integrará AnythingLLM, conectado a un servidor local de Ollama ejecutando el modelo Gemma 3 4B para la generación de respuestas. La arquitectura será híbrida: los componentes que manejen datos sensibles, la base de conocimiento vectorial y los registros de auditoría podrán residir en infraestructura local, mientras que los servicios de inferencia o escalabilidad podrán operar en la nube, sujeto a las políticas institucionales. Asimismo, se implementarán APIs seguras, mecanismos de autenticación, autorización y observabilidad. 

6 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

### **6.3 Alcance organizacional** 

El proyecto se integrará con la página institucional como un widget o módulo embebido. Requerirá la definición de responsables de contenido en las dependencias académicas para validar la actualización documental. El sistema se articulará con los canales de atención humana existentes, actuando como un filtro de primer nivel y un facilitador de información, sin alterar los flujos de trabajo transaccionales de la universidad. 

### **6.4 Alcance de seguridad y privacidad** 

Se aplicará el principio de mínimo privilegio y control de acceso basado en roles (RBAC). Se garantizará el cifrado en tránsito y la protección de credenciales. Se implementará la minimización de datos personales en los registros de auditoría, sujetando las políticas de retención y anonimización a la normatividad institucional. Se incluirán mecanismos de protección frente a ataques de prompt injection y se restringirá estrictamente el chatbot a las fuentes documentales aprobadas, exigiendo revisión humana para contenidos críticos. 

## **7. Equipo de trabajo y roles** 

El desarrollo del proyecto está a cargo del siguiente equipo de trabajo: 

- Hader Jose Vargas Mejia: Encargado del backend, desarrollo de servicios API, integración del motor de IA local, base de datos vectorial y lógica del servidor. 

- 

- Sergio Andres Quintero: Encargado del frontend, diseño de la interfaz conversacional, experiencia de usuario y desarrollo de componentes web en React. 

## **8. Exclusiones y limitaciones** 

El sistema NO emitirá decisiones académicas oficiales, ni realizará matrículas, pagos, modificaciones de notas o trámites transaccionales. NO reemplazará a funcionarios, asesores académicos ni dependencias institucionales. NO brindará asesoría legal, médica, psicológica o financiera. NO garantizará exactitud cuando las fuentes oficiales estén ausentes, ambiguas o desactualizadas. NO utilizará información personal sensible para entrenar modelos sin autorización institucional expresa. NO expondrá documentos internos, confidenciales o restringidos. NO accederá a sistemas institucionales sensibles sin integración autorizada. Las funciones no contempladas en los lineamientos de gobernanza del Módulo 1 no serán consideradas. 

7 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

## **9. Requisitos del sistema** 

### **9.1 Requisitos funcionales** 

|**Código**|**Requisito**<br>**funcional**|**Descripción**|**Prioridad**|**Criterio de**<br>**aceptación**|
|---|---|---|---|---|
|RF-01|Interfaz<br>conversacional|El sistema debe<br>proveer una interfaz<br>web en React para<br>interacción textual.|Alta|La interfaz carga en<br>el navegador y<br>permite<br>enviar/recibir<br>mensajes.|
|RF-02|Consulta semántica|El sistema debe<br>convertir la consulta<br>del usuario en<br>embeddings para<br>buscar en pgvector.|Alta|Se recuperan los k<br>fragmentos más<br>similares según la<br>similitud coseno.|
|RF-03|Generación con<br>RAG|El sistema debe<br>generar la respuesta<br>utilizando<br>exclusivamente el<br>contexto<br>recuperado.|Alta|La respuesta no<br>contiene información<br>que no esté en los<br>fragmentos<br>recuperados.|
|RF-04|Citación de fuentes|El sistema debe<br>mostrar el<br>documento, sección<br>o enlace de origen<br>de la respuesta.|Alta|Cada respuesta<br>incluye al menos<br>una referencia<br>clicable o<br>identificable.|
|RF-05|Manejo de sin<br>respuesta|El sistema debe<br>indicar sus límites si<br>la similitud o<br>confianza es baja.|Alta|Se muestra un<br>mensaje estándar<br>derivando al canal<br>humano<br>correspondiente.|
|RF-06|Escalamiento a<br>canales|El sistema debe<br>proveer enlaces o<br>datos de contacto de<br>dependencias<br>específicas.|Media|Los enlaces de<br>escalamiento son<br>validados y<br>funcionales.|



8 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

|**Código**|**Requisito**<br>**funcional**|**Descripción**|**Prioridad**|**Criterio de**<br>**aceptación**|
|---|---|---|---|---|
|RF-07|Ingestión de<br>documentos|El panel admin debe<br>permitir cargar<br>PDFs/DOCX, así<br>como de páginas<br>web institucionales<br>autorizadas<br>mediante sus URL y<br>generar sus<br>embeddings.|Alta|El sistema permite<br>procesar un<br>documento PDF o<br>DOCX y una URL<br>institucional<br>autorizada; el<br>contenido queda<br>indexado y puede<br>recuperarse<br>mediante una<br>consulta semántica,<br>conservando la<br>referencia a su<br>fuente original.|
|RF-08|Actualización<br>documental|El sistema debe<br>permitir desactivar o<br>reemplazar<br>documentos<br>obsoletos.|Media|Los documentos<br>desactivados no se<br>recuperan en<br>nuevas consultas.|
|RF-09|Registro de auditoría|El sistema debe<br>guardar la consulta,<br>la respuesta y los<br>fragmentos<br>recuperados.|Alta|Se genera un log<br>estructurado sin<br>almacenar PII<br>innecesaria.|
|RF-10|Feedback de<br>usuario|El sistema debe<br>permitir al usuario<br>calificar la utilidad de<br>la respuesta.|Media|Existen botones de<br>'Útil' / 'No útil' que<br>actualizan el<br>registro.|
|RF-11|Reporte de no<br>resueltas|El panel admin debe<br>listar las consultas<br>donde el sistema<br>derivó a canales<br>humanos.|Media|Se genera un<br>reporte filtrable por<br>fecha y tema.|
|RF-12|Gestión de roles|El sistema debe<br>diferenciar entre<br>usuarios finales y<br>administradores de<br>contenido.|Alta|Los endpoints<br>administrativos<br>retornan 403 si el rol<br>no es autorizado.|



9 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

### **9.2 Requisitos no funcionales** 

|**Código**|**Categoría**|**Descripción**|**Prioridad**|**Criterio de**<br>**aceptación**|
|---|---|---|---|---|
|RNF-01|Seguridad|El sistema debe<br>proteger las<br>credenciales y<br>aplicar cifrado<br>HTTPS en todas las<br>transmisiones.|Alta|Todas las<br>conexiones utilizan<br>TLS 1.3 y no se<br>exponen claves en<br>código.|
|RNF-02|Privacidad|El sistema no debe<br>almacenar datos<br>personales<br>identificables (PII)<br>en los logs de<br>conversación.|Alta|Auditoría de logs<br>confirma ausencia<br>de PII o<br>enmascaramiento<br>automático.|
|RNF-03|Rendimiento|El tiempo de<br>respuesta de<br>búsqueda y<br>generación debe ser<br>adecuado para la<br>interacción fluida.|Alta|Tiempo medio de<br>respuesta < 5s en<br>condiciones<br>normales de carga.|
|RNF-04|Disponibilidad|La arquitectura<br>híbrida debe<br>mantener alta<br>disponibilidad de los<br>servicios web.|Media|Disponibilidad<br>garantizada del 99%<br>durante periodos<br>académicos lectivos.|
|RNF-05|Usabilidad|La interfaz<br>conversacional debe<br>ser accesible e<br>intuitiva para<br>cualquier estudiante.|Media|Cumplimiento de<br>pautas básicas de<br>accesibilidad WCAG<br>2.1 AA.|



## **10. Criterios de Éxito** 

|**Código**|**Criterio de éxito**|**Meta / Condición**|**Método de validación**|
|---|---|---|---|
|CE-01|Cobertura documental|100% de los documentos|Revisión de base de datos|
||institucional|del alcance inicial<br>indexados.|pgvector.|



10 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

|**Código**|**Criterio de éxito**|**Meta / Condición**|**Método de validación**|
|---|---|---|---|
|CE-02|Calidad de recuperación<br>semántica|Los fragmentos correctos<br>en el top 3 de resultados.|Evaluación con dataset de<br>prueba manual.|
|CE-03|Trazabilidad factual con<br>citas|> 95% de respuestas<br>exitosas incluyen<br>referencia.|Análisis de logs de<br>auditoría.|
|CE-04|Manejo correcto de límites|100% de preguntas fuera<br>de contexto derivan a<br>humano.|Pruebas con prompts<br>adversariales.|
|CE-05|Seguridad y protección de<br>datos|0 exposiciones en<br>pruebas y red teaming.|Auditoría de seguridad y<br>pruebas de inyección.|
|CE-06|Satisfacción de usuarios|> 80% de calificaciones<br>positivas en pruebas.|Análisis de feedback de<br>usuarios.|
|CE-07|Estabilidad del sistema|Sin caídas críticas del<br>backend o base de datos.|Monitoreo de logs y<br>observabilidad.|
|CE-08|Rendimiento y latencia|Respuestas en tiempo<br>aceptable para el usuario.|Pruebas de carga y<br>medición de tiempos.|
|CE-09|Accesibilidad web|Navegación completa sin<br>uso de ratón.|Auditoría con lectores de<br>pantalla.|
|CE-10|Gubernanza y<br>cumplimiento|Matriz NIST AI RMF<br>completa y aprobada.|Revisión por comité de<br>gobierno de IA.|



## **11. Matriz de riesgos NIST AI RMF** 

La siguiente matriz adapta el enfoque del NIST AI Risk Management Framework (AI RMF) al contexto de un chatbot académico universitario con arquitectura híbrida y RAG. Las funciones GOVERN, MAP, MEASURE y MANAGE estructuran la identificación, evaluación y tratamiento de los riesgos asociados a la generación de lenguaje natural, la recuperación de documentos y la interacción con usuarios finales. 

11 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

|**ID**|**Riesgo / Escenario**|**Función NIST**|**Nivel**|**Control preventivo /**<br>**Tratamiento**|
|---|---|---|---|---|
|R-01|Alucinaciones o<br>respuestas no<br>sustentadas|MEASURE|Alto|Forzar System Prompt<br>estricto con contexto<br>RAG.|
|R-02|Documentos<br>desactualizados u<br>obsoletos|MANAGE|Alto|Flujo de aprobación y<br>retiro inmediato de<br>versiones.|
|R-03|Exposición de datos<br>personales o PII|GOVERN|Alto|Clasificación previa,<br>filtros de PII y<br>minimización de logs.|
|R-04|Prompt injection o<br>ataques de extracción|MEASURE|Alto|Sanitización de<br>entradas y separación<br>estricta de contextos.|
|R-05|Acceso no autorizado<br>al panel admin|GOVERN|Alto|Autenticación robusta,<br>MFA y RBAC estricto.|
|R-06|Sesgo o trato desigual<br>en respuestas|MAP|Medio|Selección cuidadosa<br>de fuentes y<br>evaluación de salidas.|
|R-07|Respuestas ambiguas<br>sobre normativas|MAP|Alto|Instrucciones de no<br>interpretar normas,<br>solo citarlas.|
|R-08|Indisponibilidad de<br>componentes locales|MANAGE|Alto|Monitoreo de salud y<br>planes de<br>contingencia en<br>servidor.|
|R-09|Dependencia de<br>modelos o<br>herramientas|GOVERN|Medio|Uso de modelos<br>locales abiertos<br>(Gemma 3) en<br>Ollama.|
|R-10|Errores de indexación<br>y chunking|MEASURE|Medio|Configuración<br>validada de overlap y<br>pruebas de<br>recuperación.|
|R-11|Falta de trazabilidad<br>documental|GOVERN|Medio|Exigencia de<br>metadatos de fuente<br>en cada respuesta<br>generada.|



12 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

|**ID**|**Riesgo / Escenario**|**Función NIST**|**Nivel**|**Control preventivo /**<br>**Tratamiento**|
|---|---|---|---|---|
|R-12|Uso indebido fuera de<br>alcance académico|MAP|Alto|Detección de<br>intenciones y<br>redirección a canales<br>institucionales.|
|R-13|Falta de gobernanza<br>del conocimiento|GOVERN|Alto|Asignación formal de<br>dueños de contenido<br>por dependencia.|
|R-14|Incumplimiento de<br>retención de datos|GOVERN|Alto|Políticas automáticas<br>de purga de logs y<br>auditoría.|
|R-15|Vulnerabilidades en<br>dependencias<br>software|MANAGE|Alto|Escaneo periódico de<br>paquetes en CI/CD y<br>parcheo.|
|R-16|Sobreconfianza del<br>usuario en la IA|MAP|Alto|Disclaimers visibles<br>en interfaz y tono<br>cauteloso.|



Priorización de riesgos para la primera versión: 

- **R-01 (Alucinaciones):** Crítico para la credibilidad institucional; se mitigará con RAG estricto. 

- **R-03 (Exposición de PII):** Riesgo legal y ético alto; requiere control preventivo en la ingestión. 

- **R-04 (Prompt Injection):** Amenaza de seguridad directa; requiere sanitización y pruebas de red teaming. 

- **R-07 (Ambigüedad en reglamentos):** Impacto directo en los derechos de los estudiantes; requiere derivación humana. 

- **R-13 (Falta de gobernanza):** Riesgo organizacional; sin dueños de contenido, el sistema se volverá obsoleto rápidamente. 

## **12. Propuesta Tecnológica de Alto Nivel** 

La arquitectura propuesta se fundamenta en un flujo de datos controlado, gobernable y modular. Para el desarrollo del software se utilizará OpenCode como entorno asistido de codificación, estructurando la solución en las siguientes capas técnicas y operativas: 

### **12.1 Flujo de datos y arquitectura RAG** 

- **Interfaz de usuario** : El estudiante formula una pregunta desde la interfaz conversacional desarrollada en React, diseñada para integrarse de manera embebida en el sitio web institucional. 

13 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

- **Servicios backend y seguridad** : El frontend envía la solicitud de manera segura a una API construida en Node.js con Express. El backend aplica validaciones de entrada, controles de acceso, gestión de sesión y filtrado de solicitudes para mitigar riesgos de inyección y garantizar el uso adecuado de los recursos. 

- **Recuperación semántica (Vector Search)** : El backend interactúa con el ecosistema de orquestación RAG gestionado por AnythingLLM, el cual consulta la base de datos PostgreSQL mediante la extensión pgvector. Allí se realiza una búsqueda por similitud semántica para recuperar los fragmentos de texto más relevantes provenientes de documentos institucionales autorizados y páginas web institucionales previamente indexadas. 

- **Construcción del contexto e inferencia** : AnythingLLM estructura un prompt enriquecido que combina la pregunta del usuario, las reglas de comportamiento del sistema y los fragmentos recuperados de la base de conocimiento. Este contexto se envía al modelo de lenguaje procesado localmente mediante Ollama. 

- **Generación de respuestas y auditoría** : La respuesta se genera fundamentándose estrictamente en el contexto recuperado y se entrega al frontend, incluyendo referencias explícitas a las fuentes, advertencias de alcance o la derivación a canales de atención humana cuando corresponda. Simultáneamente, se almacenan registros técnicos y de auditoría respetando las políticas institucionales de minimización de datos. 

### **12.2 Modelo de lenguaje local** 

Para el componente de generación de respuestas se implementará un modelo de lenguaje de tamaño reducido (SLM) ejecutado en infraestructura local mediante el motor Ollama: 

- **Candidato principal** : Se considerará la familia Gemma 3 en su variante de 4 mil millones de parámetros (Gemma 3 4B), utilizando versiones cuantizadas para optimizar el consumo de recursos de hardware (RAM y VRAM). 

- **Criterios de evaluación** : La selección definitiva del modelo dependerá de pruebas empíricas con consultas académicas en español, evaluando la precisión semántica, el seguimiento de instrucciones, la capacidad de fundamentación en el contexto recuperado (hallucination mitigation), la latencia de respuesta y el impacto en memoria 

- **Integración** : El motor de inferencia local se conectará con el backend a través de las APIs locales de Ollama (http://localhost:11434) y la capa de orquestación de AnythingLLM. 

- **Manejo de evidencia insuficiente** : La lógica del sistema incluirá reglas y evaluaciones continuas para identificar respuestas no sustentadas en los documentos e informar al usuario de forma transparente cuando no exista evidencia suficiente para responder. 

### **12.3 Despliegue e infraestructura híbrida** 

La arquitectura es híbrida por diseño: 

- Capa Local / Privada (Soberanía de Datos): Los componentes que gestionan la base de conocimiento sensible, el motor de base de datos PostgreSQL con pgvector, el orquestador RAG, los registros de auditoría y los modelos de inferencia local con 

14 

PROYECTO INTEGRADOR: ASISTENTE CONVERSACIONAL ACADÉMICO BASADO EN RAG Y ARQUITECTURA HÍBRIDA 

Ollama se mantendrán en infraestructura local o en una nube privada institucional. Esto garantiza el control total y la soberanía sobre los datos académicos. 

- Capa de Nube / Escalabilidad: La API web, el frontend interactivo o los servicios de monitoreo y observabilidad podrán escalar en entornos de nube pública, según la evaluación de riesgos y las políticas tecnológicas de la universidad. 

## **13. Conclusión** 

El presente documento establece el planteamiento del problema y la formulación inicial para el desarrollo de un asistente conversacional académico institucional. Se identifica que la dispersión de la información y la falta de canales de consulta semántica generan fricción en la comunidad estudiantil y sobrecarga en las dependencias administrativas. La propuesta de un sistema basado en el patrón RAG aborda esta necesidad al centralizar la recuperación de información en fuentes documentales verificables y autorizadas, mitigando el riesgo de desinformación y alucinaciones propias de los modelos de lenguaje generativo. 

La solución propuesta equilibra la innovación tecnológica con la rigurosidad de la ingeniería de software y la gobernanza de la IA. Al adoptar una arquitectura híbrida local-nube, respaldada por la ejecución local de modelos de lenguaje mediante Ollama (Gemma 3), la orquestación con AnythingLLM y la persistencia en PostgreSQL con pgvector, el proyecto garantiza la trazabilidad, la privacidad y la adaptabilidad a los estrictos requisitos de soberanía de datos de la institución. El sistema no pretende sustituir el juicio humano ni los trámites formales, sino actuar como una capa de infraestructura programable que orienta, informa y deriva responsablemente. 

Los requisitos, el alcance, las exclusiones y la matriz de riesgos basada en el NIST AI RMF detallados en este documento servirán como la línea base para las siguientes etapas de desarrollo. La ejecución de esta propuesta no solo cumplirá con los objetivos académicos del diplomado, sino que proporcionará a la institución un prototipo funcional, evaluable y gobernable, sentando las bases para una adopción de la inteligencia artificial alineada con la ética, la seguridad y las necesidades reales del ecosistema universitario 

15 

