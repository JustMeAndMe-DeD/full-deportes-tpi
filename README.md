# Full Deportes – Módulo de control de stock multicanal

Trabajo Práctico Integrador – Organización Empresarial
Documentación del proyecto: análisis de la organización, planificación, modelado y procesos.

## Descripción

Full Deportes es un comercio de indumentaria y artículos deportivos que vende en local físico y por tienda online. El proyecto propone un módulo de control de stock que unifica el inventario de ambos canales, para evitar sobreventas y alertar a tiempo cuando una variante (talle y color) llega a su stock mínimo.

Este repositorio aloja la documentación completa del TPI: sistema abierto y enfoque sistémico (Entrega 1), diagnóstico y planeación (Entrega 2), estructura y diccionario de datos (Entrega 3) y modelado del proceso, gestión ágil e indicadores (Entrega 4).

## Integrante

| Apellido y nombre | Legajo | Rol |
|---|---|---|
| Stabile Tome, Lucas Gonzalo | 105289 | Autor único del trabajo |

- Materia: Organización Empresarial – Tecnicatura Universitaria en Programación (UTN)
- Docente titular: Prof. Gabriela Martínez
- Comisión / Grupo: [COMPLETAR]

## Enlaces

- Repositorio: [COMPLETAR URL DEL REPO PÚBLICO]
- Tablero de gestión (GitHub Projects / Jira): [COMPLETAR URL DEL TABLERO]

## Estructura del repositorio

```
/
├── README.md
├── docs/
│   ├── entrega-1-organizacion-enfoque-sistemico.pdf
│   ├── entrega-2-diagnostico-y-planeacion.pdf
│   ├── entrega-3-estructura-y-diccionario-de-datos.pdf
│   └── entrega-4-procesos-y-control.pdf
├── bpmn/
│   ├── bpmn_full_deportes.png
│   └── bpmn_full_deportes.svg
└── gestion/
    └── historias-e-indicadores.xlsx
```

## Proceso modelado (BPMN)

Proceso: **venta y descuento de stock en local físico y tienda online**.

- Pools: Cliente, Full Deportes y Proveedor (colapsado).
- Lanes de Full Deportes: Vendedor / tienda online, Administración y Facturación, Sistema de stock, Encargado de depósito.
- Compuertas exclusivas: ¿Hay stock?, ¿Pago aprobado? y ¿Stock ≤ mínimo?.

Diagrama: `bpmn/bpmn_full_deportes.png`

## Historias de usuario

| ID | Historia |
|---|---|
| HU-01 | Como encargado de depósito, quiero registrar cada ingreso, egreso y ajuste de mercadería, para que el stock del sistema refleje lo que hay físicamente. |
| HU-02 | Como vendedor, quiero consultar la disponibilidad real de una variante antes de cerrar la venta, para no vender productos que no tenemos. |
| HU-03 | Como dueño del negocio, quiero recibir una alerta cuando una variante llegue a su stock mínimo, para reponerla a tiempo. |

El detalle con criterios de aceptación está en el tablero y en `gestion/historias-e-indicadores.xlsx`.

## Indicadores de control

Los indicadores I-1 a I-5 derivan de las metas M1 a M5 de la Entrega 2; I-6 a I-8 son complementarios.

| # | Indicador | Meta origen | Valor objetivo |
|---|---|---|---|
| I-1 | Sincronización de stock | M1 | ≤ 5 s en el 95 % de las operaciones |
| I-2 | Reducción de sobreventas | M2 | ≥ 90 % respecto de la línea base (S1–S2), en los 3 primeros meses de uso |
| I-3 | Rendimiento de consultas | M3 | ≤ 2 s en el 95 % de las consultas (10 usuarios, 5.000 registros) |
| I-4 | Cumplimiento del plazo | M4 | En producción al cierre de S14 (22/01/2027), desvío ≤ 1 semana |
| I-5 | Capacitación del personal | M5 | 100 % de los usuarios |
| I-6 | Exactitud de inventario | Complementario | ≥ 95 % |
| I-7 | Cobertura de alertas | Complementario | 100 % |
| I-8 | Avance del backlog | Gestión del proyecto | 100 % al cierre |

## Flujo de trabajo con Git

- `main`: versión estable y entregable.
- Una rama por tarea, con nombre descriptivo: `docs/bpmn`, `docs/historias-usuario`, `docs/indicadores`, `fix/ortografia-entrega-1`.
- Commits en imperativo y con mensaje descriptivo, por ejemplo: `Agrega diagrama BPMN del proceso de venta`.
- Los cambios se integran a `main` mediante Pull Request.

## Declaración de uso de Inteligencia Artificial

Herramienta utilizada: **Claude (Anthropic)**, usada como asistente para la Entrega 4. Las Entregas 1 a 3 mantienen las declaraciones de IA incluidas en cada documento.

### Qué se hizo con IA

| Parte del trabajo | Uso de la IA | Qué hizo el autor |
|---|---|---|
| Lectura de las Entregas 1 a 3 | Resumen del recorrido del proyecto y detección de inconsistencias (campos sin completar, errores de ortografía, falta de las historias de usuario) | Aporté mis tres entregas y confirmé que eran las correctas para el trabajo integrador. |
| Diagrama BPMN | Propuso el proceso, los pools, lanes y compuertas, y generó el dibujo mediante un script | Elegí modelar el proceso de venta y descuento de stock. Al contrastarlo con mi organigrama, decidí mover el cobro al área de Administración y Facturación. |
| Historias de usuario | Redactó el borrador de las tres historias y sus criterios de aceptación a partir del BPMN | Pedí que se armaran a partir del BPMN y las pasé a una tabla para cargarlas en el tablero. |
| Indicadores de control | Propuso los indicadores y las fórmulas; luego los corrigió para alinearlos con las metas M1 a M5 de mi Entrega 2 | Pedí los indicadores y usé mis metas M1 a M5 como base. |
| Hoja de cálculo, README y sección de la Entrega 4 | Generó la estructura de los tres archivos | Pedí cada archivo, completé mis datos y los subí al repositorio con GitHub Desktop. |

### Prompts utilizados

Resumen de los pedidos realizados a la IA:

1. Pegué la consigna de la Entrega 4 y adjunté el PDF.
2. Adjunté mis Entregas 1, 2 y 3 y consulté si eran las correctas.
3. Pedí modelar en BPMN el proceso de venta y descuento de stock.
4. Pedí redactar las tres historias de usuario y pasarlas a una tabla.
5. Pedí definir los indicadores de control y generar una hoja de cálculo con todo.
6. Pedí armar este README con la declaración de uso de IA.
7. Pedí una guía de Git y GitHub, y la sección de la Entrega 4 en el formato de mis trabajos.

### Verificación y correcciones humanas

- Imprecisión de la IA en los indicadores: sus indicadores iniciales no coincidían con mis metas M1 a M5; se corrigieron al leer mi Entrega 2.
- Imprecisión de la IA en el BPMN: ubicó el cobro en el rol del vendedor, pero según el organigrama de mi Entrega 3 los cobros corresponden a Administración y Facturación. Decidí moverlo, junto con el aviso de pago rechazado, a ese carril.
- Preparo la defensa oral de cada diagrama y decisión para el Coloquio Integrador.

### Responsabilidad

El contenido final es responsabilidad del autor. La IA se utilizó como apoyo y no reemplaza el análisis propio de la organización.
