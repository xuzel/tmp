# Lecture 9 · AI in Healthcare — 考试冲刺包

---

## ① ⚡ 30 秒速记卡（Core Terms）

- **AI in Healthcare 5 大章节** = Introduction / Diagnosis & Treatment / Privacy & Confidentiality / Bias & Fairness / Personalized Medicine
- **Improved Diagnostic Capabilities** = AI 提升 **accuracy + speed** via pattern recognition
- **Personalized treatment planning** = AI 分析患者数据并预测结果
- **Early disease detection** = 例如 **lung cancer nodules on CT scans**
- **Misdiagnosis risk** = 偏见/算法错误 → 不当或延误治疗
- **"Black box" nature** = 解释 AI 辅助决策复杂
- **Deskilling** = 过度依赖 AI → 医疗人员技能退化
- **Informed consent（AI 版）** = 需包含 AI 参与诊断/治疗的解释
- **Patient autonomy** = 量身定制治疗增强患者自主权
- **Algorithmic accountability** = 医疗 AI 决策可解释可追责
- **Data minimization principle** = 只收集必要数据
- **WHO Ethical Guidelines** = 世卫组织医疗 AI 伦理指引
- **Data altruism** = 数据利他主义（患者为研究捐赠数据）
- **Blockchain for healthcare** = 安全数据共享 + 可扩展性挑战
- **Differential privacy** = 医疗匿名化的高级手段
- **Homomorphic encryption + SMC** = 医疗隐私增强技术
- **Data bias** = 训练集不代表目标人群
- **Algorithmic bias** = 设计选择/假设编码偏见
- **Sampling bias** = 特定群体过度/不足代表
- **Feature selection bias** = 相关变量被省略
- **Labeling bias** = 人类专家标注不一致
- **Temporal bias** = 历史数据不反映当前医学知识
- **Selection bias** = 非代表性样本训练
- **Confounding bias** = 错把相关当因果
- **Measurement bias** = 数据收集系统性错误
- **Automation bias** = 人类过度依赖 AI
- **Adversarial debiasing** = 去除敏感信息保持性能
- **Multistakeholder model development** = clinicians + patients + ethicists
- **AI-powered personalized medicine** = 基因+病史+生活方式的定制
- **Adverse drug reactions（ADR）** = 基于基因预测减少药物不良反应
- **Re-identification** = 聚合分析数据 → 重识别匿名患者
- **Two-tiered healthcare** = 两层医疗（AI 精准 vs. 传统）
- **Synthetic data / Federated learning** = 保护隐私同时训练 AI
- **Open-source AI models** = 透明但增加对抗攻击风险
- **Adversarial attacks in medical diagnosis** = 微小扰动误导 AI 诊断
- **Monetization of health data** = 健康数据货币化（主教材案例）

---

## ② 🔢 编号清单全收录

### 🔸 Roadmap 5 大章节
1. Introduction
2. Ethical Implications in Medical Diagnosis and Treatment
3. Privacy and Confidentiality in AI-driven Healthcare
4. Bias and Fairness in AI-assisted Medical Decision-Making
5. Ethical Considerations in AI-powered Personalized Medicine

### 🔸 AI 医疗 4 大增益能力
1. 诊断 **accuracy + speed**
2. **Personalized treatment planning**
3. 医学影像解读（**subtle abnormalities**）
4. **Early disease detection**（如 CT 肺结节）

### 🔸 AI 医疗 4 大隐忧（M-P-B-O）
1. **Misdiagnosis risk**
2. **Privacy issues**
3. **"Black box" nature**
4. **Overreliance → Deskilling**

### 🔸 Provider 5 大责任
1. 透彻理解 AI（含局限/偏见/数据质量）
2. 向患者保持 transparency
3. 定期更新知识
4. 报告错误/偏见/意外结果
5. 平衡 AI 与 **human touch and empathy**

### 🔸 Equity & Access 3 原则
1. 确保 equitable access
2. 考虑 AI 潜在偏见（种族/族裔）
3. 评估 AI 技术分布（避免新不平等）

### 🔸 Clinical Judgment 4 大作用
1. **Validate** AI 建议
2. **Interpret & contextualize** AI 输出
3. 处理 **complex / unusual** 病例
4. **Detect & correct** 偏见/错误

### 🔸 Synergistic Approach 4 原则
1. **Integrate** 人类判断 + AI
2. 处理 **ethical nuances**（end-of-life）
3. **Explain** AI 决策给患者
4. 保留 **override** 能力

