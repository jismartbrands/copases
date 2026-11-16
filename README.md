# Copa Salvando el Semestre 🛟

Sistema de **evaluación entre pares** para las exposiciones del tercer parcial de **Marketing Digital · ICOM261** (UAP, Gestión II-2026). Docente: Ing. Jimmy Luis Laruta Villarreal.

Los estudiantes que están sentados califican desde su celular al compañero que expone. El sistema guarda todo en Google Sheets, calcula la nota sobre 5 y permite descargar las notas en Excel.

---

## Cómo se califica

Cada evaluador elige un nivel en cinco criterios:

| Nivel | Vale |
|---|---|
| 🆘 Pide rescate (no suficiente) | 1 |
| 🛟 Se salva (suficiente) | 2 |
| 🏆 ¡Salvó el semestre! (excelente) | 3 |

Criterios: **Dominio del tema · Momento memorable · Caso real de Cobija · Claridad y tiempo · Responde preguntas**.

- **Nota de cada evaluador** = suma de los 5 criterios (de 5 a 15) ÷ 3 → nota sobre 5. Ejemplo: 13 ÷ 3 = 4,33.
- **Nota final del expositor** = promedio de todas las evaluaciones recibidas. Solo cuentan los presentes que evaluaron.
- **Ausente** = 0.
- Para enviar, el evaluador escribe **por qué** pone esa nota y **qué entendió** del tema.
- Nadie evalúa a su propio grupo. Solo se puede evaluar con el **código de la sala** del día, que se ve en el proyector.

---

## Cómo está montado

| Pieza | Dónde está |
|---|---|
| Página web (`index.html`) | Este repositorio, publicado en **https://jismartbrands.github.io/copases/** |
| Datos | Hoja de Google **COPA SALVANDO EL SEMESTRE - BASE ICOM261** (en el Drive del docente): Estudiantes, Evaluaciones, Resultados, Accesos y Control |
| Lógica | Proyecto de Apps Script **Copa Salvando el Semestre - Sistema**, publicado como aplicación web. Su código no se sube aquí porque contiene los RU. |

---

## El día de la exposición

1. Abre **https://jismartbrands.github.io/copases/#docente** en la computadora del aula y entra con tu PIN.
2. Elige la sesión (miércoles 18 o jueves 19) y guarda un **código de sala** nuevo (toca *Generar* y luego *Guardar*).
3. Toca **Proyector**: muestra el QR, el código y el reloj de 5 minutos.
4. Los estudiantes escanean el QR, escriben su RU y el código, y confirman su nombre («¿Eres tú?»).
5. Toca **Siguiente expositor**: aparece en todos los celulares y arranca el reloj de 5 minutos. *Reiniciar 5 min* lo vuelve a poner en cero.
6. Si alguien falta, toca **Ausente** (nota 0). Al terminar, **Cerrar evaluaciones de la sesión**.
7. En **Resultados** ves el podio y las notas, y descargas el **Excel**. Las mismas notas quedan en la hoja **Resultados** de Google Sheets.

---

## Si cambias el código de Apps Script

En el editor de Apps Script: **Implementar → Administrar implementaciones → Editar (lápiz) → Versión: Nueva versión → Implementar**. Así la URL `/exec` no cambia y la web sigue conectada.
