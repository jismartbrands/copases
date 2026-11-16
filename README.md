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

## Archivos

| Archivo | Dónde va |
|---|---|
| `index.html` | **GitHub** (es la página web) |
| `Code.gs` | **Google Apps Script**. ⚠️ **No lo subas a GitHub**: contiene los RU de los estudiantes. |

Si abres `index.html` sin configurarlo, funciona en **modo demostración** (RU 1001 a 1028, código `2026`, PIN docente `1234`), con datos guardados solo en ese navegador.

---

## Instalación (unos 15 minutos, una sola vez)

### 1. Crea la hoja de cálculo
1. Entra a [sheets.google.com](https://sheets.google.com) y crea una hoja nueva. Ponle de nombre **Copa Salvando el Semestre – ICOM261**.

### 2. Pega el código
1. En la hoja: **Extensiones → Apps Script**.
2. Borra todo lo que aparece y pega el contenido completo de `Code.gs`.
3. En la línea `const PIN_DOCENTE = 'CAMBIA-ESTE-PIN';` escribe tu propio PIN (lo usarás en el panel del docente).
4. Guarda (ícono del disquete).

### 3. Instala las hojas
1. Arriba, en la lista de funciones, elige **instalar** y toca **▶ Ejecutar**.
2. Google pedirá permisos: **Revisar permisos → tu cuenta → Configuración avanzada → Ir a … (no seguro) → Permitir**. Es tu propio script.
3. Vuelve a la hoja: verás las pestañas **Estudiantes, Evaluaciones, Resultados, Accesos y Control**.

### 4. Publica el sistema
1. En Apps Script: **Implementar → Nueva implementación**.
2. Tipo (ícono de engranaje): **Aplicación web**.
3. **Ejecutar como:** Yo. **Quién tiene acceso:** Cualquier usuario.
4. **Implementar** y copia la **URL de la aplicación web** (termina en `/exec`).

### 5. Conecta la página
1. Abre `index.html` con el Bloc de notas (o en GitHub con el lápiz ✏️).
2. Busca la línea `const API_URL = '';` y pega tu URL entre las comillas:
   `const API_URL = 'https://script.google.com/macros/s/XXXX/exec';`
3. Guarda.

### 6. Súbelo a GitHub
1. En GitHub crea un repositorio **público**, por ejemplo `copases`.
2. **Add file → Upload files** → sube `index.html` (y este `README.md` si quieres) → **Commit changes**.
3. **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
4. En uno o dos minutos tu página estará en:
   `https://TU-USUARIO.github.io/copases/`

### 7. Prueba antes de la clase
1. Abre la página agregando `#docente` al final y entra con tu PIN.
2. Toca **Generar** y **Guardar** para crear un código de sala.
3. Abre la página normal en tu celular, entra con un RU de prueba y el código.
4. En el panel, pon a alguien **En escena** y evalúalo desde el celular.
5. Revisa que la evaluación aparezca en la hoja **Evaluaciones**. Después **borra esa fila** para empezar limpio.

---

## Uso en clase

**Página del docente:** `https://TU-USUARIO.github.io/copases/#docente`

1. **Antes de empezar:** elige la sesión (**Mié 18 · Sesión 1** o **Jue 19 · Sesión 2**), genera un **código nuevo** y toca **Abrir proyector**. El proyector muestra el **QR** de la página, el código y quién está en escena.
2. **Cada exposición:** toca **Siguiente expositor**. Los celulares se actualizan solos en pocos segundos y el expositor queda abierto para evaluar. El panel muestra cuántas evaluaciones recibió de las esperadas.
3. **Si alguien falta:** toca **Ausente** en su fila (nota 0). Si llega, toca **Presente**.
4. **Al terminar la sesión:** **Cerrar evaluaciones de la sesión** (hay que tocar dos veces).
5. **Notas:** pestaña **Resultados → Descargar Excel**. El archivo trae la hoja **Notas finales** y la hoja **Detalle de evaluaciones**, con lo que escribió cada evaluador.

También puedes descargar desde Google Sheets: hoja **Resultados → Archivo → Descargar → Microsoft Excel (.xlsx)**.

---

## Preguntas frecuentes

**¿Cambio el código cada sesión?** Sí. Un código nuevo cada día evita que alguien evalúe sin estar en el aula. Quien tenga el código viejo deberá volver a entrar.

**Un estudiante se equivocó en su evaluación.** Mientras el expositor siga abierto, puede volver a evaluarlo: la nueva evaluación reemplaza a la anterior.

**Quiero anular una evaluación sin sustento.** Borra esa fila en la hoja **Evaluaciones**. La nota se recalcula sola.

**Cambié algo en `Code.gs`.** En Apps Script: **Implementar → Administrar implementaciones → ✏️ Editar → Versión: Nueva versión → Implementar**. La URL no cambia.

**La página dice «No hay conexión con el sistema».** Revisa que la URL pegada en `index.html` termine en `/exec` y que la implementación tenga acceso para **Cualquier usuario**.

**¿Los RU quedan públicos?** No. La página de GitHub no contiene RU: los nombres y RU solo están en tu hoja de Google y en tu Apps Script.