### 🔸 Informed Consent 4 大挑战
1. 调整流程包含 AI 参与解释
2. 尊重 **right to refuse** AI 辅助
3. 患者理解复杂算法的挑战
4. AI 预测未来健康 → 信息披露两难

### 🔸 Data Privacy in Personalized Medicine 4 议题
1. 数据所有权/隐私/信息范围
2. AI 个性化 → 增强 patient autonomy
3. 遵守 AI 建议的压力平衡
4. **Safeguards**（anonymization / secure storage）

### 🔸 Data Vulnerabilities & Unintended Disclosures 6 大风险
1. 敏感患者数据访问 → 泄露漏洞
2. **Unintended disclosure** via 数据推断
3. AI + 医疗系统整合 → 新攻击向量
4. Predictive analytics 揭示敏感健康信息
5. **Real-time health data**（wearable/IoT）新隐私顾虑
6. **Re-identification** 匿名数据

### 🔸 Cloud-based 3 议题
1. 跨司法管辖区数据存储/传输
2. 国际数据传输协议（International data transfer agreements）
3. 云提供商 robust security measures（at rest + in transit）

### 🔸 伦理原则与问责 3 项
1. **Principle of data minimization**
2. **WHO Ethical Guidelines**（transparency/accountability/fairness）
3. **Algorithmic accountability**

### 🔸 Data Utility vs. Privacy 4 大权衡
1. 大数据集 → 模型稳健 vs. 隐私风险
2. 跨机构数据共享 → 加速研究 vs. 保密
3. **Synthetic data / Federated learning** → 隐私但性能限制
4. **Open-source models** → 透明 vs. 对抗攻击

### 🔸 Ethical Trade-offs 3 项
1. **Data altruism** 鼓励研究数据共享 vs. 自主权同意
2. 严格访问控制/匿名化 → 保护隐私 vs. 拖慢创新
3. **Blockchain** → 隐私增强 vs. scalability/compliance 挑战

### 🔸 技术安全 4 大措施
1. Robust encryption + access control（at rest + in transit）
2. 高级匿名化（**differential privacy**）
3. 定期 security audits + vulnerability assessments
4. **Privacy-enhancing technologies**（**homomorphic encryption / SMC**）

### 🔸 治理最佳实践 5 项
1. Comprehensive data governance policies
2. Transparent data management（患者可访问/更正）
3. **Ethical review boards** 专注医疗 AI
4. 教育培训（healthcare professionals + AI devs）
5. **Incident response plan**

### 🔸 ★ 医疗 AI 偏见来源 6 大（与 Topic 3 呼应）
1. **Data bias** 不代表目标人群
2. **Algorithmic bias** 设计编码偏见
3. **Sampling bias** 群体过度/不足代表
4. **Feature selection bias** 相关变量被省略
5. **Labeling bias** 专家标注不一致
6. **Temporal bias** 历史数据不反映当前

### 🔸 医疗 AI 特定偏见 4 类型
1. **Selection bias**
2. **Confounding bias**（相关 → 错当因果）
3. **Measurement bias**（系统性错误）
4. **Automation bias**（人类过度依赖）

### 🔸 偏见检测方法 5 项
1. **Fairness metrics**
2. **Bias auditing**
3. **Data preprocessing**
4. **Adversarial debiasing**
5. **Multistakeholder model development**（clinicians + patients + ethicists）

### 🔸 Tailoring Medical Treatments 6 大能力
1. 分析大数据集（基因/病史/生活方式）
2. **Patterns & correlations** 识别
3. **Continuous update** 建议
4. 减少 **Adverse Drug Reactions**
5. **Optimizes resource allocation**
6. **Earlier disease detection**

### 🔸 Personalized Medicine 隐私 5 风险
1. 敏感信息量大
2. 数据泄露
3. 匿名化挑战
4. 基因数据存储/共享伦理
5. 需要 **robust data governance frameworks**

### 🔸 Algorithmic Bias & Fairness 5 大挑战（个性化医疗）
1. Algorithmic bias 不公建议
2. **"Black box" nature** 信任问题
3. 多元代表性数据挑战
4. 定义衡量公平的伦理
5. **Ongoing monitoring & auditing**

### 🔸 Clinical Judgment & Responsibility 5 议题
1. 减少人类判断/专业
2. AI 生成洞察的 **ownership**
3. **Responsibility and liability** 错误
4. 明确 AI 角色与权限边界
5. **Human oversight** 至关重要

