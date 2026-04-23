# Lecture 3 · Bias and Fairness — 考试冲刺包

> ⚠️ **本讲为考试重点**——术语、列表、案例都是高频考点。

---

## ① ⚡ 30 秒速记卡（Core Terms）

- **AI bias** = AI 系统中的 **系统性错误或不公平**，导致歧视性结果
- **Fairness in AI** = 确保 AI 公正对待所有个体/群体，不基于 protected attributes 歧视
- **Protected attributes** = 不应影响 AI 决策的特征（**ethnicity, gender, age, disability status**）
- **Algorithmic fairness** = 开发 AI 使其决策不歧视特定群体/个人
- **Algorithmic bias** = 系统性错误 → 不公平结果
- **Selection bias** = 训练数据未代表目标群体
- **Sampling bias** = 数据中某些群体被过度或不足代表
- **Proxy variables（代理变量）** = 与受保护属性相关的变量（如邮政编码代理种族）→ 最阴险
- **Feedback loops（反馈循环）** = 部署后的反馈随时间放大偏见
- **Individual fairness** = 相似个体相似结果
- **Group fairness** = 群体间预测保持一致/平衡
- **Counterfactual fairness** = 改变敏感属性后决策不变
- **Demographic parity（DP）** = 不同群体获得正预测的比率相同
- **Equal opportunity（EO）** = 真阳性率（TPR）在群体间相等
- **Equalized odds（EQ）** = 真阳性率 + 假阳性率都在群体间相等
- **Impossibility theorem** = 多种公平准则 **不可能同时满足**
- **Accuracy-fairness trade-off** = 提升公平指标可能降低准确率
- **Pareto optimality** = 多目标权衡的可视化方法
- **"Fairness through unawareness"** = 删字段 ≠ 消除偏见（**入门陷阱**）
- **COMPAS** = 再犯预测工具；黑人被告风险评分系统性偏高
- **Amazon recruiting tool** = 性别偏见，歧视女性
- **Apple Card** = 性别偏见，女性信用额度更低
- **Google Photos** = 将黑人错误标注为 "gorillas"
- **Echo chamber / Filter bubble** = 内容推荐引发的回音壁 / 过滤气泡
- **AIF360** = IBM 开源偏见检测缓解库

---

## ② 🔢 编号清单全收录

### 🔸 4 大核心定义
AI bias · Fairness in AI · Protected attributes · Algorithmic fairness

### 🔸 3 大偏见类型（常见 type）
1. **Algorithmic bias** · 2. **Selection bias** · 3. **Sampling bias**

### 🔸 6 大偏见来源（必背！考点密集）
1. **Data collection**（数据收集）
2. **Data labeling**（数据标注）
3. **Feature selection**（特征选择）
4. **Proxy variables**（代理变量）
5. **Developer biases**（开发者偏见）
6. **Feedback loops**（反馈循环）

记忆法：**"数据—标注—特征—代理—人—反馈"**

### 🔸 7 大受影响领域（必背）
1. Hiring & Lending
2. Facial Recognition
3. Healthcare
4. Education
5. Content Recommendation
6. Criminal Justice
7. **Large Language Models**（LLM 生成与放大刻板印象）

### 🔸 6 大"臭名昭著"真实案例
1. **COMPAS**（再犯预测，种族）
2. **执法人脸识别**（种族/肤色）
3. **Amazon 招聘 AI**（性别）
4. **Apple Card**（性别）
5. **Google Photos "gorillas"**（种族）
6. **医疗 AI 肤色问题**（深色肤色准确率低）

### 🔸 3 大公平观（Notions of Fairness）
1. **Individual fairness** · 2. **Group fairness** · 3. **Counterfactual fairness**

### 🔸 3 大公平指标（Metrics）
**DP → EO → EQ**（从宽松到严格）
1. **Demographic parity**
2. **Equal opportunity**
3. **Equalized odds**

### 🔸 算法公平的 3 大目标
1. Public trust · 2. Legal compliance · 3. Ethical integrity

### 🔸 4 大算法公平挑战
1. 公平定义间的固有权衡（Impossibility）
2. 现实场景复杂性
3. 非预期后果
4. 多学科协作需求（**Computer scientists + Ethicists + Legal + Domain specialists**）

### 🔸 3 大反歧视策略
1. **Fairness through unawareness**（不够）
2. **Algorithmic transparency & explainability**
3. **Proactive measures**（多元数据 + 定期审计 + 缓解技术）

### 🔸 3 大权衡概念
1. **Impossibility theorem**
2. **Accuracy-fairness trade-offs**
3. **Pareto optimality**

### 🔸 3 大管理权衡技术
1. Multi-objective optimization · 2. Constrained optimization · 3. Adversarial debiasing

### 🔸 偏见缓解的 3 阶段框架（核心！）
```
Data Preprocessing → Smart Model Design → Postprocessing
```

