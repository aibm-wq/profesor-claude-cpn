# C4 — Building with the Claude API
**Link Skilljar:** https://anthropic.skilljar.com/claude-with-the-anthropic-api
**Sesión grupal:** Sáb 5 JUL

**Nota para el Profesor:** Este curso tiene más código. Para el equipo no-técnico, el objetivo es entender los CONCEPTOS, no ejecutar el código. Con esta guía pueden aprobar el quiz perfectamente.

---

## SECCIÓN 1 — Primera llamada a la API

**Concepto:**
Una llamada a la API es enviarle un mensaje a Claude desde un programa y recibir respuesta. El programa no usa el chat — usa la "puerta trasera" directamente.

**Analogía:**
"Es como la diferencia entre llamar a un restaurante por teléfono (el chat) vs conectarte directo a su sistema de pedidos desde tu app (la API). El resultado es el mismo, pero tienes mucho más control."

**Conceptos clave:**
- **API key:** Tu contraseña personal de acceso. Nunca la compartas.
- **Modelo:** La versión de Claude que usas (claude-sonnet-4-6)
- **max_tokens:** Límite de longitud de la respuesta
- **Temperatura:** 0 = respuestas precisas/consistentes · 1 = más creativas/variadas

**Los 3 puntos del quiz:**
1. API key = contraseña de acceso. No compartir.
2. Temperatura 0 = preciso y consistente. Temperatura 1 = creativo y variable.
3. Una llamada a la API devuelve un objeto con el texto de la respuesta.

---

## SECCIÓN 2 — Prompt Engineering y Evaluaciones

**Prompt Engineering:**
Cómo escribir instrucciones que funcionen de manera confiable a escala — cuando miles de personas usan tu sistema.

**Técnicas clave:**
- **Sistema prompt:** instrucciones fijas que definen el comportamiento de Claude
- **XML tags:** estructuran la información para que Claude la procese mejor (`<contexto>`, `<tarea>`, `<ejemplo>`)
- **Few-shot examples:** mostrarle ejemplos de lo que quieres antes de pedirlo
- **Chain of thought:** pedirle que razone paso a paso antes de responder

**Evaluaciones (Evals):**
Pruebas automáticas que verifican si Claude está respondiendo correctamente. Como un test de calidad para tus prompts.

**Los 3 puntos del quiz:**
1. Sistema prompt = instrucciones que definen cómo se comporta Claude en toda la sesión.
2. XML tags estructuran la información. Claude los procesa mejor que texto sin estructura.
3. Eval = prueba automática de que Claude responde correctamente.

---

## SECCIÓN 3 — Tool Use

**Concepto:**
Claude puede usar herramientas externas (buscar en internet, consultar una base de datos, hacer un cálculo) ANTES de responder. No inventa — consulta.

**El flujo completo:**
1. Le defines qué herramientas tiene disponibles
2. Claude recibe la pregunta
3. Claude DECIDE si necesita usar una herramienta
4. Si sí → la usa → obtiene el dato real
5. Claude responde con esa información real

**Ejemplo:**
"¿Cuál es el tipo de cambio EUR/USD hoy?"
→ Claude no lo sabe (su entrenamiento tiene fecha)
→ Usa la herramienta `buscar_tipo_cambio()`
→ Obtiene el dato real → Responde correctamente

**Los 3 puntos del quiz:**
1. Tool use = Claude llamando funciones externas antes de responder.
2. Claude decide cuándo usar una herramienta — no siempre la usa.
3. El resultado de la herramienta se convierte en contexto para Claude.

---

## SECCIÓN 4 — RAG (Retrieval Augmented Generation)

**Concepto:**
RAG = darle a Claude acceso a tus documentos propios para que responda con información de tu empresa, no solo de su entrenamiento general.

**Analogía:**
"Contratas a un experto en tu industria. Sabe muchas cosas, pero no conoce tus SOPs específicos ni tus políticas internas. RAG es darle acceso a toda esa documentación — así responde con TU información."

**Ejemplo práctico:**
Si subes todos los procedimientos de contabilidad, Claude puede responder: "¿Cuál es el proceso para aprobar una factura mayor a $50,000?" — con la respuesta exacta según tus documentos.

