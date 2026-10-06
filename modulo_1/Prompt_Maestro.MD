Eres un investigador académico, arquitecto de software y especialista senior en gestión de riesgos de Inteligencia Artificial, con experiencia en redacción de proyectos integradores universitarios, ingeniería de requisitos, arquitectura híbrida local-nube y el marco NIST AI RMF.

Tu tarea es redactar un documento académico formal, con estructura y tono de tesis universitaria, correspondiente al “Planteamiento del problema” de un proyecto integrador.

Debes analizar cuidadosamente el PDF adjunto y utilizar exclusivamente la información pertinente al Módulo 1 como fuente principal de contexto académico, lineamientos, competencias, entregables, restricciones y criterios que allí se indiquen.

No inventes requisitos, normas institucionales, datos cuantitativos, nombres de dependencias, procesos internos ni estadísticas que no estén presentes en el PDF o en el contexto proporcionado. Cuando falte una precisión institucional relevante, redacta de forma prudente usando expresiones como:

* “la institución deberá definir”
* “se propone validar con las dependencias académicas responsables”
* “sujeto a las políticas institucionales vigentes”
* “a partir de la información disponible”

No menciones que eres un modelo de IA, no expliques tu proceso interno y no incluyas frases como “según el prompt”, “como IA”, “puedo ayudarte” o “no tengo acceso”. Entrega directamente el documento final.

# 1\. Contexto obligatorio del proyecto

El proyecto consiste en diseñar y desarrollar un chatbot institucional integrado en la página web de una universidad.

Su objetivo es funcionar como asistente académico para estudiantes, permitiéndoles consultar información institucional y académica, entre ella:

* Reglamentos estudiantiles y académicos.
* Procesos académicos y administrativos relacionados con estudiantes.
* Opciones de grado.
* Horarios y orientaciones para consultar información académica.
* Procedimientos institucionales.
* Manuales, guías y documentos oficiales.
* Preguntas frecuentes de la comunidad estudiantil.
* Información académica autorizada y publicada por la universidad.

El chatbot no reemplazará decisiones humanas, asesoría jurídica, atención psicológica, calificaciones oficiales, matrículas, certificaciones, trámites formales ni decisiones académicas. Cuando no encuentre evidencia suficiente en las fuentes institucionales autorizadas, deberá informar sus límites y orientar al usuario hacia el canal institucional competente.

La arquitectura será híbrida, combinando recursos locales y en la nube, con las siguientes tecnologías obligatorias:

Frontend:

* React.

Backend:

* Node.js.
* Express.

Base de datos:

* PostgreSQL.
* Extensión pgvector para búsqueda semántica y recuperación de documentos.

Enfoque funcional esperado:

* Interfaz conversacional integrada en el sitio web institucional.
* Recuperación aumentada por generación, RAG, basada en documentos institucionales autorizados.
* Indexación semántica de documentos mediante embeddings almacenados en PostgreSQL con pgvector.
* Respuestas contextualizadas que prioricen contenido institucional verificable.
* Capacidad de indicar la fuente documental, enlace, sección o referencia institucional cuando sea técnicamente posible.
* Arquitectura híbrida: información y/o servicios sensibles podrán gestionarse localmente, mientras que determinados componentes de cómputo, modelo de lenguaje o servicios escalables podrán operar en la nube, según las políticas y decisiones de la universidad.
* Mecanismos de autenticación, autorización, trazabilidad, monitoreo, protección de datos y administración de fuentes documentales.
* Diseño orientado a seguridad, privacidad, accesibilidad, mantenibilidad y escalabilidad.

# 2\. Objetivo principal de tu respuesta

Genera un documento formal de tipo tesis que desarrolle el planteamiento del problema y los elementos de formulación inicial del proyecto, teniendo en cuenta el Módulo 1 del PDF adjunto.

El documento debe cubrir obligatoriamente:

1. Título del proyecto.
2. Introducción.
3. Planteamiento del problema y al final la pregunta de investigación.
4. Justificación.
5. Objetivo general.
6. Entre 4 y 5 objetivos específicos.
7. Usuarios y actores involucrados.
8. Alcance funcional, técnico, organizacional y de seguridad.
9. Exclusiones o límites explícitos del proyecto.
10. Requisitos funcionales.
11. Requisitos no funcionales.
12. Criterios de éxito verificables.
13. Matriz de riesgos basada en NIST AI RMF.
14. Conclusión del planteamiento.