**阶段 1（Preprocessing）工具箱**：
- Oversampling, Undersampling, Data Augmentation
- Feature Selection, Feature Engineering, Data Cleaning, Normalization
- Bias Detection Algorithms, Fairness Constraints, Causal Inference

**阶段 2（Smart Design）工具箱**：
- Regularization, Ensemble Methods, Dropout
- Adversarial Debiasing, Multi-Task Learning, Fair Representation Learning
- Transfer Learning, Domain Adaptation, Continual Learning

**阶段 3（Postprocessing）工具箱**：
- Threshold Adjustment, Calibration, Reject Option Classification
- Reweighting, Equalized Odds Postprocessing, Fairness Constraints
- Counterfactual Fairness, Causal Inference, Fairness through Unawareness

---

## ③ ⚠️ 易混概念对比表

### A. 三大偏见类型（Type）
| 类型 | 含义 |
|---|---|
| **Algorithmic bias** | 算法设计层面的系统性错误 |
| **Selection bias** | 训练数据不代表目标人群 |
| **Sampling bias** | 某些群体过度/不足代表 |

### B. 三大公平观对比（必背）
| 公平观 | 核心逻辑 | 一句话 |
|---|---|---|
| **Individual** | 相似个体相似结果 | "相似人相似待" |
| **Group** | 群体间结果平衡 | "群间一致" |
| **Counterfactual** | 改敏感属性决策不变 | "改种族，结果不变" |

### C. 三大公平指标对比（超高频！）
| 指标 | 等式要求 | 强度 |
|---|---|---|
| **Demographic parity（DP）** | 正预测率（P(ŷ=1)）相同 | 最宽松 |
| **Equal opportunity（EO）** | **TPR** 相同（只在真标签=1 上） | 中等 |
| **Equalized odds（EQ）** | **TPR + FPR** 都相同 | 最严格 |

### D. Individual fairness vs. Group fairness（经典冲突）
- 它们 **可能冲突**：做到个体一致，未必群体均衡；反之亦然
- **Impossibility theorem** 表明多种公平准则不可能同时满足

### E. Oversampling vs. Undersampling
- **Oversampling**：**增加**少数类样本
- **Undersampling**：**减少**多数类样本

### F. Bias 类型 vs. Bias 来源（易混！）
- **Type（类型）**= 3 个：Algorithmic / Selection / Sampling
- **Source（来源）**= 6 个：Data collection / Labeling / Feature / Proxy / Developer / Feedback

---

## ④ 📌 案例 → 概念速查

| 案例 | 偏见主轴 | 核心来源 | 关键教训 |
|---|---|---|---|
| **COMPAS** | 种族偏见（再犯预测） | Data collection + Proxy + Feedback | 历史司法数据 → 继承种族不平等 |
| **执法人脸识别** | 种族/肤色（准确率） | Sampling（训练集白人为主） | 肤色越深识别越差 |
| **Amazon 招聘 AI** | 性别 | Data collection（简历历史男性为主）+ Proxy（含"女子学院"等词） | 学历关键词代理性别 |
| **Apple Card** | 性别（信用额度） | Proxy + Developer biases | 同等条件女性额度低 |
| **Google Photos** | 种族（分类错误） | Sampling + Labeling | 将黑人标为 "gorillas" |
| **医疗 AI（肤色）** | 肤色（准确率） | Sampling（浅色肤色样本为主） | 深色肤色诊断误差大 |
| **邮政编码→种族** | Proxy variables 经典 | Feature + Proxy | "删掉种族字段"依然歧视 |
| **推荐系统 echo chamber** | Feedback loop 经典 | Feedback + Feature | 部署后偏见自放大 |

---

## ⑤ 🧠 缩写 / 工具速查

| 缩写/工具 | 含义 |
|---|---|
| **DP** | Demographic Parity |
| **EO** | Equal Opportunity |
| **EQ / EOd** | Equalized Odds |
| **TPR** | True Positive Rate |
| **FPR** | False Positive Rate |
| **COMPAS** | Correctional Offender Management Profiling for Alternative Sanctions |
| **AIF360** | IBM AI Fairness 360（开源库） |
| **What-If Tool** | Google 模型公平性可视化工具 |
| **Fairlearn** | Microsoft 偏见评估与缓解工具 |
| **Gender Shades** | Buolamwini & Gebru (2018) 实证研究 |

### 关键论文（可作为 MCQ 来源选项）
- **Angwin et al. (2016)** — *Machine Bias*（COMPAS 调查报道，ProPublica）
- **Buolamwini & Gebru (2018)** — *Gender Shades*（人脸识别性别×肤色偏见）
- **Hardt et al. (2016)** — *Equality of Opportunity in Supervised Learning*（EO 理论）
- **Chouldechova (2017)** — *Fair Prediction with Disparate Impact*（不可能性定理）

---

## ⑥ 🕳️ 常见出题陷阱

