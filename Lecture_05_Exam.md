# Lecture 5 · Transparency and Explainability — 考试冲刺包

---

## ① ⚡ 30 秒速记卡（Core Terms）

- **Transparency** = 让 AI 的决策过程/算法/数据对利益相关方 **open, understandable, accountable**
- **Explainability** = 提供 **清晰、可解读的解释**，说明 AI 如何得出输出
- **Interpretability** = **人类能理解并推理** AI 决策过程的 **程度**
- **Transparency-Explainability Tradeoff** = 透明需求 vs. 性能/专有信息保护
- **Right to Explanation** = GDPR Article 22，自动化决策有权要求解释
- **Algorithmic accountability** = 开发者与部署者的责任
- **AI literacy** = 公众对 AI 能力与局限的理解
- **Open-source AI initiatives** = 开源 AI 推进透明度
- **XAI（Explainable AI）** = 可解释 AI 领域总称
- **Feature importance** = 量化输入特征对输出的贡献
- **Saliency map** = 显著性图（高亮决策相关区域，CV 常见）
- **Local explanation** = 单次预测级别的解释（LIME / SHAP）
- **Counterfactual explanation** = "what-if" 情景分析（"若 X 不同，输出会..."）
- **Rule-based explanation** = 从复杂模型提取人类可读逻辑规则
- **Model-agnostic** = 适用任意 ML 模型的解释技术
- **LIME** = Local Interpretable Model-agnostic Explanations（Ribeiro 2016）
- **SHAP** = SHapley Additive exPlanations（Lundberg & Lee 2017）
- **DARPA XAI program** = 美国国防高级研究计划局 XAI 框架
- **IBM AI Explainability 360（AIX360）** = IBM 开源 XAI 工具包
- **Microsoft InterpretML** = 微软开源 XAI 工具包
- **Tiered Transparency** = 分层透明度（Public → Regulatory → Internal）
- **Model Cards** = Google 模型卡，类似"食品标签"
- **Datasheets for Datasets** = 数据表标准
- **EU AI Act** = 高风险 AI 的严格透明度要求
- **China Algorithmic Recommendation Provisions** = 中国《互联网信息服务算法推荐管理规定》
- **Secure enclaves** = 安全飞地，支持第三方审计不暴露 IP

---

## ② 🔢 编号清单全收录

### 🔸 4 大核心概念
1. Transparency · 2. Explainability · 3. Interpretability · 4. Transparency-Explainability Tradeoff

### 🔸 3 层概念辨析（必考区分）
```
Transparency（制度层 · 公开流程）
        ↓
Explainability（技术层 · 输出解释）
        ↓
Interpretability（认知层 · 人类理解）
```

### 🔸 XAI 的 7 大价值
1. **Trust**（信任）
2. **Compliance**（合规）
3. **Debugging & Improvement**（调试与改进）
4. **Scientific Understanding**（科学理解）
5. **Human-AI Collaboration**（人机协作）
6. **Bias & Discrimination Mitigation**（偏见缓解）
7. **Adoption**（采用率）

### 🔸 XAI 5 大技术家族
1. **Feature Importance**（特征重要性，含 Saliency maps）
2. **Local Explanations**（局部解释，如 LIME/SHAP）
3. **Counterfactual Explanations**（反事实解释）
4. **Rule-based Explanations**（规则型解释）
5. **Model-agnostic Explanation Techniques**（模型无关技术）

### 🔸 3 大 XAI 工具框架（必背）
1. **DARPA XAI Program Framework**（可解释模型 + 解释界面 + 心理学理论）
2. **IBM AI Explainability 360（AIX360）**（多领域/多模型）
3. **Microsoft InterpretML**（统一方法）

### 🔸 XAI 5 大局限/挑战
1. 性能-可解释性权衡（深度模型越强越难解释）
2. 解释本身可能被 **adversarial attacks** 攻击
3. **Causal vs. Correlational** 解释的挑战
4. 计算开销与时间约束
5. 详尽 vs. 简洁的平衡（不同用户群体）