# 3\. Reglas para analizar el PDF

Antes de redactar:

1. Identifica el nombre de la asignatura, proyecto integrador o módulo, si aparece.
2. Identifica los resultados de aprendizaje, competencias, entregables, restricciones, rúbricas, productos esperados o lineamientos relacionados con el Módulo 1.
3. Integra esos elementos al documento sin copiarlos innecesariamente de forma literal.
4. Si el PDF contiene una estructura obligatoria, respétala y adapta los apartados solicitados a ella.
5. Si existen contradicciones entre este prompt y el PDF, prioriza el PDF para los requerimientos académicos del Módulo 1, excepto las tecnologías obligatorias del proyecto: React, Node.js con Express, PostgreSQL y pgvector.
6. No incluyas contenido de módulos posteriores salvo que sea indispensable para comprender el alcance inicial del Módulo 1.

# 4\. Estilo de redacción

Redacta en español académico formal, claro, coherente, objetivo y profesional.

Usa tercera persona y redacción impersonal cuando sea posible. Ejemplos:

* “Se identifica la necesidad de…”
* “La institución enfrenta el desafío de…”
* “Se propone el desarrollo de…”
* “El sistema permitirá…”

Evita:

* Lenguaje promocional.
* Afirmaciones absolutas no verificables.
* Párrafos excesivamente largos.
* Repeticiones.
* Jerga técnica sin explicación.
* Listas vagas como “rápido, seguro y moderno” sin convertirlas en requisitos verificables.
* Inventar porcentajes de mejora o reducción de tiempos.
* Confundir un chatbot informativo con un sistema transaccional oficial.

El resultado debe parecer redactado para una tesis, anteproyecto o documento de proyecto integrador universitario.

# 5\. Estructura obligatoria de salida

Utiliza exactamente los siguientes encabezados principales, con numeración:

# Título del proyecto

# 1\. Introducción

# 2\. Planteamiento del problema

En este apartado:

* Explica la dispersión potencial de la información institucional.
* Describe las dificultades que enfrenta un estudiante al buscar reglamentos, procedimientos, horarios, manuales, opciones de grado y procesos académicos.
* Expón las consecuencias de la consulta en fuentes no oficiales, información desactualizada, demoras de atención y sobrecarga de dependencias administrativas.
* Explica por qué un chatbot con RAG y fuentes institucionales puede mitigar el problema sin sustituir los canales humanos ni los trámites formales.
* Relaciona el problema con la necesidad de trazabilidad, actualización documental, privacidad, seguridad y calidad de las respuestas.

# 3\. Justificación

La justificación debe considerar:

* Relevancia para estudiantes.
* Impacto en la experiencia de consulta de información académica.
* Centralización lógica y recuperación semántica de fuentes documentales.
* Disminución de respuestas inconsistentes derivadas de fuentes no oficiales.
* Apoyo a dependencias académicas y administrativas, sin reemplazarlas.
* Viabilidad técnica mediante React, Node.js/Express, PostgreSQL y pgvector.
* Pertinencia de una arquitectura híbrida local-nube.
* Importancia de privacidad, seguridad, accesibilidad, transparencia y supervisión humana.

# 4\. Objetivos

## 4.1 Objetivo general

Debe iniciar con un verbo en infinitivo y describir el propósito global del sistema.

## 4.2 Objetivos específicos

Formula entre 4 y 5 objetivos específicos. Deben ser medibles, realizables y coherentes con el alcance del Módulo 1.

Deben incluir, cuando corresponda:

* Levantamiento y clasificación de fuentes documentales institucionales autorizadas.
* Diseño de la arquitectura híbrida.
* Desarrollo de interfaz en React.
* Desarrollo de API backend con Node.js y Express.
* Implementación de PostgreSQL con pgvector para recuperación semántica.
* Validación de calidad de respuestas, seguridad, experiencia de usuario y trazabilidad.

# 5\. Usuarios y actores involucrados

Incluye una tabla con estas columnas:

| Actor o usuario | Necesidad o interés | Interacción con el sistema | Nivel de acceso o responsabilidad |

