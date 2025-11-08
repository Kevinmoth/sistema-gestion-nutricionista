# Retrospectiva - Iteración 3
## Sistema de Gestión para Nutricionistas

---

##  Información

| Aspecto | Detalle |
|---------|---------|
| **Iteración** | 3 |
| **Fecha** | 05/01/2026 |
| **Participantes** | Todo el equipo (4 personas) |
| **Duración reunión** | 1 hora 45 min |

---

## Cumplimiento de los Objetivos

| Historia de Usuario | Puntos | Estado | Observaciones |
|---------------------|--------|--------|---------------|
| HU-10: Crear Plan Alimentario | 8 | ✅ Completado | Formulario largo pero bien organizado |
| HU-11: Asignar Plan a Paciente | 3 | ✅ Completado | Lógica de desactivación funciona bien |
| HU-12: Ver Plan Alimentario Activo | 3 | ✅ Completado | Visualización clara y profesional |
| HU-14: Ver Historial de Consultas | 3 | ✅ Completado | Tabla ordenada correctamente |

**Resultado**: 17/17 puntos completados (100% funcional, 100% según DoD)

---

##  Qué salió bien?

1. **Cumplimos al 100% con el Definition of Done**
   - Todas las HU tienen tests completos (casos positivos y negativos)
   - Code reviews fueron exhaustivos y constructivos
   - Testing cruzado detectó 3 bugs antes del Sprint Review

2. **HU-10 se manejó bien a pesar de ser la más grande**
   - La división en tareas fue acertada
   - Pair programming ayudó a mantener el enfoque
   - El formulario quedó intuitivo a pesar de tener muchos campos

3. **Las daily meetings diarias siguen siendo efectivas**
   - 15/15 reuniones realizadas (95% asistencia)
   - Formato de 10 minutos funciona perfecto
   - Se resolvieron impedimentos el mismo día

4. **La rotación de parejas sigue enriqueciendo al equipo**
   - Andrea y Ayelen trabajaron muy bien en HU-10
   - Kevin y Daniel resolvieron la lógica compleja de HU-11 eficientemente
   - Todos aportaron ideas valiosas

5. **La gestión de Git mejoró aún más**
   - Solo 1 conflicto menor en toda la iteración
   - 58 commits bien distribuidos
   - Mensajes de commit muy descriptivos

6. **La funcionalidad de planes quedó robusta**
   - La lógica de desactivar plan anterior funciona sin bugs
   - Solo 1 plan activo por paciente se cumple correctamente
   - Los campos TEXT en BD funcionaron sin problemas

7. **El sistema ya tiene valor real**
   - El PO (Andrea) puede gestionar pacientes completamente
   - Puede hacer seguimiento con consultas
   - Puede crear y asignar planes personalizados
   - Es un MVP funcional! 

---

##  ¿Qué mejorar?

| Problema Identificado | Impacto | Solución Propuesta | Responsable | Plazo |
|----------------------|---------|-------------------|-------------|--------|
| HU-10 tomó 2 días más de lo estimado | Medio | Para HU grandes (+5 pts) | Daniel (SM) | Planning futuras |
| Feriados afectaron disponibilidad en semana 3 | Medio | Hay que planificar entregas importantes antes de feriados | Todos | Planning futuras |
| Algunos tests de HU-11 fallaron por datos hardcodeados | Bajo | Usar datos generados dinámicamente en tests | Todos | Desde hoy |
| La interfaz de planes es funcional pero podría ser más visual | Bajo | Dedicar tiempo a mejorar UI en próxima iteración | Ayelen | Iteración 4 |
| No documentamos las decisiones de diseño de BD | Medio | Crear documento de arquitectura técnica | Kevin | 10/01/2026 |
| Testing manual tomó más tiempo del estimado | Bajo | Crear scripts con datos de prueba para agilizar | Todos | Iteración 4 |

---

##  Métricas

| Métrica | Estimado | Real | Diferencia |
|---------|----------|------|------------|
| Duración | 3 semanas | 3 semanas | 0 ✅ |
| Puntos completados | 17 | 17 | 0 ✅ |
| Commits realizados | ~50 | 58 | +8 |
| Tests escritos | 8 (2 por HU) | 9 | +1 |
| Code reviews realizados | 4 | 4 | 0 |
| Daily meetings | 15 | 15 | 0 ✅ |
| Bugs encontrados en testing cruzado | N/A | 3 | - |
| Bugs encontrados en producción | 0 | 0 | 0 ✅ |
| Conflictos de merge | ~2 | 1 | -1 ✅ |
| Horas extras por feriados | 0 | ~4 hrs | +4 |

---

##  Aprendizajes Técnicos

- **JPA Avanzado**: Relaciones muchos a muchos, entidades de unión, consultas con joins
- **Campos TEXT en MySQL**: diferencias con VARCHAR
- **Lógica de negocio compleja**: Desactivar registros relacionados al crear nuevos
- **Formularios extensos**: Organización visual con secciones, validación de múltiples campos
- **Bootstrap avanzado**: Uso de cards y layouts complejos

---

##  Aprendizajes de Proceso

