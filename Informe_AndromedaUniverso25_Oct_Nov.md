# INFORME RESUMEN ANDROMEDA — ANÁLISIS DEFENSIVO DE CANALES TELEGRAM (OCT–NOV 2026)

**Clasificación:** OSINT / Análisis defensivo de amenazas
**Periodo del volcado:** 2025-12-05 a 2026-11-21 (fechas de los mensajes)
**Fecha de compilación:** 2026-11-22
**Fuente:** Volcado de scraping de canales públicos de Telegram
**Estado:** Sin verificación independiente. Contenido atribuido a la fuente original.

---

## ⚠️ ADVERTENCIA ÉTICA Y DE USO

Este documento es **análisis defensivo de fuentes públicas**. **No contiene datos personales, credenciales, enlaces a foros criminales, ni acceso a datos filtrados.** No facilita la comisión de delitos ni la amplificación de campañas de desinformación.

Su propósito es exclusivamente **defensivo**: permitir a analistas, SOC y equipos de concienciación comprender las **tácticas, técnicas y procedimientos (TTPs)** y las **narrativas** de actores de amenaza, sin reproducir el contenido de sus ataques.

**Bajo ninguna circunstancia** debe utilizarse este material para:
- Acceder a datos filtrados.
- Contactar a los actores.
- Amplificar leaks o propaganda.
- Facilitar acceso a foros criminales.

Los indicadores aquí listados son de **actividad narrativa**, no artefactos técnicos verificados. Se marcan explícitamente como tales.

---

## 0. COBERTURA DEL ANÁLISIS

El volcado contiene mensajes parseados de **11 canales con contenido real**. Los canales que solo devuelven error ("No se pudo obtener mensajes") se descartan por no aportar contenido. El archivo declara un barrido de 737 canales, pero se trunca en el canal 30/737.

### 0.1. Canales analizados (handle público + periodo + temática)

| Handle | Periodo | Temática | Nivel de análisis |
|---|---|---|---|
| `QuietSecRUS` | 2026-10-14 a 2026-11-21 | Hacktivismo prorruso contra infraestructura ucraniana | TTPs + narrativa |
| `QuietSecurity` | 2026-08-16 a 2026-11-10 | Hacktivismo prorruso contra instituciones europeas | TTPs + narrativa |
| `Qxcyber666` | 2026-11-10 a 2026-11-21 | Hacktivismo/DDoS en Sudeste Asiático | TTPs + narrativa |
| `xzarussec` | 2026-10-28 a 2026-11-09 | DDoS contra infraestructura israelí | TTPs + narrativa |
| `unknown_cambodia` | 2026-11-08 a 2026-11-21 | Hacktivismo camboyano + scam alerts | Narrativa |
| `K3YOFFF4CE` | 2026-11-06 | Hacktivismo camboyano (canal nuevo) | Narrativa |
| `bnbshnick` | 2026-11-15 a 2026-11-21 | Propaganda estatal rusa (FSB) | Narrativa |
| `atodapotencia` | 2026-11-21 | Propaganda rusa (decadencia europea) | Narrativa |
| `z_arhiv` | 2026-11-17 a 2026-11-21 | Mapas de guerra prorrusos (Ucrania) | Narrativa |
| `hackhaxx` | 2026-01-29 a 2026-02-06 | Canal adaptador (sin contenido operativo) | Descartado por bajo valor |
| `Super007X` | 2026-11-21 | Apuestas/leaks (posible ruido) | Descartado por bajo valor |

### 0.2. Canales descartados (solo fallback, sin contenido)

`qxcyberchat`, `tribute`, `+5Q-AbruRPvs1ODg1`, `tass_es53577`.

### 0.3. Nota sobre la sanitización

Este informe **no incluye**:
- Enlaces a foros criminales ni a mensajes que anuncien leaks.
- Nombres de víctimas concretas con detalle.
- Volúmenes exactos de datos filtrados.
- Enlaces directos a herramientas maliciosas.

Se sustituyen por descripciones genéricas y por el handle del canal + fecha, que es suficiente para trazabilidad sin facilitar acceso.

---

## 1. RESUMEN EJECUTIVO (BLUF)

Entre octubre y noviembre de 2026, los canales analizados muestran un ecosistema de **hacktivismo prorruso, cibercriminalidad y propaganda estatal** con los siguientes ejes:

