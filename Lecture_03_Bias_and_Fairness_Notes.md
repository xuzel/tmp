# ARIN 5104 · Lecture 3 课堂笔记
# Bias and Fairness（偏见与公平）

> 📚 **教授寄语**：上一讲我们在哲学的高空谈"什么是公平"，这一讲我们要 **脚踏实地** 地回答——**当你坐在代码编辑器前，面对一个模型，如何让它真的变得公平？** 这是整门课里 **工程工具箱最丰富** 的一讲，也是 AI 伦理从"价值观"走向"可实施技术"的分水岭。
>
> 请记住一句话：**"Fairness is not a property of the algorithm alone—it is a property of the algorithm + data + context + deployment."**（公平不是算法单独的属性，而是算法 + 数据 + 情境 + 部署的联合属性。）

---

## 📍 本讲 Roadmap（四段式结构）

```
① Introduction（基本概念与社会影响）
        ↓
② Types and Sources of Bias in AI Systems（偏见的类型与来源）
        ↓
③ Algorithmic Fairness and Non-discrimination（算法公平与反歧视）
        ↓
④ Techniques for Mitigating Bias in AI Models（偏见缓解技术）
```

---

# 第一部分 · Introduction（导论）

## 1.1 四个核心定义（Key Concepts and Definitions）

| 概念 | 英文 | 定义 |
|------|------|------|
| **AI 偏见** | AI bias | AI 系统中 **系统性错误或不公平**，可能导致 **歧视性结果或决策** |
| **AI 公平** | Fairness in AI | 确保 AI 系统 **公正对待所有个体或群体**，不基于 **受保护属性** 产生歧视 |
| **受保护属性** | Protected attributes | 不应影响 AI 决策的特征，以防止歧视（如 **ethnicity, gender, age, disability status**） |
| **算法公平** | Algorithmic fairness | 开发 AI 系统，使其决策 **不歧视特定群体或个人** |

> 🎓 **教授点评**：注意 **Bias** 与 **Unfairness** 是一对互为因果的概念——**偏见** 是系统内部的系统性倾斜，**不公** 是其对外显现的结果。消除其一，另一才能真正被解决。

---

## 1.2 AI 偏见对不同社区的影响（Impact on Different Communities）

### 总体规律
> AI bias 可以 **延续并加剧（perpetuate and exacerbate）** 既有的 **社会不平等** 与对 **边缘化社区（marginalized communities）** 的歧视。

### 七大领域影响清单

| # | 领域 | 具体危害 |
|---|------|---------|
| 1 | **Hiring & Lending（招聘 & 借贷）** | 限制 **弱势群体** 的经济机会与上升通道 |
| 2 | **Facial Recognition（人脸识别）** | **错误逮捕** 与 **冤案**，不成比例地影响 **有色人种社区** |
| 3 | **Healthcare（医疗）** | 医疗差异、**误诊**、特定人群健康结果更差 |
| 4 | **Education（教育）** | 强化 **学业差距**，限制弱势学生获取资源与机会 |
| 5 | **Content Recommendation（内容推荐）** | 限制多元视角暴露，强化 **回音壁（echo chambers）** 与极端观点 |
| 6 | **Criminal Justice（刑事司法）** | 更严厉的量刑，延续 **已被过度代表群体** 的监禁循环 |

> 🎓 **教授点评**：注意看——这些都是 **涉及"机会分配"或"权利判断"** 的高风险领域。AI 偏见在低风险领域（如音乐推荐）可能只是"不爽"，但在这七大领域，它直接决定一个人的命运。

---

# 第二部分 · Types and Sources of Bias in AI Systems

## 2.1 常见偏见类型（Common Types of Bias）

| 类型 | 英文 | 定义 |
|------|------|------|
| **算法偏见** | Algorithmic bias | AI 系统中的 **系统性错误**，导致不公平结果 |
| **选择偏见** | Selection bias | **训练数据未能代表目标群体** 时出现 |
| **采样偏见** | Sampling bias | 数据中 **某些群体被过度或不足代表** |

> 📌 **关键观点**：三者都会产生错误结果，但 **来源于不同过程**，对数据分析与决策的影响也不同。

> 🎓 **教授点评**：学生常把"偏见"当成一个抽象骂名。其实在技术层面，它是 **三种不同的数据工程问题** —— 算法层、数据代表性层、采样层，每层都有独立的解决方案。

---

## 2.2 AI 偏见的六大来源（Sources of AI Bias）

**务必逐条记忆——这是本讲最常出现在考题中的知识点**。