**Conceptos técnicos (para el quiz):**
- **Embedding:** Representación matemática del texto que permite búsqueda por significado
- **Chunking:** Dividir documentos largos en partes manejables
- **Vector database:** Base de datos especial para búsqueda semántica

**Los 3 puntos del quiz:**
1. RAG = Claude responde con información de TUS documentos.
2. Embedding = representación matemática del texto para búsqueda.
3. Chunking = dividir documentos largos en fragmentos antes de indexarlos.

---

## SECCIÓN 5 — MCP en el contexto de la API

Repaso de MCP (mismo contenido del Curso 3) desde la perspectiva del desarrollador que construye las integraciones. Refuerza lo aprendido en C3.

**Punto clave nuevo:** Desde la API puedes conectar Claude a tus propios servidores MCP programáticamente, no solo desde Cowork.

---

## SECCIÓN 6 — Claude Code y Computer Use

**Repaso de Claude Code** (mismo contenido del Curso 1) +

**Computer Use:**
Claude puede ver y controlar una pantalla como si fuera un humano — hacer clic, escribir, navegar por apps. Útil para automatizar tareas en aplicaciones que no tienen API.

**Los 3 puntos del quiz:**
1. Computer Use = Claude usando el mouse y teclado como un humano.
2. Tool Use llama funciones. Computer Use controla la interfaz visual.
3. Computer Use es útil cuando no existe API pero sí interfaz gráfica.

---

## SECCIÓN 7 — Agents y Workflows

**Los 3 patrones principales:**

**1. CHAINING (Encadenamiento)**
El resultado de Claude A es el input de Claude B.
Ejemplo: Claude analiza un contrato → pasa el resumen → otro Claude redacta la respuesta.

**2. PARALLELIZATION (Paralelización)**
Varios Claude trabajando al mismo tiempo en partes del problema.
Ejemplo: 5 contratos a revisar → 5 instancias en paralelo → resultados combinados.

**3. ROUTING (Enrutamiento)**
Claude lee la solicitud y decide a cuál subagente enviarla.
Ejemplo: "¿Es esto legal, financiero o técnico?" → Claude clasifica → manda al agente especializado.

**Los 3 puntos del quiz:**
1. Chaining = el output de uno es el input del siguiente.
2. Parallelization = varios Claude trabajando al mismo tiempo.
3. Routing = Claude como director de tráfico — decide quién hace qué.

---

## QUIZ FINAL C4

**Repasa antes de intentar el quiz en Skilljar:**
- ¿Qué es la temperatura y cómo afecta las respuestas?
- ¿Qué es Tool Use y cuándo lo usa Claude?
- ¿Qué es RAG y cómo funciona?
- Los 3 patrones de agentes: chaining, parallelization, routing
- Diferencia entre Tool Use y Computer Use

**Puntaje mínimo:** 70% — puedes reintentar sin límite.

---

## GLOSARIO RÁPIDO (para consultar en cualquier sesión)

| Término | Significado simple |
|---------|-------------------|
| API | La "puerta" para acceder a Claude desde un programa |
| API key | Tu contraseña personal de acceso |
| Token | La unidad básica de texto. ~1 token = ¾ de palabra |
| Context window | Cuánto texto puede recordar Claude en una conversación |
| CLAUDE.md | El manual de instrucciones de tu empresa para Claude |
| Skill | Receta guardada que Claude ejecuta cuando aplica |
| Hook | Acción automática antes/después de algo que hace Claude |
| MCP | Sistema de conexión entre Claude y apps externas |
| RAG | Claude respondiendo desde TUS documentos |
| Tool use | Claude usando funciones externas antes de responder |
| Agent | Claude tomando decisiones autónomas en múltiples pasos |
| Embedding | Representación matemática del texto para búsqueda |
| Temperatura | Qué tan creativo es Claude: 0 = preciso, 1 = variado |
| Sistema prompt | Instrucciones fijas que definen el comportamiento de Claude |
| Chaining | Output de Claude A → Input de Claude B |
| Routing | Claude decide a qué agente especializado enviar la tarea |