Considera como mínimo:

* Estudiantes de pregrado y posgrado.
* Aspirantes, si aplica de acuerdo con el alcance.
* Personal administrativo académico.
* Dependencias académicas responsables de la información.
* Administradores del sistema.
* Equipo de desarrollo.
* Área de tecnologías de información.
* Responsable de protección de datos, seguridad o gobierno de IA, si existe o si debe ser designado.
* Docentes o coordinadores académicos, cuando su rol sea pertinente.

Distingue claramente entre:

* Usuario final.
* Dueño de contenido.
* Administrador técnico.
* Responsable de gobierno y riesgo.
* Responsable de validación académica.

# 7\. Alcance del proyecto

Divide este apartado así:

## 7.1 Alcance funcional

Detalla funcionalidades incluidas, tales como:

* Consulta conversacional de documentos institucionales aprobados.
* Búsqueda semántica mediante pgvector.
* Recuperación de fragmentos documentales relevantes.
* Respuestas con advertencia o derivación cuando no exista evidencia suficiente.
* Visualización de referencias, fuentes o enlaces cuando estén disponibles.
* Panel o mecanismo administrativo para gestionar fuentes documentales, si es coherente con el PDF.
* Registro de consultas, eventos y errores con protección de datos.
* Escalamiento a canales humanos o institucionales.

## 7.2 Alcance técnico

Explica de manera concreta:

* React como interfaz web.
* Node.js y Express como backend/API.
* PostgreSQL como base de datos relacional.
* pgvector para vectores y similitud semántica.
* Patrón RAG para recuperar contenido institucional antes de generar respuestas.
* Arquitectura híbrida: separación de componentes locales y en nube según sensibilidad, costo, disponibilidad y políticas institucionales.
* API segura y mecanismos de autenticación/autorización.
* Registro, monitoreo y observabilidad.
* Gestión de versiones y actualización de documentos.
* Estrategias generales de respaldo y recuperación.

## 7.3 Alcance organizacional

Explica cómo se integrará el proyecto con:

* La página institucional.
* Responsables de contenido.
* Dependencias académicas.
* Procesos de validación y actualización documental.
* Canales de atención humana existentes.

## 7.4 Alcance de seguridad y privacidad

Incluye:

* Principio de mínimo privilegio.
* Control de acceso por roles.
* Cifrado en tránsito.
* Protección de credenciales y secretos.
* Registro de auditoría.
* Minimización de datos personales.
* Políticas de retención y anonimización de conversaciones, sujetas a normatividad institucional.
* Protección frente a ataques de prompt injection.
* Restricción del chatbot a fuentes documentales aprobadas.
* Revisión humana de contenidos críticos o ambiguos.

# 8\. Exclusiones y limitaciones

Define explícitamente lo que el sistema NO hará. Incluye, como mínimo:

* No emitirá decisiones académicas oficiales.
* No realizará matrículas, pagos, modificaciones de notas ni trámites transaccionales.
* No reemplazará a funcionarios, asesores académicos ni dependencias institucionales.
* No dará asesoría legal, médica, psicológica o financiera.
* No garantizará exactitud cuando las fuentes oficiales estén ausentes, ambiguas o desactualizadas.
* No utilizará información personal sensible para entrenar modelos sin autorización institucional expresa.
* No expondrá documentos internos, confidenciales o restringidos.
* No accederá a sistemas institucionales sensibles sin integración autorizada y controles de seguridad.
* No podrá considerar completadas funciones no contempladas en el Módulo 1 del PDF.

# 9\. Requisitos del sistema

## 9.1 Requisitos funcionales

Presenta una tabla con las siguientes columnas:

| Código | Requisito funcional | Descripción | Prioridad | Criterio de aceptación |

Incluye entre 10 y 15 requisitos funcionales. Usa códigos RF-01, RF-02, etc.

Como guía, considera requisitos relacionados con:

* Interfaz conversacional.
* Consulta de información institucional.
* Recuperación semántica.
* Indexación y actualización documental.
* Visualización de fuentes.
* Manejo de preguntas sin respuesta.
* Derivación a canales institucionales.
* Administración de documentos o base de conocimiento.
* Registro de auditoría.
* Gestión de usuarios y roles, si aplica.
* Integración con página institucional.
* Reporte de consultas no resueltas.
* Feedback de usuario sobre utilidad de respuestas.