1. **Ataques a infraestructura ucraniana** (servicios de registro militar, mensajería táctica, clínicas médicas, sistemas eléctricos, instituciones europeas).
2. **DDoS y defacements** contra Israel, Tailandia y Camboya.
3. **Leaks de datos** de gobiernos y empresas (Marruecos, Camboya, Francia, Ucrania).
4. **Propaganda estatal rusa** (FSB, mapas de guerra, decadencia europea).
5. **Hacktivismo camboyano** (guerra Khmer vs Khmer, canales nuevos).

**Evento de mayor relevancia operativa:** el acceso y corte de energía en sistemas de generadores y subestaciones en una región de Ucrania, reportado por `QuietSecRUS`.

**Evento de mayor relevancia estratégica:** el hackeo de servicios de registro militar y mensajería táctica de las Fuerzas Armadas de Ucrania, reportado por `QuietSecRUS`.

**Actor de mayor actividad:** `Qxcyber666` (DDoS, defacements, leaks, hackeo de base de datos militar tailandesa).

**Campaña de mayor impacto:** `QuietSecRUS` / `QuietSecurity` (hacktivismo prorruso contra infraestructura ucraniana y europea).

**Limitación principal:** ningún evento está verificado de forma independiente. La mayoría son declaraciones de partes interesadas.
```

## 2. TÁCTICAS, TÉCNICAS Y PROCEDIMIENTOS (TTPs) OBSERVADOS

> **Nota:** se describen TTPs a alto nivel, sin detalles operativos que permitan replicarlos.

### 2.1. Hacktivismo prorruso contra infraestructura ucraniana (`@QuietSecRUS`, `@QuietSecurity`)

| TTP | Descripción | Evidencia (handle + fecha) | MITRE ATT&CK |
|---|---|---|---|
| Acceso a servicios de registro militar | Compromiso de servicios de registro y mensajería táctica de las FFAA ucranianas | `QuietSecRUS`, 2026-10-14 | T1190 (Exploit Public-Facing Application) |
| Acceso a sistemas de control industrial | Acceso a sistemas de monitoreo de generadores y subestaciones eléctricas | `QuietSecRUS`, 2026-10-14 | T1078 (Valid Accounts), T1059 (Command and Scripting) |
| Acceso a clínicas médicas | Compromiso de paneles administrativos de clínicas y laboratorios | `QuietSecRUS`, 2026-10-14 | T1190, T1078 |
| Ataque a institución europea | Interrupción de servicio de la Fiscalía Europea (ePPO) | `QuietSecurity`, 2026-11-08 | T1489 (Service Stop) |
| Ataque a app civil de alertas | Interrupción de app de alertas aéreas ucraniana (Veleta) | `QuietSecurity`, 2026-11-09 | T1489 |
| Leak de datos de empresa | Publicación de datos de tienda de lujo ucraniana | `QuietSecurity`, 2026-11-21 | T1530 (Data from Cloud Storage) |
| Narrativa de "huelga" | Uso de lenguaje de "huelga" y "gloria a Rusia" para enmarcar ataques | `QuietSecRUS`, varios | T1585 (Establish Accounts) |

### 2.2. Hacktivismo/DDoS en Sudeste Asiático (`Qxcyber666`, `xzarussec`)

| TTP | Descripción | Evidencia (handle + fecha) | MITRE ATT&CK |
|---|---|---|---|
| DDoS a infraestructura gubernamental | Ataques DDoS a sitios de gobierno (Israel, Zimbabue) | `xzarussec`, 2026-10-31; `Qxcyber666`, 2026-11-13 | T1498 (Network Denial of Service) |
| Defacement de sitios | Modificación de páginas web de empresas y gobiernos | `Qxcyber666`, 2026-11-18 | T1491 (Defacement) |
| Hackeo de base de datos militar | Compromiso de sistema de base de datos militar tailandés | `Qxcyber666`, 2026-11-19 | T1190, T1078 |
| Leak de datos gubernamentales | Publicación de datos de ministerios camboyanos | `Qxcyber666`, 2026-11-17 | T1530 |
| Uso de "proof" de DDoS | Enlaces a servicios de monitoreo (check-host.net) como prueba | `xzarussec`, varios | T1585 |

### 2.3. Hacktivismo camboyano (`unknown_cambodia`, `K3YOFFF4CE`)

| TTP | Descripción | Evidencia (handle + fecha) | MITRE ATT&CK |
|---|---|---|---|
| Creación de canales nuevos | Canales creados para campañas de hacktivismo | `K3YOFFF4CE`, 2026-11-06; `unknown_cambodia`, 2026-11-08 | T1585 |
| Narrativa de guerra Khmer vs Khmer | Encuadre de conflicto interno camboyano | `unknown_cambodia`, 2026-11-08 | T1585 |
| Scam alerts | Publicación de alertas de estafa (posible ruido o servicio) | `unknown_cambodia`, 2026-11-21 | - |

### 2.4. Propaganda estatal rusa (`@bnbshnick`, `@atodapotencia`, `@z_arhiv`)

| TTP | Descripción | Evidencia (handle + fecha) | MITRE ATT&CK |
|---|---|---|---|
| Narrativa de "operación frustrada" | Presentación de operaciones del FSB como exitosas | `bnbshnick`, 2026-11-17 | T1585 |
| Narrativa de decadencia europea | Reportajes sobre condiciones militares en Noruega | `atodapotencia`, 2026-11-21 | T1585 |
| Mapas de guerra con cifras | Actualizaciones diarias de avances territoriales | `z_arhiv`, 2026-11-17 a 2026-11-21 | T1585 |
| Casos históricos (Litvinenko/Skripal) | Uso de casos históricos para narrativa anti-occidental | `bnbshnick`, 2026-11-19 | T1585 |

### 2.5. Leaks de datos (marruecos, francia, ucrania)

| TTP | Descripción | Evidencia (handle + fecha) | MITRE ATT&CK |
|---|---|---|---|
| Leak de datos de salud | Publicación de datos de programa de asistencia médica marroquí | `jabaroot_off`, 2026-08-24 | T1530 |
| Leak de datos de inteligencia | Publicación de datos de agentes de inteligencia marroquí | `jabaroot_off`, 2026-08-24 | T1530 |
| Brechas en sitios franceses | Compromiso de sitios web franceses con datos de usuarios | `xvdpx1`, 2026-08-11 a 2026-08-23 | T1190, T1530 |
| Leak de datos de tienda ucraniana | Publicación de datos de usuarios de tienda de lujo | `QuietSecurity`, 2026-11-21 | T1530 |

> **Nota:** los volúmenes exactos, nombres de víctimas y enlaces a los leaks **se omiten deliberadamente** por ética y para no facilitar su acceso.

---

## 3. NARRATIVAS IDENTIFICADAS

### Esquema 1: Flujo de la narrativa

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         FLUJO DE LA NARRATIVA                                │
└─────────────────────────────────────────────────────────────────────────────┘

  [Evento real o reportado]
            │
            ▼
  ┌─────────────────────┐
  │  SELECCIÓN          │  Se eligen eventos que encajan en la narrativa.
  │  (¿Qué se publica?) │  Se omiten éxitos del adversario.
  └─────────────────────┘
            │
            ▼
  ┌─────────────────────┐
  │  ENCUADRE           │  "Rusia responde", "OTAN agrede",
  │  (¿Cómo se cuenta?) │  "Occidente decae", "Ucrania colapsa".
  └─────────────────────┘
            │
            ▼
  ┌─────────────────────┐
  │  AMPLIFICACIÓN      │  Multiplicación en canales aliados.
  │  (¿Quién lo difunde?)│
  └─────────────────────┘
            │
            ▼
  ┌─────────────────────┐
  │  LEGITIMACIÓN       │  Cita de fuentes (Mash, FSB, check-host.net)
  │  (¿Quién lo avala?) │  para dar apariencia de verdad.
  └─────────────────────┘
            │
            ▼
  ┌─────────────────────┐
  │  ACCIÓN             │  Influir en opinión pública, justificar ataques,
  │  (¿Para qué?)       │  erosionar confianza institucional, reclutar.
  └─────────────────────┘
```

