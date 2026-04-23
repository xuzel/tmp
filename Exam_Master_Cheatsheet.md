# ARIN 5104 · Exam Master Cheatsheet

> 📌 **用法**：考前 30 分钟最后一轮扫读。每一节都是跨讲高频整合，查漏补缺。

---

## ① 全课 10 讲一张图

```
┌────────────────────────────────────────────────────────┐
│            ARIN 5104: AI Ethics 知识骨架                │
├────────────────────────────────────────────────────────┤
│                                                        │
│  【Part 1 · 哲学基础】                                   │
│  L1 Introduction → F-P-T-A-S-B 6 原则 + U/D/V 3 框架   │
│  L2 Philosophical Foundations → U/D/V 深挖 + Trolley   │
│                                                        │
│  【Part 2 · 四大核心议题】                               │
│  L3 Bias & Fairness → 3 类型 / 6 来源 / 3 公平 / 3 指标│
│  L4 Privacy → DFHSPM 6 PETs + GDPR/PIPL/HIPAA         │
│  L5 Transparency → T/E/I 3 层 + LIME/SHAP + Tiered    │
│  L6 Accountability → R/A/L 3 区分 + Meaningful Oversight│
│                                                        │
│  【Part 3 · 宏观与应用】                                 │
│  L7 Social Impact → Displacement/Complementarity +    │
│                   Liar's Dividend + PVM + Helicopter  │
│  L8 Autonomous Systems → AV + AWS + Ethics-by-Design  │
│  L9 AI in Healthcare → 6 来源×4 类型×5 方法            │
│                     + WHO 指南 + Two-tiered          │
│  L10 Governance → 4 阵营 + EU AI Act + OECD/UNESCO/IEEE│
│                                                        │
└────────────────────────────────────────────────────────┘
```

---

## ② 跨讲高频考点 Top 30

| # | 考点 | 来源讲 | 关键词 |
|---|---|---|---|
| 1 | AI 伦理 6 大原则（F-P-T-A-S-B） | L1 | Fairness/Privacy/Transparency/Accountability/Safety/Beneficence |
| 2 | 3 大伦理学框架 | L1, L2 | Utilitarianism / Deontology / Virtue Ethics |
| 3 | 功利主义代表人物 | L2 | Bentham（hedonistic calculus） + Mill（rule utilitarianism） |
| 4 | 义务论代表人物 | L2 | Kant（Categorical Imperative） |
| 5 | 德性伦理代表 + 核心概念 | L2 | Aristotle + eudaimonia + phronesis |
| 6 | "The end justifies the means" 属哪个框架 | L2 | Utilitarianism（义务论相反） |
| 7 | 3 种偏见类型 | L3 | Algorithmic / Selection / Sampling |
| 8 | 6 种偏见来源 | L3 | Data/Labeling/Feature/Proxy/Developer/Feedback |
| 9 | 3 种公平观 | L3 | Individual / Group / Counterfactual |
| 10 | 3 种公平指标 | L3 | DP / EO / EQ |
| 11 | Impossibility Theorem | L3 | 多公平标准不可同时满足 |
| 12 | "Fairness through unawareness" 为何失败 | L3 | Proxy variables 仍能泄露敏感属性 |
| 13 | 6 种核心 PETs | L4 | Differential Privacy / Federated Learning / HE / SMC / PPRL / Masking |
| 14 | GDPR + PIPL + HIPAA 三大法规 | L4, L10 | EU / China / USA Healthcare |
| 15 | GDPR 两大衍生权利 | L4 | Right to be forgotten + Right to Explanation |
| 16 | Transparency / Explainability / Interpretability 三层 | L5 | 制度 / 技术 / 认知 |
| 17 | 3 大 XAI 工具框架 | L5 | DARPA / IBM AIX360 / Microsoft InterpretML |
| 18 | LIME + SHAP | L5 | Local + Model-agnostic |
| 19 | Tiered Transparency 3 层 | L5 | Public / Regulatory / Internal |
| 20 | Responsibility vs. Accountability vs. Liability | L6 | ex ante / ex post / legal |
| 21 | Proportionality Principle | L6 | 归责与过错相称 |
| 22 | Automation Bias | L6, L8, L9 | 人类过度信任自动化 |
| 23 | Foreseeability 在 AI 语境失效 | L6 | 开发者自己无法预见输出 |
| 24 | Displacement vs. Complementarity | L7 | 就业双效应 |
| 25 | Liar's Dividend | L7 | 真内容被怀疑 |
| 26 | Prime Vulnerability Moments | L7 | 脆弱时刻剥削 |
| 27 | Helicopter Research | L7 | 数据殖民主义 |
| 28 | 94% 事故源于人为失误 | L8 | 自动驾驶功利论据 |
| 29 | Distinction + Proportionality（IHL） | L8 | 区分 + 比例 |
| 30 | EU AI Act 4 风险等级 | L10 | Unacceptable / High / Limited / Minimal |