Cada requisito debe ser específico, comprobable y coherente con el alcance.

## 9.2 Requisitos no funcionales

Presenta una tabla con estas columnas:

| Código | Categoría | Requisito no funcional | Métrica o condición verificable | Prioridad |

Incluye entre 12 y 18 requisitos no funcionales con códigos RNF-01, RNF-02, etc.

Cubre al menos estas categorías:

* Rendimiento.
* Disponibilidad.
* Escalabilidad.
* Seguridad.
* Privacidad.
* Usabilidad.
* Accesibilidad.
* Mantenibilidad.
* Observabilidad.
* Confiabilidad.
* Trazabilidad.
* Compatibilidad.
* Calidad de respuesta.
* Recuperación ante fallos.
* Gestión de cambios.
* Interoperabilidad.
* Ética y transparencia de IA.

No inventes valores excesivamente específicos sin base. Cuando sea necesario, utiliza valores objetivo razonables señalados como “a validar durante las pruebas” o “según los acuerdos de nivel de servicio institucionales”.

# 10\. Criterios de éxito

Presenta una tabla con estas columnas:

| Código | Criterio de éxito | Indicador o evidencia | Meta o condición de cumplimiento | Método de validación |

Incluye entre 8 y 12 criterios.

Los criterios deben evaluar:

* Cobertura de documentos institucionales priorizados.
* Capacidad de recuperación de información relevante.
* Calidad factual y trazabilidad de respuestas.
* Porcentaje de respuestas con fuente cuando aplique.
* Manejo correcto de preguntas no respondibles.
* Ausencia de exposición de información no autorizada en pruebas.
* Usabilidad y satisfacción de usuarios piloto.
* Disponibilidad o estabilidad durante pruebas.
* Rendimiento de las consultas.
* Registro de eventos relevantes.
* Cumplimiento de requisitos de accesibilidad definidos.
* Validación de seguridad básica y protección contra prompt injection.

No presentes métricas como hechos logrados. Preséntalas como objetivos, umbrales de aceptación o metas sujetas a validación en pruebas.

# 11\. Matriz de riesgos NIST AI RMF

Elabora una matriz de riesgos basada en NIST AI RMF. Usa las funciones:

* GOVERN: gobierno, políticas, roles, responsabilidades, documentación y supervisión.
* MAP: contexto, usuarios, fuentes, impactos, límites del sistema y riesgos identificados.
* MEASURE: evaluación, pruebas, métricas, monitoreo y verificación de riesgos.
* MANAGE: priorización, tratamiento, mitigación, respuesta y seguimiento continuo.

Antes de la tabla, incluye un párrafo breve explicando que la matriz adapta el enfoque NIST AI RMF al contexto de un chatbot académico universitario con arquitectura híbrida y recuperación aumentada por generación.

Luego presenta una tabla con estas columnas exactas:

| ID | Riesgo | Función NIST AI RMF | Causa o escenario | Probabilidad | Impacto | Nivel de riesgo inherente | Controles preventivos | Controles de detección | Plan de tratamiento o respuesta | Riesgo residual | Responsable |

Incluye entre 12 y 16 riesgos y utiliza códigos R-01, R-02, etc.

Incluye, como mínimo, los siguientes riesgos:

1. Alucinaciones o generación de respuestas no sustentadas en documentos institucionales.
2. Uso de documentos desactualizados, duplicados o no aprobados.
3. Exposición de datos personales, conversaciones o información sensible.
4. Prompt injection o manipulación de instrucciones del chatbot.
5. Acceso no autorizado al panel administrativo, documentos o registros.
6. Sesgo o trato desigual hacia grupos de usuarios.
7. Respuestas ambiguas sobre reglamentos, sanciones, derechos u obligaciones.
8. Indisponibilidad de componentes locales o de nube.
9. Dependencia o cambios en servicios externos, modelos o proveedores de nube.
10. Errores de indexación, embeddings o recuperación semántica con pgvector.
11. Falta de trazabilidad, evidencia documental o explicabilidad de las respuestas.
12. Uso indebido del chatbot para solicitudes fuera de su alcance o búsqueda de asesoría sensible.
13. Falta de actualización y gobernanza del conocimiento institucional.
14. Incumplimiento de obligaciones institucionales de privacidad, retención o protección de datos.
15. Vulnerabilidades en la API, base de datos, dependencias o integración con el sitio institucional.
16. Sobreconfianza de usuarios en respuestas generadas por el chatbot.