1. **Las HU grandes necesitan más atención**: HU-10 (8 pts) requirió casi el doble de tiempo que las de 3 pts
2. **El testing cruzado es invaluable**: Los 3 bugs detectados habrían llegado al PO
3. **La documentación técnica es importante**: Faltó documentar decisiones de diseño de BD
4. **Los feriados impactan más de lo pensado**: Aunque se planificaron, igual afectaron la velocidad
5. **El MVP está completo**: Tenemos un sistema funcional y útil

---

##  Compromisos para Iteración 4

1. **Crear documento de arquitectura técnica**: Documentar modelo de datos y decisiones de diseño
2. **Agregar buffer a HU grandes**: Si una HU tiene +5 pts, considerar +20% de tiempo
3. **Crear scripts de datos de prueba**: Facilitar testing manual con datos precargados
4. **Mejorar UI de planes**: Hacer la visualización más atractiva visualmente
5. **Mantener disciplina de daily meetings**: Continuar con formato exitoso
6. **Considerar refactoring**: Evaluar código duplicado y oportunidades de mejora

---

##  Comentarios del Equipo

**Andrea (PO)**: "El sistema ya puede gestionar todo lo esencial: pacientes, consultas y planes alimentarios. Es exactamente lo que necesitaba. La funcionalidad de desactivar el plan anterior automáticamente esta perfecta."

**Daniel (SM)**: "Nuestra mejor iteración hasta ahora. HU-10 fue un desafío pero lo superamos bien. Propongo que en la próxima iteración dediquemos tiempo a refactorizar y mejorar de código."

**Kevin (Dev)**: "La relación muchos a muchos de HU-11 fue más compleja de lo que pensé inicialmente, pero trabajar con Daniel me ayudó a entenderla bien. Los tests de esta HU me enseñaron mucho sobre testing con datos relacionados. Me siento listo para funcionalidades más avanzadas."

**Ayelen (Dev)**: "HU-10 fue la más grande que hemos hecho. Al principio me asusté, pero dividiéndola en pasos fue manejable. Me gusto trabajar con Andrea. Me gustaría mejorar la parte visual de los planes en la próxima iteración, creo que podemos hacerlo más bonito."

---

## Velocity del Equipo

- **Iteración 1 (Setup)**: 7 tareas completadas
- **Iteración 2**: 17 puntos completados
- **Iteración 3**: 17 puntos completados
- **Velocity consolidada**: 17 puntos por iteración de 3 semanas

**Recomendación para Iteración 4**: Comprometer 16-17 puntos (mantener rango probado)

---

##  Planificación Iteración 4

**Tema**: Gestión de Mediciones Antropométricas y Mejoras

**HU candidatas** (a definir en Sprint Planning):
- HU-06: Registrar Mediciones Antropométricas (5 pts)
- HU-07: Calcular IMC (Índice de Masa Corporal) Automáticamente (2 pts)
- HU-08: Ver Historial de Mediciones (5 pts)
- HU-09: Ver Diferencia entre Mediciones (3 pts)
- HU-21: Gráfico de Evolución de Peso (5 pts) - Si da el tiempo

**Tareas técnicas adicionales**:
- Refactoring de código duplicado (2-3 hrs)
- Documento de arquitectura técnica (2 hrs)
- Scripts de datos de prueba (1 hr)
- Mejoras visuales en UI de planes (2 hrs)

**Fecha inicio**: 06/01/2026  
**Sprint Planning**: 06/01/2026 9:00 AM  
**Duración estimada**: 3 semanas (hasta 26/01/2026)

---

## Logros del Proyecto hasta Ahora

### Funcionalidad Completada
✅ **Gestión completa de pacientes** (CRUD)  
✅ **Búsqueda de pacientes**  
✅ **Registro de consultas**  
✅ **Historial de consultas**  
✅ **Creación de planes alimentarios**  
✅ **Asignación de planes a pacientes**  
✅ **Visualización de plan activo**

### Métricas Acumuladas
- **Total de puntos completados**: 41 puntos (de ~232 del backlog total)
- **Progreso en HU "Debe tener"**: 10 de 14 HU completadas (71%)
- **Total de commits**: ~167 commits
- **Total de tests**: ~20 tests unitarios
- **Bugs en producción**: 0 ✅

### Estado del MVP
 **MVP Funcional**: El sistema ya puede usarse en un consultorio real para gestión básica de pacientes y planes

---

##  Satisfacción General

**Satisfacción general**: ⭐⭐⭐⭐⭐ 5/5

**Ánimo del equipo**: Excelente - Todo el  equipo está muy orgulloso del progreso y motivado para continuar

**Nota del equipo**: "Tenemos un sistema real y funcional, Cada iteración nos esta sumando un valor tangible al proyecto. "

---

##  Reflexión Final de la Iteración

Esta iteración fuen un hito importante: **completamos el núcleo funcional del sistema**. Un nutricionista ya puede usar nuestra aplicación para gestionar su consultorio de principio a fin: registrar pacientes, hacer consultas, crear planes y asignarlos.

El equipo maduro significativamente en:
- Trabajo colaborativo (pair programming consolidado)
- Gestión de Git (casi sin conflictos)
- Calidad de código (tests robustos, code reviews efectivos)
- Disciplina de proceso (daily meetings, DoD estricto)

**Próximos pasos**: Agregar mediciones antropométricas (Mediciones del cuerpo) para completar el seguimiento físico de los pacientes y comenzar con funcionalidades de visualización (gráficos).

---
