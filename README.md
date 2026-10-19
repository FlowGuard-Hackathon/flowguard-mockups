# flowguard-mockups

Referencias visuales de FlowGuard: así es como se va a ver la app. Sirve para que todo el equipo —sobre todo Dev 2— tenga la misma idea en la cabeza antes de implementar el diseño real en `flowguard-app`.

**Este repo es solo diseño, no código.** No bloquea nada del desarrollo: el frontend ya funciona con un layout mínimo (ver [flowguard-app](https://github.com/FlowGuard-Hackathon/flowguard-app)); estas imágenes son el objetivo visual al que apuntar, no un requisito para avanzar.

## Qué hay aquí

| Carpeta | Contenido |
|---|---|
| [`pantallas/`](pantallas/) | Las imágenes generadas (mockups PNG) |
| [`logo/`](logo/) | Referencias e imágenes del logo |
| [`prompts/prompts-imagenes.md`](prompts/prompts-imagenes.md) | Los prompts de generación de imagen de cada pantalla y del logo, para regenerarlas o generar las que faltan |

## Las 9 pantallas del producto

1. Login
2. Dashboard (Panel de supervisión)
3. Solicitudes de pago (lista)
4. Detalle de solicitud (bloqueada)
5. Simulador de aprobación
6. Centro de evidencias
7. Historial de ejecuciones
8. Gestión de usuarios
9. Configuración — con 3 pestañas: Reglas de pago, Parámetros, Categorías

Estado de cada una (qué ya tiene imagen y qué solo tiene prompt pendiente) en la tabla de [`prompts/prompts-imagenes.md`](prompts/prompts-imagenes.md#estado).

## Estilo visual (resumen)

- Tema oscuro, fondo navy profundo `#0F1B2D`, acento azul eléctrico `#2F6FED`.
- Semántica de decisión: verde `ALLOW`, rojo `BLOCK`, ámbar `INDETERMINATE` — siempre distinto del azul de marca.
- Sidebar fijo a la izquierda con navegación + usuario logueado abajo.
- Logo: escudo con check + wordmark "FlowGuard" + tagline "DETECT · VERIFY · PROTECT".

## Reglas de este repo

- **No inventar reglas de negocio nuevas.** Todo lo que aparece en los mockups (reglas `PAY-001..005`, categorías `OPERACIONES/SOFTWARE/VIAJES`, estados `ALLOW/BLOCK/INDETERMINATE`) debe coincidir con [flowguard-docs](https://github.com/FlowGuard-Hackathon/flowguard-docs). Si un mockup muestra algo que no está en la documentación técnica, se corrige el mockup, no al revés.
- **No mostrar infraestructura al usuario final.** Se descartó a propósito una pestaña "Integraciones" en Configuración (detalles de Supabase/Nebius) — eso es información operativa, no algo que un administrador de negocio deba ver desde la app.
- Las imágenes son de **referencia**, no el diseño final pixel-perfect — Dev 2 decide la implementación real en `flowguard-app`.

## Otros repositorios de FlowGuard-Hackathon

| Repositorio | Contenido |
|---|---|
| [`flowguard-docs`](https://github.com/FlowGuard-Hackathon/flowguard-docs) | Documentación técnica — la fuente de verdad de reglas, contratos y arquitectura |
| [`flowguard-app`](https://github.com/FlowGuard-Hackathon/flowguard-app) | Frontend real (Next.js) |
| [`flowguard-src`](https://github.com/FlowGuard-Hackathon/flowguard-src) | Backend: motor de reglas, persistencia, agente |
| [`flowguard-supabase`](https://github.com/FlowGuard-Hackathon/flowguard-supabase) | Esquema de base de datos |
| [`flowguard-mocks`](https://github.com/FlowGuard-Hackathon/flowguard-mocks) | Fixtures de datos de prueba |
| [`flowguard-tests`](https://github.com/FlowGuard-Hackathon/flowguard-tests) | Pruebas |
| [`flowguard`](https://github.com/FlowGuard-Hackathon/flowguard) | Repositorio combinado final |