Para cada riesgo:

* Define probabilidad como Baja, Media o Alta.
* Define impacto como Bajo, Medio, Alto o Crítico.
* Clasifica el riesgo inherente y residual como Bajo, Medio, Alto o Crítico.
* Propón controles realistas y específicos.
* Asigna un responsable genérico apropiado, por ejemplo: Administrador de plataforma, Área TI, Responsable de contenidos, Oficial de protección de datos, Comité de gobierno de IA, Equipo de desarrollo o Dependencia académica responsable.
* Asegura coherencia entre riesgo, controles, respuesta y responsable.

Al final de la matriz, agrega una breve priorización de los cinco riesgos más relevantes para una primera versión del sistema y justifica cada prioridad en una línea.

# 12\. Propuesta tecnológica de alto nivel

Incluye una explicación breve y académica de la arquitectura propuesta, sin convertirla en un manual de implementación.

Explica el flujo general:

1. El estudiante formula una pregunta desde la interfaz React integrada al sitio institucional.
2. El frontend envía la solicitud a una API construida en Node.js con Express.
3. El backend aplica validaciones, controles de seguridad, gestión de sesión y filtrado de solicitudes.
4. El sistema consulta PostgreSQL y pgvector para recuperar fragmentos relevantes de documentos institucionales autorizados.
5. El componente de generación elabora una respuesta fundamentada prioritariamente en el contexto recuperado.
6. La respuesta se entrega con referencias, advertencias de alcance o derivación a atención humana cuando corresponda.
7. Se almacenan registros técnicos y de auditoría respetando las políticas de minimización, retención y protección de datos.
8. Los documentos y vectores se actualizan mediante un proceso controlado, validado y trazable.

Describe claramente la arquitectura híbrida:

* Componentes potencialmente locales: base de conocimiento institucional sensible, PostgreSQL/pgvector, registros de auditoría, control de acceso y documentos restringidos.
* Componentes potencialmente en la nube: servicios de inferencia, escalamiento, monitoreo, almacenamiento no sensible o herramientas administradas, según evaluación de riesgos y políticas institucionales.
* Principio de decisión: los datos sensibles y los componentes críticos deben mantenerse o procesarse conforme a la clasificación de información, requisitos legales, disponibilidad, presupuesto y controles de seguridad definidos por la universidad.

# 13\. Conclusión

Redacta una conclusión de 2 a 4 párrafos que:

* Sintetice el problema.
* Reafirme la pertinencia del chatbot institucional.
* Destaque que la solución se basa en documentos institucionales verificables y no en generación libre sin control.
* Subraye el equilibrio entre innovación, seguridad, privacidad, supervisión humana y calidad de la información.
* Señale que los requisitos, alcance, riesgos y criterios de éxito servirán como base para las siguientes etapas del proyecto.

# 6\. Criterios de calidad antes de entregar

Antes de finalizar, revisa que:

* El documento esté completamente redactado en español.
* Se haya tenido en cuenta el Módulo 1 del PDF adjunto.
* Existan todas las secciones solicitadas.
* Las tablas sean legibles en Markdown.
* Los requisitos estén codificados y sean verificables.
* La matriz NIST AI RMF incluya entre 12 y 16 riesgos.
* Los criterios de éxito sean verificables y no afirmaciones sin evidencia.
* Se diferencie claramente entre alcance y exclusiones.
* Se reflejen React, Node.js con Express, PostgreSQL y pgvector.
* Se explique la arquitectura híbrida local-nube.
* Se mencione RAG como enfoque de recuperación de documentos institucionales.
* Se incluyan controles para alucinaciones, datos desactualizados, privacidad, prompt injection, sesgo, seguridad, indisponibilidad y trazabilidad.
* El tono sea el de un documento académico formal.
* No se agreguen referencias bibliográficas ficticias.
* No se usen datos, cifras ni nombres institucionales no suministrados por el usuario o el PDF.

