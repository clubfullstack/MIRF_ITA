# MIRF_ITA
Repo para Proposta de Doutorado, 
@Todos os direitos Reservados – o conteúdo de pesquisa desse documento não pode ser reproduzido sem autorização prévia – Att, Jackson T. Veiga (03-06-2025)

# MIRF — Módulo Inteligente Reativo a Falhas: Jackson T. Veiga

🚀 Repositório para desenvolvimento de um sistema tolerante a falhas embarcado, voltado à assistência inteligente a pilotos de aeronaves durante panes críticas, com base em doutrinas aeronáuticas (QHR, POH, AFM) e técnicas de inteligência artificial.

## 📌 Objetivos

- Capturar e interpretar eventos de falha durante o voo em tempo real.
- Fornecer recomendações automáticas baseadas em conhecimento aeronáutico codificado (QHR/FTA).
- Aprender padrões de falha e sugerir ações otimizadas ao piloto.
- Simular cenários com falhas para treinamento, análise e resposta.

---

## 🧱 Estrutura do Repositório

MIRF/
├── docs/ → Diagramas e documentação de conhecimento
├── data/ → Dados crus (PDFs) e processados (JSON)
├── notebooks/ → Análises exploratórias e parsers
├── src/
│ ├── ai/ → Algoritmos de diagnóstico e IA
│ ├── cockpit_ui/ → Simulador visual de cockpit
│ ├── ingestion/ → Interfaces com sistemas da aeronave
│ └── knowledge/ → Ontologias e modelos de doutrina
├── simulator/ → Cenários e injeção de falhas
├── tests/ → Testes automatizados
└── README.md
---
## ✈🧠 ARQUITETURA PROPOSTA: *Módulo Inteligente de Resposta a Falhas em Voo (MIRF)*

### 🔧 1. *Visão Geral Arquitetural*


             +--------------------------------------------+
             |       Cockpit Operacional / Fly-by-Wire    |
             |     (FMS, FADEC, ECAM/EICAS, PFD, etc.)     |
             +--------------------------------------------+
                                ||         
                                \/        
              +------------------++------------------+
              |  Módulo Inteligente Reativo a Falhas |
              +--------------------------------------+
              |                                      |
              |  🔸 Sensor Bus / Data Acquisition     |
              |  🔸 Módulo de Diagnóstico ML          |
              |  🔸 Base de Conhecimento (FTA, QHR)   |
              |  🔸 Simulador Virtual (what-if)       |
              |  🔸 Assistente Preditivo ao Piloto     |
              |  🔸 Comunicação com FMS/ATC            |
              +--------------------------------------+
                                ||         
                                \/        
                      +--------------------+
                      | Cockpit Virtual AI |
                      | - Feedback Visuais |
                      | - Alertas Táticos  |
                      | - Checklists Ativos|
                      +--------------------+

### 🧩 2. *Componentes-Chave*

| Módulo                                          | Função                                                                                                          |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| *Data Bus Ingestion*                          | Capta dados do ECAM/EICAS, FDR, FADEC e sensores ambientais (via ARINC 429, CAN, etc).                          |
| *Motor de Diagnóstico ML*                     | Detecta padrões de falhas e anomalias com base em aprendizado supervisionado e não supervisionado.              |
| *Árvore de Falhas Baseada em FTA*             | Estrutura lógica que permite prever falhas decorrentes (cascata).                                               |
| *Motor de Simulação Virtual (gemelo digital)* | Permite simular em tempo real "e se", para apoio à decisão.                                                     |
| *Base QHR/POH/AOM embutida*                   | Estrutura embarcada de conhecimento com sugestões compatíveis com a doutrina da aeronave.                       |
| *Piloto Digital (UI)*                         | Sistema interativo visual e sonoro com feedback reativo, adaptado ao estilo de voo e carga cognitiva do piloto. |

---
## 📚 MAPA DE ESTUDOS E DESENVOLVIMENTO

### *FASE 1: Fundamentos Críticos*

