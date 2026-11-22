# INFORME ANDROMEDA UNIVERSO 25 — MONITOR DDoS: GRUPOS DETECTADOS (2026-11-22)

**Clasificación:** OSINT / Análisis defensivo de amenazas DDoS
**Periodo del volcado:** 2026-11-22 03:57:13
**Fuentes:** Blocklist.de, GreenSnow, CI Army, malware, DShield, Mirai + listas de grupos (`killnet_proxies.txt`, `noname_controller_ips.csv`, `noname_attacking_ips.csv`, `darkstorm_ips.txt`, `grupo_*.txt`)
**Estado:** Sin verificación independiente. Mayoría de IPs marcadas como "reportada en canal público, no verificada".
**Advertencia:** Este documento es **análisis defensivo**. No es una lista de bloqueo. Muchas IPs pertenecen a CDN, cloud y ISPs residenciales compartidos; bloquearlas en masa causaría falsos positivos masivos.

---

# Monitor DDoS Andromeda Universo 25

## 📊 RESUMEN DEL MONITOR DDoS (ANDRÓMEDA) · 2026-11-22 03:57:13

**IPs analizadas:** 42.488 · **Con geolocalización:** 42.480 (99%) · **En algún grupo:** 19.660 · **En alguna botnet:** 22.123 · **Tiempo:** 16m50s (42,0 IPs/s)

---

## 🌍 TOP PAÍSES

| País | IPs | % |
|---|---:|---:|
| United States | 10.515 | 24,7% |
| China | 4.028 | 9,5% |
| Russia | 3.654 | 8,6% |
| Indonesia | 2.438 | 5,7% |
| Brazil | 1.725 | 4,1% |
| India | 1.508 | 3,5% |
| United Kingdom | 1.251 | 2,9% |
| Germany | 1.164 | 2,7% |

---

## 🚩 GRUPOS DETECTADOS

| Grupo | IPs |
|---|---:|
| Killnet | 19.099 |
| NoName057(16) | 386 |
| Ciberamenaza | 76 |
| Chaos | 26 |
| Shinyhunters | 14 |
| Spider | 11 |

---

## 🔥 TOP BOTNETS / FUENTES

| Fuente | IPs |
|---|---:|
| Blocklist.de | 21.273 |
| GreenSnow | 553 |
| CI Army | 221 |
| malware | 38 |
| DShield | 18 |
| Mirai | 11 |

---

## 🏢 TOP ASN

| ASN | Organización | IPs |
|---|---|---:|
| AS57026 | JSC "ER-Telecom Holding" | 2.048 |
| AS396190 | LeaseWeb USA, Inc. Seattle | 2.043 |
| AS394380 | Leaseweb USA, Inc. | 771 |
| AS13445 | Cisco Spark | 768 |
| AS7922 | Comcast Cable Communications | 768 |

## 1. RESUMEN EJECUTIVO (BLUF)

El monitor analizó **42.488 IPs** (99% geolocalizadas), de las cuales **19.660 están asociadas a algún grupo** y **22.123 a alguna botnet**. El ecosistema está dominado por **Killnet (19.099 IPs, 97% del total de grupos)** y **NoName057(16) (386 IPs)**.

**Hallazgo principal:** la mayoría de las IPs no son infraestructura dedicada de los grupos, sino **nodos residenciales, cloud y CDN comprometidos o utilizados como proxies**. Esto implica:

1. **No son IOCs de alta fidelidad.** Son indicadores de actividad de baja confianza.
2. **No deben bloquearse en masa.** Incluyen Cloudflare, Vultr, Contabo, Hetzner, Comcast, China Unicom, ER-Telecom, LeaseWeb, entre otros. El bloqueo indiscriminado rompería servicios legítimos.
3. **Su valor es contextual.** Sirven para monitorizar, correlacionar y priorizar investigación, no para bloqueo automatizado.

**Grupos con mayor volumen:** Killnet (19.099), NoName057(16) (386), Ciberamenaza (76), Chaos (26), Shinyhunters (14), Spider (11).
**Fuente principal de detección:** Blocklist.de (21.273 IPs, 99% del total de botnets/fuentes).

---

## 2. PANORAMA DE GRUPOS DETECTADOS

