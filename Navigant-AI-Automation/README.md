# 🤖 Navigant AI Automation & Agentic Engine

This module focuses on the implementation of deterministic automated data flows and their evolution into fully autonomous, tool-equipped AI Agents. 

## 🛠️ Infrastructure & Environment
The runtime ecosystem is fully containerized locally using Docker to manage service dependencies securely, lower API throttling risks, and eliminate public cloud operational overhead.

*   **Runtime Orchestration:** `docker-compose.yml` defining the local processing clusters.
*   **Workflow Core Engine:** Configured local pipeline tracking workflows.
*   **Model Providers:** Integrated with Google Gemini Chat Models via secure API Studio endpoints.

## 🔄 Architectural Evolution: Predefined Workflows vs. Goal-Directed Agents

### Phase 1: Predefined Sequential Workflow (FL-04)
Initially built as a linear sequence where data movements were rigidly controlled by developer logic:
`Manual Trigger ➔ Notion Student Extraction ➔ LLM Evaluation (Gemini) ➔ Report Formatting`
*   *Limitation:* Low adaptability. The system performed static tasks and lacked the structural capability to alter its sequence when encountering unknown criteria.

### Phase 2: Autonomous Agentic Function-Calling (FI-07)
Upgraded to a goal-directed system where the LLM is given explicit tools and autonomously manages its own execution loops:
*   **Dynamic Tool Selection:** The agent automatically inspects incoming student files. If missing data or criteria anomalies occur, it actively initiates the `uk_university_requirements_lookup` tool.
*   **Hallucination Prevention Guardrails:** Configured with strict Deterministic Data Fallback rules. If the prerequisite lookup returns null values, the agent freezes processing and outputs a strict status: `Halted: Data Incomplete / Human Intervention Required`. This prevents the model from relying on soft weights to guess compliance scores.

## 🧪 Pre-Build Testing Matrix & Validation Cases
The execution pipeline was verified against five strict student profile mock evaluation matrices to eliminate edge-case errors before staging live executions:
1.  **Ideal Pathway Verification:** Tested with complete high-tier profile parameters resulting in immediate validation passes.
2.  **Deficit Assessment Verification:** Tested with intentional GPA criteria deficits. The agent calculated precise parameter mismatches and cleanly suggested lower-tier pathways without data errors.

## 🎥 System Walkthrough & Loop Test Evidence

For a comprehensive end-to-end evaluation of the agent architecture, dynamic tool execution loops, and automated error-trapping guardrails under concurrency loads, watch the official walkthrough:

👉 **[Watch Live Walkthrough: Agent Configuration & Loop Test Evidence](https://drive.google.com/file/d/1q4DclW3f-SOeQ6AVT9WiDug0IKxhP4DW/view)**



## Contact & Connect
* **Portfolio Showcase:** [syeda-munazza-bukhari-portfolio.netlify.app](https://syeda-munazza-bukhari-portfolio.netlify.app/)
* **GitHub Center:** [github.com/SyedaMun](https://github.com/SyedaMun)


With regards,  
**Syeda Munazza Bukhari**  
*Backend & AI Engineer*