### 🔸 Real-World XAI 实施 4 大难点
1. 基于用户需求与专业水平 **Customizing** 解释
2. 平衡可解释性与 **Performance & Efficiency**
3. 跨模型版本/数据子集的 **Consistency**
4. 从敏感数据生成解释时处理 **Privacy concerns**

### 🔸 3 大透明度重要性机制（Lack of Visibility 部分）
1. Opaque AI decision-making
2. 无法解释引发伦理担忧
3. Algorithmic accountability

### 🔸 公众信任 4 大机制
1. 透明度 → 培育 public trust
2. XAI 让决策可解读
3. **AI literacy**（AI 素养）
4. Open-source AI initiatives

### 🔸 Stakeholder 7 方视角（IP vs. Transparency）
1. AI 开发者（保护专有算法）
2. 用户（要求可解释，尤其高风险）
3. 监管机构（平衡创新与安全）
4. 公众（理解 AI 对生活的影响）
5. 学术研究者（倡导开源）
6. 伦理委员会（识别偏见）
7. 法律专家（定义披露层级）

### 🔸 分层透明度 3 层级（黄金方案！）
| 层级 | 受众 | 披露内容 |
|---|---|---|
| **High（Public-facing）** | 公众 | 高层次 insights |
| **Middle（Regulatory）** | 监管 | 更详细信息（合规验证） |
| **Deep（Internal）** | 内部团队 | 完全访问专有算法 |

### 🔸 标准化透明度报告 4 要素
1. 行业级框架
2. **关键性能指标 + 数据源 + 模型局限**
3. 跨 AI 系统/供应商 comparisons
4. 指标与披露层级达成一致的挑战

### 🔸 透明度技术解决方案（7 项，与 Topic 4 PETs 复用）
1. **Secure enclaves**（支持第三方审计）
2. Differential Privacy
3. XAI 解释技术本身
4. Federated Learning
5. **Blockchain**（不可篡改的决策记录）
6. Homomorphic Encryption
7. Model Compression（本地透明度）

### 🔸 3 大区域透明度法规
| 地区 | 法规 |
|---|---|
| **EU** | **EU AI Act**（风险分级 + 严格透明度） |
| **China** | **Internet Information Service Algorithmic Recommendation Management Provisions** |
| **USA** | **Sector-specific regulations** |

### 🔸 AI 开发流程的 3 大监管影响
1. 透明度监管改变开发流程
2. 合规透明度影响产品开发
3. 可解释性监管 → 影响 **模型选择**（高风险不能用纯黑箱）

### 🔸 运营与协作 3 大变化
1. 跨部门协作增加
2. 持续监控与审计
3. 行业竞争动态变化

### 🔸 主教材案例
- Ch.7, Case 1：**Unfair dismissal**（不公平解雇）

---

## ③ ⚠️ 易混概念对比表

### A. Transparency vs. Explainability vs. Interpretability（超高频！）
| | Transparency | Explainability | Interpretability |
|---|---|---|---|
| 层级 | **制度层** | **技术层** | **认知层** |
| 主体 | 流程/算法/数据公开 | AI 产生解释 | 人类能理解 |
| 类比 | "公开食材" | "写配方" | "看得懂配方" |
| 可能冲突 | 可能透明但不可解释（开源 100 万参数模型） | 可能可解释但不透明（内部知道不对外） | 可能能解释但外行看不懂 |

### B. Causal vs. Correlational Explanations（经典坑）
| | Causal（因果） | Correlational（相关） |
|---|---|---|
| 说法 | "这个特征**导致**了输出" | "这个特征**与**输出相关" |
| 工具 | 因果推断（极难） | SHAP/LIME 的默认输出 |
| 风险 | 难实现 | **混用会得错误结论** |

