Práctica 2 - Implementación de CRUD y Gestión Universitaria
La práctica dos se solucionó con los siguientes cambios:

1. CRUD de Materias y Asignación a Docentes
Se agregó la relación @ManyToOne entre Materia y Docente, permitiendo la asignación de profesores a materias.

MateriaDTO incluye validaciones con @NotBlank, @NotNull y @Min para garantizar datos correctos.

Se documentaron los endpoints en MateriaController usando Swagger y validaciones con @Valid.

La entidad Persona ahora incorpora @Version para control de concurrencia en JPA.

2. CRUD de Inscripciones de Estudiantes a Materias
Se creó la entidad Inscripcion para gestionar la inscripción de estudiantes en materias.

InscripcionDTO implementa validaciones con @NotNull y @NotBlank para evitar datos incorrectos.

InscripcionServiceImpl optimiza la lógica con integración de caché Redis.

Los endpoints en InscripcionController fueron documentados con Swagger y validaciones @Valid.

3. Archivos Comunes y Configuración
GlobalExceptionHandler maneja errores centralizados en ambos módulos.

application.properties configura PostgreSQL, Redis y habilita Swagger para documentación automática.