| Narrativa | Canales | Técnica | Objetivo | Nivel de evidencia |
|---|---|---|---|---|
| Ucrania es agresor | QuietSecRUS, QuietSecurity | Victimización + escalada | Justificar represalias | Bajo (solo fuente prorrusa) |
| Israel es agresor | xzarussec | DDoS + hashtags | Probar respuesta israelí | Bajo |
| Tailandia reprime | Qxcyber666 | Defacement + DDoS | Justificar ataques | Bajo |
| Camboya es fuerte | unknown_cambodia, K3YOFFF4CE | Hacktivismo + leak | Proyectar poder regional | Bajo |
| Occidente decae | atodapotencia, bnbshnick | Schadenfreude + propaganda | Desmoralizar apoyo a Ucrania | Bajo |
| Marruecos es corrupto | jabaroot_off | Leak masivo | Desestabilizar | Bajo |
| Francia es vulnerable | xvdpx1 | Brechas + leaks | Demostrar capacidad | Bajo |
| Rusia avanza | z_arhiv | Mapas + cifras | Justificar victoria | Bajo |

---

## 4. MATRIZ DE CORROBORACIÓN

| Evento | Fuente en volcado | Fuente citada | ¿Verificado? | Confianza |
|---|---|---|---|---|
| Hackeo de servicios militares ucranianos | QuietSecRUS | Mash, DarkWarios | No | Bajo |
| Corte de energía en región ucraniana | QuietSecRUS | PerunSwaroga | No | Bajo |
| Ataque a ePPO | QuietSecurity | Propia | No | Bajo |
| Hackeo de base militar tailandesa | Qxcyber666 | Propia | No | Bajo |
| Leak de gobiernos camboyanos | Qxcyber666 | Foro criminal (redactado) | No | Bajo |
| Leak de tienda ucraniana | QuietSecurity | PerunSwaroga | No | Bajo |
| Leak de programa de salud marroquí | jabaroot_off | Propia | No | Bajo |
| Leak de agencia de inteligencia marroquí | jabaroot_off | Foro criminal (redactado) | No | Bajo |
| Brechas en sitios franceses | xvdpx1 | Propia | No | Bajo |
| DDoS a Israel | xzarussec | check-host.net | Parcial (proof) | Medio |
| Ataque a app de alertas ucraniana | QuietSecurity | Propia | No | Bajo |
| Operación "Web 2.0" frustrada | bnbshnick | FSB | No | Bajo |
| Hacktivismo camboyano | unknown_cambodia, K3YOFFF4CE | Propia | No | Bajo |
| Mapas de guerra Ucrania | z_arhiv | Propia | No | Bajo |
| Condiciones militares en Noruega | atodapotencia | Forsvarets Forum | Parcial (fuente citada) | Medio |

