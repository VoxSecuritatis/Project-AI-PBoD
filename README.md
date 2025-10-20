# 🧠 Personal Board of Directors (PBoD)
Published:  2025-10-19

**Video demo** (click the View raw link to download the video, 181 MB MP4):  [Personal Board of Directors Demo Video](https://github.com/VoxSecuritatis/Project-AI-PBoD/blob/main/PBoD.mp4)

### *AI-Powered Multi-Persona Decision Support System*

---

## 📘 Overview

The **Personal Board of Directors (PBoD)** is an interactive AI-driven decision support framework designed to simulate the experience of consulting a diverse panel of experts, leaders, and thinkers — each powered by its own **distinct persona**.

Built entirely in **Python**, PBoD uses modular architecture, YAML persona profiles, and OpenAI’s GPT models to create realistic advisory discussions on complex topics ranging from business strategy to personal growth.

Each persona represents a unique worldview, reasoning style, and domain of expertise — allowing users to experience well-rounded, multi-perspective decision-making in real time.

---

## 🎯 Purpose

Originally developed as a **portfolio project** for the Post Graduate Program in **Artificial Intelligence and Machine Learning (PGP-AIML)** at **The University of Texas at Austin**, PBoD now stands as a demonstration of:

- **Applied LLM reasoning** using structured, context-aware prompts.  
- **System design for explainable AI collaboration.**  
- **Human-AI augmentation in leadership, governance, and education.**

Beyond its academic foundation, PBoD offers potential **enterprise applications** in IT governance, change management, vendor risk assessment, and GRC (Governance, Risk & Compliance).

---

## 🚀 Features

### 🔹 Modular Design
Each component serves a specific function, ensuring flexibility and clarity:
- **`persona_loader.py`** – Loads and validates persona YAML files.  
- **`prompt_composer.py`** – Constructs structured prompts per persona.  
- **`board_chat.py`** – Manages concurrent persona responses and board logic.  
- **`session_logger.py`** – Saves meeting results in Markdown and JSON format.  
- **`pbo_cli.py`** – The interactive command-line interface that drives it all.  

### 🔹 Dynamic Persona Engine
- Personas are defined via YAML (e.g., `v_SunTzu.yaml`, `v_Oprah.yaml`, etc.).  
- Each persona includes fields like `name`, `domain`, `temperature`, and `anchor_quote`.  
- Easily add new personas or modify existing ones without touching any core code.  

### 🔹 Interactive CLI
- Select personas by number or use the default board.  
- Reuse previous session boards.  
- Ask new questions, reuse old questions, or start over entirely.  
- Exit with or without saving reports.  

### 🔹 Rich Output & Reports
- Colorized console display for clarity and readability.  
- Session logs automatically saved as:
  - **Markdown Reports** (for human reading)
  - **JSON Records** (for data analytics or dashboards)
- Optional index tracking for previous sessions.  

### 🔹 Configurable via YAML
- A `pbo_config.yaml` allows you to define:
  - Default model (e.g., `gpt-5`, `gpt-4o-mini`)
  - Auto-save behavior  
  - Directory paths for logs and sessions  

### 🔹 Example Default Board
| Persona ID | Real Name | Short Description |
|-------------|------------|------------------|
| v_Buddha | Siddhartha Gautama | Mindfulness, detachment, and reflective clarity. |
| v_Indra | Indra Nooyi | Purpose-driven leadership and empathy. |
| v_Mandela | Nelson Mandela | Moral courage and reconciliation. |
| v_Steve | Steve Jobs | Visionary innovation and simplicity. |
| v_Oprah | Oprah Winfrey | Emotional intelligence and authenticity. |
| v_Covey | Stephen Covey | Principle-centered leadership and ethics. |
| v_Barak | Barack Obama | Diplomacy, communication, and optimism. |
| v_SunTzu | Sun Tzu | Strategy, timing, and competitive advantage. |
| v_Ratan | Ratan Tata | Ethical capitalism and humility. |

---

## 🧩 System Architecture

+-------------------+  
| pbo_cli.py        | ← Interactive CLI interface  
+-------------------+  
↓  
+-------------------+  
| prompt_composer   | ← Builds question prompts  
+-------------------+  
↓  
+-------------------+  
| board_chat.py     | ← Handles persona responses (GPT)  
+-------------------+  
↓  
+-------------------+  
| session_logger.py | ← Saves Markdown + JSON reports  
+-------------------+  
↓  
+-------------------+  
| persona_loader.py | ← Loads and manages YAML personas  
+-------------------+  

This modular design supports expansion into a **GUI (NiceGUI / Streamlit)** or an **agentic AI architecture** for multi-threaded reasoning in future releases.

---

## 🧠 Enterprise Use Cases

While PBoD began as an academic and creative exploration, it has clear business potential across **IT and GRC workflows**:

| Function | Virtual Board Type | Value Delivered |
|-----------|-------------------|-----------------|
| IT Operations | Change Advisory Board | Faster, consistent, risk-aware approvals |
| Program Management | Portfolio Review Board | Balanced prioritization of IT investments |
| Vendor Governance | Supply Chain Risk Board | Transparent and auditable vendor oversight |
| Compliance & Legal | Policy Review Board | Regulatory assurance and audit readiness |
| Enterprise Risk | Contingency Planning Council | Predictive decision-making and scenario modeling |

---

## 📊 Learnings & Insights

Developing PBoD involved deep exploration across **AI design, governance modeling, and prompt engineering**:

- **LLM Behavior Control:** Tuning persona “temperature” values changes reasoning style, tone, and creativity — critical for realistic advisory dialogue.  
- **Structured Context Delivery:** YAML persona files and prompt templates enforce consistent, deterministic output.  
- **Human-Centric Design:** The project illustrates how AI can *amplify* human reflection, not replace it.  
- **Explainability Through Dialogue:** Simulated discussions naturally expose reasoning logic — a key goal in enterprise AI adoption.  
- **Scalability Potential:** Modular structure makes it adaptable to enterprise GRC systems, ITSM platforms (e.g., ServiceNow), or even change management frameworks.  

---

## 🧩 Future Enhancements

- Integration with **Streamlit or NiceGUI** for a web-based dashboard.  
- Persona clustering (e.g., “Innovators”, “Ethicists”, “Strategists”) for themed consultations.  
- Weighted consensus scoring between personas.  
- Real-time keyword and sentiment extraction for board discussions.  
- Integration with enterprise APIs (e.g., ServiceNow, Jira, or Power BI dashboards).  

---

## 🧾 Technology Stack

| Category | Tool / Library |
|-----------|----------------|
| Language | Python 3.12+ |
| AI Model | OpenAI GPT-5 / GPT-4o-mini |
| Data Format | YAML, JSON, Markdown |
| CLI Enhancements | Colorama, Rich |
| Logging | Native logging + JSON session logs |
| Architecture | Modular, object-oriented |

---

## 📁 Directory Structure

+--------------------------------------------+  
| Personal_Board_of_Directors/               |  
+--------------------------------------------+  
│  
├── personas/  
│   ├── v_Barak.yaml  
│   ├── v_Buddha.yaml  
│   ├── v_SunTzu.yaml  
│   └── ...  
│  
├── sessions/  
│   ├── session_YYYY-MM-DD_HH-MM-SS.md  
│   ├── session_YYYY-MM-DD_HH-MM-SS.json  
│   └── index.json  
│  
├── logs/  
│   └── error_YYYY-MM-DD_HH-MM-SS.log  
│  
├── pbo_cli.py  
├── persona_loader.py  
├── prompt_composer.py  
├── board_chat.py  
├── session_logger.py  
└── README.md  

---

## 🎓 Developer & Project Context

**Developer:** Brock Frary  
**Project Type:** Portfolio Demonstration / Applied AI System Design  

---

## 💡 Key Takeaway

> *"Artificial Intelligence isn’t just about automating answers — it’s about expanding how we think."*  
> — *Brock Frary, Developer of PBoD*

PBoD demonstrates how human insight and AI reasoning can converge to form a **collaborative, explainable, and ethical framework for decision support.**  
It’s a bridge between machine intelligence and human wisdom — a prototype for the next generation of enterprise advisory systems.

---

## 🤖 Persona List

| Persona ID | Real Name | Short Description |
|-------------|------------|------------------|
| v_Bezos | Jeff Bezos | Entrepreneurship, innovation, and long-term vision. |
| v_Bolívar | Simón Bolívar | Leadership, liberation, and justice. |
| v_Branson | Richard Branson | Entrepreneurship, adventure, and brand innovation. |
| v_Brown | Brené Brown | Leadership, vulnerability, and emotional intelligence. |
| v_Buddha | Siddhartha Gautama | Mindfulness, clarity, and detachment. |
| v_Buffett | Warren Buffett | Investment, business ethics, and long-term strategy. |
| v_Chavez | César Chávez | Labor rights, equity, and perseverance. |
| v_Churchill | Winston Churchill | Political leadership and wartime strategy. |
| v_Covey | Stephen R. Covey | Principle-centered leadership and effectiveness. |
| v_Cuban | Mark Cuban | Entrepreneurship, market realism, and innovation. |
| v_Curie | Marie Curie | Science, discovery, and perseverance. |
| v_DaVinci | Leonardo da Vinci | Innovation, art, and scientific creativity. |
| v_DalaiLama | Tenzin Gyatso (14th Dalai Lama) | Compassion, mindfulness, and peace. |
| v_Dweck | Carol Dweck | Growth mindset, learning, and resilience. |
| v_Einstein | Albert Einstein | Science, philosophy, and intellectual creativity. |
| v_Freeman | Morgan Freeman | Acting, narration, and wisdom. |
| v_Gandhi | Mahatma Gandhi | Social activism, peace, and moral leadership. |
| v_Gates | Bill Gates | Technology, philanthropy, and innovation. |
| v_Jobs | Steve Jobs | Visionary design, innovation, and simplicity. |
| v_Jordan | Michael Jordan | Excellence, performance, and competitive mindset. |
| v_Kennedy | John F. Kennedy | Leadership, courage, and vision. |
| v_Kondo | Marie Kondo | Organization, mindfulness, and simplicity. |
| v_Lincoln | Abraham Lincoln | Political leadership, justice, and unity. |
| v_Machel | Graça Machel | Education, human rights, and leadership. |
| v_Machiavelli | Niccolò Machiavelli | Political strategy, power dynamics, and realism. |
| v_Mandela | Nelson Mandela | Moral courage, reconciliation, and resilience. |
| v_Montessori | Maria Montessori | Education, human development, and empowerment. |
| v_MotherTeresa | Mother Teresa (Saint Teresa of Calcutta) | Compassion, service, and faith in action. |
| v_Musk | Elon Musk | Innovation, disruption, and systems thinking. |
| v_Nightingale | Florence Nightingale | Medicine, reform, and compassion. |
| v_Nooyi | Indra Nooyi | Purpose-driven leadership, empathy, and corporate vision. |
| v_Nye | Bill Nye | Science communication, innovation, and education. |
| v_Obama | Barack Obama | Diplomacy, communication, and strategic optimism. |
| v_Patton | George S. Patton | Military leadership, strategy, and courage. |
| v_PopeFrancis | Pope Francis | Religious leadership, compassion, and humility. |
| v_Powell | Colin Powell | Leadership, strategy, and discipline. |
| v_Putin | Vladimir Putin | Political leadership, statecraft, and control. |
| v_Robbins | Tony Robbins | Peak performance, mindset, and motivation. |
| v_Roosevelt | Franklin D. Roosevelt | Political leadership, crisis management, and reform. |
| v_Rowling | J.K. Rowling | Creativity, storytelling, and resilience. |
| v_Ruth | Babe Ruth | Sportsmanship, resilience, and confidence. |
| v_Sandberg | Sheryl Sandberg | Technology leadership and women’s empowerment. |
| v_Schultz | Howard Schultz | Business leadership, culture, and social impact. |
| v_Serling | Rod Serling | Storytelling, imagination, and social commentary. |
| v_Sharpe | Shannon Sharpe | Sports commentary, leadership, and communication. |
| v_Socrates | Socrates | Ethics, philosophy, and critical thinking. |
| v_Spielberg | Steven Spielberg | Storytelling, creativity, and emotional depth. |
| v_SunTzu | Sun Tzu | Strategy, timing, and power dynamics. |
| v_Tata | Ratan Tata | Ethical capitalism, humility, and long-term vision. |
| v_Toyoda | Akio Toyoda | Continuous improvement, discipline, and innovation. |
| v_Tracy | Brian Tracy | Goal setting, self-discipline, and success principles. |
| v_Trump | Donald Trump | Politics, business, and media influence. |
| v_Turing | Alan Turing | Computing, logic, and problem-solving. |
| v_Tyson | Neil deGrasse Tyson | Science communication, curiosity, and cosmic perspective. |
| v_Whitman | Meg Whitman | Organizational scaling and operational excellence. |
| v_Williams | Serena Williams | Excellence, discipline, and resilience. |
| v_Winfrey | Oprah Winfrey | Emotional intelligence, storytelling, and empowerment. |
| v_XiJinping | Xi Jinping | Political leadership, governance, and state control. |
| v_Yew | Lee Kuan Yew | Governance, economic reform, and nation-building. |
| v_Yousafzai | Malala Yousafzai | Education, activism, and peace. |

---

© 2025 Brock Frary — All Rights Reserved.