---

## ③ 跨讲易混对比

### A. Transparency 系列概念（超高频）
| 讲 | 概念 | 核心 |
|---|---|---|
| L1 | Transparency（原则 3） | 与 Explainability 合并为一个原则 |
| L5 | **Transparency** | 制度层公开 |
| L5 | **Explainability** | 技术层解释 |
| L5 | **Interpretability** | 认知层理解 |
| L6 | Algorithmic accountability | 开发者/部署者负责 |
| L10 | Transparency in Governance | 多利益方披露 |

### B. Responsibility 系列概念
| 讲 | 概念 | 说明 |
|---|---|---|
| L2 | **Moral responsibility** | 伦理行动 + 承担后果 |
| L6 | **Responsibility**（ex ante） | 我本该做什么 |
| L6 | **Accountability**（ex post） | 出事了谁负责 |
| L6 | **Liability**（法律） | 谁赔偿 |
| L6 | **Moral agency** | AI 能否成为责任主体 |
| L8 | **Shared responsibility** | 人+AI 共担 |

### C. Bias 概念在不同讲出现
| 讲 | 概念 | 作用 |
|---|---|---|
| L3 | **3 Types** | Algorithmic/Selection/Sampling |
| L3 | **6 Sources** | Data/Labeling/Feature/Proxy/Developer/Feedback |
| L6 | **Automation bias** | 人类过信 AI |
| L7 | **Recommendation bias → Echo chamber** | 回音壁 |
| L9 | **医疗 6 来源 + 4 类型** | 扩展 L3 |
| L9 | **Confounding bias** | 医疗 AI 特有——相关当因果 |

### D. Privacy 概念在不同讲出现
| 讲 | 重点 |
|---|---|
| L1 | 6 原则之一 |
| L4 | 全面展开（PETs + 法规） |
| L5 | 隐私 vs. 透明 IP 平衡 |
| L7 | 监控资本主义 |
| L9 | 医疗敏感数据 + 再识别 |
| L10 | GDPR 与治理法规 |

### E. 3 大伦理框架的跨讲复用
| 讲 | 应用 |
|---|---|
| L1 | 初次引入 |
| L2 | 深入对比 U/D/V |
| L4 | 数据伦理应用（4 框架含 Social Contract + Care） |
| L7 | 社会影响伦理分析 |
| L8 | 自动驾驶 Trolley Problem |
| L9 | 医疗伦理决策 |

---

## ④ 命名案例总表（30+ 案例）

### 偏见与公平（L3）
- **COMPAS** = 再犯预测（种族偏见）
- **执法人脸识别** = 种族/肤色
- **Amazon 招聘 AI** = 性别歧视女性
- **Apple Card** = 性别（信用额度）
- **Google Photos "gorillas"** = 种族（分类错误）
- **医疗 AI 肤色** = 深色肤色准确率低

### 隐私（L4）
- **Netflix 2006 匿名数据集** = 再识别经典
- **Cambridge Analytica** = 数据挪用（亦出现于 L7/L10）
- **Genetic privacy** = Stahl Ch.3 Case 2
- **Biometric surveillance** = Stahl Ch.3 Case 3
- **Smart home hubs security** = Stahl Ch.6 Case 2

### 透明度（L5）
- **Unfair dismissal** = Stahl Ch.7 Case 1
- **Model Cards（Google）** = 透明度标准化实现
- **LIME（Ribeiro 2016）** / **SHAP（Lundberg & Lee 2017）** / **Counterfactual（Wachter et al. 2017）** / **Rudin (2019)**

### 问责（L6）
- **Matthias (2004) Responsibility Gap** = 学习自动机责任鸿沟
- **Floridi et al. (2018) AI4People** = 五大原则
- **AI Incident Database / AIAAIC** = 事件登记
- **EU AI Liability Directive (2022)**
- **NIST AI RMF (2023)**

