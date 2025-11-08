# Documento de Planificación - Iteración 3
## Sistema de Gestión para Nutricionistas

---

##  Información General

| Aspecto | Detalle |
|---------|---------|
| **Iteración** | 3 |
| **Duración** | 3 semanas |
| **Objetivo** | Implementar gestión de planes alimentarios |
| **Puntos comprometidos** | 17 puntos |

---

##  Equipo y Parejas XP

- Product Owner: [Andrea Natalia Cabra]
- Scrum Master: [Daniel Skromeda]
- Desarrolladores: [Kevin Kronbauer], [Ayelen Carla De León]

**Rotación de parejas**:
- Pareja A: [Andrea Natalia Cabra] + [Ayelen Carla De León]
- Pareja B: [Kevin Kronbauer] + [Daniel Skromeda]

---

##  Historias de Usuario Seleccionadas

| HU | Descripción | Criterios de Aceptación | Tareas Técnicas | Pareja | Puntos |
|----|-------------|------------------------|-----------------|---------|---------|
| **HU-10** | **Crear Plan Alimentario**<br><br>Como nutricionista, quiero crear planes alimentarios con título, objetivo y definir múltiples comidas para asignarlos a mis pacientes. | 1. Formulario con campos: título del plan, objetivo, fecha de creación<br>2. Secciones para cada comida: Desayuno, Colación AM, Almuerzo, Colación PM, Merienda, Cena<br>3. Cada comida es un campo de texto largo (textarea)<br>4. Todos los campos obligatorios<br>5. Botón "Guardar Plan"<br>6. Mensaje de éxito al crear<br>7. Redireccionar a lista de planes | - Crear entidad PlanAlimentario<br>- Crear PlanAlimentarioRepository<br>- Crear formulario crear-plan.html<br>- Crear PlanAlimentarioController<br>- Validaciones backend<br>- Test unitario del service<br>- Test de validaciones | **Pareja A** | 8 |
| **HU-11** | **Asignar Plan a Paciente**<br><br>Como nutricionista, quiero asignar un plan alimentario específico a un paciente con fecha de inicio para que comience a seguirlo. | 1. Desde la ficha del paciente, botón "Asignar Plan"<br>2. Seleccionar plan de una lista desplegable<br>3. Campo fecha de inicio (por defecto: hoy)<br>4. Solo puede haber 1 plan activo por paciente<br>5. Si ya tiene plan activo, mostrar advertencia<br>6. Al asignar, el plan anterior se marca como inactivo<br>7. Mensaje de éxito al asignar | - Crear entidad PlanPaciente (relación)<br>- Crear PlanPacienteRepository<br>- Formulario asignar-plan.html<br>- Lógica para desactivar plan anterior<br>- Validación de plan activo único<br>- Test de asignación<br>- Test de desactivación automática | **Pareja B** | 3 |
| **HU-12** | **Ver Plan Alimentario Activo**<br><br>Como nutricionista, quiero ver rápidamente el plan alimentario activo de un paciente para consultarlo durante la atención. | 1. En la ficha del paciente, mostrar sección "Plan Activo"<br>2. Mostrar: título, objetivo, fecha de inicio<br>3. Mostrar todas las comidas organizadas<br>4. Si no tiene plan activo, mostrar mensaje y botón "Asignar Plan"<br>5. Botón "Ver Historial de Planes" | - Método en controller para obtener plan activo<br>- Consulta en repository (plan activo por paciente)<br>- Actualizar vista ficha-paciente.html<br>- Diseño de sección plan con Bootstrap<br>- Test de consulta plan activo | **Pareja A** | 3 |
| **HU-14** | **Ver Historial de Consultas**<br><br>Como nutricionista, quiero ver todas las consultas previas de un paciente ordenadas por fecha para revisar su evolución y tratamiento. | 1. Botón "Historial de Consultas" en ficha del paciente<br>2. Mostrar tabla con: fecha, observaciones (primeras 50 caracteres)<br>3. Ordenar por fecha descendente (más reciente primero)<br>4. Botón "Ver detalle" para cada consulta<br>5. Si no hay consultas, mostrar mensaje<br>6. Botón "Nueva Consulta" y "Volver" | - Crear vista historial-consultas.html<br>- Método en ConsultaController<br>- Consulta ordenada en repository<br>- Vista detalle de consulta<br>- Tabla responsive con Bootstrap<br>- Test de ordenamiento | **Pareja B** | 3 |

