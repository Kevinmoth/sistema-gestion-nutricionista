# Retrospectiva - Iteración 2
## Sistema de Gestión para Nutricionistas

---

## Información

| Aspecto | Detalle |
|---------|---------|
| **Iteración** | 2 |
| **Fecha** | 13/12/2025 |
| **Participantes** | Todo el equipo (4 personas) |
| **Duración reunión** | 1 hora 15 min |

---

##  Cumplimiento de Objetivos

| Historia de Usuario | Puntos | Estado | Observaciones |
|---------------------|--------|--------|---------------|
| HU-01: Registrar Nuevo Paciente | 5 | ✅ Completado | Validaciones funcionando correctamente |
| HU-02: Ver Lista de Pacientes | 3 | ✅ Completado | Tabla responsive implementada |
| HU-03: Buscar Paciente | 3 | ✅ Completado | Búsqueda funciona por los 3 campos |
| HU-04: Ver Ficha Completa | 3 | ✅ Completado | Vista limpia y ordenada |
| HU-05: Editar Paciente | 3 | ⚠️ Parcial | Faltó test unitario |

**Resultado**: 17/17 puntos completados (100% funcional, 95% según DoD)

---

##  ¿Qué salió bien?

1. **Cumplimos el objetivo principal**
   - Todas las HU están funcionando en producción
   - El CRUD de pacientes está completo y operativo
   
2. **Mejoramos significativamente en commits**
   - Pasamos de 12 commits (iteración 1) a 47 commits
   - Los mensajes fueron más descriptivos y claros

3. **El pair programming está consolidado**
   - Las rotaciones cada hora se respetaron
   - Ambas parejas reportan mayor productividad y aprendizaje
   - Menos errores detectados gracias a la revisión

4. **Code reviews fueron efectivos**
   - Se detectaron 3 bugs antes de mergear a la rama main
   - Todos participaron en las revisiones
   - Feedback constructivo

5. **Las validaciones quedaron robustas**
   - DNI único funcionando correctamente
   - Validaciones tanto en frontend como backend
   - Mensajes de error claros para el usuario

6. **La interfaz quedó profesional**
   - Bootstrap bien aplicado
   - Diseño responsive funciona en mobile
   - Navegación intuitiva

---

## ¿Qué mejorar?

| Problema Identificado | Impacto | Solución Propuesta | Responsable | Plazo |
|----------------------|---------|-------------------|-------------|--------|
| HU-05 no cumplió DoD(Definición de Hecho) por falta de test | Medio | Escribir el test pendiente antes de comenzar iteración 3 | Pareja A | 16/12/2025 |
| Algunos tests muy básicos, no cubren casos edge | Medio | Dedicar más tiempo a pensar escenarios de prueba | Todos | Iteración 3 |
| Tardamos 3 días en resolver conflicto de merge | Alto | Hacer pull más frecuente y mergear a main diariamente | Todos | Desde hoy |
| No se respetó el límite de 3 semanas (tomó 3.5) | Bajo | Ser más realistas con estimaciones | Daniel (SM) | Planning Iteración 3 |
| Faltó comunicación entre parejas en semana 2 | Medio | Daily meetings OBLIGATORIAS, no opcionales | Daniel (SM) | Desde hoy |
| No todos probaron las HU de la otra pareja | Medio | Checklist de testing manual antes de Sprint Review | Ayelen | 16/12/2025 |

---

##  Métricas

| Métrica | Estimado | Real | Diferencia |
|---------|----------|------|------------|
| Duración | 2-3 semanas | 3.5 semanas | +0.5 semanas |
| Puntos completados | 17 | 17 | 0 |
| Commits realizados | ~40 | 47 | +7 |
| Tests escritos | 5 (1 por HU) | 4 | -1 |
| Code reviews realizados | 5 | 5 | 0 |
| Bugs encontrados en review | N/A | 3 | - |
| Bugs encontrados en producción | N/A | 0 | - |

---

##  Aprendizajes Técnicos

- **Spring MVC**: Controllers, RequestMapping, Model, RedirectAttributes
- **Spring Data JPA**: Métodos personalizados en repositorios, consultas con OR
- **Validación**: mensajes de error personalizados
- **Bootstrap 5**: Sistema de grid, tablas, formularios, botones
- **Git**: Resolución de conflictos complejos, estrategias de merge

---

##  Aprendizajes de Proceso

1. **Los daily meetings son cruciales**: Cuando los saltamos, hubo descoordinación
2. **El DoD debe cumplirse estrictamente**: No se puede marcar como "terminado" si falta algo
3. **Los code reviews salvan tiempo**: Los 3 bugs detectados habrían tomado horas de debugging
4. **Las estimaciones mejoran con práctica**: HU-01 nos tomó más tiempo del estimado, pero las siguientes fueron más rapidas

---

## Compromisos para la Iteración 3

1. **Completar el test faltante de HU-05** antes de comenzar nuevas HU
2. **Daily meetings obligatorias** a las 9:00 AM, sin excepciones
3. **Pull de main al menos 2 veces al día** para evitar conflictos grandes
4. **Testing cruzado**: Cada pareja prueba las HU de la otra antes del Sprint Review
5. **Escribir tests más completos**: Incluir todos los casos posibles

---

##  Comentarios del Equipo

**Andrea (PO)**: "Estoy muy contenta con el resultado. El sistema ya permite gestionar pacientes de forma completa. La interfaz se ve profesional."

**Daniel (SM)**: "Buen trabajo del equipo, aunque debemos ser más disciplinados con los daily meetings. El conflicto de merge nos costó tiempo valioso. Propongo reuniones más cortas (10 min) pero TODOS los días sin falta."

**Kevin (Dev)**: "Me siento mucho más cómodo con Spring ahora. El pair programming con Andrea funcionó excelente. Necesito mejorar en escribir tests más completos, los míos son muy básicos."

**Ayelen (Dev)**: "Esta iteración fue más fluida que la anterior. Me gustó trabajar en la parte visual con Bootstrap. Admito que me faltó probar las HU de la Pareja A antes del demo, lo voy a hacer en la próxima."

---

## Velocity del Equipo

- **Iteración 1 (Setup)**: 7 tareas completadas
- **Iteración 2**: 17 puntos completados (con 1 test pendiente)
- **Velocity promedio**: ~17 puntos por iteración de 3 semanas

**Recomendación para Iteración 3**: Comprometer 15-17 puntos (mantener rango conservador)

---

##  Planificación Iteración 3

**Tema**: Gestión de Mediciones Antropométricas

**HU candidatas** (a definir en Sprint Planning):
- HU-06: Registrar Medición
- HU-07: Ver Historial de Mediciones
- HU-08: Comparar Mediciones
- HU-09: Calcular IMC automáticamente

**Fecha inicio**: 16/12/2025  
**Sprint Planning**: 16/12/2025 9:00 AM  
**Duración estimada**: 3 semanas (hasta 05/01/2026)

---

## Satisfacción General

**Satisfacción general**: ⭐⭐⭐⭐⭐ 4.5/5

**Ánimo del equipo**: Muy Positivo -  motivados para seguir

**Nota del equipo**: "Ya tenemos un MVP funcional! "

---