| Grupo | IPs | % del total de grupos | Fuente principal | Naturaleza |
|---|---|---|---|---|
| Killnet | 19.099 | 97,1% | `killnet_proxies.txt` | Hacktivismo prorruso; proxies y nodos comprometidos |
| NoName057(16) | 386 | 2,0% | `noname_*.csv` | Hacktivismo prorruso; CDN y residencial |
| Ciberamenaza | 76 | 0,4% | `grupo_ciberamenaza.txt` | Genérico; IPs no verificadas |
| Chaos | 26 | 0,1% | `grupo_chaos.txt` | Genérico; IPs no verificadas |
| Shinyhunters | 14 | <0,1% | `grupo_shinyhunters.txt` | Extorsión; IPs no verificadas |
| Spider | 11 | <0,1% | `grupo_spider.txt` | Ransomware; IPs no verificadas |
| Hook | 7 | <0,1% | `grupo_hook.txt` | Ransomware; IPs no verificadas |
| Pegasus | 6 | <0,1% | `grupo_pegasus.txt` | Spyware; IPs no verificadas |
| MuddyWater | 5 | <0,1% | `grupo_muddywater.txt` | APT iraní; IPs no verificadas |
| Blackhatsect0Randdxqrtxx | 5 | <0,1% | `grupo_blackhatsect0*.txt` | Hacktivismo; IPs no verificadas |
| The Gentlemen | 5 | <0,1% | `grupo_the-gentlemen.txt` | Ransomware; IPs no verificadas |
| Qilin | 4 | <0,1% | `grupo_qilin.txt` | Ransomware; IPs no verificadas |
| Quantum | 3 | <0,1% | `grupo_quantum.txt` | Ransomware; IPs no verificadas |
| Masalalunyasecurity | 3 | <0,1% | `grupo_masalalunyasecurity.txt` | Hacktivismo; IPs no verificadas |
| Mustang Panda | 2 | <0,1% | `grupo_mustang-panda.txt` | APT chino; IPs no verificadas |
| Ruby | 2 | <0,1% | `grupo_ruby.txt` | Ransomware; IPs no verificadas |
| Mirai | 2 | <0,1% | `grupo_mirai.txt` | Botnet IoT; IPs no verificadas |
| DarkStormTeam | 1 | <0,1% | `darkstorm_ips.txt` | Hacktivismo pro-palestino |
| Aglegends | 1 | <0,1% | `grupo_aglegends.txt` | Desconocido; IP no verificada |
| Warlock | 1 | <0,1% | `grupo_warlock.txt` | Ransomware; IP no verificada |
| Lazarus | 1 | <0,1% | `grupo_lazarus.txt` | APT norcoreano; IP no verificada |

**Conclusión:** Killnet y NoName057(16) concentran el 99,1% del volumen. El resto son detecciones puntuales, en su mayoría **no verificadas**.

---

## 3. DISTRIBUCIÓN GEOGRÁFICA

| País | IPs | % | Comentario |
|---|---|---|---|
| Estados Unidos | 10.515 | 24,7% | Dominado por cloud (AWS, Azure, Vultr, M247, LeaseWeb, Comcast) |
| China | 4.028 | 9,5% | Principalmente China Unicom (AS4837, AS17621) y Chinanet (AS4134) |
| Rusia | 3.654 | 8,6% | Incluye ER-Telecom (AS57026), Sibirtelecom (AS12389), UFO Technologies |
| Indonesia | 2.438 | 5,7% | Principalmente PT Hipernet Indodata (AS38758) |
| Brasil | 1.725 | 4,1% | V tal (AS8167), AMX Argentina |
| India | 1.508 | 3,5% | Cloudflare WARP, Hosterdaddy, DigitalOcean |
| Reino Unido | 1.251 | 2,9% | Cdn77 LON, UK MoD (reportado, no verificado) |
| Alemania | 1.164 | 2,7% | Leaseweb Deutschland, Hetzner, CDN77, M247 |

**Lectura:** la distribución refleja **infraestructura comprometida o utilizada como proxy**, no necesariamente origen de los atacantes. La sobrerrepresentación de EE.UU. y China se explica por la concentración de cloud y CDN.

---

## 4. TOP ASN (SISTEMAS AUTÓNOMOS)

| ASN | Organización | IPs | Comentario |
|---|---|---|---|
| AS57026 | JSC "ER-Telecom Holding" | 2.048 | ISP ruso; IPs residenciales |
| AS396190 | LeaseWeb USA, Inc. Seattle | 2.043 | Cloud/hosting; IPs compartidas |
| AS394380 | Leaseweb USA, Inc. | 771 | Cloud/hosting |
| AS13445 | Cisco Spark | 768 | Servicio cloud (Webex) |
| AS7922 | Comcast Cable Communications | 768 | ISP residencial EE.UU. |

