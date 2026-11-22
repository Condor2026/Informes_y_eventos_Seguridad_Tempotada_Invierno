# Informes y Eventos de Seguridad — Temporada de Invierno

[![License: CC BY 4.0](https://img.shields.io/github/license/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno?color=lightgrey)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno/blob/main/LICENSE)
[![Último commit](https://img.shields.io/github/last-commit/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno?color=blue)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno/commits/main)
[![Tamaño del repo](https://img.shields.io/github/repo-size/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno?color=purple)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno)
[![Issues](https://img.shields.io/github/issues/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno?color=orange)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno/issues)
[![Stars](https://img.shields.io/github/stars/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno?color=yellow)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno/stargazers)
[![CTI](https://img.shields.io/badge/CTI-Inteligencia%20de%20Amenazas-red)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno)
[![OSINT](https://img.shields.io/badge/OSINT-Fuentes%20P%C3%BAblicas-blueviolet)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno)
[![Uso Defensivo](https://img.shields.io/badge/Uso-Defensivo-green)](https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno/blob/main/SECURITY.md)

Repositorio de **informes de inteligencia de amenazas (CTI)** y **registros de eventos de seguridad globales**, en formato de titulares de evento (sin desarrollo analítico extendido). Cada informe es un archivo Markdown autocontenido, versionado y fechado.

**Repositorio:** https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno
**Autor:** Condor2026
**Licencia:** CC BY 4.0

---

## Propósito

Este repositorio existe para:

1. **Preservar** un registro cronológico de eventos de seguridad global (terrorismo, ciberataques, disturbios, conflictos, desastres, crimen organizado, leaks y hacktivismo) tal como fueron observados en el periodo de corte.
2. **Servir como fuente primaria de referencia** para análisis posteriores, sin pretender ser un producto de inteligencia acabado ni una evaluación de severidad propia.
3. **Estandarizar** el formato de informes de evento para que sean comparables entre periodos y fuentes.

> **Aviso importante:** Este repositorio contiene únicamente **informes de eventos**. No contiene exploits, IOCs accionables, herramientas ofensivas, ni datos personales de víctimas. La severidad indicada en cada titular es la del feed de origen, no una evaluación propia del mantenedor.

---

## Estructura del repositorio

```text
.
├── README.md                                    # Este archivo
├── LICENSE                                      # Licencia CC BY 4.0
├── CONTRIBUTING.md                              # Guía de contribución
├── SECURITY.md                                  # Política de seguridad
├── requirements.txt                             # Dependencias opcionales (validación/exportación)
├── .gitignore                                   # Exclusiones de Git
├── .gitattributes                               # Normalización de finales de línea
├── Eventos_Globales_Andromeda.md                # Informe de eventos globales (Andromeda)
├── Informe_Andromeda_1.md                       # Informe Andromeda (parte 1)
├── Informe_Nexsus_Osint_X_12_Noviembre.md       # Informe OSINT X — 12 nov
└── Informe_Octubre_Noviembre.md                 # Informe octubre–noviembre
```

## Índice de informes

| Informe | Periodo / Alcance | Archivo | Estado |
|---|---|---|---|
| **Eventos Globales Andromeda** | Eventos globales de seguridad (registro) | [`Eventos_Globales_Andromeda.md`](Eventos_Globales_Andromeda.md) | Activo |
| **Informe Andromeda 1** | Informe Andromeda — parte 1 | [`Informe_Andromeda_1.md`](Informe_Andromeda_1.md) | Activo |
| **Nexsus OSINT X — 12 Nov** | OSINT X — 12 de noviembre | [`Informe_Nexsus_Osint_X_12_Noviembre.md`](Informe_Nexsus_Osint_X_12_Noviembre.md) | Activo |
| **Octubre–Noviembre** | Eventos de seguridad oct–nov | [`Informe_Octubre_Noviembre.md`](Informe_Octubre_Noviembre.md) | Activo |

*Actualiza esta tabla cuando añadas nuevos informes.*

---

## Formato de los informes

Cada informe sigue una estructura fija:

- **Encabezado:** periodo, alcance, fuente, fecha de corte.
- **Secciones temáticas:** terrorismo y violencia política, ciberataques (brechas, ransomware, vulnerabilidades, infraestructura crítica, IA y cadena de suministro), disturbios y protestas, conflictos geopolíticos, desastres naturales, crimen urbano, leaks y hacktivismo, otros.
- **Notas de fuente:** metodología, severidad, tratamiento de duplicados y ruido.

Los informes se publican **tal como se reciben del proceso de monitorización OSINT**, con edición mínima de formato.

---

## Uso

```bash
git clone https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno.git
cd Informes_y_eventos_Seguridad_Tempotada_Invierno
```

No requiere dependencias para leer los informes (son Markdown plano). Las dependencias de `requirements.txt` son solo para validación y exportación opcional.

---

## Contribuir

Ver [`CONTRIBUTING.md`](CONTRIBUTING.md). Las contribuciones se limitan a **correcciones de formato, erratas y metadatos**; no se aceptan informes nuevos sin revisión de metodología.

---

## Seguridad

Ver [`SECURITY.md`](SECURITY.md). Para reportar problemas de seguridad, datos personales mal anonimizados o errores graves de atribución, abre un issue privado o contacta al mantenedor.

---

## Mantenimiento

### Renombrar el archivo con coma

Si quieres corregir `Eventos_Globales_Andromeda,md` (coma) a `Eventos_Globales_Andromeda.md` (punto):

```bash
git mv "Eventos_Globales_Andromeda,md" "Eventos_Globales_Andromeda.md"
git commit -m "fix: rename Eventos_Globales_Andromeda,md to .md"
git push
```

### Añadir un nuevo informe

1. Crea el archivo `.md` en la raíz del repo (o en subcarpeta por año, si se decide).
2. Añádelo a la tabla del **Índice de informes**.
3. Actualiza el `CHANGELOG.md` si existe (si no, créalo).
4. Haz commit y push.

### Validar Markdown

```bash
# Opcional: validar enlaces y formato
markdownlint "*.md"
markdown-link-check "*.md"
```

---

## Licencia

Contenido bajo **Creative Commons Attribution 4.0 International (CC BY 4.0)**. Ver [`LICENSE`](LICENSE).

El código de utilidades, si lo hubiera, se distribuye bajo MIT.

---

## Descargo de responsabilidad

Los informes se basan en fuentes públicas identificables (medios internacionales, feeds OSINT, canales de Telegram, `Ransomware.live`, `NoName057(16)`, `Killnet`, `Blocklist.de`, `ET Compromised`, IODA, ADS-B). No hay infiltración ni acceso a grupos cerrados. La exactitud, verificación y vigencia de cada titular corresponde a la fuente original.

Este repositorio **no constituye asesoramiento legal, financiero ni de seguridad operacional**. El mantenedor no se hace responsable del uso indebido del material.

---

## Contacto

- **GitHub:** [@Condor2026](https://github.com/Condor2026)
- **Repositorio:** https://github.com/Condor2026/Informes_y_eventos_Seguridad_Tempotada_Invierno
