# Prompts de generación de imagen

Cada prompt genera **una imagen de referencia visual**, no código. Están pensados para un generador de imágenes tipo Midjourney/DALL·E/Stable Diffusion. Mismo estilo en todos: dashboard SaaS oscuro, fondo navy `#0F1B2D`, acento azul `#2F6FED`, mockup tipo Figma, sin fotorrealismo.

Todos los datos de ejemplo (reglas `PAY-001..005`, categorías, estados `ALLOW/BLOCK/INDETERMINATE`) salen de [flowguard-docs](https://github.com/FlowGuard-Hackathon/flowguard-docs). Si un prompt contradice la documentación técnica, manda la documentación — estas son solo referencias visuales.

## Estado

| # | Pantalla | Imagen generada | Prompt |
|---|---|---|---|
| 1 | Login | ❌ pendiente | [§ Login](#1-login) |
| 2 | Dashboard | ❌ pendiente | [§ Dashboard](#2-dashboard) |
| 3 | Solicitudes de pago (lista) | ❌ pendiente | [§ Solicitudes de pago](#3-solicitudes-de-pago) |
| 4 | Detalle de solicitud (bloqueada) | ❌ pendiente | [§ Detalle de solicitud](#4-detalle-de-solicitud) |
| 5 | Simulador de aprobación | ❌ pendiente | [§ Simulador de aprobación](#5-simulador-de-aprobación) |
| 6 | Centro de evidencias | ❌ pendiente | [§ Centro de evidencias](#6-centro-de-evidencias) |
| 7 | Historial de ejecuciones | ❌ pendiente | [§ Historial de ejecuciones](#7-historial-de-ejecuciones) |
| 8 | Gestión de usuarios | ❌ pendiente | [§ Gestión de usuarios](#8-gestión-de-usuarios) |
| 9 | Configuración — Reglas de pago | ✅ [`pantallas/09-configuracion-reglas-de-pago.png`](../pantallas/09-configuracion-reglas-de-pago.png) | [§ Configuración · Reglas de pago](#9a-configuración--reglas-de-pago) |
| 9b | Configuración — Parámetros | ❌ pendiente | [§ Configuración · Parámetros](#9b-configuración--parámetros) |
| 9c | Configuración — Categorías | ❌ pendiente | [§ Configuración · Categorías](#9c-configuración--categorías) |
| — | Logo (versión 3D) | ❌ pendiente (referencia subida) | [§ Logo — versión 3D](#10-logo--versión-3d) |

También existe [`pantallas/referencia-set-9-pantallas.png`](../pantallas/referencia-set-9-pantallas.png): el mockup original de las 9 pantallas que sirvió de punto de partida para todos los prompts de abajo. Y [`logo/referencia-logo-3d.png`](../logo/referencia-logo-3d.png): la referencia visual (estilo 3D glossy) para el prompt del logo.

**Descartado a propósito:** una pestaña "Integraciones" en Configuración (mostraría detalles de infraestructura — proyecto de Supabase, estado del modelo de Nebius — que no le corresponde ver a un administrador de negocio desde la app; es información operativa, no una regla de negocio).

---

## 1. Login

```
Modern dark-mode SaaS login screen UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism.

Split-screen layout, 16:9 browser-window frame:

LEFT HALF: dark navy panel with a large centered shield-with-checkmark
logo mark in electric blue, white wordmark "FlowGuard" below it in bold
sans-serif, small tracked-out uppercase tagline "DETECT · VERIFY ·
PROTECT", and below that three short lines of supporting copy in
muted gray: "Supervisa aprobaciones. Detecta riesgos. Protege tu
organización." Subtle abstract wave/network texture in the background,
very low opacity, dark blue tones only.

RIGHT HALF: lighter elevated card (#16233A) centered vertically,
containing a login form: heading "Bienvenido a FlowGuard", subtext
"Inicia sesión para continuar", a labeled input field "Correo
electrónico" with placeholder "maria.gonzalez@empresa.com", a labeled
password input "Contraseña" with dots and a show/hide eye icon, a
"Recordarme" checkbox aligned left and "¿Olvidaste tu contraseña?"
link aligned right, a full-width filled blue button "Iniciar sesión",
a small "o" divider, an outlined secondary button "Continuar con SSO
(empresa)", and a small gray footer line: "Uso exclusivo para personal
autorizado. Todas las actividades son registradas."

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding inside the card,
professional product-design portfolio quality.
```

## 2. Dashboard

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard" (active, highlighted blue background), "Solicitudes
de pago", "Simulador", "Centro de evidencias", "Historial de
ejecuciones", "Configuración"; at the bottom, a user avatar circle,
name "María López", role "Analista de Finanzas", small green "En
línea" status dot.

TOP of content area: page title "Panel de supervisión", subtitle
"Monitorea las aprobaciones y detecta riesgos antes de ejecutar un
pago.", two buttons top-right: filled blue "Simular aprobación" and
outlined "Ver historial".

ROW 1: four metric cards side by side, each with a small icon, a big
number, a label, and a trend line below:
- "128" / "Solicitudes supervisadas" / "+12% vs. semana anterior"
- "76" / "Aprobaciones permitidas" / "59% del total"
- "38" / "Pagos bloqueados" / "30% del total"
- "14" / "Pendientes de revisión" / "11% del total"

ROW 2, two panels side by side:
LEFT PANEL "Actividad de las solicitudes (últimos 7 días)": a stacked
bar chart with days on the x-axis (16 abr–22 abr), bars split into
three colors — green, red, amber — with a small legend "ALLOW / BLOCK
/ INDETERMINATE".
RIGHT PANEL "Alertas recientes": a short vertical list of 3-4 alert
rows, each with a colored status icon, a short title like "Pago
bloqueado por falta de autorización", a code like "PAY-2026-0158", and
a relative time like "Hace 2 horas".

ROW 3, two panels side by side:
LEFT, wider panel "Actividad reciente": a data table with columns ID
de solicitud, Solicitante, Concepto, Importe, Estado (colored pill:
green ALLOW / red BLOCK / amber INDETERMINATE), Fecha y hora, Acciones
— 5 sample rows with alternating subtle row backgrounds, "Ver todas"
link top-right of the panel.
RIGHT, narrower panel "Reglas con más incumplimientos": a short ranked
list of rule codes (PAY-001, PAY-004, PAY-005, PAY-003, PAY-002) each
with a short label (Autorización de supervisor, Factura verificada,
Presupuesto disponible, Separación de funciones, Categoría permitida)
and a horizontal bar showing a percentage (42%, 28%, 18%, ...).

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 3. Solicitudes de pago

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard", "Solicitudes de pago" (active, highlighted blue
background), "Simulador", "Centro de evidencias", "Historial de
ejecuciones", "Configuración"; at the bottom, a user avatar circle,
name "María López", role "Analista de Finanzas", small green "En
línea" status dot.

TOP of content area: page title "Solicitudes de pago", subtitle
"Consulta, filtra y revisa el estado de todas las solicitudes.",
button top-right: filled blue "Nueva solicitud".

FILTER BAR below the title, a row of compact dropdown/filter controls:
"Todos los estados", "Todas las categorías", a date-range picker
showing "16 abr 2026 – 22 abr 2026", and a search input on the far
right with placeholder "Buscar por ID, solicitante o proveedor".

MAIN CONTENT: a wide data table filling most of the screen, columns:
"ID de solicitud", "Solicitante" (with small circular avatar + name),
"Proveedor / Concepto" (two lines: provider name, smaller gray concept
line below), "Importe" (right-aligned, bold, in MXN), "Estado"
(colored pill badge: green "ALLOW", red "BLOCK", amber
"INDETERMINATE"), "Fecha" (date + time, two lines), "Acciones" (a
small "···" overflow icon).

8 sample rows with realistic Spanish data (names like Carlos Ramírez,
Ana Torres, Sofía Herrera; providers like TechSolutions, Viajes
Ejecutivos, Equipos y Sistemas; amounts from $3,500 to $20,900 MXN;
mixed ALLOW/BLOCK/INDETERMINATE pills), alternating subtle row
backgrounds, thin horizontal dividers.

BOTTOM of the table: "Mostrando 1–8 de 128" on the left, pagination
controls (numbered pages 1 2 3 4 5 ... with arrow buttons) on the
right.

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 4. Detalle de solicitud

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard", "Solicitudes de pago" (active, highlighted blue
background), "Simulador", "Centro de evidencias", "Historial de
ejecuciones", "Configuración"; at the bottom, a user avatar circle,
name "María López", role "Analista de Finanzas", small green "En
línea" status dot.

TOP of content area: a small "← Volver a solicitudes" link, then a
header row with the request ID "PAY-2026-0158" in bold next to a red
pill badge "BLOCK", subtitle "Evaluación completada el 22 abr 2026,
10:24", and top-right two buttons: outlined "Ver evidencias" and a
small "···" overflow icon.

SUMMARY CARD below: solicitante (avatar + "María González" +
"m.gonzalez@empresa.com"), proveedor ("Servicios Digitales del Centro"
+ small RFC line), concepto ("Servicios de infraestructura"), importe
large and bold ("$15,000 MXN") — laid out as 4 compact columns in one row.

ALERT BANNER: a red-tinted rounded banner with a warning icon, text
"Solicitud bloqueada por el motor determinista" and smaller line below
"La solicitud no cumple con una o más reglas de negocio. No se puede
autorizar el pago."

SECTION "Evaluación de reglas": a vertical list of 5 rule rows, each
row showing: left side a colored status icon (red X for FAIL, green
check for PASS) + rule code + rule name (PAY-001 Autorización de
supervisor FAIL, PAY-002 Categoría permitida PASS, PAY-003 Separación
de funciones PASS, PAY-004 Factura verificada PASS, PAY-005
Presupuesto disponible PASS); middle column "Motivo" with a short
explanation line (e.g. "El importe supera el umbral de $10,000 MXN y
no existe una autorización válida."); right column "Evidencia" showing
a small tag/reference (e.g. "No existe autorización verificada
asociada a la solicitud.") and a small chevron/expand icon. The FAIL
row has a subtle red-tinted background, PASS rows have a subtle green
dot and neutral background.

BOTTOM: a blue-tinted info banner "Resumen de decisión: La solicitud
fue bloqueada debido al incumplimiento de la regla PAY-001. Las demás
reglas fueron evaluadas correctamente."

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 5. Simulador de aprobación

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard", "Solicitudes de pago", "Simulador" (active,
highlighted blue background), "Centro de evidencias", "Historial de
ejecuciones", "Configuración"; at the bottom, a user avatar circle,
name "María López", role "Analista de Finanzas", small green "En
línea" status dot.

TOP of content area: page title "Simulador de aprobación", a
blue-tinted info banner below it with an info icon: "Prueba cómo
FlowGuard evalúa una solicitud de pago. No se transfiere dinero ni se
ejecuta ningún pago real."

MAIN CONTENT split into two side-by-side panels:

LEFT PANEL (wider), titled "Datos de la solicitud": a form with two
columns of labeled input fields — "Solicitante" (dropdown, "María
González"), "Proveedor" (dropdown, "Servicios Digitales del Centro"),
"Concepto" (text input, "Servicios de infraestructura"), "Importe
(MXN)" (number input, "15000"), "Categoría" (dropdown, "SOFTWARE"),
"Identificador de factura" (text input, "INV-2026-4487"), "Presupuesto
disponible (MXN)" (number input, "50000"), "Factura verificada"
(dropdown, "Sí"), "Autorización de supervisor" (dropdown, "María
González"), "Aprobador" (dropdown, "Carlos Ramírez") — below the form,
two buttons: filled blue "Evaluar solicitud" and outlined "Limpiar
formulario", and a small gray note card below: "Umbral de autorización
de supervisor: Las solicitudes que superan $10,000 MXN requieren
autorización de un supervisor (configuración del sistema)."

RIGHT PANEL (narrower), titled "Resultado de la simulación": a red
pill badge "BLOCK" at top with small text "La solicitud no cumple con
una o más reglas de negocio" below it, then two small metadata rows
"ID de ejecución: EXE-2026-0048" and "Fecha: 22 abr 2026, 11:30";
below that a compact section "Evaluación de reglas" listing all 5
rules as small rows with colored icon + code + short label + PASS/FAIL
tag (PAY-001 Autorización de supervisor FAIL red, PAY-002 Categoría
permitida PASS green, PAY-003 Separación de funciones PASS green,
PAY-004 Factura verificada PASS green, PAY-005 Presupuesto disponible
PASS green); below that a section "Evidencias utilizadas" listing
small rows with a document icon + label + small "Verificado" or "No
disponible" tag (Factura INV-2026-4487 Verificado, Presupuesto del
área Verificado, Autorización de supervisor No disponible in red).

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 6. Centro de evidencias

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard", "Solicitudes de pago", "Simulador", "Centro de
evidencias" (active, highlighted blue background), "Historial de
ejecuciones", "Configuración"; at the bottom, a user avatar circle,
name "María López", role "Analista de Finanzas", small green "En
línea" status dot.

TOP of content area: page title "Centro de evidencias", subtitle
"Consulta la información que respalda las decisiones."

FILTER BAR below the title, a row of compact dropdown/filter controls:
"Todas las solicitudes", "Todas las reglas", "Todos los tipos", "Todos
los estados", and a search input on the far right with placeholder
"Buscar evidencias...".

MAIN CONTENT split into two side-by-side panels:

LEFT PANEL (wider), a data table titled with columns "ID de
evidencia", "Solicitud" (code like PAY-2026-0158), "Regla" (code like
PAY-004), "Tipo" (label like Factura, Autorización, Presupuesto,
Catálogo, Informe IA, Sitio web), "Fuente" (label like Sistema ERP,
Sistema RRHH, Nebius Token Factory), "Estado" (small pill: green
"Verificado" or red "No disponible"), "Fecha" (date + time), a small
eye/expand icon on each row. About 6 sample rows mixing different
evidence types, one highlighted/selected row with a subtle blue-tinted
background.

RIGHT PANEL (narrower), titled "Detalle de evidencia": a document-icon
thumbnail at top, below it a bold title "Factura INV-2026-4487", then
labeled metadata rows: "Tipo: Factura", "Fuente: Sistema ERP", "Fecha
de obtención: 22 abr 2026, 10:20", "Descripción: Factura emitida por
Servicios Digitales del Centro por $15,000 MXN.", and below a small
gray file-info chip showing "INV-2026-4487.pdf · 245 KB", and a
full-width outlined button at the bottom "Ver documento".

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 7. Historial de ejecuciones

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard", "Solicitudes de pago", "Simulador", "Centro de
evidencias", "Historial de ejecuciones" (active, highlighted blue
background), "Configuración"; at the bottom, a user avatar circle,
name "María López", role "Analista de Finanzas", small green "En
línea" status dot.

TOP of content area: page title "Historial de ejecuciones", subtitle
"Revisa las evaluaciones anteriores y su trazabilidad."

FILTER BAR below the title: a search input with placeholder "Buscar
por solicitud, ejecución o solicitante", a dropdown "Todos los
estados", and a date-range picker showing "16 abr 2026 – 22 abr 2026"
on the right.

MAIN CONTENT: a wide data table filling most of the screen, columns:
"ID de ejecución" (code like EXE-2026-0048), "Solicitud" (code like
PAY-2026-0157), "Solicitante" (name), "Decisión" (colored pill: green
"ALLOW", red "BLOCK", amber "INDETERMINATE"), "Regla determinante"
(code like PAY-001, shown only when BLOCK/INDETERMINATE, dash "—" when
ALLOW), "Investigación IA" (small pill: "Completada" in blue, or
grayed "—" when not applicable), "Fecha y hora" (date + time, two
lines), "Acciones" (a small "···" overflow icon).

6 sample rows with realistic Spanish data (names like Carlos Ramírez,
Ana Torres, Luis Martínez, Sofía Herrera, Jorge Silva; mixed
ALLOW/BLOCK/INDETERMINATE decisions; execution IDs sequential like
EXE-2026-0043 to EXE-2026-0048), alternating subtle row backgrounds,
thin horizontal dividers.

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 8. Gestión de usuarios

```
Modern dark-mode SaaS dashboard UI mockup for "FlowGuard", a fintech
payment-approval monitoring platform. Style: clean enterprise dashboard
design, flat vector UI illustration, dark navy background (#0F1B2D),
electric blue accent (#2F6FED), rounded cards, subtle shadows,
high-fidelity Figma-style mockup, no photorealism, 16:9 browser-window frame.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark at top; below it a vertical nav list with
icons: "Dashboard", "Solicitudes de pago", "Simulador", "Centro de
evidencias", "Historial de ejecuciones", "Configuración" (active,
highlighted blue background, with a small sub-item "Usuarios y
permisos" indented and highlighted below it); at the bottom, a user
avatar circle, name "María López", role "Administrador", small green
"En línea" status dot.

TOP of content area: page title "Usuarios y permisos", subtitle
"Administra los usuarios y roles de la plataforma.", button top-right:
filled blue "Nuevo usuario".

FILTER BAR below the title: a search input with placeholder "Buscar
por nombre o correo", a dropdown "Todos los roles" on the right.

MAIN CONTENT: a wide data table filling most of the screen, columns:
"Nombre" (avatar + name), "Correo electrónico", "Rol" (small colored
pill: blue "Administrador", teal "Supervisor", gray "Solicitante",
purple "Auditor"), "Estado" (small pill: green "Activo" or gray
"Inactivo"), "Último acceso" (date + time), "Acciones" (small edit
pencil icon + "···" overflow icon).

6 sample rows with realistic Spanish names (María López - Administrador
- Activo; Carlos Ramírez - Supervisor - Activo; Ana Torres -
Solicitante - Activo; Luis Martínez - Solicitante - Activo; Sofía
Herrera - Auditor - Activo; one row grayed out "Inactivo" status),
alternating subtle row backgrounds, thin horizontal dividers.

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

## 9a. Configuración — Reglas de pago

Ya generada: [`pantallas/09-configuracion-reglas-de-pago.png`](../pantallas/09-configuracion-reglas-de-pago.png).

```
Modern dark-mode SaaS settings screen UI mockup for "FlowGuard", a
fintech payment-approval monitoring platform. Style: clean enterprise
dashboard design, flat vector UI illustration, dark navy background
(#0F1B2D), electric blue accent (#2F6FED), rounded cards, subtle
shadows, high-fidelity Figma-style mockup, no photorealism, 16:9
browser-window frame with macOS-style traffic-light dots top-left.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark + small tracked-out tagline "DETECT ·
VERIFY · PROTECT" at top; below it a vertical nav list with icons:
"Dashboard", "Solicitudes de pago", "Simulador", "Centro de
evidencias", "Historial de ejecuciones", "Configuración" (active,
highlighted blue background); at the bottom, a circular avatar "ML",
name "María López", role "Administrador", small green "En línea"
status dot.

TOP of content area: page title "Reglas de negocio", subtitle
"Parámetros del sistema (solo administradores).", button top-right:
filled blue "Editar configuración".

TAB BAR below the title: four tabs, "Reglas de pago" (active,
underlined blue), "Parámetros", "Categorías", "Integraciones".

MAIN CONTENT: a wide data table filling most of the screen, columns:
"ID" (code like PAY-001), "Nombre" (rule name like "Autorización de
supervisor"), "Descripción" (short gray text like "Requiere
autorización si el importe supera un umbral"), "Estado" (small green
pill "Activa"), "Parámetros" (small value like "Umbral: $10,000 MXN"
or "Categorías: 3" or dash "—"), "Acciones" (small edit pencil icon).

5 rows, one for each business rule: PAY-001 Autorización de supervisor,
PAY-002 Categoría permitida, PAY-003 Separación de funciones, PAY-004
Factura verificada, PAY-005 Presupuesto disponible — all with green
"Activa" status pills, alternating subtle row backgrounds, thin
horizontal dividers.

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, generous padding, professional
product-design portfolio quality.
```

> Nota: el prompt original incluía una cuarta pestaña "Integraciones" que se descartó a propósito (ver arriba). Si regeneras esta imagen, usa solo 3 pestañas: Reglas de pago, Parámetros, Categorías.

## 9b. Configuración — Parámetros

```
Modern dark-mode SaaS settings screen UI mockup for "FlowGuard", a
fintech payment-approval monitoring platform. Style: clean enterprise
dashboard design, flat vector UI illustration, dark navy background
(#0F1B2D), electric blue accent (#2F6FED), rounded cards, subtle
shadows, high-fidelity Figma-style mockup, no photorealism, 16:9
browser-window frame with macOS-style traffic-light dots top-left.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark + small tracked-out tagline "DETECT ·
VERIFY · PROTECT" at top; below it a vertical nav list with icons:
"Dashboard", "Solicitudes de pago", "Simulador", "Centro de
evidencias", "Historial de ejecuciones", "Configuración" (active,
highlighted blue background); at the bottom, a circular avatar "ML",
name "María López", role "Administrador", small green "En línea"
status dot.

TOP of content area: page title "Reglas de negocio", subtitle
"Parámetros del sistema (solo administradores).", button top-right:
filled blue "Editar configuración".

TAB BAR below the title: three tabs, "Reglas de pago", "Parámetros"
(active, underlined blue), "Categorías".

MAIN CONTENT: a vertical list of parameter cards, each with an icon,
a label, a short description, and a value/control on the right:

- Icon currency: "Moneda del sistema" / "Moneda en la que se evalúan
  los importes de pago." / value chip "MXN" with a small edit pencil.
- Icon clock: "Tiempo de espera del agente" / "Tiempo máximo que
  espera una respuesta del proveedor de IA antes de marcarla como
  fallida." / value "15,000 ms" with edit pencil.
- Icon repeat: "Límite de llamadas a herramientas" / "Número máximo de
  consultas que el agente puede hacer por investigación." / value "5"
  with edit pencil.
- Icon gauge: "Límite de solicitudes (rate limiting)" / "Solicitudes
  máximas por minuto antes de rechazar nuevas peticiones." / toggle
  switch "Activado" (blue, on position).
- Icon shield-lock: "Acceso a demo pública" / "Requiere usuario y
  contraseña adicionales cuando la app se expone en una URL pública."
  / toggle switch "Activado" (blue, on position).

Each card has a thin border, generous padding, consistent 8px spacing
grid between cards.

Composition: sharp UI elements, legible mock Spanish-language labels,
professional product-design portfolio quality.
```

> Nota: el prompt original incluía un sexto parámetro "Entorno de base de datos" (proyecto de Supabase) — se quitó por el mismo motivo que "Integraciones": es información de infraestructura, no una regla de negocio configurable desde la app.

## 9c. Configuración — Categorías

```
Modern dark-mode SaaS settings screen UI mockup for "FlowGuard", a
fintech payment-approval monitoring platform. Style: clean enterprise
dashboard design, flat vector UI illustration, dark navy background
(#0F1B2D), electric blue accent (#2F6FED), rounded cards, subtle
shadows, high-fidelity Figma-style mockup, no photorealism, 16:9
browser-window frame with macOS-style traffic-light dots top-left.

LEFT: fixed dark sidebar — shield-with-checkmark logo mark in electric
blue + "FlowGuard" wordmark + small tracked-out tagline "DETECT ·
VERIFY · PROTECT" at top; below it a vertical nav list with icons:
"Dashboard", "Solicitudes de pago", "Simulador", "Centro de
evidencias", "Historial de ejecuciones", "Configuración" (active,
highlighted blue background); at the bottom, a circular avatar "ML",
name "María López", role "Administrador", small green "En línea"
status dot.

TOP of content area: page title "Reglas de negocio", subtitle
"Parámetros del sistema (solo administradores).", button top-right:
filled blue "Editar configuración".

TAB BAR below the title: three tabs, "Reglas de pago", "Parámetros",
"Categorías" (active, underlined blue).

SUBTITLE below the tab bar: "Categorías de gasto permitidas por la
regla PAY-002. Toda solicitud fuera de esta lista se bloquea
automáticamente." Button top-right of this section: outlined "Agregar
categoría".

MAIN CONTENT: three category cards in a row, each a medium rounded
card with a colored icon badge at top, a bold category name, a short
description, and a small usage stat at the bottom:

- Blue icon badge (gear/cog): "OPERACIONES" / "Gastos operativos
  generales de la organización." / small bar "42% de las solicitudes".
- Purple icon badge (laptop/code): "SOFTWARE" / "Licencias, suscripciones
  y herramientas digitales." / small bar "35% de las solicitudes".
- Orange icon badge (suitcase/plane): "VIAJES" / "Viáticos, transporte
  y hospedaje por motivos de trabajo." / small bar "23% de las
  solicitudes".

Each card has a small green "Activa" pill top-right corner and a
subtle edit pencil icon bottom-right.

Below the three cards, a thin divider and a small gray note: "Estas
categorías son la política configurable del MVP, no una lista
universal — cambiarlas afecta inmediatamente la evaluación de la
regla PAY-002."

Composition: sharp UI elements, legible mock Spanish-language labels,
consistent 8px spacing grid, professional product-design portfolio
quality.
```

## 10. Logo — versión 3D

Referencia visual: [`logo/referencia-logo-3d.png`](../logo/referencia-logo-3d.png) (estilo 3D glossy, gradiente azul-verde, fondo claro de estudio). Adaptado a la paleta de FlowGuard: `#2F6FED` (acento) → `#22C55E` (el mismo verde semántico de `ALLOW`).

```
3D glossy rendered logo icon for "FlowGuard", a fintech payment-approval
security platform. Abstract shield silhouette made of curved, flowing
ribbon-like ridges — like fingerprint lines or sound waves — that
gradually morph into a stylized eye shape with a checkmark at the
bottom tip, suggesting "detect, verify, protect".

Material: smooth glossy 3D render, soft studio lighting, subtle
specular highlights and soft ambient occlusion shadows along each
ribbon edge, slight beveled/rounded thickness on every curve (not flat
vector), floating slightly above a clean, seamless, very light
neutral-gray studio background with a soft contact shadow beneath.

Color: gradient flowing diagonally through the shield — electric blue
#2F6FED at the top-left ribbons, transitioning smoothly through mid
blues to brand green #22C55E at the bottom-right where the eye and
checkmark sit, each ribbon colored by its position in the gradient
(no flat single color on any single ribbon).

Composition: centered, three-quarter front view, shield oriented
upright, symmetric overall silhouette, generous negative space around
it, square or landscape canvas, high-resolution product-render quality
suitable for an app icon, favicon, or hero graphic — no text, no
wordmark, no background pattern.
```

> Uso previsto: portada, landing, pitch deck — no el ícono plano chico que ya se usa adentro de la app (sidebar/favicon). Si se genera, considerar también una versión 2D simplificada con la misma forma para uso dentro de la UI.