### 🔸 Economic & Infrastructure 5 壁垒
1. 高实施成本 → **Two-tiered healthcare**
2. Digital infrastructure + tech literacy 差距
3. 扩展到资源有限环境
4. 创新资金模式 + 公私合作
5. **Low-cost, scalable AI solutions**

### 🔸 Socioeconomic & Health Disparities 5 议题
1. 整合需要临床工作流程变革
2. 公平可及需更广社会经济因素
3. 加剧健康差距（若不谨慎）
4. 促进平等可及政策
5. 社区参与与教育

### 🔸 Communication & Trust 5 议题
1. 沟通 AI 建议的挑战
2. 医学教育新方法
3. 透明度维持
4. 管理患者期望与信任
5. 应对顾虑与怀疑

### 🔸 主教材案例（Stahl et al. 2023）
- **Ch.4, Case 2**：**Monetization of health data**
- **Ch.6, Case 3**：**Adversarial attacks in medical diagnosis**

---

## ③ ⚠️ 易混概念对比表

### A. 医疗 AI 6 来源 vs. 4 类型 vs. 5 方法
- **6 来源**（Source）：Data / Algorithmic / Sampling / Feature / Labeling / **Temporal**
- **4 类型**（Specific）：Selection / **Confounding** / Measurement / **Automation**
- **5 方法**（Mitigation）：Fairness metrics / Bias auditing / Preprocessing / **Adversarial debiasing** / Multistakeholder

### B. 医疗 AI 4 大隐忧（M-P-B-O）
| 隐忧 | 核心机制 |
|---|---|
| **Misdiagnosis risk** | 偏见/错误 → 不当治疗 |
| **Privacy issues** | 敏感数据大量收集 |
| **"Black box"** | 决策解释复杂 |
| **Overreliance → Deskilling** | 技能退化 |

### C. Provider Responsibilities vs. Clinical Judgment 作用
- **Provider 5 责任** = 理解/透明/更新/报告/人情味
- **Clinical Judgment 4 作用** = Validate/Contextualize/复杂病例/纠错

### D. Data Altruism 双刃
- 鼓励患者捐数据推动研究 ↔ 引发自主权与同意问题

### E. Two-tiered Healthcare
- 富人 = AI 精准医疗 VIP
- 穷人 = 传统经验医疗
- → 加剧 **Digital divide**（与 Topic 7 呼应）

### F. Federated Learning in Healthcare
- 保护隐私 ↔ 可能限制模型性能

---

## ④ 📌 案例 → 概念速查

| 案例 | 核心议题 |
|---|---|
| **CT 扫描肺结节检测** | Early disease detection 超越人类 |
| **深色肤色医疗 AI** | Algorithmic bias + Sampling |
| **Wearable / IoT 健康监测** | Real-time data + Continuous monitoring 隐私 |
| **Genetic testing（如 23andMe）** | 基因数据家庭延伸 + Consent |
| **Monetization of health data（Ch.4 Case 2）** | 数据所有权 + 货币化 |
| **Adversarial attacks in medical diagnosis（Ch.6 Case 3）** | 对抗攻击 + 良/恶性误判 |
| **IBM Watson for Oncology 失败** | 医疗 AI 实施风险（与 Topic 10 联动） |
| **FDA AI/ML-based SaMD** | FDA 对医疗 AI 监管（与 Topic 10 联动） |

---

## ⑤ 🧠 缩写 / 组织 / 法规速查

| 项 | 含义 |
|---|---|
| **WHO** | World Health Organization 世卫组织 |
| **FDA** | US Food and Drug Administration |
| **HIPAA** | US 医疗隐私法 |
| **PHI** | Protected Health Information |
| **ADR** | Adverse Drug Reaction（药物不良反应） |
| **EHR** | Electronic Health Record |
| **IoT** | Internet of Things |
| **SaMD** | Software as a Medical Device |
| **CT** | Computed Tomography |
| **ML** | Machine Learning |
| **FL** | Federated Learning |
| **DP** | Differential Privacy |
| **HE** | Homomorphic Encryption |
| **SMC** | Secure Multi-Party Computation |

---

## ⑥ 🕳️ 常见出题陷阱

