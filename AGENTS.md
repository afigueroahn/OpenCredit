# OpenCredit — instrucciones de trabajo

## Autoridad y alcance
- El mantenedor decide alcance, arquitectura, tecnologías, dependencias relevantes y licencia. No asumir decisiones pendientes.
- No usar credenciales ni datos reales de clientes, ni acceder a producción. Solicitar autorización explícita para operaciones destructivas.
- Registrar decisiones significativas en ADR; no reescribir decisiones históricas, sino sustituirlas mediante un nuevo ADR.

## Flujo
- Issue para funcionalidades, errores relevantes, seguridad y decisiones; cambios triviales pueden ir directamente a PR.
- Rama temporal `feat/123-descripcion`, `fix/123-descripcion` o `docs/descripcion` si no hay issue.
- Un PR por objetivo coherente; preferir cambios pequeños, sin límite rígido.
- Conventional Commits: feat, fix, refactor, perf, docs, test, chore, ci, build, revert. Scope opcional; usar ! o BREAKING CHANGE para incompatibilidades.
- Todo cambio pasa por PR, CI satisfactoria, revisión humana y squash merge. No hacer push directo a main ni reescribir historia publicada.
- Cerrar issues vinculados con Closes #N. Eliminar ramas integradas.

## Calidad
- Pruebas según riesgo; cubrir lógica de créditos, autorización, aislamiento de datos, redondeo, concurrencia e idempotencia cuando se implementen.
- No modificar pruebas para ocultar fallos. Evitar duplicación, código muerto y dependencias innecesarias.
- No incluir secretos, información personal ni datos financieros reales en código, logs o fixtures.
- Documentar cambios en contratos, migraciones, seguridad y despliegue cuando corresponda; prever rollback y restauración.
- No publicar hasta verificar artefactos y aprobar la versión. SemVer; main puede contener cambios aún no publicados.

## Estado inicial
Stack, licencia, módulos, reglas financieras, jurisdicción y distribución pendientes. No crear implementación ni simular funcionalidades sin aprobación. La CI inicial comprueba únicamente la gobernanza; ampliar con lint, tipos, build, pruebas y seguridad cuando exista código.