**Conclusión:** Ningún evento está verificado de forma independiente. La mayoría se apoya en fuentes propias o partes interesadas. Confianza baja, salvo DDoS con proof de check-host.net y Noruega con fuente citada.
```

## 5. INDICADORES DE ACTIVIDAD NARRATIVA (IOCs)

> **Nota:** estos indicadores son de **actividad narrativa**, no artefactos técnicos. No incluyen enlaces a foros criminales, mensajes de leak ni datos personales. Su valor es contextual y de baja fidelidad.

### 5.1. Canales de Telegram (handles públicos)

| Handle | Tipo | Temática | Confianza | Acción |
|---|---|---|---|---|
| `QuietSecRUS` | Canal Telegram | Hacktivismo prorruso | Alta | Monitorizar |
| `QuietSecurity` | Canal Telegram | Hacktivismo prorruso | Alta | Monitorizar |
| `Qxcyber666` | Canal Telegram | Hacktivismo/DDoS | Alta | Monitorizar |
| `xzarussec` | Canal Telegram | DDoS Israel | Alta | Monitorizar |
| `unknown_cambodia` | Canal Telegram | Hacktivismo Camboya | Media | Monitorizar |
| `K3YOFFF4CE` | Canal Telegram | Hacktivismo Camboya | Media | Monitorizar |
| `bnbshnick` | Canal Telegram | Propaganda FSB | Alta | Monitorizar |
| `atodapotencia` | Canal Telegram | Propaganda rusa | Media | Monitorizar |
| `z_arhiv` | Canal Telegram | Mapas guerra Ucrania | Media | Monitorizar |

### 5.2. Hashtags y marcadores narrativos

| Valor | Tipo | Contexto | Confianza | Acción |
|---|---|---|---|---|
| `#QXCYBER` | Hashtag | Hacktivismo QX-CYBER | Baja | Monitorizar volumen |
| `#XZARUSSEC` | Hashtag | Hacktivismo XZARUSSEC | Baja | Monitorizar volumen |
| `#H3C4KEDZ` | Hashtag | Hacktivismo H3C4KEDZ | Baja | Monitorizar volumen |
| `#K3YOFFF4CE` | Hashtag | Hacktivismo camboyano | Baja | Monitorizar volumen |
| `#DIVINEASTRA` | Hashtag | Hacktivismo | Baja | Monitorizar volumen |
| `#Empire01Sec` | Hashtag | Hacktivismo | Baja | Monitorizar volumen |
| `#PerunSwaroga` | Hashtag | Hacktivismo prorruso | Baja | Monitorizar volumen |
| `#GloryToRussia` | Hashtag | Propaganda prorrusa | Baja | Monitorizar volumen |
| `#FreePalestine` | Hashtag | Hacktivismo propalestino | Baja | Monitorizar volumen |
| `#opzionis` | Hashtag | Operación anti-Israel | Baja | Monitorizar volumen |