**Lectura:** los cinco ASN principales son **ISP residenciales o cloud/hosting**. Ninguno es infraestructura dedicada de un grupo. **Bloquearlos afectaría a millones de usuarios legítimos.**

---

## 5. TOP BOTNETS / FUENTES

| Fuente | IPs | % | Comentario |
|---|---|---|---|
| Blocklist.de | 21.273 | 99% | Lista pública de hosts comprometidos (SSH, mail, web) |
| GreenSnow | 553 | 2,6% | Lista de IPs maliciosas |
| CI Army | 221 | 1,0% | Lista de reputación |
| malware | 38 | 0,2% | Lista de malware |
| DShield | 18 | <0,1% | Lista de SANS ISC |
| Mirai | 11 | <0,1% | Botnet IoT |

**Lectura:** la **dependencia de Blocklist.de** (99%) implica que la mayoría de las IPs son **hosts comprometidos genéricos**, no infraestructura de Killnet/NoName. Esto refuerza la baja fidelidad de los indicadores.

---

## 6. ADVERTENCIA CRÍTICA: NO BLOQUEAR EN MASA

Este es el punto ético y operativo más importante del informe:

**Las IPs listadas NO deben bloquearse de forma automatizada.** Razones:

1. **Son IPs compartidas.** Cloudflare (AS13335), Vultr (AS20473), Contabo (AS51167), Hetzner (AS24940), LeaseWeb (AS396190), Comcast (AS7922), China Unicom (AS4837), ER-Telecom (AS57026) alojan servicios legítimos. Bloquearlas rompería servicios.
2. **Son IPs residenciales.** Muchas pertenecen a usuarios domésticos comprometidos sin su conocimiento. Bloquearlas castiga a víctimas, no a atacantes.
3. **Son IPs no verificadas.** La mayoría de las IPs de "Ciberamenaza", "Chaos", "Shinyhunters", etc. están marcadas como "reportada en canal público, no verificada". No hay evidencia de que pertenezcan realmente a esos grupos.
4. **Son IPs efímeras.** Los atacantes rotan infraestructura. Una lista de IPs tiene vida útil de horas o días.
5. **El bloqueo por IP es evadible.** Killnet y NoName usan proxies, CDN y botnets; bloquear IPs no detiene el ataque, solo desplaza el tráfico.

**Recomendación:** usar estas IPs para **monitorización, correlación y priorización de investigación**, no para bloqueo. Para mitigación DDoS, usar **rate limiting, WAF, scrubbing centers y CDN con protección DDoS**.

---

## 7. INDICADORES DE ACTIVIDAD (MUESTRA, NO LISTA DE BLOQUEO)

> **Nota:** se incluye una muestra representativa. **No es una lista de bloqueo.** Cada IP debe validarse en su contexto antes de cualquier acción.

### 7.1. Killnet (muestra)

| IP | País | ASN | Nota |
|---|---|---|---|
| `200.3.252.170` | Paraguay | AS27895 Núcleo S.A | Proxy residencial |
| `90.188.53.6` | Rusia | AS12389 Sibirtelecom | ISP residencial |
| `104.24.15.158` | Canadá | AS13335 Cloudflare | CDN compartida |
| `45.32.169.213` | EE.UU. | AS20473 Vultr | Cloud |
| `31.220.78.244` | Francia | AS51167 Contabo | Hosting |
| `113.228.188.113` | China | AS4837 China Unicom | ISP residencial |
| `5.247.18.200` | Arabia Saudí | AS34400 Etihad Etisalat | ISP |
| `186.123.26.79` | Argentina | AS11664 AMX Argentina | ISP |

### 7.2. NoName057(16) (muestra)

| IP | País | ASN | Nota |
|---|---|---|---|
| `95.164.116.67` | Bulgaria | Netassist International | Hosting |
| `46.166.129.4` | Países Bajos | AS43350 NForce | Hosting |
| `84.17.42.47` | Francia | AS60068 Cdn77 | CDN |
| `149.36.51.146` | Países Bajos | AS212238 CDN77 | CDN |
| `45.87.212.180` | Alemania | AS9009 M247 | Hosting |

### 7.3. Otros grupos (muestra)

| IP | Grupo | País | Nota |
|---|---|---|---|
| `156.192.200.248` | DarkStormTeam | Egipto | AS8452 TE Data |
| `25.1.2.2` | Ciberamenaza | Reino Unido | UK MoD (no verificado) |
| `6.4.2.12` | Chaos/Ciberamenaza | EE.UU. | AS668 Dren (no verificado) |
| `193.178.158.61` | Ciberamenaza | Rusia | AS201738 UFO Technologies (no verificado) |
| `47.239.250.102` | Mustang Panda | Hong Kong | AS45102 Alibaba Cloud (no verificado) |

