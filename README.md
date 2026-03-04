# 🛡️ SAST vs. LLM: Security & Quality Analysis

Este repositorio contiene un estudio detallado sobre la detección de vulnerabilidades y mejora de la calidad de código en una arquitectura moderna **Full-stack (FastAPI, React, PostgreSQL, Docker)**. 

El objetivo principal fue evaluar la eficacia de las herramientas de análisis estático tradicionales frente a las capacidades de razonamiento de los Modelos de Lenguaje de Gran Escala (LLMs).

## 📄 Informe Completo
Puedes consultar el análisis detallado realizado durante el Máster aquí:
👉 **[Descargar Informe Técnico (PDF)](./docs/Security_Analysis_Report_SAST_vs_LLM.pdf)**

---

## 🛠️ Stack de Análisis
Para este estudio se auditaron diversos componentes del sistema utilizando:

| Herramienta | Categoría | Propósito |
| :--- | :--- | :--- |
| **Semgrep** | SAST | Detección de patrones de seguridad y vulnerabilidades conocidas en C y Python. |
| **Codacy** | Static Analysis | Monitorización de deuda técnica, estándares de estilo y mantenibilidad. |
| **GitHub Copilot Chat** | LLM | Auditoría contextual, explicación de fallos y generación de parches de seguridad. |

## 🚀 Metodología de Pruebas
1. **Auditoría Automática:** Ejecución de pipelines de Semgrep y Codacy sobre el código base de FastAPI.
2. **Auditoría Inteligente:** Uso de prompts especializados en GitHub Copilot para identificar fallos de lógica que las herramientas SAST suelen pasar por alto.
3. **Contraste de Resultados:** Evaluación de falsos positivos y capacidad de remediación de cada herramienta.

## 📊 Conclusiones Principales
- **Precisión:** Semgrep destaca en la identificación de inyecciones de código y fallos de configuración.
- **Contexto:** Las LLMs (Copilot) demostraron una superioridad notable para explicar la raíz del problema y proponer refactorizaciones que no solo arreglan el fallo, sino que mejoran la arquitectura.
- **Sinergia:** El flujo de trabajo ideal para un entorno de producción (SecDevOps) debe integrar ambas capas para una cobertura total.

---
Nota: El código fuente en este repositorio se utiliza como "Benchmarking Base" para las pruebas de seguridad y no ha sido modificado, centrándose este proyecto exclusivamente en el análisis de vulnerabilidades.
*Este proyecto forma parte de mi formación avanzada en Pruebas de Software en la Industria.*