**Nota**: HU-13 (Registrar Consulta) ya fue implementada en la iteración 2, por lo que HU-14 puede construir sobre esa base.

---

##  Planificación Semanal

### Semana 1 (16/12 - 22/12)
- **Lunes 16/12**: Sprint Planning + Completar test pendiente HU-05 (si aplica)
- **Pareja A**: HU-10 (Crear Plan Alimentario) - Parte 1: Entidad y formulario básico
- **Pareja B**: HU-11 (Asignar Plan) - Análisis y diseño de relaciones
- **Daily meetings**: 9:00 AM TODOS los días (10 min minimo)

### Semana 2 (23/12 - 29/12)
- **Lunes**: 
  - **Pareja A**: HU-10 - Parte 2: Validaciones y tests + HU-12 (Ver Plan Activo)
  - **Pareja B**: HU-11 - Implementación completa
- **Miércoles**: Code review cruzado de HU-11 por Pareja A
- **Jueves-Viernes**: 
  - **Ambas parejas**: HU-14 (Historial de Consultas)
- **Viernes**: Testing cruzado (cada pareja prueba las HU de la otra)

### Semana 3 (30/12 - 05/01)
- **Lunes-Martes**: Integración final y corrección de bugs
- **Miércoles**: Testing completo del sistema (todas las iteraciones)
- **Jueves 02/01**: Sprint Review - Demostración al PO (10:00 AM)
- **Viernes 05/01**: Retrospectiva y cierre (10:00 AM)

---

##  Definition of Done

Una HU está **TERMINADA** cuando:
1. ✅ Código implementado y funciona correctamente
2. ✅ Al menos 2 tests unitarios escritos y pasando (casos positivo y negativo)
3. ✅ Code review aprobado por otra pareja
4. ✅ Validaciones de formulario (frontend y backend)
5. ✅ Integrado en rama main sin conflictos
6. ✅ Probado manualmente por integrante de la otra pareja
7. ✅ Documentación de código (comentarios en métodos complejos)
8. ✅ Sin warnings en consola del navegador

---

##  Objetivos de Mejora

Basados en retrospectiva 2:

1. **Tests más completos**: Incluir casos edge y negativos
2. **Daily meetings obligatorias**: 9:00 AM sin excepciones
3. **Pull frecuente**: Mínimo 2 veces al día
4. **Testing cruzado**: Cada pareja prueba las HU de la otra
5. **Respetar timebox**: 3 semanas estrictas

---

##  Stack Técnico

- **Backend**: Spring Boot, Spring Data JPA
- **Frontend**: Thymeleaf, Bootstrap 5
- **Base de datos**: MySQL 8.1
- **Testing**: JUnit 5, Mockito
- **Control de versiones**: Git/GitHub

---

##  Notas Importantes

- **Commits**: Mensajes descriptivos (ej: "Crear entidad PlanAlimentario con todas las comidas")
- **Branches**: Crear rama por cada HU (ej: `feature/hu-10-crear-plan-alimentario`)
- **Pull Requests**: 
  - Título claro con número de HU
  - Descripción de qué se implementó
  - Asignar a revisor de la otra pareja
  - No mergear sin aprobación
- **Plan Activo**: Solo puede haber 1 plan con activo=true por paciente

---

##  Riesgos Identificados

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| HU-10 es la más grande (8 pts) y puede retrasar | Media | Alto | Dividir en subtareas claras, comenzar desde día 1 |
| Lógica de desactivar plan anterior puede tener bugs | Media | Alto | Tests exhaustivos, code review detallado |
| Feriados de fin de año (menos disponibilidad) | Alta | Medio | Planificar trabajo extra en semana 1 y 2 |
| Campos de texto largo pueden tener problemas de BD | Baja | Medio | Definir bien el tipo de columna desde el inicio |
| Relación muchos a muchos puede ser compleja | Media | Medio | Pair programming en HU-11, revisar documentación JPA |

---

## Velocity de Referencia

- **Iteración 1 (Setup)**: 7 tareas completadas
- **Iteración 2**: 17 puntos completados
- **Compromiso Iteración 3**: 17 puntos

---

**Fecha de inicio**: 16/12/2025  
**Fecha de finalización**: 05/01/2026  
**Sprint Review**: 02/01/2026 - 10:00 AM  
**Retrospectiva**: 05/01/2026 - 10:00 AM

---