| # | 来源 | 英文 | 解析 |
|---|------|------|------|
| 1 | **数据收集** | Data collection | 收集方法导致 **训练数据不平衡** |
| 2 | **数据标注** | Data labeling | 标注过程中 **引入人类偏见** |
| 3 | **特征选择** | Feature selection | 强调或忽略某些属性，影响公平性 |
| 4 | **代理变量** | Proxy variables | 与受保护属性 **相关** 的变量，引入 **非预期偏见**（如用邮政编码代理种族） |
| 5 | **开发者偏见** | Developer biases | 系统开发过程中 **编码进去** 的主观偏见 |
| 6 | **反馈循环** | Feedback loops | 部署后的反馈 **随时间放大既有偏见** |

> 🎓 **教授点评**：**Proxy variables（代理变量）** 是最阴险的一种——你以为删掉"种族"字段就安全了？但邮政编码、姓氏、甚至某类购物行为都可能成为种族的强代理。**"Fairness through unawareness"（通过无视实现公平）这条路基本走不通**，我们后面会专门讲。

---

## 2.3 Biased AI 的影响清单（Impact of Biased AI）

七大领域已见过，但值得在这里再复习一遍具体机制：

1. **Hiring（招聘）** → 延续职场不平等
2. **Credit scoring & Loan approval（信用评分与贷款审批）** → 限制金融机会
3. **Facial recognition（人脸识别）** → 错误识别
4. **Criminal justice（刑事司法）** → 自动化决策延续系统性种族主义
5. **Healthcare（医疗）** → 误诊与治疗不足
6. **Content recommendation（内容推荐）** → 回音壁与过滤气泡（**filter bubbles**）
7. **Large Language Models（大语言模型）** → 生成与放大刻板印象

---

## 2.4 真实世界 AI 偏见案例（Real-World AI Bias Examples）

**六个必须记住的"臭名昭著"案例**——它们是 Essay 与 Exam 最好的弹药：

| 案例 | 偏见类型 | 后果 |
|------|---------|------|
| **COMPAS recidivism prediction tool**（再犯预测工具） | 种族偏见 | 黑人被告的 **再犯风险评分** 系统性偏高 |
| **执法用的人脸识别系统** | 种族 / 肤色偏见 | 对 **少数族裔准确率更低** |
| **Amazon 的实验性 AI 招聘工具** | 性别偏见 | 系统性 **歧视女性候选人** |
| **Apple Card 信用额度争议** | 性别偏见 | 同等条件下女性额度更低 |
| **Google Photos 图像识别系统** | 种族偏见 | 曾将 **黑人错误标注为 "gorillas"** |
| **医疗 AI 系统** | 肤色偏见 | 在 **深色肤色上准确率更低** |

> 🎓 **教授点评**：这六个案例的共同点——**没有一个开发团队是故意为之**。但这反而更可怕——它说明 **即使出于善意，AI 系统也会制造歧视**。这就是为什么我们需要系统化的反偏见工程实践。

---

# 第三部分 · Algorithmic Fairness and Non-discrimination

## 3.1 什么是算法公平（What is Algorithmic Fairness）？

**定义**：算法公平 = **在自动化决策系统中消除偏见或歧视**，在不同人口群体间 **促进公平结果**。

**三大目标**：
- 维护 **public trust（公众信任）**
- 实现 **legal compliance（法律合规）**
- 保持 **ethical integrity（伦理完整性）**

---

## 3.2 算法公平的三种核心定义（Different Notions of Algorithmic Fairness）

**务必分辨清楚——这是整讲最核心的知识点之一**。

| 公平观 | 英文 | 定义 | 核心逻辑 |
|-------|------|------|---------|
| **个体公平** | Individual fairness | **相似的个体应得到相似的结果**，无论所属群体 | "相似人相似待" |
| **群体公平** | Group fairness | 算法预测应在 **不同人口群体间保持一致或平衡**（如种族、性别） | "群间结果平衡" |
| **反事实公平** | Counterfactual fairness | 若个体的 **敏感属性**（如种族）被改变、其他因素不变，决策应保持不变 | "改了种族，结果不变" |

> 🎓 **教授点评**：这三种定义 **互相之间可能冲突**——你做到了"个体公平"，不一定做到"群体公平"；做到了"群体公平"，不一定做到"反事实公平"。这就引出下一个重要概念。

---

## 3.3 公平指标（Fairness Metrics）

**三大经典指标**：
- **Demographic parity（人口均等）**：不同群体获得正预测的比率应相同
- **Equal opportunity（机会均等）**：真阳性率应在不同群体间相等
- **Equalized odds（几率均等）**：真阳性率 + 假阳性率都应在不同群体间相等