### 社会影响（L7）
- **Cambridge Analytica** = 选举操纵（Ch.5 Case 1）
- **Prime Vulnerability Moments** = Ch.5 Case 2
- **Sex robots** = Ch.7 Case 2
- **Care robots** = Ch.7 Case 3
- **Climate forecasting in resource-limited settings** = Ch.8 Case 1
- **Helicopter Research** = Ch.8 Case 2

### 自主系统（L8）
- **Moral Machine Experiment（MIT, Awad 2018）**
- **Uber Elaine Herzberg (2018)** = AV 致死事故
- **Tesla Autopilot 系列** = Shared responsibility
- **Stop Killer Robots 运动**
- **Fatal crash involving self-driving car** = Stahl Ch.6 Case 1
- **Swarm warfare（乌克兰战场）**

### 医疗（L9）
- **CT 肺结节检测** = Early detection 超越人类
- **IBM Watson Oncology** = 医疗 AI 失败（亦 L10）
- **FDA SaMD** = 医疗 AI 监管（亦 L10）
- **Monetization of health data** = Stahl Ch.4 Case 2
- **Adversarial attacks in medical diagnosis** = Stahl Ch.6 Case 3

### 治理（L10）
- **Cambridge Analytica** = 社交媒体治理
- **San Francisco facial recognition ban**
- **EU AI Act（风险分级）**
- **NHTSA guidelines + State-level AV laws**
- **IBM Watson + FDA AI/ML SaMD**

---

## ⑤ 法规 + 年份总表

| 法规 | 全称 | 地区 | 年份 | 要点 |
|---|---|---|---|---|
| **GDPR** | General Data Protection Regulation | EU | **2018** 生效 | 最高罚 **4%** 年收入；Right to be forgotten + Right to Explanation |
| **PIPL** | Personal Information Protection Law | China | **2021** 生效 | 最高罚 **5%** 年收入；数据本地化 |
| **HIPAA** | Health Insurance Portability and Accountability Act | USA | **1996** | 保护 **PHI** 健康信息 |
| **EU AI Act** | Artificial Intelligence Act | EU | 2024 生效 / 2026 全面 | 4 风险等级；全球首个综合 AI 法律 |
| **China 算法推荐规定** | Internet Information Service Algorithmic Recommendation Management Provisions | China | 2022 | 算法专项 |
| **OECD AI Principles** | - | 41 国采纳 | 2019 | 非约束性 |
| **UNESCO Recommendation on AI Ethics** | - | UN | 2021 | 伦理框架 |
| **IEEE Ethically Aligned Design** | - | 标准组织 | 2019 (v1) | 工程指引 |
| **Dartmouth Conference** | - | USA | **1956** | AI 学科命名 |
| **AI Winter** | - | - | **1970s–1980s** | 伦理讨论暂停期 |

---

## ⑥ 哲学框架总表（在 6+ 讲复用）

| 框架 | 核心 | 代表 | 问法 |
|---|---|---|---|
| **Utilitarianism** | 结果/福祉 | Bentham, Mill | "Does it produce net good?" |
| **Deontology** | 规则/义务 | Kant | "Does it follow the rule?" |
| **Virtue Ethics** | 品格/美德 | Aristotle | "Does it contribute to virtue?" |
| **Consequentialism** | 后果主义大类 | - | Utilitarianism 的母类 |
| **Social Contract Theory**（L4） | 公平互惠 | Rousseau/Rawls | AI 开发者-公众契约 |
| **Rights-based**（L4） | 基本权利 | Locke | 隐私/非歧视保护 |
| **Care Ethics**（L4） | 关系/情境 | Gilligan/Noddings | 医患关系 |
| **Distributive Justice**（L7） | 公平分配 | **Rawls** | AI 财富如何分配 |

---

## ⑦ 常见出题陷阱 10 大类型 + 应对

### 1. NOT 型（"Which is NOT..."）
✅ **策略**：把所有选项列出看谁不在原始列表；4 大/6 大/3 大定论要烂熟。

### 2. EXCEPT 型（"All of the following EXCEPT..."）
✅ **策略**：和 NOT 型同类；注意错选项可能是"概念相关但不在清单中"，如"Blockchain consensus 不是 6 种 PETs"。

### 3. BEST 型（"Which BEST describes..."）
✅ **策略**：选最精准、最覆盖核心的定义；排除"太窄"或"太泛"的。