### 5.3. Términos de búsqueda para monitorización (OSINT)

| Término | Contexto | Acción |
|---|---|---|
| `Reserva+` + `Milchat` | Hackeo servicios militares ucranianos | Búsqueda OSINT |
| `Ivano-Frankivsk` + `generadores` | Hackeo energía Ucrania | Búsqueda OSINT |
| `ePPO` + `hackeado` | Ataque Fiscalía Europea | Búsqueda OSINT |
| `Royal Thai Army` + `hackeado` | Hackeo base militar tailandesa | Búsqueda OSINT |
| `RAMED` + `leak` | Leak programa salud Marruecos | Búsqueda OSINT |
| `DGST` + `leak` | Leak agencia inteligencia Marruecos | Búsqueda OSINT |
| `K3YOFF F4CE` | Hacktivismo Camboya | Búsqueda OSINT |
| `unknown_cambodia` | Hacktivismo Camboya | Búsqueda OSINT |

---

## 6. MAPEO MITRE ATT&CK (ADAPTADO A INFLUENCIA)

> **Nota:** MITRE ATT&CK está diseñado para comportamiento de adversarios cibernéticos. El mapeo siguiente adapta sus tácticas al **comportamiento de actores de influencia**. Se indica la limitación en cada caso.

| Táctica ATT&CK | Técnica | Comportamiento observado | Limitación |
|---|---|---|---|
| **Reconocimiento (TA0043)** | T1592 | Monitorización de infraestructura ucraniana/israelí/tailandesa | Reconocimiento narrativo, no técnico |
| **Desarrollo de Recursos (TA0042)** | T1585 | Canales de Telegram consolidados | Los canales ya existen |
| **Acceso Inicial (TA0001)** | T1566 | Difusión de enlaces a leaks y foros | Captación de audiencia, no phishing técnico |
| **Ejecución (TA0002)** | T1204 | El usuario debe hacer clic en enlaces | Ejecución narrativa, no de código |
| **Persistencia (TA0003)** | T1136 | Suscripción a canales; migración a nuevos canales | Persistencia de audiencia |
| **Evasión de Defensa (TA0005)** | T1027 | Encuadres selectivos, omisión de contexto | Ofuscación narrativa |
| **Colección (TA0009)** | T1598 | Solicitud de suscripciones, interacción | Recolección de audiencia |
| **Comando y Control (TA0011)** | T1105 | Distribución de enlaces a Odysee, X, Facebook | C2 narrativo |
| **Impacto (TA0040)** | T1565 | Edición de declaraciones para alterar percepción | Manipulación informativa |

**Técnicas de influencia adicionales (no mapeadas a ATT&CK):**
- Amplificación de leaks reales para erosionar confianza.
- Legitimación de actores hostiles mediante encuadre de represalia.
- Deshumanización del adversario mediante lenguaje emotivo.
- Inversión de roles (Rusia como víctima, Ucrania como agresor).
- Catastrofismo demográfico.
- DDoS como arma de propaganda.

---

## 7. EVALUACIÓN DE RIESGO (PERSPECTIVA DEFENSIVA)

| Riesgo | Probabilidad | Impacto | Nivel | Recomendación |
|---|---|---|---|---|
| Hackeo de infraestructura militar ucraniana | Alta | Alto | **Crítico** | Monitorizar CISA/SSSCIP |
| Leak de datos de inteligencia (Marruecos) | Media | Alto | **Alto** | Verificar con fuentes marroquíes |
| Leak de datos de salud (Marruecos) | Media | Alto | **Alto** | Monitorizar HHS/ONP |
| Brechas en sitios franceses | Alta | Medio | **Alto** | Monitorizar CNIL/ANSSI |
| Ataque a ePPO | Media | Alto | **Alto** | Verificar con Europol |
| Hackeo de base militar tailandesa | Media | Alto | **Alto** | Monitorizar NCSC Tailandia |
| Leak de gobiernos camboyanos | Media | Alto | **Alto** | Monitorizar CERT Camboya |
| DDoS a Israel | Alta | Medio | **Medio** | Monitorizar INCD Israel |
| Propaganda FSB | Alta | Bajo | **Medio** | Concienciación |
| Hacktivismo camboyano | Media | Medio | **Medio** | Monitorizar CERT Camboya |
| Mapas de guerra prorrusos | Alta | Bajo | **Bajo** | Monitorizar DeepState/ISW |

