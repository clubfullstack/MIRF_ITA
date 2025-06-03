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