1. **AI 在诊断上 "potentially surpasses" 人类**——用词谨慎，不是"全面取代"。
2. **Deskilling 是长期隐藏风险**——不是立即显现的问题。
3. **Provider Responsibilities 最后一条是"Balance with human touch and empathy"**——别漏。
4. **Override AI 能力是 Synergistic Approach 的第 4 条**——医生必须保留推翻 AI 权。
5. **医疗偏见 6 来源 vs. 4 类型** 别混——前者是产生偏见的过程，后者是具体形式。
6. **Temporal bias = 历史数据过时**，非"时间点偏见"。
7. **Confounding bias ≠ Sampling bias**——前者相关误认因果，后者群体代表性。
8. **Automation bias 在本讲再次出现**——与 Topic 6 呼应。
9. **Data altruism 引发的是 autonomy & consent 问题**——不是安全问题。
10. **Federated Learning 可能限制性能**——不是万能方案。
11. **Two-tiered healthcare 是现实**，不是假设——富人已享有 AI 精准医疗。
12. **WHO 提出的伦理指南强调 transparency/accountability/fairness**——记住 3 要素。
13. **基因数据特殊：影响家族成员**——传统同意框架难覆盖。
14. **Stahl 教材指定案例只有 2 个**：Ch.4 Case 2 + Ch.6 Case 3。
15. **Adversarial attacks 在医疗是"对抗扰动误导诊断"**——不是"医患对抗"。

---

## ⑦ 🎯 本讲练习题（10 道 MCQ）

**Q1.** Which of the following is NOT among the four main concerns ("drawbacks") of AI in healthcare discussed?
- A. Misdiagnosis risk
- B. Privacy issues
- C. "Black box" opacity
- D. Faster board meetings

**Q2.** **Deskilling** refers to:
- A. Reducing the number of medical specialties
- B. Overreliance on AI leading to loss of independent clinician judgment
- C. Removing AI from clinical workflows
- D. Outsourcing diagnosis to other hospitals

**Q3.** Which of the following is a **source** (not a type) of bias in medical AI?
- A. Confounding bias
- B. Automation bias
- C. Temporal bias
- D. Selection bias

**Q4.** The **synergistic approach** in AI-assisted medicine requires clinicians to:
- A. Fully replace human decisions with AI outputs
- B. Retain the ability to override AI recommendations when clinically necessary
- C. Publish all algorithms openly
- D. Disable AI tools outside business hours

**Q5.** **Data altruism** most directly raises concerns about:
- A. Cybersecurity of cloud servers
- B. Individual autonomy and informed consent
- C. Network bandwidth
- D. GDP growth

**Q6.** Which bias type occurs when an AI model mistakenly treats **correlated variables as causal**?
- A. Sampling bias
- B. Confounding bias
- C. Labeling bias
- D. Feature selection bias

**Q7.** Which technique is NOT listed as a bias detection/mitigation method for medical AI?
- A. Fairness metrics
- B. Bias auditing
- C. Adversarial debiasing
- D. Cryptocurrency mining

**Q8.** Which organization's ethical guidelines are highlighted as emphasizing **transparency, accountability, and fairness** in AI-driven healthcare?
- A. IEEE
- B. WHO
- C. FDA
- D. UNESCO

**Q9.** The phrase **"two-tiered healthcare system"** in this lecture warns that:
- A. Hospitals may have two types of operating rooms
- B. High AI costs may restrict personalized medicine to wealthy institutions
- C. AI models should be trained in two stages
- D. Patients must pay twice for AI consultations

**Q10.** The **adversarial attack** case from Stahl Ch.6 Case 3 illustrates that:
- A. Medical AI is immune to manipulation
- B. Small perturbations can cause AI to misclassify malignant vs. benign tumors
- C. Adversarial training always improves accuracy
- D. Only open-source models can be attacked

---

## 📎 Appendix · 答案与解析

| Q | Ans | 解析 |
|---|---|---|
| 1 | **D** | 四隐忧 = M/P/B/O；"faster board meetings"是杜撰。 |
| 2 | **B** | 过度依赖 AI 导致独立判断能力退化。 |
| 3 | **C** | 6 来源含 Temporal；4 类型含 Confounding/Automation/Selection 等。 |
| 4 | **B** | Synergistic 4 原则包含保留 override。 |
| 5 | **B** | Data altruism 主要引发自主权与同意问题。 |
| 6 | **B** | Confounding bias 的定义。 |
| 7 | **D** | 5 方法 = Fairness metrics / Auditing / Preprocessing / Adversarial / Multistakeholder。 |
| 8 | **B** | WHO 的伦理指南被点名。 |
| 9 | **B** | 两层医疗 = 富人 AI 精准 vs. 穷人传统。 |
| 10 | **B** | 微小扰动让 AI 误判良恶性肿瘤。 |