### C. LIME vs. SHAP
| | LIME | SHAP |
|---|---|---|
| 全称 | Local Interpretable Model-agnostic Explanations | SHapley Additive exPlanations |
| 奠基 | Ribeiro et al. 2016 | Lundberg & Lee 2017 |
| 特点 | 局部线性近似 | 基于 Shapley 值（博弈论） |
| 类型 | Local / Model-agnostic | Local + Global / Model-agnostic |

### D. Local vs. Global Explanations
- **Local**：单次预测的解释（"为什么这一笔贷款被拒？"）
- **Global**：整个模型的解释（"这个模型最重视哪些特征？"）

### E. Counterfactual vs. Rule-based Explanations
- **Counterfactual**：**如果** X 不同，输出会...（可行动建议）
- **Rule-based**：**如果** X > 阈值 **则** 输出 Y（可读逻辑规则）

### F. Tiered Transparency 的 3 层
- **Public** = 高层 insights
- **Regulatory** = 详细合规信息
- **Internal** = 完全访问

---

## ④ 📌 案例 → 概念速查

| 案例 / 工具 | 用途 |
|---|---|
| **GDPR Article 22** | Right to Explanation 的法律来源 |
| **EU AI Act** | 高风险 AI 的严格透明度要求 |
| **中国算法推荐管理规定** | 算法专项监管 |
| **LIME** | Ribeiro 2016，局部线性近似解释 |
| **SHAP** | Lundberg & Lee 2017，基于 Shapley 值 |
| **DARPA XAI** | 三件套（模型+界面+心理学） |
| **IBM AIX360** | 多领域 XAI 工具包 |
| **Microsoft InterpretML** | 统一方法库 |
| **Google Model Cards** | 模型卡（行业透明度报告实现） |
| **Datasheets for Datasets** | 数据表标准 |
| **Rudin (2019)** | "Stop Explaining Black Box..." —— 主张高风险场景直接用可解释模型 |
| **Wachter et al. (2017)** | 反事实解释奠基 |
| **Unfair dismissal (Ch.7 Case 1)** | 本讲主教材案例 |

---

## ⑤ 🧠 缩写 / 法规 / 论文速查

| 项 | 含义 |
|---|---|
| **XAI** | Explainable AI |
| **LIME** | Local Interpretable Model-agnostic Explanations |
| **SHAP** | SHapley Additive exPlanations |
| **DARPA** | Defense Advanced Research Projects Agency（美国国防高级研究计划局） |
| **AIX360** | IBM AI Explainability 360 |
| **InterpretML** | Microsoft 开源 XAI 库 |
| **GDPR Art. 22** | 自动化个人决策条款 → Right to Explanation |
| **EU AI Act** | 欧盟 AI 法案（风险分级） |

### 关键论文
- **Ribeiro et al. (2016)** — *"Why Should I Trust You?"*（LIME 原文）
- **Lundberg & Lee (2017)** — *A Unified Approach to Interpreting Model Predictions*（SHAP 原文）
- **Wachter et al. (2017)** — *Counterfactual Explanations without Opening the Black Box*
- **Rudin (2019)** — *Stop Explaining Black Box ML Models...*（主张可解释模型优先）

---

## ⑥ 🕳️ 常见出题陷阱

1. **Transparency / Explainability / Interpretability 三词不同**：考题可能同时给三个选项，注意哪个是"制度层 / 技术层 / 认知层"。
2. **"可以透明但不可解释"**是真的——开源 100 万参数深度网络即是如此。
3. **Right to Explanation 来自 GDPR Article 22**，不是 HIPAA 或 EU AI Act。
4. **LIME 是 Local，SHAP 也是 Local**（但可聚合成 Global）。别选"Global only"。
5. **Counterfactual ≠ Factual**：反事实是 "if X were different...", 不是 "why X happened"。
6. **Saliency maps 主要用于 CV（图像）**，不是 NLP 文本的首选。
7. **Causal vs. Correlational 是 XAI 五大局限之一**——很多工具给的是相关性，不是因果。
8. **Tiered Transparency 的 3 层要记清**：Public / Regulatory / Internal（从高到低）。
9. **DARPA 是美国的**，不是欧盟或日本。
10. **Model-agnostic 意为"适用任意模型"**，不是"没有模型"。
11. **Rudin (2019) 的主张是"高风险场景不要用黑箱"**，不是"XAI 无用"。
12. **"对抗攻击解释"是 XAI 局限之一**——解释可被操纵。
13. **Algorithmic accountability 是本讲概念之一**（在 Topic 6 中会深挖）。
14. **高风险场景下监管可能限制模型选择**——可解释性反过来约束了可用模型。