> 📌 **记忆法**：**DP → EO → EQ**，从最宽松到最严格。

---

## 3.4 算法公平的四大挑战（Challenges of Algorithmic Fairness）

1. **不同公平定义之间的固有权衡**（Inherent trade-offs）
2. **现实场景的复杂性**（Complexity of real-world scenarios）
3. **非预期后果**（Unintended consequences）
4. **需要多学科协作**（Multidisciplinary approach）：
   - Computer scientists（计算机科学家）
   - Ethicists（伦理学家）
   - Legal experts（法律专家）
   - Domain specialists（领域专家）

---

## 3.5 反歧视策略（Strategies for Ensuring Non-discrimination）

### 三大策略

1. **"Fairness through unawareness"（通过无视实现公平）** ⚠️
   - 做法：从数据中删除受保护属性
   - 问题：**由于存在相关特征（代理变量），这种方法通常不够**

2. **算法透明度与可解释性**（Algorithmic transparency and explainability）
   - 对 **识别与处理歧视性模式** 至关重要

3. **主动反歧视措施**（Proactive measures for non-discrimination）
   - Diverse and **representative** training data（多元且代表性的训练数据）
   - Regular bias **audits**（定期偏见审计）
   - 贯穿 AI 生命周期的 bias **mitigation** techniques（偏见缓解技术）

> 🎓 **教授点评**：记住——**删字段 ≠ 消除偏见**。这是伦理公平的"入门陷阱"。真正的反歧视需要系统化的审计与主动干预。

---

## 3.6 模型设计中的权衡（Trade-offs in Model Design）

### 三大核心权衡概念

| 概念 | 英文 | 含义 |
|------|------|------|
| **不可能性定理** | "Impossibility theorem" | 证明 **多种公平准则无法同时被满足** |
| **准确率-公平权衡** | Accuracy-fairness trade-offs | 提升公平指标可能 **降低整体模型准确率** |
| **帕累托最优** | Pareto optimality | 分析与可视化 **多个目标（公平、准确率）之间的权衡** |

### 管理权衡的三大技术

- **Multi-objective optimization**（多目标优化）
- **Constrained optimization**（约束优化）
- **Adversarial debiasing**（对抗性去偏）

> 📌 **每种技术都有独特的 strengths and limitations（优势与局限）**。

---

## 3.7 驾驭权衡（Navigating Trade-offs）

五大原则：

1. **公平指标的选择会影响其他性能指标**
2. **取决于具体情境、利益相关者优先级、AI 应用的伦理考量**
3. **需考虑长期社会影响，而非仅即时性能指标**
4. **确保可持续（sustainable）与伦理（ethical）的 AI 部署**
5. 过程涉及三大实践：
   - **Iterative refinement**（迭代精细化）
   - **Stakeholder engagement**（利益相关者参与）
   - **Ongoing monitoring**（持续监控）

---

# 第四部分 · Techniques for Mitigating Bias in AI Models

## 4.1 偏见缓解的三阶段框架（Unfairness Reduction Approaches）

```
Data Preprocessing（数据预处理）
        ↓
Smart Model Design（智能模型设计）
        ↓
Postprocessing（后处理）
```

这是整个技术体系的 **"三明治结构"**——每一阶段都有对应的工具箱。

---

## 4.2 【阶段 1】数据预处理：Data Resampling and Augmentation

### 重采样（Resampling）
- 用于 **平衡不均衡数据集中的表示**
- **Oversampling（过采样）**：增加 **少数类实例** 的数量
- **Undersampling（欠采样）**：减少 **多数类实例** 的数量

### 数据增强（Data Augmentation）
- **增加训练数据的多样性**
- 为 **代表不足群体** 生成 **合成（synthetic）样本**
- 对现有数据点应用 **变换**（如旋转、平移）

---

## 4.3 【阶段 1】数据预处理：Feature Engineering and Data Cleaning

| 技术 | 作用 |
|------|------|
| **Feature selection（特征选择）** | 识别并移除 **引入偏见的特征** |
| **Feature engineering（特征工程）** | 修改现有特征以 **降低偏见** |
| **Data cleaning（数据清洗）** | 确保 **不同群体间的一致表示** |
| **Normalization（归一化）** | 减少数值特征中的 **非预期偏见** |

---

## 4.4 【阶段 1】数据预处理：Bias Detection and Mitigation Algorithms

| 技术 | 作用 |
|------|------|
| **Bias detection algorithms** | 识别训练数据中的 **潜在偏见来源** |
| **Fairness constraints** | 在数据预处理中 **纳入公平性约束** |
| **Causal inference（因果推断）** | 理解与缓解偏见 |