> **Caveat:** "no verificado" significa que la IP fue reportada en un canal público sin evidencia independiente. No debe tratarse como atribución confirmada.

---

## 8. MAPEO MITRE ATT&CK (DDoS)

| Táctica | Técnica | Evidencia |
|---|---|---|
| **Impacto (TA0040)** | T1498 — Network Denial of Service | Volumen masivo de IPs en Killnet/NoName |
| **Impacto (TA0040)** | T1498.001 — Direct Network Flood | Listas de proxies y controllers |
| **Impacto (TA0040)** | T1498.002 — Reflection Amplification | Uso de CDN y servicios cloud |
| **Recursos (TA0042)** | T1583 — Acquire Infrastructure | Proxies residenciales, cloud, CDN |
| **Recursos (TA0042)** | T1584 — Compromise Infrastructure | Hosts comprometidos (Blocklist.de) |
| **Acceso Inicial (TA0001)** | T1190 — Exploit Public-Facing Application | Botnets IoT (Mirai) |
| **Ejecución (TA0002)** | T1059 — Command and Scripting | Controllers de NoName |

---

## 9. EVALUACIÓN DE RIESGO (DEFENSIVA)

| Riesgo | Prob. | Impacto | Nivel | Recomendación |
|---|---|---|---|---|
| DDoS volumétrico de Killnet/NoName | Alta | Medio | **Alto** | CDN con protección DDoS, rate limiting |
| Falsos positivos por bloqueo de IPs | Alta | Alto | **Crítico** | **No bloquear**; usar monitorización |
| DDoS a servicios públicos | Media | Alto | **Alto** | Coordinar con CERTs nacionales |
| Uso de IPs residenciales como proxies | Alta | Bajo | **Medio** | Notificar a ISPs, no bloquear |
| Atribución errónea por IPs no verificadas | Media | Medio | **Medio** | Validar antes de atribuir |
| Botnets IoT (Mirai) | Media | Medio | **Medio** | Segmentar IoT, actualizar firmware |

---

## 10. RECOMENDACIONES

### Para SOC / TI
- **No importar** estas IPs en blocklists automáticas. Son de baja fidelidad.
- **Usar** para monitorización, correlación y priorización de investigación.
- **Cruzar** con fuentes primarias (CERTs, CISA, ENISA) antes de cualquier acción.
- **Implementar** mitigación DDoS real: CDN, scrubbing, rate limiting, WAF.
- **Monitorizar** ASN y países, no IPs individuales.

### Para liderazgo
- **No comunicar** estas listas como "IOCs de Killnet". Son indicadores de actividad, no de atribución.
- **No bloquear** a nivel de red: el impacto en servicios legítimos sería mayor que el beneficio.
- **Coordinar** con CERTs nacionales para mitigación DDoS.

### Para concienciación
- Explicar la diferencia entre **IOC de alta fidelidad** (hash de malware) y **lista de IPs de baja fidelidad**.
- Enfatizar el riesgo de **falsos positivos** en bloqueos masivos.

---

## 11. LIMITACIONES Y GAPS

1. **No hay verificación independiente** de la mayoría de IPs (marcadas como "no verificadas").
2. **La dependencia de Blocklist.de** (99%) implica que son hosts comprometidos genéricos, no infraestructura de los grupos.
3. **No se distingue** entre IP de atacante, proxy, víctima comprometida y CDN.
4. **No hay contexto temporal** (cuándo se observó cada IP).
5. **No hay contexto de ataque** (a qué objetivo, con qué método).
6. **Killnet** concentra el 97% del volumen; el resto son detecciones puntuales.
7. **El monitor no distingue** entre IPs activas y obsoletas.

---

## 12. DECLARACIÓN DE INTEGRIDAD

Este informe se ha elaborado bajo principios de **inteligencia ética**:
- **Atribución clara** de cada IP a su fuente.
- **No amplificación**: no se publican listas completas, solo muestras.
- **No facilitación**: no se proporciona acceso a infraestructura de los grupos.
- **Transparencia sobre limitaciones**: baja fidelidad, no verificación, riesgo de falsos positivos.
- **Uso exclusivamente defensivo**: el objetivo es proteger, no atacar.

**El repositorio no se hace responsable del uso indebido de este informe.**


---

*Fin — 2026-11-22*