### 4. 对比型（Transparency vs. Explainability）
✅ **策略**：Transparency = 制度；Explainability = 技术；Interpretability = 认知。

### 5. 案例匹配型（"Which case BEST illustrates..."）
✅ **策略**：Cambridge Analytica = 社交/民主；COMPAS = 刑事司法；Amazon = 招聘性别；Moral Machine = 文化差异。

### 6. 人物配对型（"Who formulated..."）
✅ **策略**：Categorical Imperative → Kant；Hedonistic Calculus → Bentham；Eudaimonia → Aristotle；Responsibility Gap → Matthias；Age of Surveillance Capitalism → Zuboff。

### 7. 缩写辨识型
✅ **策略**：GDPR/PIPL/HIPAA/LIME/SHAP/DP/FL/HE/SMC/V&V/AWS/AV 必须一眼识别。

### 8. 年份/数字型
✅ **策略**：1956 Dartmouth；1970s-80s AI Winter；2018 GDPR；2021 PIPL；94% 人为失误；130 万年度交通死亡。

### 9. 分类/等级型
✅ **策略**：EU AI Act 4 等级：Unacceptable/High/Limited/Minimal；Tiered Transparency：Public/Regulatory/Internal。

### 10. 顺序型（"Which comes FIRST..."）
✅ **策略**：
- 三阶段偏见缓解：**Preprocessing → Model Design → Postprocessing**
- 5 步伦理分析：**Stakeholders → Consequences → Frameworks → Moral Uncertainty → Trade-offs**
- Responsibility → Accountability → Liability

---

## 🎯 考前 15 分钟极速清单

### 必背 10 条
1. **6 原则 F-P-T-A-S-B**（Topic 1 核心）
2. **3 框架 U-D-V**（Topic 2 核心）+ 代表人物
3. **6 种 PETs**（DFHSPM）+ **3 大法规**（GDPR/PIPL/HIPAA）
4. **3 公平观 + 3 公平指标**（Individual/Group/Counterfactual; DP/EO/EQ）
5. **3 层概念**（Transparency/Explainability/Interpretability）+ **LIME/SHAP**
6. **R/A/L 3 概念辨析** + **Proportionality**
7. **Displacement vs. Complementarity** + **Liar's Dividend + PVM + Helicopter Research**
8. **Moral Machine + 94% 人为失误 + Ethics-by-Design + Distinction/Proportionality**
9. **医疗 6 来源 × 4 类型 × 5 方法** + **WHO 指南**
10. **EU AI Act 4 等级 + 4 阵营 + O/U/I 国际指南**

### 看到这些关键词就选对应答案
- "Categorical Imperative" → **Kant, Deontology**
- "Hedonistic Calculus" → **Bentham, Utilitarianism**
- "Eudaimonia / Phronesis" → **Aristotle, Virtue Ethics**
- "Right to be forgotten / Explanation" → **GDPR**
- "4% annual revenue" → **GDPR**；"5%" → **PIPL**
- "Protected Health Information（PHI）" → **HIPAA**
- "Social scoring prohibited" → **EU AI Act**
- "Federated Learning" → **数据不出本地**
- "Homomorphic encryption" → **加密数据直接计算**
- "Differential Privacy" → **加噪声保统计效用**
- "Impossibility Theorem" → **Topic 3 多公平准则不可同时满足**
- "Fairness through unawareness fails" → **Proxy variables**
- "COMPAS" → **再犯预测种族偏见**
- "Cambridge Analytica" → **社交媒体操纵民主**
- "Moral Machine" → **自动驾驶文化差异**
- "94% human error" → **自动驾驶事故数据**
- "Distinction + Proportionality" → **IHL AWS**
- "Meaningful Human Control" → **军控辩论 AWS**
- "Liar's Dividend" → **真内容被质疑**
- "Prime Vulnerability Moments" → **脆弱时刻剥削**
- "Helicopter Research" → **数据殖民主义**
- "Ethics-by-design" → **自主系统 4 工程原则之首**
- "WHO Guidelines" → **医疗 AI**
- "IBM Watson" → **医疗 AI 失败**
- "NHTSA" → **美国 AV 监管**
- "FDA SaMD" → **美国医疗 AI 监管**
- "Risk-tiered" → **EU AI Act**
- "Non-binding / Fragmentation / Representation" → **N-F-R 全球治理 3 局限**
- "OECD / UNESCO / IEEE" → **3 大国际指南**（O-U-I）
