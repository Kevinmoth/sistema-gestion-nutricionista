# Retrospectiva - Iteración 4 (FINAL)
## Sistema de Gestión para Nutricionistas

---

## Información

| Aspecto | Detalle |
|---------|---------|
| **Iteración** | 4 (Final) |
| **Fecha** | 24/01/2026 |
| **Participantes** | Todo el equipo (4 personas) |
| **Duración reunión** | 2 horas |

---

##  Cumplimiento de Objetivos

| Historia de Usuario | Puntos | Estado | Observaciones |
|---------------------|--------|--------|---------------|
| HU-06: Registrar Mediciones | 5 | ✅ Completado | Validaciones funcionando perfectamente |
| HU-07: Calcular IMC | 2 | ✅ Completado | Integrado perfectamente con la HU-06 |
| HU-08: Ver Historial de Mediciones | 5 | ✅ Completado | Tabla ordenada y con resaltado de última medición |
| HU-09: Ver Diferencia entre Mediciones | 3 | ✅ Completado | Colores y símbolos correctos |
| HU-21: Gráfico de Evolución | 2 | ✅ Completado |  integrado y responsive |

**Tareas Técnicas Adicionales**:
-  Documento de arquitectura técnica creado
- Scripts de datos de prueba generados
-  Mejoras visuales en UI de planes completadas
-  Refactoring de código duplicado realizado

**Resultado**: 17/17 puntos completados + 4 tareas técnicas (100% completado)

---

## ✅ ¿Qué salió bien?

1. **Completamos el proyecto exitosamente! **
   - Todas las funcionalidades core están implementadas
   - El sistema es completamente funcional y usable
   - Cumplimos con los objetivos del Product Owner

2. **La mejor iteración en calidad de código**
   - Todos los tests pasaron en el primer intento
   - El refactoring eliminó ~200 líneas de código duplicado
   - Documentación Java completa en servicios
   - Documento de arquitectura técnica muy útil

3. **Chart.js se integró más fácil de lo esperado**
   - La experiencia de la iteración 3 ayudó
   - El gráfico quedó profesional y responsive
   - Los datos se cargan dinámicamente sin problemas

4. **El cálculo de IMC es preciso y robusto**
   - Tests con 10 casos conocidos, todos pasaron
   - Manejo correcto de decimales
   - Sin errores de redondeo

5. **La funcionalidad de diferencias quedó excelente**
   - Los colores son intuitivos
   - Los símbolos de subir/bajar= ayudan mucho visualmente
   - La lógica maneja todos los casos edge

6. **Las daily meetings fueron impecables**
   - 15/15 reuniones realizadas
   - Todos llegaron puntuales (Salvo Kevin)
   - Impedimentos resueltos el mismo día

7. **Testing cruzado detectó 2 bugs importantes**
   - Bug en conversión de cm a metros (test no lo detectó)
   - Bug en colores cuando peso sube (lógica invertida)
   - Ambos corregidos antes del Sprint Review

8. **El equipo trabajó de forma excepcional**
   - Colaboración constante
   - Apoyo mutuo en problemas técnicos
   - Excelente ambiente de trabajo

9. **La mejora de UI en planes fue un éxito**
   - Uso de Bootstrap cards
   - Mejor organización visual
   - Feedback muy positivo del PO

---

##  ¿Qué mejorar? (Para futuros proyectos)

| Problema Identificado | Impacto | Lección Aprendida | Para el Futuro |
|----------------------|---------|-------------------|----------------|
| Bug de conversión no detectado por tests | Alto | Los tests no cubrían conversión de unidades | Agregar tests de integración, no solo unitarios |
| Algunas estimaciones fueron optimistas | Bajo | HU-08 tomó 6 hrs en vez de 5 | Siempre agregar buffer del 20% |
| La UI podría ser aún más profesional | Bajo | Nos enfocamos más en funcionalidad que estética | Dedicar tiempo específico a UX/UI desde el inicio |
| Documentación de usuario no existe | Medio | Solo documentamos código, no uso del sistema | Crear manual de usuario o videos tutoriales |
| No hicimos tests de performance | Bajo | No sabemos cómo se comporta con muchos datos | Incluir tests de carga en proyectos futuros |
| Git flow podría ser más sofisticado | Bajo | Usamos estrategia simple que funcionó, pero en proyectos grandes necesitaríamos más | Explorar GitFlow o trunk-based development |

