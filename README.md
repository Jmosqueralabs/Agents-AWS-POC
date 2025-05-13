# Agents-AWS-POC

Trabajar con agentes en la nube de AWS: prueba de concepto para soluciones de Voicebot inteligentes.

## 🗣️ Voicebot Inteligente con Capacidades de Agente

### 🎯 Objetivo

Desarrollar un prototipo funcional de un **agente inteligente controlado por voz**, capaz de:

- Interpretar instrucciones habladas.
- Procesarlas internamente (simular acciones o consultar datos).
- Generar una **respuesta coherente y contextual**, ya sea en texto o en voz.

---

### 🤖 ¿Qué resuelve este proyecto?

El proyecto busca demostrar la capacidad de un voicebot inteligente de:

- Recibir instrucciones por voz (input del usuario).
- Interpretar el lenguaje natural.
- Consultar fuentes de datos estructuradas y no estructuradas.
- Simular la operación de una API externa.
- Responder al usuario por texto y voz.

> Este prototipo puede servir como base para asistentes virtuales, sistemas de atención automatizada o soporte técnico inteligente, entre otros.

---

### 🧠 Enfoque Modular y por Niveles

Este proyecto avanza por niveles de madurez incremental:

#### 🧩 Nivel 1 – Básico: Text-to-Text con Lógica de Agentes

- Framework de agentes usando [CrewAI](https://docs.crewai.com/), [LangGraph](https://www.langgraph.dev/), o Amazon Bedrock (Agents o Flows).
- Prototipo en Jupyter Notebook.
- Agente Supervisor orquestando tareas.
- Enfoque 100% textual (entrada y salida).
- Evaluación inicial de supervisión del flujo.

#### 🎛️ Nivel 2 – Intermedio: Voice-to-Text + Capa Cognitiva

- Incorporación de entrada por voz mediante **Amazon Transcribe** o **Nova Sonic**.
- UI simple para interacción por voz.
- Mejoras en la dinámica de consultas, razonamiento y flujos de respuesta.

#### 🔊 Nivel 3 – Avanzado: Conversación en Tiempo Real

- Interacción completamente por voz.
- Respuestas generadas en voz (Text-to-Speech).
- UI con experiencia conversacional enriquecida (feedback, animaciones, contexto).
- Supervisión avanzada y colaboración entre subagentes.

---

### 🧱 Arquitectura (Avance modular por niveles)

---

## 🔧 Tecnologías Utilizadas

| Componente              | Herramienta / Servicio                            |
| ----------------------- | ------------------------------------------------- |
| Agentes Cognitivos      | CrewAI / LangGraph / Bedrock Agents               |
| Transcripción de voz    | Amazon Transcribe / Nova Sonic                    |
| Generación de voz       | Amazon Polly                                      |
| Modelo fundacional      | Amazon Bedrock (Nova Micro/Lite/Pro/Sonic)        |
| Datos estructurados     | DynamoDB / RDS                                    |
| Datos no estructurados  | Amazon S3 + Embeddings (Vector DB)                |
| UI                      | Streamlit / Flask / Gradio                        |
| Orquestación            | Jupyter / Python Scripts                          |
| Métricas de rendimiento | Logging + Evaluación manual (latencia, precisión) |

---

## 📦 Estructura del Proyecto

```

voicebot-agent-prototype/
│
├── level1_text_to_text/
│ ├── agent_framework.ipynb
│ ├── config/
│ └── examples/
│
├── level2_voice_input/
│ ├── app.py
│ ├── ui/
│ └── audio_transcribe/
│
├── level3_voice_full_duplex/
│ ├── real_time_voicebot.py
│ ├── tts/
│ └── feedback_ui/
│
├── data_sources/
│ ├── structured/ (ej. DynamoDB, CSV)
│ └── unstructured/ (PDF, TXT, JSON)
│
├── diagrams/
│ ├── architecture.png
│ └── functional_flow.md
│
├── docs/
│ └ problem/
│       └ images/
│         └── general_problem.png
│         └── lvl1_proposal.png
│         └── lvl2_proposal.png
│         └── lvl3_proposal.png
└── README.md

```

---

## 📈 Métricas de Evaluación

- **Precisión de interpretación (NLP)**.
- **Latencia de respuesta (voz y texto)**.
- **Costo estimado por interacción** (uso de servicios AWS).
- **Supervisión de subagentes**.
- **Análisis de logs y errores**.

---

## 🔐 Consideraciones de Seguridad y Networking

Aunque no se implementan completamente en el prototipo, se incluyen como documentación:

- **Seguridad en servicios AWS**: IAM Roles, encriptación de datos en S3.
- **Networking**: Configuración privada/VPC para servicios como RDS o DynamoDB.
- **Límites conocidos**: Uso gratuito de Bedrock o límites de tokens en LLMs.

---

## 🚀 Próximos Pasos

- Agregar más subagentes especializados (por dominio).
- Optimizar los flujos de voz en tiempo real.
- Explorar estrategias de despliegue (SageMaker, ECS, o serverless).
- Monitoreo con Amazon CloudWatch.

---

## 📚 Recursos útiles

- 🔗 [Guía oficial de muestras Generative AI Latam (AWS)](https://github.com/aws-samples/generative-ai-ml-latam-samples/tree/main/samples)
- 🔗 [Bedrock Flows](https://hubs.la/Q03ls3RZ0)

---

¿Tienes feedback o quieres colaborar? ¡Abre un issue o contáctame!

```
jmosquera@morrisopazo.com
```
