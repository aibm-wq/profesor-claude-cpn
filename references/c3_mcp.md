# C3 — Introduction to Model Context Protocol (MCP)
**Link Skilljar:** https://anthropic.skilljar.com/introduction-to-model-context-protocol
**Sesión grupal:** Sáb 28 JUN

---

## SECCIÓN 1-2 — ¿Qué es MCP?

**Concepto:**
MCP (Model Context Protocol) es el sistema estándar que permite a Claude conectarse con cualquier app o sistema externo de forma segura. Es el "idioma universal" que hablan Claude y las aplicaciones.

**Analogía:**
"Antes de los enchufes estándar, cada país tenía su propio sistema. MCP es como haber inventado el enchufe universal — Claude habla el mismo idioma con Odoo, con tu calendario, con Google Drive, con cualquier sistema."

**Ya lo están usando:**
Cuando Claude revisa el calendario, lee emails, o interactúa con Odoo — todo eso pasa a través de servidores MCP. Lo usan sin saberlo.

**La arquitectura básica:**
- **Cliente MCP:** Claude (el que usa, el que hace preguntas)
- **Servidor MCP:** La app externa (el que responde, el que da acceso)
- **Protocolo:** El lenguaje estándar entre los dos

**Los 3 puntos del quiz:**
1. MCP = sistema de conexión estandarizado entre Claude y apps externas.
2. Cliente MCP = Claude. Servidor MCP = la aplicación.
3. Cada integración (Odoo, Gmail, Calendar) = un servidor MCP separado.

---

## SECCIÓN 3-4 — Los Tres Componentes MCP

**1. TOOLS (Herramientas) — HACER**
Acciones que Claude puede ejecutar: buscar, crear, actualizar, eliminar.
Ejemplo: buscar_facturas(), crear_evento(), enviar_mensaje()

**2. RESOURCES (Recursos) — LEER**
Información que Claude puede consultar: documentos, bases de datos, archivos.
Ejemplo: leer el manual de procedimientos, consultar el historial de un cliente.

**3. PROMPTS (Plantillas) — INSTRUCCIONES**
Instrucciones pre-definidas para flujos de trabajo específicos.

**Analogía perfecta:**
"Claude es un asistente recién contratado. Tools = lo que puede hacer. Resources = lo que puede consultar. Prompts = los procedimientos escritos que debe seguir."

**Los 3 puntos del quiz:**
1. Tools = hacer (ejecutar acciones). Resources = leer (consultar). Prompts = instrucciones.
2. Un servidor MCP puede tener los tres componentes o solo algunos.
3. Claude decide cuándo y qué herramienta usar según el contexto.

---

## SECCIÓN 5-6 — Proyecto Completo y MCP Inspector

**Proyecto completo:**
Construir un servidor MCP que conecta Claude con una fuente de datos real. Incluye definir las Tools, los Resources, y las Prompts del servidor.

**MCP Inspector:**
Herramienta para probar que un servidor MCP funciona correctamente antes de conectarlo a Claude. Es como un panel de diagnóstico — verificas que todo funciona antes de ponerlo en producción.

**Cómo funciona el descubrimiento:**
El servidor MCP expone sus capacidades automáticamente — Claude las descubre solo al conectarse. No hay que decirle manualmente qué puede hacer.

**Los 3 puntos del quiz:**
1. MCP Inspector = herramienta de debugging/testing para servidores MCP.
2. El servidor MCP expone sus capacidades y Claude las descubre automáticamente.
3. Cada integración = un servidor MCP separado.

---

## QUIZ FINAL C3

**Repasa antes de intentar el quiz en Skilljar:**
- ¿Qué es MCP y para qué sirve?
- ¿Cuál es el cliente y cuál es el servidor en MCP?
- Diferencia entre Tools, Resources y Prompts
- ¿Para qué sirve el MCP Inspector?

**Puntaje mínimo:** 70% — puedes reintentar sin límite.
