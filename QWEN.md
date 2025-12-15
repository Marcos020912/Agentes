# Qwen Code Assistant - Workflow Guide

## Project Structure
```
ultree
Trading_bot/
├── documentacion-requisitos/
│   ├── formularios/
│   │   └── captura/
│   │       ├── FR1_nombre_proyecto.html
│   │       ├── FR1_nombre_proyecto.json
│   │       ├── FR2_nombre_proyecto.html
│   │       └── FR2_nombre_proyecto.json
│   ├── 00-contexto.md
│   ├── 01-requisitos-funcionales.md
│   ├── 02-requisitos-no-funcionales.md
│   ├── 03-modelo-dominio.md
│   ├── 04-trazabilidad.md
│   └── templates/
├── arquitectura-software/
│   ├── 00-contexto-operativo.md
│   ├── 01-vision-arquitectonica.md
│   ├── 02-diseño-conceptual.md
│   ├── 03-diseño-logico.md
│   ├── 04-diseño-fisico.md
│   └── 05-decisiones-arquitectonicas/
├── documentacion-pruebas/
│   ├── 00-plan-pruebas.md
│   ├── 01-casos-prueba-funcionales.md
│   ├── 02-casos-prueba-no-funcionales.md
│   ├── 03-procedimientos-ejecucion.md
│   ├── 04-reporte-defectos.md
│   ├── 05-metricas-cobertura.md
│   └── templates/
├── src/
│   └── (source code of the project)
├── tests/
│   └── (automated tests)
├── .env
├── .gitignore
├── pyproject.toml
├── README.md
└── QWEN.md (this file)
```

## Workflow Process

### Phase 1: Requirements Analysis Forms
1. **subagent**: analista-requisitos
2. **Action**: Create the forms to understand the business and then create the requirements documentation. This step is iterative and may occur multiple times.

### Phase 2: Project Manager Review Forms
1. **subagent**: proyect-manager
2. **Action**: Check that the form has been created by the analyst. After this step, the workflow must be stopped until the form response is in capture. This step is also iterative. Whenever step 1 is executed, this one must also be executed. Update the `PM-log.md` file.

### Phase 3: Requirements Analysis
1. **subagent**: analista-requisitos
2. **Action**: Start creating the documentation corresponding to requirements capture.

### Phase 4: Project Manager Review Requirements Docs
1. **subagent**: proyect-manager
2. **Action**: Verify that all documentation has been created and update `PM-log.md`. If any document is missing, notify analista-requisitos.
.
### Phase 5: Architecture Design
1. **subagent**: arquitecto-software
2. **Action**:Start creating the documentation corresponding to the solution design based on requirements.

### Phase 6: Project Manager Review Design Docs
1. **subagent**: proyect-manager
2. **Action**:Verify that all documentation has been created and update `PM-log.md`. If any document is missing, notify arquitecto-software.

### Phase 7: Test Planning
1. **subagent**: ingeniero-pruebas
2. **Action**: Start designing and documenting tests and test cases for the project.

### Phase 8: Project Manager Review Tests
1. **subagent**: proyect-manager
2. **Action**:Verify that all documentation has been created, create the ToDo_List.md with all tasks that the programmer must fulfill and update `PM-log.md`. If any document is missing, notify ingeniero-pruebas.

### Phase 9: Implementation
1. **subagent**: programmer
2. **Action**: Implement the solution based on all generated documentation and fulfilling the tasks proposed by the project manager.

### Phase 10: Project Manager Review Implementation
1. **subagent**: proyect-manager
2. **Action**: Verify that all tasks in the `ToDo_List.md` file are marked as completed and update `PM-log.md`.

Available subagents:
- `analista-requisitos` - Requirements analysis
- `arquitecto-software` - Software architecture
- `ingeniero-pruebas` - Test planning
- `proyect-manager` - Project coordination
- `programmer` - Implement functionalities


>[!tip] Always work in Spanish (Cuba/LATAM technical terminology)