1. **"删除敏感属性 = 实现公平"→ 错！** Proxy variables 会出卖你——这是 **Fairness through unawareness** 的经典陷阱。
2. **3 种偏见类型 vs. 6 种偏见来源**——不要混。**Type = Algorithmic/Selection/Sampling；Source = 六项（含 Data collection/Labeling 等）**。
3. **Demographic Parity 不等于 Equal Opportunity**：DP 要求正预测率相同（可能让真正合格的少数被拒），EO 只在真标签=1 的人群中要求 TPR 相同。
4. **Impossibility Theorem 说的是"多种公平标准无法同时被满足"**，不是"公平无法实现"。
5. **COMPAS = 再犯预测（criminal justice）**，不要和医疗 AI 或招聘 AI 搞混。
6. **Amazon 的招聘工具是实验性的，后被停用**，不是商业部署失败后持续使用。
7. **Google Photos 的 "gorillas" 事件是种族/分类偏见**，不是 gender 偏见。
8. **Oversampling 是加少数**，Undersampling 是减多数——别搞反。
9. **Feedback loops 属于"偏见来源"**，不是"偏见类型"或"公平指标"。
10. **Pareto optimality 是用来"分析权衡"的工具**，不是一种公平指标。
11. **Counterfactual fairness ≠ Equal Opportunity**：前者是公平观（因果视角），后者是公平指标。
12. **LLM 也会延续偏见**——本讲 7 大领域里包含 Large Language Models。

---

## ⑦ 🎯 本讲练习题（10 道 MCQ）

**Q1.** Which of the following is NOT one of the six sources of AI bias?
- A. Data collection
- B. Proxy variables
- C. Algorithmic transparency
- D. Feedback loops

**Q2.** The **COMPAS** tool is best known for bias in:
- A. Hiring recommendations
- B. Credit card limits
- C. Recidivism prediction in criminal justice
- D. Image classification

**Q3.** Which fairness metric requires BOTH **true positive rate AND false positive rate** to be equal across groups?
- A. Demographic parity
- B. Equal opportunity
- C. Equalized odds
- D. Counterfactual fairness

**Q4.** "Fairness through unawareness" (dropping protected attributes) is generally **insufficient** because:
- A. It violates GDPR
- B. Proxy variables can still encode sensitive information
- C. It reduces model accuracy to zero
- D. It is computationally too expensive

**Q5.** The **Impossibility Theorem** in algorithmic fairness states that:
- A. AI bias cannot be measured
- B. Multiple fairness criteria cannot all be satisfied simultaneously
- C. Fairness and accuracy are independent
- D. Group fairness is always preferable to individual fairness

**Q6.** The **Amazon** experimental recruiting AI exhibited which primary bias?
- A. Racial bias
- B. Age bias
- C. Gender bias against women
- D. Disability bias

**Q7.** Which technique belongs to the **Postprocessing** stage of bias mitigation?
- A. Oversampling
- B. Adversarial debiasing
- C. Threshold adjustment
- D. Data cleaning

**Q8.** **Counterfactual fairness** means that:
- A. All individuals get identical predictions
- B. If a person's protected attribute were changed while keeping other factors constant, the decision would remain the same
- C. True positive rates are equal across groups
- D. Protected attributes are removed before training

**Q9.** Which of the following is NOT one of the 3 notions of fairness discussed?
- A. Individual fairness
- B. Group fairness
- C. Counterfactual fairness
- D. Regulatory fairness

**Q10.** **Feedback loops** as a source of bias refer to:
- A. Biased labels during data annotation
- B. Deployed-system outcomes reinforcing existing biases over time
- C. Developer preferences affecting model architecture
- D. Use of proxy variables

---

## 📎 Appendix · 答案与解析

| Q | Ans | 解析 |
|---|---|---|
| 1 | **C** | 6 大来源：Data collection/Labeling/Feature/Proxy/Developer/Feedback loops。Transparency 是"策略"不是"来源"。 |
| 2 | **C** | COMPAS = 再犯预测工具，刑事司法领域。 |
| 3 | **C** | Equalized Odds 同时要求 TPR + FPR 相等，是最严格的指标。 |
| 4 | **B** | Proxy variables（如邮政编码代理种族）是核心原因。 |
| 5 | **B** | Impossibility Theorem 的核心主张。 |
| 6 | **C** | Amazon 工具歧视女性候选人（简历中含"女子学院"等词被降权）。 |
| 7 | **C** | Threshold adjustment 是后处理；Oversampling 和 Data cleaning 是预处理；Adversarial debiasing 是模型设计阶段。 |
| 8 | **B** | Counterfactual fairness 的定义。 |
| 9 | **D** | 3 种公平观是 Individual / Group / Counterfactual，无"Regulatory fairness"。 |
| 10 | **B** | Feedback loops = 部署后反馈随时间放大既有偏见。 |