---

## 8. LAGUNAS DE INFORMACIÓN (GAPS)

1. **No hay verificación independiente** de los hechos reportados. La mayoría son declaraciones de partes interesadas.
2. **El volcado tiene codificación corrupta** (mojibake) en caracteres cirílicos y emojis.
3. **No se incluyen fechas exactas** para algunos eventos.
4. **No hay evidencia técnica** (hashes, IPs, dominios maliciosos) en el volcado.
5. **La atribución de los ataques** proviene de las mismas fuentes que los reportan.
6. **No se enlazan las fuentes citadas** (Mash, FSB, check-host.net, foros criminales) por razones éticas.
7. **Faltan los mensajes completos** de algunos canales (fallback fallido).
8. **No hay contexto sobre la autoría** de los canales ni su vinculación con actores estatales.
9. **No se analiza la audiencia** ni el alcance de los canales.
10. **No se comparan las narrativas** con medios occidentales.
11. **El archivo se trunca** en canal 30/737.

---

## 9. RECOMENDACIONES

### Para SOC / Threat Intelligence
- **No bloquear** los canales de Telegram a nivel de red; son fuentes de monitorización, no malware.
- **Monitorizar** los términos de búsqueda de la sección 5.3.
- **Cruzar** los eventos con fuentes primarias (CISA, SSSCIP, Europol, CERT Camboya, INCD Israel).
- **Enriquecer** los IOCs narrativos con datos de alcance si se dispone de acceso.
- **Automatizar** la monitorización mediante herramientas OSINT éticas.

### Para equipos de concienciación
- Utilizar las narrativas de la sección 3 como ejemplos de **manipulación informativa**.
- Enfatizar la **falta de verificación** y el uso de **encuadres selectivos**.
- Explicar el **flujo de la narrativa** (esquema 1) como modelo de desinformación.

### Para liderazgo
- El riesgo principal no es técnico, sino **reputacional y de escalada**.
- **No amplificar** el contenido. La monitorización debe ser silenciosa y defensiva.
- **Documentar** la evolución de la narrativa para análisis posteriores.

---

## 10. FUENTES Y TRAZABILIDAD

| Fuente | Tipo | Identificador | Fecha de acceso |
|---|---|---|---|
| `QuietSecRUS` | Canal Telegram | Handle público | 2026-11-21 |
| `QuietSecurity` | Canal Telegram | Handle público | 2026-11-21 |
| `Qxcyber666` | Canal Telegram | Handle público | 2026-11-21 |
| `xzarussec` | Canal Telegram | Handle público | 2026-11-09 |
| `unknown_cambodia` | Canal Telegram | Handle público | 2026-11-21 |
| `K3YOFFF4CE` | Canal Telegram | Handle público | 2026-11-06 |
| `bnbshnick` | Canal Telegram | Handle público | 2026-11-21 |
| `atodapotencia` | Canal Telegram | Handle público | 2026-11-21 |
| `z_arhiv` | Canal Telegram | Handle público | 2026-11-21 |
| Volcado original | Archivo de texto | No público | 2026-11-22 |

**Metodología:** Lectura manual del volcado, identificación de TTPs y narrativas, estructuración en secciones CTI, mapeo ATT&CK adaptado a influencia, generación de IOCs narrativos, correlación temporal y temática, matriz de corroboración.

**Limitación metodológica:** El volcado presenta corrupción de codificación (mojibake). Se ha interpretado el contenido por contexto. No se ha realizado traducción automática ni verificación externa.

---

## 11. DECLARACIÓN DE INTEGRIDAD

Este informe se ha elaborado siguiendo los principios de **inteligencia ética**:
- **Atribución clara** de todas las afirmaciones a sus fuentes originales.
- **No amplificación** de propaganda: el contenido se cita para análisis, no para difusión.
- **No facilitación** de acceso a datos filtrados, foros criminales ni herramientas maliciosas.
- **Transparencia sobre limitaciones** y falta de verificación.
- **Uso exclusivamente defensivo** del material.

**El repositorio no se hace responsable del uso indebido de este informe.**

---

*Fin del Informe Resumen Andromeda — 2026-11-22*