---

## ⑦ 🎯 本讲练习题（10 道 MCQ）

**Q1.** Which term best describes **"the degree to which a human can understand the cause of a model's decision"**?
- A. Transparency
- B. Explainability
- C. Interpretability
- D. Accountability

**Q2.** **LIME** and **SHAP** are both examples of:
- A. Global, model-specific explanation methods
- B. Local, model-agnostic explanation methods
- C. Rule-based explanation only
- D. Counterfactual explanation only

**Q3.** The **Right to Explanation** originates from:
- A. EU AI Act Article 5
- B. GDPR Article 22
- C. HIPAA Privacy Rule
- D. China's Algorithmic Recommendation Provisions

**Q4.** Which is NOT one of the three XAI toolkits/frameworks mentioned?
- A. DARPA XAI program framework
- B. IBM AI Explainability 360
- C. Microsoft InterpretML
- D. Google Cloud AutoML

**Q5.** A **counterfactual explanation** for a loan rejection would most likely state:
- A. "Your credit score has a SHAP value of -0.42"
- B. "If your income were $5,000 higher, the loan would have been approved"
- C. "Decision trees outperform neural nets on this task"
- D. "The model is 87% accurate on the test set"

**Q6.** **Tiered transparency** means:
- A. Publishing everything to the public by default
- B. Different levels of disclosure for public, regulators, and internal teams
- C. Encrypting all model weights
- D. Outsourcing explanations to a third party

**Q7.** Which limitation of XAI involves explanations being **manipulated to mislead users**?
- A. Performance trade-off
- B. Adversarial attacks on explanation methods
- C. Causal vs. correlational confusion
- D. Customization challenges

**Q8.** Which of the following is a valid statement about **Transparency vs. Explainability**?
- A. They are synonymous
- B. A system can be transparent (e.g., open-weighted) yet still not explainable
- C. Explainability implies full IP disclosure
- D. Transparency is only a technical property

**Q9.** According to Rudin (2019), for **high-stakes decisions**, we should prefer:
- A. Black box models with post-hoc explanations
- B. Inherently interpretable models over explaining black boxes
- C. Federated learning only
- D. Models with no transparency requirements

**Q10.** Which regulation uses a **risk-tiered approach** with strict transparency requirements for high-risk AI?
- A. HIPAA
- B. GDPR
- C. EU AI Act
- D. PIPL

---

## 📎 Appendix · 答案与解析

| Q | Ans | 解析 |
|---|---|---|
| 1 | **C** | Interpretability 是"认知层 / 人类理解程度"；Explainability 更偏"AI 产生解释"。 |
| 2 | **B** | LIME/SHAP 都是 local + model-agnostic。 |
| 3 | **B** | GDPR Article 22 的自动化决策条款。 |
| 4 | **D** | 三大工具框架是 DARPA/AIX360/InterpretML；Google AutoML 不是 XAI 框架。 |
| 5 | **B** | 反事实解释 = "if X were different..."。 |
| 6 | **B** | 分层透明 = Public/Regulatory/Internal 三层不同披露。 |
| 7 | **B** | 对抗攻击 XAI 是五大局限之一。 |
| 8 | **B** | 经典例子：开源大深度模型透明但难解释。 |
| 9 | **B** | Rudin 主张高风险直接用可解释模型而非解释黑箱。 |
| 10 | **C** | EU AI Act = 风险分级 + 高风险严格透明度。 |
