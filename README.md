# Solucionario de hidráulica

Aplicación web de una sola página para resolver problemas de hidráulica con el desarrollo completo paso a paso: fórmulas, sustitución numérica y resultado con unidades.

No necesita instalación, servidor ni conexión a internet. Abre `index.html` y listo.

---

## Contenido

| # | Tema | Método |
|---|------|--------|
| 1 | Tubería simple | Darcy–Weisbach · Swamee–Jain · pérdidas menores |
| 2 | Tuberías en serie | Resistencia equivalente · hasta 4 tramos |
| 3 | Tuberías en paralelo | Conductancias · reparto de caudal |
| 4 | Redes ramificadas | Cota piezométrica del nodo por bisección |
| 5 | Canal de Manning | Flujo uniforme · sección trapezoidal · Froude |
| 6 | Energía específica | Estado crítico · grada · estrangulamiento |
| 7 | Salto hidráulico | Bélanger · disipación de energía · control de cola |

## Características

- **Desarrollo verificable:** cada paso muestra la fórmula, la sustitución con los datos y el resultado.
- **Resultados destacados:** tarjetas con las magnitudes principales de cada problema.
- **Diagnóstico automático:** avisa de regímenes de transición, flujo cercano al crítico, verificaciones que no cumplen y resultados inconsistentes.
- **Cinco decimales** en todos los resultados, con separadores en español.
- **Exportación:** copiar el desarrollo, descargar CSV (compatible con Excel) e imprimir o guardar como PDF con formato A4.
- **Tema claro y oscuro**, diseño adaptable a móvil y navegación por teclado.
- **Persistencia local:** recuerda los datos y el tema entre visitas.
- **Sin dependencias:** HTML, CSS y JavaScript en un único archivo.

## Uso

1. Abre `index.html` en cualquier navegador moderno.
2. Elige el tema en la barra superior.
3. Modifica los datos: los resultados se recalculan al escribir.
4. Usa **Copiar**, **CSV** o **Imprimir** para llevarte el desarrollo.

También puedes enlazar directamente a un tema con el ancla, por ejemplo:

```
index.html#manning
```

## Estructura

```
solucionario-hidraulica/
├── index.html   # aplicación completa (HTML + CSS + JS)
├── README.md
└── LICENSE
```

El motor de cálculo está en el bloque «Módulos de cálculo» de `index.html`. Cada módulo declara sus datos de entrada y una función `solve(v)` que devuelve la lista de pasos. Para añadir un tema basta con agregar un objeto a `MODS`.

## Criterios de cálculo

- Sistema Internacional de unidades.
- Formato numérico con cinco decimales; notación científica por debajo de `1·10⁻⁴` o por encima de `1·10⁷`.
- El factor de fricción usa la aproximación explícita de Swamee–Jain a Colebrook–White; en régimen laminar, `f = 64/Re`.
- Las hipótesis y referencias de cada método aparecen en el propio desarrollo, al pie de cada tema.

## Referencias

- Swamee, P. K. y Jain, A. K. (1976). *Explicit equations for pipe-flow problems*. Journal of the Hydraulics Division, ASCE.
- Chow, V. T. (1959). *Open-Channel Hydraulics*. McGraw-Hill.
- White, F. M. *Fluid Mechanics*. McGraw-Hill.
- Streeter, V. L. y Wylie, E. B. *Fluid Mechanics*.

## Aviso

Herramienta con fines docentes. Los resultados deben verificarse antes de utilizarse en un proyecto real.

## Licencia

MIT. Consulta [LICENSE](LICENSE).
