# Informes y Eventos de Seguridad — Temporada de Invierno

Repositorio de **informes de inteligencia de amenazas (CTI)** que documentan y registran eventos de seguridad globales en formato de **titulares de evento** (sin desarrollo analítico extendido). Cada informe es un archivo Markdown autocontenido, versionado y fechado.

**Repositorio:** https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno

## Propósito

Este repositorio existe para:

1. **Preservar** un registro cronológico de eventos de seguridad global (terrorismo, ciberataques, disturbios, conflictos, desastres, crimen organizado) tal como fueron observados en el periodo de corte.
2. **Servir como fuente primaria de referencia** para análisis posteriores, sin pretender ser un producto de inteligencia acabado ni una evaluación de severidad propia.
3. **Estandarizar** el formato de informes de evento para que sean comparables entre periodos.

> **Aviso importante:** Este repositorio contiene únicamente **informes de eventos**. No contiene exploits, IOCs accionables, herramientas ofensivas, ni datos personales de víctimas. La severidad indicada en cada titular es la del feed de origen, no una evaluación propia del mantenedor.

## Estructura

- `Informe_Octubre_Noviembre/` — informes por periodo. Nomenclatura: `<periodo>_<alcance>.md`.
- `docs/methodology.md` — metodología, fuentes y criterios de inclusión.
- `CHANGELOG.md` — registro de cambios por informe.

## Índice de informes

| Periodo | Alcance | Archivo |
|---|---|---|
| Oct–Nov 2026 | Eventos globales | [`Informe_Octubre_Noviembre/2026-10_2026-11_global-events.md`](Informe_Octubre_Noviembre/2026-10_2026-11_global-events.md) |
| 12–13 Nov 2026 | Eventos de seguridad (sweep) | [`Informe_Octubre_Noviembre/2026-11-12_2026-11-13_sweep.md`](Informe_Octubre_Noviembre/2026-11-12_2026-11-13_sweep.md) |

*(Actualiza esta tabla a medida que añadas informes.)*

## Formato de los informes

Cada informe sigue una estructura fija:

- **Encabezado:** periodo, formato, fecha de corte.
- **Secciones temáticas:** terrorismo y violencia política, ciberataques (brechas, ransomware, vulnerabilidades, infraestructura crítica, IA y cadena de suministro), disturbios y protestas, conflictos geopolíticos, desastres naturales, crimen urbano, otros.
- **Notas de fuente:** metodología, severidad, tratamiento de duplicados y ruido.

Los informes se publican **tal como se reciben del proceso de monitorización OSINT**, con edición mínima de formato.

## Uso

```bash
git clone https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno.git
cd Informes_y_eventos_Seguridad_Tempotada_Invierno
```

No requiere dependencias para leer los informes (son Markdown plano). Las dependencias de `requirements.txt` son solo para validación/exportación opcional.

## Contribuir

Ver [`CONTRIBUTING.md`](CONTRIBUTING.md). Las contribuciones se limitan a **correcciones de formato, erratas y metadatos**; no se aceptan informes nuevos sin revisión de metodología.

## Licencia

Contenido bajo **CC BY 4.0** (ver [`LICENSE`](LICENSE)). El código de utilidades, si lo hubiera, bajo MIT.

## Descargo de responsabilidad

Los informes se basan en fuentes públicas identificables (medios internacionales, feeds OSINT, `Ransomware.live`, `NoName057(16)`, `Killnet`, `Blocklist.de`, `ET Compromised`, IODA, ADS-B). No hay infiltración ni acceso a grupos cerrados. La exactitud, verificación y vigencia de cada titular corresponde a la fuente original. Este repositorio no constituye asesoramiento legal, financiero ni de seguridad operacional.
