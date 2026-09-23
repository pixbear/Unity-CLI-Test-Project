# 🤖 Unity AI Agent Benchmarking & Test (Qwen2.5 7B)

This repository serves as a **test environment and benchmark log** exploring the integration of the `unity-cli-server` MCP tool with the **Qwen2.5 7B Local AI model**. The goal was to evaluate how effectively a lightweight local LLM agent can execute game development tasks in Unity through iterative prompt adjustments.

---

## 💻 1. Test Environment & Specs
*   **AI Model**: `Qwen2.5 7B` (Local LLM)
*   **Operating System**: macOS
*   **Interface Tool**: `unity-cli-server` MCP Tools & Terminal CLI
*   **Target Task**: Basic object placement and automated C# script generation within the active scene.

---

## 📊 2. Overall Test Summary

> **"Due to the model's parameters (7B), it is not yet ready for production-level development. However, it successfully handles simple, short-term generation tasks."**

### 🟢 What Works (Strengths)
*   **Basic Task Generation**: Excellent at executing standalone, single-step commands such as spawning geometric primitives (Cubes/Spheres) and setting up fundamental C# script skeletons.
*   **Cost & Privacy**: Leveraging a 7B local model allows for zero-cost infrastructure and private prototyping without external API dependencies.

### 🔴 Limitations (Weaknesses)
*   **Sequential Progression Flaws**: Struggles with complex, long-term task chaining, occasionally falling into infinite read/scan loops on the same file directory.
*   **Lack of Autonomous Self-Healing**: When encountering Unity CLI syntax errors or parameter mismatches, the model tends to blindly guess alternative arguments instead of diagnosing the actual root cause.

---

## 💡 3. Conclusion & Next Steps

*   **Not Ready for Practical Projects**: Entrusting an entire game project to a local 7B agent is currently unfeasible due to reasoning limits.
*   **Future Requirements**: To achieve reliable control and maximize the utility of a 7B-class model, implementing **hyper-specific, granular command constraints and highly structured prompt engineering** is absolutely necessary.


-------------------------------------------------


# 🤖 Unity AI Agent Benchmarking & Test (Qwen2.5 7B)

이 프로젝트는 `unity-cli-server` MCP 도구와 **Qwen2.5 7B 로컬 AI 모델**을 연동하여, AI 에이전트가 유니티 환경에서 게임 개발 임무를 얼마나 수행할 수 있는지 검증한 **실험용 테스트 저장소**입니다. 프롬프트를 실시간으로 수정하며 에이전트의 가능성과 한계를 기록했습니다.

---

## 💻 1. 테스트 환경 (Environment)
*   **AI Model**: `Qwen2.5 7B` (Local LLM)
*   **Operating System**: macOS
*   **Interface Tool**: `unity-cli-server` MCP Tools & Terminal CLI
*   **Target Task**: 유니티 활성 씬 내부 오브젝트 배치 및 간단한 스크립트 작성

---

## 📊 2. 종합 테스트 결과 (Test Summary)

> **"로컬 AI 모델 체급의 한계로 실제 프로젝트 개발에 투입하기엔 무리이나, 간단한 생성 명령은 훌륭히 수행"**

### 🟢 가능성 (What Works)
*   **간단한 명령 생성**: 큐브/플레이어 생성, 물리 기반 스크립트 기초 뼈대 구축 등 단발성 명령은 잘 수행합니다.
*   **비용 및 보안적 이점**: 7B 체급의 가벼운 로컬 모델을 활용하여 인프라 비용 없이 빠른 프로토타입 실험이 가능합니다.

### 🔴 한계점 (Limitations)
*   **연속 태스크 수행력 부족**: 턴 제어가 꼬이거나 동일한 파일만 반복해서 스캔하는 무한 루프 현상이 발생합니다.
*   **자가 치유(Self-Healing) 부족**: 유니티 CLI나 파라미터 문법 오류가 났을 때 원인을 정확히 분석하지 못하고 무작정 찍어서 인자를 대입하는 한계를 보입니다.

---

## 💡 3. 결론 및 향후 과제 (Conclusion & Next Step)

*   **실무 적용 시기상조**: 현 상태에서 AI 에이전트에게 전체 프로젝트 개발을 통째로 맡기는 것은 불가능에 가깝습니다.
*   **향후 과제**: 7B 체급 모델에서 발생하는 오작동을 제어하기 위해서는 **더욱 정밀하고 촘촘하게 설계된 하드코딩 수준의 디테일한 명령어와 프롬프트 고도화(Tuning)**가 필수적입니다.