---

## 📈 Métricas Finales

### Iteración 4
| Métrica | Estimado | Real | Diferencia |
|---------|----------|------|------------|
| Duración | 3 semanas | 3 semanas | 0 ✅ |
| Puntos completados | 17 | 17 | 0 ✅ |
| Commits realizados | ~50 | 64 | +14 |
| Tests escritos | 10 | 12 | +2 |
| Code reviews realizados | 5 | 5 | 0 |
| Daily meetings | 15 | 15 | 0 ✅ |
| Bugs encontrados en testing cruzado | N/A | 2 | - |
| Bugs encontrados en producción | 0 | 0 | 0 ✅ |
| Conflictos de merge | ~2 | 0 | -2 ✅ |
| Líneas de código refactorizadas | ~150 | 203 | +53 |

### Proyecto Completo (4 Iteraciones)
| Métrica | Total |
|---------|-------|
| **Duración total** | 10.5 semanas (~2.5 meses) |
| **Puntos completados** | 58 puntos |
| **Historias de Usuario completadas** | 14 HU |
| **Commits totales** | ~235 commits |
| **Tests unitarios** | 33 tests |
| **Code reviews** | 18 reviews |
| **Bugs en producción** | 0 ✅ |
| **Velocity promedio** | 17 puntos/iteración |

---

##  Aprendizajes Técnicos (Iteración 4)

- **Cálculos matemáticos precisos**: Manejo de doubles, redondeo, conversión de unidades
- **Chart.js avanzado**: Configuración responsive, personalización de ejes
- **Testing de precisión numérica**: Comparación de doubles con delta
- **Refactoring seguro**: Técnicas para refactorizar sin romper funcionalidad
- **Optimización de consultas**: índices en Bd

---

##  Aprendizajes de Proceso (Proyecto Completo)

### Lo que funcionó excelentemente:
1. **Pair Programming (XP)**: Redujo bugs, aumentó aprendizaje, mejoró calidad
2. **Daily Meetings diarias**: Comunicación constante, detección temprana de problemas
3. **Code Reviews cruzados**: Detectaron ~10 bugs antes de producción
4. **Testing cruzado manual**: Invaluable para encontrar bugs que tests automatizados no detectan
5. **Iteraciones de 3 semanas**: Tiempo ideal para planificar y ejecutar
6. **Definition of Done estricta**: Aseguró calidad consistente
7. **Rotación de parejas**: Todos trabajaron con todos, conocimiento compartido

### Lo que mejoraríamos:
1. **Tests de integración**: Complementar tests unitarios con tests end-to-end
2. **Documentación de usuario**: Crear guías para usuarios finales
3. **Diseño UX/UI**: Dedicar más tiempo a la experiencia de usuario
4. **Performance testing**: Probar con grandes volúmenes de datoS

---

##  Logros del Proyecto

###  Funcionalidades Implementadas (14 HU)

**Gestión de Pacientes** ✅
- HU-01: Registrar Nuevo Paciente
- HU-02: Ver Lista de Pacientes
- HU-03: Buscar Paciente
- HU-04: Ver Ficha Completa
- HU-05: Editar Datos del Paciente

**Mediciones Antropométricas** ✅
- HU-06: Registrar Mediciones
- HU-07: Calcular IMC Automáticamente
- HU-08: Ver Historial de Mediciones
- HU-09: Ver Diferencia entre Mediciones
- HU-21: Gráfico de Evolución de Peso

**Planes Alimentarios** ✅
- HU-10: Crear Plan Alimentario
- HU-11: Asignar Plan a Paciente
- HU-12: Ver Plan Alimentario Activo

**Consultas** ✅
- HU-13: Registrar Consulta
- HU-14: Ver Historial de Consultas