---

## 4.5 【阶段 2】智能模型设计：Regularization and Ensemble Methods

| 技术 | 作用 |
|------|------|
| **Regularization（正则化）** | 防止 **过拟合到有偏模式** |
| **Ensemble methods（集成方法）** | 组合多个多样化模型 **降低偏见** |
| **Dropout layers（dropout 层）** | 神经网络中 **提升对偏见的鲁棒性** |

---

## 4.6 【阶段 2】智能模型设计：Adversarial Debiasing and Multi-Task Learning

| 技术 | 作用 |
|------|------|
| **Adversarial debiasing（对抗性去偏）** | 在训练中 **显式优化公平性** |
| **Multi-task learning（多任务学习）** | **联合优化性能与公平** |
| **Fair representation learning（公平表示学习）** | 创造 **无偏中间表示** |

---

## 4.7 【阶段 2】智能模型设计：Transfer Learning and Fine-Tuning Strategies

| 技术 | 作用 |
|------|------|
| **Transfer learning（迁移学习）** | 利用预训练模型，**同时为公平性做适配** |
| **Domain adaptation（领域适配）** | 调整数据分布差异 |
| **Continual learning（持续学习）** | **新数据到来时保持公平** |

---

## 4.8 【阶段 3】后处理：Threshold Adjustment and Calibration

| 技术 | 作用 |
|------|------|
| **Threshold adjustment（阈值调整）** | **平衡不同群体间的错误率** |
| **Calibration（校准）** | **让模型置信度对齐真实概率** |
| **Reject option classification（拒绝选项分类）** | **处理可能存在偏见的决策** |

---

## 4.9 【阶段 3】后处理：Reweighting and Equalized Odds

| 技术 | 作用 |
|------|------|
| **Reweighting（重加权）** | 基于群体归属 **调整预测** |
| **Equalized odds postprocessing** | 实现 **不同群体间相似的错误率** |
| **Fairness constraints** | 在决策过程中 **纳入公平性约束** |

---

## 4.10 【阶段 3】后处理：Counterfactual Fairness and Causal Approaches

| 技术 | 作用 |
|------|------|
| **Counterfactual fairness（反事实公平）** | 基于 **因果关系** 调整输出 |
| **Causal inference（因果推断）** | 理解与缓解不公 |
| **Fairness through unawareness（无视实现公平）** | 从决策过程中 **移除受保护属性**（但前面已指出其局限） |

---

## 🗂️ 偏见缓解技术全景速查表

### 三阶段 × 核心技术矩阵

| 阶段 | 数据层面 | 模型层面 | 输出层面 |
|------|---------|---------|---------|
| **Data Preprocessing** | Oversampling, Undersampling, Data Augmentation, Feature Selection, Data Cleaning, Normalization, Bias Detection, Fairness Constraints, Causal Inference | — | — |
| **Smart Model Design** | — | Regularization, Ensemble, Dropout, Adversarial Debiasing, Multi-Task Learning, Fair Representation Learning, Transfer Learning, Domain Adaptation, Continual Learning | — |
| **Postprocessing** | — | — | Threshold Adjustment, Calibration, Reject Option, Reweighting, Equalized Odds, Counterfactual Fairness, Causal Inference, Fairness through Unawareness |

> 🎓 **教授点评**：面对一个偏见问题，请依次问自己三个问题：
> 1. **数据够不够多元？**（Preprocessing）
> 2. **模型架构本身是否公平感知？**（Smart Design）
> 3. **输出分布在不同群体间是否平衡？**（Postprocessing）
> 三层漏斗全走一遍，偏见才能被系统性压制。

---

# 第五部分 · Case Studies（案例研究）

## 📁 来自主教材（Stahl et al. 2023）的三大案例

| # | 主题 | 教材位置 |
|---|------|---------|
| Case 1 | **招聘工具中的性别偏见** | Chapter 2, Case 1 |
| Case 2 | **执法与预测性警务中的歧视性使用 AI** | Chapter 2, Case 2 |
| Case 3 | **基于肤色的歧视** | Chapter 2, Case 3 |

> 🎓 **教授建议**：请在本周内读完主教材 Chapter 2 的三个案例，并练习用以下模板分析它们。

---

## 🧠 Bias & Fairness 标准分析模板