* ✅ *FTA (Fault Tree Analysis)*
  → Domínio das causas raiz e cascatas de falhas

* ✅ *POH / AFM / QHR Analysis*
  → Taxonomia de falhas e respostas normalizadas

* ✅ *Arquitetura de Sistemas Embarcados Aeronáuticos*

  * ARINC 429, CAN-Aerospace
  * Avionics Bus & Middleware

---

### *FASE 2: Inteligência Artificial e Diagnóstico*

* 🧠 *Machine Learning Aplicado a Aviação*

  * Anomaly Detection com autoencoders / Isolation Forest
  * Classificação supervisionada com Random Forest / XGBoost
  * Time Series Forecasting (LSTM, Prophet)

* 🧠 *Técnicas de Fusão de Dados (Sensor Fusion)*

  * Kalman Filters
  * Bayesian Networks para avaliação de confiança

---
### *FASE 3: Desenvolvimento de Sistema Embarcado*

* 🔧 *Edge AI com TensorRT / Coral TPU / NVIDIA Jetson*

  * Rodar IA localmente com baixo consumo
* 🔧 *Simuladores de Testes e Injeção de Panes*

  * JSBSim + ROS 2 + Gazebo para simulação de voo com panes
  * Ferramentas: Simulink, Dymola, Modelica

---

### *FASE 4: Engenharia de Conhecimento e Interface*

* 📘 *Formalização da Doutrina (com NLP e LLMs)*

  * Parser de QHRs para estrutura JSON/YAML navegável
  * Motor semântico: "Falha em bomba hidráulica ➝ ação correta"

* 🎛 *UI/UX adaptada ao Cockpit*

  * Design de feedback visual em tempo real (HUD, EFB, voice)

---
## 📌 FERRAMENTAS RECOMENDADAS

| Categoria                  | Ferramentas                           |
| -------------------------- | ------------------------------------- |
| Simulação                  | JSBSim, FlightGear, ROS2, Gazebo      |
| ML embarcado               | TensorRT, Edge Impulse, Jetson Nano   |
| Engenharia de Conhecimento | Prolog, RDF/OWL, Haystack             |
| Visualização UI            | Qt, HTML5 Canvas for EFB, OpenEFB     |
| Linguagens                 | C++, Python, Rust (sistemas críticos) |

---

## 🌐 EXEMPLOS REAIS INSPIRADORES

* *Honeywell Forge Flight Health AI*
* *NASA Langley Self-Healing Avionics*
* *DAA (Detect and Avoid) AI do projeto Skyborg (USAF)*
---

## 🧠 Fontes de Conhecimento

- ✅ **QHR (Quick Reference Handbook)**: Checklists de falhas e respostas imediatas.
- ✅ **FTA (Fault Tree Analysis)**: Árvores causais para diagnósticos estruturados.
- ✅ **AFM / POH**: Regras de operação e performance.
- ✅ **FDR / Sensor Bus**: Dados reais de sensores e atuação.

---

## 📚 Tecnologias Utilizadas

- Python 3.11+
- Scikit-learn, PyTorch, NetworkX
- PDFMiner / PyMuPDF para parsing
- Graphviz para árvores de falha
- Qt / Tkinter para cockpit virtual
- JSBSim / ROS para simulação de voo

---

## ✅ Roadmap Inicial

- [x] Estrutura do repositório
- [x] Parser de QHR para JSON
- [ ] Motor FTA em Python
- [ ] Dashboard de simulação em tempo real
- [ ] Integração com simulação JSBSim
- [ ] Lógica de inferência embarcável com IA

---

## 📄 Licença

Este projeto é de código aberto e pode ser usado para fins acadêmicos e de pesquisa. Consulte `LICENSE` para detalhes.

Proposta de Doutorado, 
@Todos os direitos Reservados – o conteúdo de pesquisa desse documento não pode ser reproduzido sem autorização prévia – Att, Jackson T. Veiga (03-06-2025)
