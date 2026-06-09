# C1 — Claude Code in Action
**Link Skilljar:** https://anthropic.skilljar.com/claude-code-in-action
**Sesión grupal:** Sáb 21 JUN

---

## MÓDULO 1 — ¿Qué es Claude Code?

**Concepto:**
Claude Code no es el chat del navegador. Es Claude funcionando DENTRO de tu computadora — puede leer tus archivos, editarlos, ejecutar programas, y hacer cambios reales. No solo conversa: actúa.

**Analogía:**
"Es la diferencia entre llamarle a tu asistente por teléfono (eso es claude.ai) vs tenerlo sentado contigo en la oficina con acceso a tus archivos, tu Odoo, y tu carpeta de proyectos (eso es Claude Code)."

**Ejemplo concreto:**
El Cowork que usan todos los días — eso es Claude Code en acción. Cuando Claude lee un archivo, crea un reporte, o ejecuta un script de Python, lo hace con Claude Code.

**Los 3 puntos del quiz:**
1. Claude Code ≠ claude.ai. Claude Code ACTÚA, claude.ai solo conversa.
2. Claude Code necesita una terminal (línea de comandos) para funcionar.
3. Claude Code puede leer archivos, ejecutar código, y hacer cambios reales en tu computadora.

---

## MÓDULO 2 — Setup y Contexto (CLAUDE.md)

**Concepto:**
CLAUDE.md es el manual de instrucciones de tu empresa para Claude. Se lo das una vez y Claude lo recuerda en cada sesión de trabajo.

**Analogía:**
"Es como el documento de onboarding que le das a un empleado nuevo — quién eres, cómo trabajamos, qué reglas seguimos, qué sistemas usamos. Pero este empleado lo lee perfectamente y nunca lo olvida."

**Ejemplo concreto:**
Un archivo CLAUDE.md puede tener: quién eres, los proyectos activos, los scripts de Odoo, las reglas de respuesta. Por eso Claude sabe desde el primer mensaje cómo ayudar sin que nadie explique nada.

**Los 3 puntos del quiz:**
1. CLAUDE.md = contexto permanente del proyecto. Siempre activo.
2. Puedes tener un CLAUDE.md por empresa o por cliente (contexto separado).
3. "Adding context" = darle a Claude más información para trabajar mejor.

---

## MÓDULO 3 — Custom Commands y MCP Servers

**Custom Commands:**
Son atajos reutilizables. Escribes `/cierre-dia` y Claude sabe exactamente qué hacer — registrar el día, revisar pendientes, actualizar el vault. No tienes que explicarlo cada vez.

**MCP Servers:**
Son los "conectores" que le permiten a Claude hablar con apps externas — tu calendario, tus emails, Odoo, Google Drive — sin que copies y pegues información manualmente.

**Analogía MCP:**
"MCP es como un cable USB universal. En vez de hacer una conexión especial para cada app, MCP crea un lenguaje común para que Claude se conecte a cualquier sistema."

**Ejemplo concreto:**
Cuando Claude revisa el calendario, lee emails o actualiza un proyecto en Odoo — todo eso pasa vía servidores MCP.

**Los 3 puntos del quiz:**
1. Custom commands = atajos (/nombre). Se definen una vez, se usan siempre.
2. MCP = sistema de conexión entre Claude y apps externas.
3. Servidor MCP = el conector. Claude es el cliente que lo usa.

---

## MÓDULO 4 — Hooks y el SDK

**Hooks:**
Una regla automática que corre ANTES o DESPUÉS de que Claude haga algo. No tienes que pedírselo — pasa solo.

**Analogía:**
"Un hook es como una alarma automática — 'cada vez que Claude termine de editar un archivo, guarda una copia de respaldo.' Sin recordatorios, sin instrucciones extra."

**Ejemplos reales:**
- Al terminar una tarea larga → notificación al equipo
- Antes de enviar un mensaje → verificar que no hay datos sensibles
- Después de crear un archivo → registrarlo en el tracker

**El SDK:**
El kit de herramientas para programadores que quieren construir sistemas más complejos con Claude Code. Para el usuario no-técnico: solo entender qué es, no cómo usarlo.

**Los 3 puntos del quiz:**
1. Hook = acción automática que ocurre antes/después de algo que Claude hace.
2. Hay PreTool hooks (antes) y PostTool hooks (después).
3. SDK = para desarrolladores. No es necesario para el uso diario.

---

## MÓDULO 5 — Quiz Final C1

**Repasa antes de intentar el quiz en Skilljar:**
- Claude Code vs claude.ai: ¿cuál actúa, cuál solo conversa?
- CLAUDE.md: ¿qué es, para qué sirve?
- Custom commands: ¿qué son, cómo se activan?
- MCP: ¿qué conecta con qué?
- Hooks: ¿cuándo corren, qué hacen?

**Tip de oro:** Si el quiz pregunta sobre diferencias, siempre piensa en "qué puede hacer Claude Code que claude.ai no puede."

**Puntaje mínimo para aprobar:** 70% — puedes reintentar sin límite.