```
【第 1 步：识别偏见类型】
- Algorithmic bias / Selection bias / Sampling bias？

【第 2 步：定位偏见来源（六选其一或多）】
- Data collection / Data labeling / Feature selection
- Proxy variables / Developer biases / Feedback loops

【第 3 步：选择公平观】
- 追求 Individual fairness / Group fairness / Counterfactual fairness？
- 为什么？

【第 4 步：选择公平指标】
- Demographic parity / Equal opportunity / Equalized odds？

【第 5 步：开出缓解方案（三阶段）】
- Preprocessing：数据层面做什么？
- Smart Design：模型层面做什么？
- Postprocessing：输出层面做什么？

【第 6 步：分析权衡】
- 与准确率的冲突？
- 与其他公平指标的冲突？
- 长期社会影响？
```

---

# 🎯 本讲重点提炼（复习口诀）

## 🔑 四大核心定义
**AI bias + Fairness in AI + Protected attributes + Algorithmic fairness**

## 🔑 三大偏见类型
**Algorithmic + Selection + Sampling**

## 🔑 六大偏见来源（记忆："数据-标注-特征-代理-人-反馈"）
**Data collection → Labeling → Feature selection → Proxy variables → Developer biases → Feedback loops**

## 🔑 六大"臭名昭著"案例
**COMPAS · FRT · Amazon recruiting · Apple Card · Google Photos · Healthcare AI**

## 🔑 三大公平观
**Individual · Group · Counterfactual**

## 🔑 三大公平指标
**Demographic parity · Equal opportunity · Equalized odds**

## 🔑 三大不可能性 / 权衡
**Impossibility theorem · Accuracy-fairness trade-off · Pareto optimality**

## 🔑 缓解偏见的三阶段框架
**Preprocessing → Smart Design → Postprocessing**

## 🔑 一个伦理陷阱
**"Fairness through unawareness"（删字段不等于消除偏见，代理变量会出卖你）**

## 🔑 一条黄金原则
**公平是算法 + 数据 + 情境 + 部署的联合属性，永远需要多学科协作。**

---

# 📝 课后思考题（供 Essay 与 Exam 备战）

1. 假设你发现模型对女性贷款申请人的通过率显著低于男性，请依次使用 **三阶段框架**（Preprocessing / Smart Design / Postprocessing）给出 **至少各 2 条** 具体缓解方案。
2. **Impossibility Theorem** 为何重要？它对"完美公平的 AI"的追求意味着什么？请结合 COMPAS 案例说明。
3. 为什么 **"Fairness through unawareness"** 在工程实践中常常失败？请以真实例子说明 **代理变量（proxy variables）** 的危险。
4. **Individual fairness** 与 **Group fairness** 在何种情境下会冲突？作为工程师你如何选择？是否存在调和方案？
5. **Counterfactual fairness** 相较前两者的理论优势是什么？它在实现上又面临哪些挑战（提示：因果图构建）？
6. 以 **Amazon 招聘工具** 为例，追溯其偏见的六大来源中哪些最有可能成立？并据此提出避免该问题的工程修复方案。

---

# 📖 延伸学习建议

- **主教材** Ch.2：Stahl et al. (2023). *Ethics of Artificial Intelligence*. Springer.（三个重点案例）
- **经典论文**：
  - Angwin et al. (2016). *Machine Bias*（ProPublica 关于 COMPAS 的调查报道）
  - Buolamwini & Gebru (2018). *Gender Shades*（人脸识别性别 × 肤色偏见实证）
  - Hardt et al. (2016). *Equality of Opportunity in Supervised Learning*（Equalized Odds 理论原文）
  - Chouldechova (2017). *Fair Prediction with Disparate Impact*（不可能性定理）
- **工具包**：
  - **IBM AI Fairness 360（AIF360）**：开源偏见检测与缓解库
  - **Google What-If Tool**：模型公平性可视化
  - **Microsoft Fairlearn**：偏见评估与缓解

---

> 📌 **教授结语**：
>
> 本讲让你们拥有了一整套 **工具箱**。但请记住——**工具不会替你做伦理判断**。
>
> 当你在项目中选择 Demographic Parity 还是 Equal Opportunity 时，你其实是在替某些群体的未来做一个 **价值抉择**。当你在 Accuracy 与 Fairness 之间划 Pareto 曲线时，你在决定 **哪些错误可以被接受、哪些错误无论如何都要避免**。
>
> **这不是一个数学问题，这是一个政治与伦理问题披着数学的外壳。**
>
> 真正有能力的 AI 工程师，能同时看到 Python 代码和它背后的社会后果。这就是这一讲的终极教学目标。
>
> —— 下一讲我们进入 **Topic 4: Privacy and Data Protection**，从"群体公平"转向"个体权利"，请预习主教材第 3 章。