### 📊 Progreso del Backlog
- **HU "Debe tener" completadas**: 14 de 14 (100%) ✅
- **Puntos del backlog completados**: 58 de 232 (25%)
- **MVP completado**: SÍ ✅

---

##  Comentarios del Equipo

**Andrea (PO)**: "Estoy absolutamente encantada con el resultado! El sistema tiene TODO lo que necesito para gestionar un consultorio. La funcionalidad de mediciones con el gráfico es increíble, los pacientes van a poder ver su progreso de forma muy clara. El equipo superó mis expectativas."

**Daniel (SM)**: "Comenzamos sin saber nada de Spring Boot y terminamos con un sistema profesional y funcional. El equipo creció exponencialmente. Las prácticas ágiles funcionaron perfectamente: Scrum, XP, daily meetings, retrospectivas. Muy orgulloso de lo que logramos. Esta experiencia me preparó para proyectos reales."

**Kevin (Dev)**: "Este proyecto cambió mi forma de programar. Aprendí Spring Boot, JPA, testing, Git, trabajo en equipo, y monton de cosas más. El pair programming al principio me incomodaba, pero terminó siendo mi técnica favorita. Los tests me dieron mucha confianza al codificar."

**Ayelen (Dev)**: "Fue mi primer proyecto completo de software y me encantó. Ver cada iteración agregando valor real fue muy motivador. Aprendí tanto de mis compañeros. La parte visual de los planes y el gráfico fueron mis favoritos. Ahora entiendo cómo se trabaja en equipo en desarrollo."

---

##  Velocity y Productividad

### Evolución del Velocity
| Iteración | Puntos Comprometidos | Puntos Completados | % Cumplimiento |
|-----------|---------------------|-------------------|----------------|
| 1 (Setup) | 7 tareas | 7 tareas | 100% |
| 2 | 17 puntos | 17 puntos | 100% |
| 3 | 17 puntos | 17 puntos | 100% |
| 4 | 17 puntos | 17 puntos | 100% |

**Velocity consolidada**: 17 puntos por iteración de 3 semanas

### Productividad del Equipo
-  Completamos exactamente lo que comprometimos en cada iteración
- **Predictibilidad alta**: Después de iteración 2, pudimos predecir con precisión
- **Calidad consistente**: 0 bugs en producción en 4 iteraciones
- **Mejora continua**: Cada retrospectiva generó acciones que se cumplieron

---

##  Habilidades Desarrolladas por el Equipo

### Técnicas
- ✅ Spring Boot (MVC, JPA)
- ✅ MySQL (diseño de BD, relaciones, consultas)
- ✅ HTML/CSS (Bootstrap, diseño responsive)
- ✅ JavaScript (Chart.js)
- ✅ Git/GitHub (branches, PRs, resolución de conflictos)
- ✅ Testing (JUnit, casos edge)
- ✅ Maven (gestión de dependencias)

### Metodológicas
- ✅ Scrum (roles, eventos, artefactos)
- ✅ XP (pair programming, refactoring)
- ✅ Historias de Usuario (escritura, estimación, criterios de aceptación)
- ✅ Planning Poker (estimaciones)
- ✅ Daily Meetings (comunicación diaria)
- ✅ Retrospectivas (mejora continua)
- ✅ Code Reviews (calidad de código)

### Blandas
- ✅ Trabajo en equipo
- ✅ Comunicación efectiva
- ✅ Resolución de conflictos
- ✅ Gestión del tiempo
- ✅ Adaptabilidad
- ✅ Aprendizaje continuo

---

##  Estado Final del Sistema

### ✅ Funcional
- CRUD completo de pacientes
- Búsqueda de pacientes
- Registro y visualización de mediciones antropométricas
- Cálculo automático de IMC
- Comparación de mediciones con colores
- Gráfico de evolución de peso
- Creación de planes alimentarios
- Asignación de planes a pacientes
- Registro de consultas
- Historial de consultas

### 🎨 Visual
- Interfaz limpia y profesional
- Diseño responsive (funciona en mobile)
- Bootstrap 5 bien aplicado
