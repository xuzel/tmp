# ARIN 5104 · Lecture 9 课堂笔记
# AI in Healthcare（AI 在医疗中的应用伦理）

> 📚 **教授寄语**：同学们，欢迎来到整个课程最 **高赌注（high-stakes）** 的一讲。如果说 Topic 8 讨论的自动驾驶把 AI 伦理变得"物理化"，那么这一讲把它变得 **生命化**。
>
> 医疗是 AI 所有应用场景中 **风险最高、信任要求最严、后果最不可逆** 的领域——这里的 bias 不是"推错广告"，是 **"漏诊癌症"**；这里的 privacy 不是"购物记录泄露"，是 **"HIV 状态被公开"**；这里的 black box 不是"导航走错路"，是 **"错误放化疗方案"**。
>
> 记住这句话：**"In healthcare AI, the question is never 'Is it accurate enough?'—it is always 'Is it accurate enough for whom, at what cost, under whose oversight?'"**（医疗 AI 的问题从来不是"够不够准确"，而是"对谁够准确、代价多大、谁来监督"。）

---

## 📍 本讲 Roadmap（五段式结构）

```
① Introduction（导论：医疗 AI 的双刃剑）
        ↓
② Ethical Implications in Medical Diagnosis and Treatment（诊疗伦理）
        ↓
③ Privacy and Confidentiality in AI-driven Healthcare（隐私与保密）
        ↓
④ Bias and Fairness in AI-assisted Medical Decision-Making（医疗决策偏见）
        ↓
⑤ Ethical Considerations in AI-powered Personalized Medicine（个性化医疗伦理）
```

---

# 第一部分 · Introduction（导论）

## 1.1 Improved Diagnostic Capabilities（AI 在医疗中的增益能力）

四大核心增益：

1. **AI 提升医疗诊断的 accuracy（准确性）与 speed（速度）** → 通过 **pattern recognition（模式识别）** 与 **large dataset analysis（大数据分析）**
2. **机器学习算法辅助 personalized treatment planning（个性化治疗规划）** → 通过分析患者数据、预测治疗结果
3. **AI 驱动系统提升 medical imaging interpretation（医学影像解读）** → 能识别人类放射科医生可能遗漏的 **subtle abnormalities（细微异常）**
4. **Early disease detection（早期疾病检测）在某些场景已 potentially surpasses 人类临床医生**
   - 经典例子：**CT 扫描上的肺癌结节（lung cancer nodules on CT scans）**

> 🎓 **教授点评**：注意"**potentially surpasses**"——用词非常谨慎。这不是说 AI 在所有诊断上都超过医生，而是在 **特定、狭窄、数据充分** 的任务上（如影像识别）可能超过。教材没有说"AI 能取代放射科医生"，这个措辞要精准记忆。

---

## 1.2 Potential Drawbacks and Concerns（AI 医疗的潜在弊端）

四大核心隐忧：

1. **Misdiagnosis risk（误诊风险）** → 来自训练数据的偏见或算法错误 → 导致 **inappropriate or delayed treatment（不当或延误治疗）**
2. **Privacy issues（隐私问题）** → 来自为 AI 系统收集和分析 **大量敏感患者数据**
3. **"Black box" nature（黑箱性质）** → 使 AI 辅助决策的 **explanation（解释）** 变得复杂
4. **Overreliance on AI systems（过度依赖 AI 系统）** → 可能导致医疗专业人员 **deskilling（技能退化）**，降低 **independent judgment abilities（独立判断能力）**

> 🎓 **教授点评**：记住"deskilling"这个词——这是 AI 医疗最隐蔽但最致命的长期风险。**短期内 AI 让 10 个普通医生变成 10 个优秀医生；长期来看 AI 可能让 10 个优秀医生退化成 10 个"看屏幕的人"**。一旦某天 AI 故障，会发生什么？

> 🔑 **助记口诀**：AI 医疗四隐忧 = **M-P-B-O**（Misdiagnosis, Privacy, Black box, Overreliance）

---

# 第二部分 · Ethical Implications in Medical Diagnosis and Treatment

## 2.1 Provider Responsibilities（医疗提供者的五大责任）

1. **Thorough understanding（透彻理解）** AI 系统，包括其 **局限性、潜在偏见、数据质量**
2. **Transparency（透明性）** → 向患者说明 AI 在医疗中的使用，解释决策过程与潜在影响
3. **Regularly update knowledge（定期更新知识）** → 关注最新进展与伦理议题
4. **Report errors, biases, or unexpected outcomes（报告错误、偏见或意外结果）**
5. **Balance（平衡）** AI 技术整合与 **human touch and empathy（人性温度与同理心）**

> 🎓 **教授点评**：第 5 点最容易被工程师忽视——患者不仅需要"对的诊断"，还需要 **"被看见的感受"**。一个冷冰冰的 AI 报告说"你有 87% 概率患癌"，和一个医生握着你的手说"我们一起面对"——前者是数据，后者是医疗。**Healthcare is not just diagnosis; it's care.**

---

## 2.2 Equity and Access（公平与可及性三大原则）

1. **Ensure equitable access（确保公平可及）** → 防止歧视、解决社会经济差距
2. **Consider potential biases（考虑潜在偏见）** → AI 系统可能不利于特定人群（如种族或少数民族）
3. **Evaluate the distribution（评估技术分布）** → 避免创造新的医疗不平等

> 🎓 **教授点评**：AI 医疗有个残酷的规律 —— **"先服务富人"**。一台 AI 辅助的早癌筛查系统通常先进驻三甲医院和私立医院，而农村卫生院、社区诊所可能 10 年也用不上。**如果不刻意干预，AI 会把已有的健康不平等放大 10 倍。** 这也是为什么要"evaluate distribution"。

---

## 2.3 Importance of Clinical Judgment（临床判断的不可替代性）

四大核心作用：

1. **Validate（验证）** AI 生成的建议，尤其在 **high-stakes 医疗决策** 中
2. **Interpret and contextualize（解读与情境化）** → 将 AI 输出放在更广泛的患者情境中（含 AI 未捕捉的因素）
3. **Handle complex or unusual cases（处理复杂或罕见病例）** → 超出 AI 算法典型模式的情况
4. **Detect and correct（检测与纠正）** AI 系统中的潜在偏见或错误，尤其是 **代表性不足的人群或罕见病**

> 🎓 **教授点评**：AI 擅长处理"常见病"，但 **医学真正的挑战是罕见病**——那些一年只能遇到 3 例、教科书只有半页的病。AI 没见过足够多的样本，但一位经验丰富的医生凭直觉就能识别。这就是"clinical judgment"的真正价值。

---

## 2.4 Synergistic Approach（协同方法四原则）

1. **Integrate human judgment with AI capabilities（整合人类判断与 AI 能力）** → 结合优势，提升整体患者护理
2. **Address ethical decision-making nuances（处理伦理决策的细微差别）** → 如 **end-of-life care decisions（临终关怀决策）** 等 AI 无法处理的场景
3. **Explain（解释）** AI 辅助决策给患者 → 回应顾虑、确保 **informed consent（知情同意）**
4. **Maintain ability to override（保留推翻 AI 建议的能力）** → 当临床判断认为必要时

> 🔑 **助记模型**：医疗 AI 的理想范式 = **Human-AI Synergy（人机协同）** = **AI 做广度，医生做深度；AI 处理"常规"，医生处理"例外"；AI 给建议，医生拿决策。**

---

## 2.5 Informed Consent and Decision-Making（知情同意四大挑战）

1. **Adapt informed consent processes（调整知情同意流程）** → 包含 AI 参与诊疗的解释
2. **Respect patients' right to refuse（尊重患者拒绝的权利）** → 为偏好传统方法的患者提供替代选择
3. **Address challenges in patient understanding（处理患者理解复杂 AI 算法的挑战）** → 这影响他们真正知情决策的能力
4. **Consider implications of AI predicting future health outcomes（考虑 AI 预测未来健康结果的影响）** → 可能引发关于信息披露的伦理困境

> 🎓 **教授点评**：第 4 点是新兴伦理难题——如果 AI 预测你 65 岁将患阿尔茨海默症，概率 73%，医生要不要告诉你？告诉你影响你的人生规划与心理健康；不告诉你剥夺你的知情权与准备时间。这叫 **"预测医学的伦理两难"**，Topic 11 会深化讨论。

---

## 2.6 Data Privacy and Personalized Medicine（数据隐私与个性化医疗四议题）

1. **Evaluate questions（评估关键问题）** → 数据所有权、隐私、AI 决策使用的信息范围
2. **Assess potential（评估潜力）** → AI 驱动个性化医疗通过 **tailored treatment options（量身定制治疗）** 增强 **patient autonomy（患者自主权）**
3. **Consider pressure to comply（考虑遵守 AI 建议的压力）** → 平衡个性化与患者选择权
4. **Implement safeguards（实施保障措施）** → 保护 AI 系统中的患者数据（如 **anonymization、secure data storage**）

---

# 第三部分 · Privacy and Confidentiality in AI-driven Healthcare

## 3.1 Data Vulnerabilities and Unintended Disclosures（六大数据风险）

**前三风险**：

1. **Sensitive patient data（敏感患者数据）** → AI 系统需要访问大量此类数据，造成 **数据泄露与未授权访问** 的漏洞
2. **Unintended disclosure（意外泄露）** → 机器学习算法通过 **数据推断与模式识别** 可能导致个人信息意外泄露
3. **New attack vectors（新攻击向量）** → AI 与现有医疗系统整合可能为 **cybercriminals（网络犯罪分子）** 创造新的利用路径

**后三风险**：

4. **Predictive analytics 泄露敏感健康信息** → 未经明确同意或知晓的情况下
5. **Real-time health data 带来新隐私顾虑** → 来自 wearable devices 和 IoT sensors（如健身追踪器、智能手表）持续监控与数据所有权问题
6. **Re-identification（再识别）** → AI 系统聚合分析多样数据源的能力可能重新识别匿名化的患者数据

> 🎓 **教授点评**：Topic 4 我们讲过"**再识别攻击**"——AI 医疗把这个问题放大了 100 倍。想象：**一个人的心率模式（从 Apple Watch）+ 就诊记录（从医院）+ 处方记录（从药店）——三者组合，去匿名化几乎是确定的事。** 这就是为什么现代医疗隐私保护不是单点问题，而是 **生态系统问题**。

> 🔑 **助记口诀**：医疗数据六大风险 = **S-U-N / P-R-R**（Sensitive, Unintended, New attacks / Predictive, Real-time, Re-identification）

---

## 3.2 Cloud-based Solutions and Jurisdictional Challenges（云解决方案三大议题）

1. **Data storage, transmission, processing across different jurisdictions** → 不同司法管辖区的隐私法差异
2. **International data transfer agreements（国际数据传输协议）** → 成为维持隐私合规的关键
3. **Cloud providers must implement robust security measures** → 保护传输中（in transit）与静态（at rest）的患者数据

> 🎓 **教授点评**：一家中国三甲医院用 AWS 美国节点做 AI 训练——合规吗？涉及 PIPL（数据跨境）、HIPAA（美国隐私法）、云服务商合同。**同一个模型，同一份数据，合规成本差 10 倍。** 这就是"跨司法管辖"的现实。

---

## 3.3 Ethical Principles and Accountability（三大伦理原则）

1. **Principle of data minimization（数据最小化原则）** → 医疗 AI 系统只能收集和处理达成预期目的所需的 **最小量** 个人数据
2. **Ethical guidelines（伦理指南）** → 如 **WHO（世界卫生组织）** 提出的指南，强调 **transparency, accountability, fairness**
3. **Algorithmic accountability（算法问责）** → 医疗组织必须能 **explain and justify** AI 系统影响患者护理与隐私的决策

---

## 3.4 Balancing Data Utility and Privacy Protection（数据效用 vs. 隐私保护的四维权衡）

1. **Larger and more diverse datasets** → 更准确、更稳健的 AI 模型 → 但增加隐私风险
2. **Data sharing across institutions（跨机构数据共享）** → 加速 AI 研究与开发 → 但可能损害患者保密（若无适当保障）
3. **Synthetic data（合成数据）or federated learning（联邦学习）** → 在保护隐私的同时支持 AI 开发 → 但可能引入模型性能限制
4. **Open-source AI models（开源 AI 模型）** → 促进透明与协作 → 但可能增加 **adversarial attacks（对抗攻击）** 或敏感信息滥用风险

---

## 3.5 Ethical Considerations and Trade-offs（三大伦理权衡）

1. **Data altruism（数据利他主义）** → 鼓励患者为医学研究的更大利益分享健康数据 → 但引发关于 **个人自主权与同意** 的伦理问题
2. **Strict data access controls and anonymization** → 保护患者隐私 → 但可能拖慢 AI 创新、限制数据驱动医疗的益处
3. **Blockchain technology（区块链技术）** → 安全数据共享带来隐私增强机会 → 但引入 **scalability（可扩展性）与 regulatory compliance（合规）** 新挑战

> 🎓 **教授点评**：注意"**data altruism**"——EU 的 Data Governance Act 已经为此立法。这是新兴概念：**患者可以"捐赠"自己的医疗数据给研究机构**，类似器官捐献。但这又引发新问题：**儿童能捐吗？精神疾病患者能捐吗？死后能代捐吗？**

---

## 3.6 Technical Security Measures（技术安全四大措施）

1. **Robust encryption and access control（强加密与访问控制）** → 保护 AI 系统内静态与传输中的患者数据
2. **Advanced anonymization techniques（高级匿名化技术）** → 如 **differential privacy（差分隐私）**，在保护个体身份的同时保持训练数据集的效用
3. **Regular security audits and vulnerability assessments（定期安全审计与漏洞评估）**
4. **Privacy-enhancing technologies（隐私增强技术）** → 如 **homomorphic encryption（同态加密）** 或 **secure multi-party computation（安全多方计算）**，允许 AI 对加密数据进行分析

> 🔗 **与 Topic 4 联动**：Topic 4 我们学过 6 种 PETs（DP, FL, HE, SMC, PPRL, Data Masking），**医疗领域是这 6 种技术最密集、最必需的应用场景**。

---

## 3.7 Governance and Best Practices（治理最佳实践五大项）

1. **Comprehensive data governance policies（全面数据治理政策）** → 明确定义 AI 驱动医疗中处理患者数据的角色、责任与程序
2. **Transparent data management practices（透明数据管理实践）** → 让患者能方便地访问、更正、控制其个人健康信息
3. **Ethical review boards（伦理审查委员会）** → 专注于医疗 AI，在部署前评估新应用的隐私与安全影响
4. **Education and training programs（教育与培训项目）** → 确保医疗专业人员与 AI 开发者理解并遵循最佳实践
5. **Incident response plan（事件响应计划）** → 快速有效应对数据泄露或隐私违规

---

# 第四部分 · Bias and Fairness in AI-assisted Medical Decision-Making

## 4.1 Sources of Data and Algorithmic Bias（六大医疗 AI 偏见来源）

**第一组：数据相关偏见**

1. **Data bias（数据偏见）** → 训练数据集不代表目标人群 → AI 模型在不同人群中表现不均
2. **Algorithmic bias（算法偏见）** → 来自 AI 模型开发中的设计选择与假设 → 可能编码人类偏见或历史不平等
3. **Sampling bias（抽样偏见）** → 特定患者群体在临床试验或电子健康记录中的过度或不足代表

**第二组：方法相关偏见**

4. **Feature selection bias（特征选择偏见）** → 跨人群差异的相关变量被省略或赋予不足权重
5. **Labeling bias（标签偏见）** → 人类专家不一致或不准确地标注训练数据，可能强化现有医疗偏见
6. **Temporal bias（时间偏见）** → 基于历史数据训练的 AI 模型未反映当前医学知识或变化中的人口统计

> 🎓 **教授点评**："**Temporal bias**"是个常被忽视的维度——**50 年前的医学认为女性心脏病症状与男性相同，今天我们知道完全不同**。如果 AI 基于 50 年数据训练，它会用"男性标准"诊断女性心脏病——漏诊率高达 40%。**历史数据不是中立的。**

> 🔑 **助记口诀**：医疗 AI 六大偏见 = **D-A-S / F-L-T**（Data, Algorithmic, Sampling / Feature, Labeling, Temporal）

---

## 4.2 Specific Bias Types in Medical AI（医疗 AI 四个具体偏见类型）

1. **Selection bias（选择偏见）** → AI 系统在 **非代表性样本** 上训练
2. **Confounding bias（混淆偏见）** → AI 模型错误地将 **相关变量** 归因为 **因果关系**
3. **Measurement bias（测量偏见）** → 来自数据收集中的 **系统性错误或不一致**
4. **Automation bias（自动化偏见）** → 人类 **过度依赖自动化系统**，可能忽略矛盾信息

> 🎓 **教授点评**："**Automation bias**"与前面讲的"overreliance / deskilling"相呼应——这不是技术偏见，而是 **人机协作的心理偏见**。研究表明，当医生看到 AI 建议时，即使 AI 是错的，医生推翻 AI 的概率也会显著下降。**AI 在悄悄地改变人类决策的认知基线。**

---

## 4.3 Bias Detection and Mitigation Methods（偏见检测与缓解五大方法）

1. **Fairness metrics（公平性指标）** → 量化并比较 AI 模型在不同人口群体中的表现（回顾 Topic 3：demographic parity, equal opportunity, equalized odds）
2. **Bias auditing（偏见审计）** → 系统性使用多样数据集测试 AI 系统，识别不同人群子组中的表现或结果差异
3. **Data preprocessing（数据预处理）** → 平衡训练数据集中的代表性，在模型开发前缓解偏见
4. **Adversarial debiasing（对抗去偏）** → 从 AI 模型输入中去除敏感信息，同时保持整体预测性能
5. **Multistakeholder model development（多利益相关方模型开发）** → 整合 **clinicians, patients, ethicists** 的多样团队，在 AI 生命周期中识别与应对偏见来源

> 🔗 **与 Topic 3 联动**：这里 5 种方法 = Topic 3 的"**三阶段缓解框架**"的医疗版本。Preprocessing 对应 pre-model，Adversarial 对应 in-model，Auditing 与 Multistakeholder 对应 post-model + governance。

---

# 第五部分 · Ethical Considerations in AI-powered Personalized Medicine

## 5.1 Tailoring Medical Treatments with AI（个性化医疗的六大能力）

**第一组：技术能力**

1. **AI-powered personalized medicine** 利用 AI 算法分析 **大数据集**（基因数据、病史、生活方式因素），为个体患者量身定制医疗
2. **Patterns and correlations（模式与关联）** → 机器学习模型识别人类临床医生不易察觉的模式，带来更准确的诊断与治疗
3. **Continuous update（持续更新）** → AI 系统根据新数据与结果不断优化建议，提高治疗效果

**第二组：临床价值**

4. **Reduces adverse drug reactions（减少药物不良反应）** → 基于基因特征和其他因素预测个体对特定药物的反应
5. **Optimizes resource allocation（优化资源分配）** → 识别最可能从特定干预或预防措施中获益的患者
6. **Earlier disease detection（更早的疾病检测）** → 通过分析患者数据的细微模式，提升治疗结果并降低医疗成本

> 🎓 **教授点评**：个性化医疗的愿景很美——**"同样的病，不同的药；同样的药，不同的剂量"**。但实现这个愿景需要 **海量基因数据 + 算力 + 临床验证 + 监管批准**——每一步都是伦理战场。

---

## 5.2 Data Privacy and Security Concerns（个性化医疗的五大隐私风险）

1. **Sensitive patient information（敏感患者信息）** → 个性化医疗需要大量此类信息，引发隐私与安全顾虑
2. **Data breaches or unauthorized access（数据泄露或未授权访问）** → 个人健康信息
3. **Anonymization challenges（匿名化挑战）** → 在匿名化的同时保持 AI 算法的效用
4. **Genetic data storage and sharing（基因数据存储与共享）** → 跨机构与国界的伦理考量
5. **Robust data governance frameworks（强数据治理框架）** → 成为刚需

> 🎓 **教授点评**：**基因数据是最特殊的隐私数据**——它不仅属于你，还属于你的父母、子女、兄弟姐妹。**你同意分享你的基因组数据，等于未经同意地分享了家族成员的部分遗传信息。** 这是传统"个人同意"框架无法覆盖的新问题。

---

## 5.3 Algorithmic Bias and Fairness（个性化医疗的五大公平性挑战）

1. **Algorithmic bias** 带来不公平或歧视性治疗建议
2. **"Black box" nature** 使医疗提供者与患者难以理解、信任治疗建议的理由
3. **Diverse and representative training data（多样化与代表性训练数据）** 的确保挑战
4. **Ethical considerations in defining and measuring fairness（定义与衡量公平性的伦理考量）**
5. **Ongoing monitoring and auditing（持续监控与审计）** → 检测并应对偏见

---

## 5.4 Clinical Judgment and Responsibility（临床判断与责任五大问题）

1. **Reliance on AI may reduce human clinician judgment and expertise（依赖 AI 可能降低人类临床医生的判断力与专业性）**
2. **Ethical concerns over ownership and control（所有权与控制的伦理顾虑）** → AI 生成的洞察与治疗建议归谁所有？
3. **Responsibility and liability（责任与法律责任）** → AI 建议导致的错误或不良结果谁来承担？
4. **Clear guidelines needed（需要明确指南）** → AI 在临床决策中的角色与其权限的边界
5. **Human oversight（人类监督）** 至关重要

> 🔗 **与 Topic 6 联动**：这里的"责任追究"问题就是 Topic 6 讨论的"**Many Hands Problem**"在医疗领域的具体化。AI 建议错误导致患者死亡，责任是：医生、医院、AI 开发商、数据供应商、监管机构——谁？

---

## 5.5 Economic and Infrastructure Barriers（经济与基础设施五大壁垒）

1. **High implementation costs（高实施成本）** → AI 驱动个性化医疗系统可能仅限于资金充足的机构 → 创造 **two-tiered healthcare system（两层医疗体系）**
2. **Disparities in digital infrastructure and technological literacy（数字基础设施与技术素养差距）** → 不同人群访问 AI 驱动个性化医疗服务的壁垒
3. **Scaling to resource-limited settings（扩展到资源有限环境）** → 农村地区的挑战
4. **Innovative funding models and public-private partnerships（创新资金模式与公私合作）** → 促进公平可及
5. **Low-cost, scalable AI solutions（低成本、可扩展 AI 方案）** → 对广泛采纳至关重要

> 🎓 **教授点评**："**Two-tiered healthcare**" = "双轨制医疗" = 富人享受 AI 精准医疗，穷人享受传统经验医疗。**这不是科幻——这是正在发生的现实。** 一个癌症治疗的 CAR-T 疗法 AI 定制方案要价 50 万美元/疗程。

---

## 5.6 Socioeconomic Factors and Health Disparities（社会经济因素与健康差距五议题）

1. **Integration challenges（整合挑战）** → AI 个性化医疗整合到现有医疗系统需要临床工作流程与培训的重大变革，对资源有限环境构成挑战
2. **Equitable access requires addressing broader socioeconomic factors（公平可及需要应对更广泛的社会经济因素）** → 影响医疗可及与结果
3. **Exacerbate existing health disparities（加剧现有健康差距）** → 若不谨慎设计与实施
4. **Policies that promote equal access（促进平等可及的政策）**
5. **Community engagement and education（社区参与与教育）** → 促进接受与利用

---

## 5.7 Communication and Trust in AI-Assisted Healthcare（沟通与信任五大议题）

1. **Communication challenges（沟通挑战）** → 以可理解、可执行的方式向患者传达 AI 建议 → 影响患者信任与治疗依从性
2. **New approaches to medical education（医学教育新方法）** → 确保医疗提供者能有效解读与利用 AI 洞察
3. **Maintain transparency（保持透明）** → AI 在医疗决策中的使用
4. **Manage patient expectations and trust（管理患者期望与信任）**
5. **Address patient concerns and skepticism（应对患者顾虑与怀疑）**

> 🎓 **教授点评**：最后一点很重要——**患者对医疗 AI 的态度光谱极广**，从"完全拒绝用任何 AI"到"只相信 AI 不相信医生"。医疗 AI 不仅要技术过硬，还要 **建立信任的文化** ——这是比算法更难解决的工程。

---

# 第六部分 · Case Studies（案例研究）

## 6.1 参考案例（Stahl et al. 2023 教材）

1. **Chapter 4, Case 2**: **Monetization of health data（健康数据的货币化）**
   - 核心议题：医疗数据可以被卖吗？谁拥有？谁从中获利？患者能从自己数据的商业化中分成吗？
2. **Chapter 6, Case 3**: **Adversarial attacks in medical diagnosis（医疗诊断中的对抗攻击）**
   - 核心议题：攻击者通过微小的像素扰动可以让 AI 将"良性肿瘤"识别为"恶性"（反之亦然）——这对患者和保险行业意味着什么？

> 🎓 **教授点评**：对抗攻击在医疗场景是 **隐秘的恐怖**。想象一个黑客在云端模型上植入攻击——某个医院的所有 CT 筛查结果被微调，医生看到的是"没事"的报告，而病人的肿瘤在悄悄扩大。**这种攻击几乎无法被患者察觉，却可能致命。**

---

# 🧠 知识迁移：医疗 AI 分析模板

遇到任何"AI + 医疗"的伦理问题，用以下 **5 维模型** 逐一评估：

```
┌──────────────────────────────────────────────────┐
│         医疗 AI 伦理五维分析法                    │
├──────────────────────────────────────────────────┤
│                                                  │
│   ① Diagnosis Quality（诊断质量）                 │
│      → 准确性、覆盖人群、罕见病处理               │
│                                                  │
│   ② Privacy & Security（隐私与安全）              │
│      → 数据最小化、再识别风险、跨境传输           │
│                                                  │
│   ③ Bias & Fairness（偏见与公平）                 │
│      → 六大偏见来源、四种偏见类型、五种缓解       │
│                                                  │
│   ④ Clinical Responsibility（临床责任）           │
│      → 人机协同、knockout 权、deskilling 风险     │
│                                                  │
│   ⑤ Equity & Access（公平与可及）                 │
│      → 两层医疗、数字鸿沟、跨国差距               │
│                                                  │
└──────────────────────────────────────────────────┘
```

---

# 🎯 课后思考题（6 题）

1. **个性化医疗的悖论**：AI 需要海量个人数据才能实现"为你量身定制"，但数据越多隐私风险越大。如果你是某三甲医院的伦理委员会主席，如何设计一套"最少数据、最多效用"的个性化医疗框架？（结合 Topic 4 的 PETs）

2. **deskilling 的长期风险**：如果未来 10 年所有放射科医生都依赖 AI 读片，他们独立读片的能力必然退化。一旦某天全球 AI 系统因网络攻击或基础设施故障宕机 72 小时，医疗会发生什么？我们今天要做什么准备？

3. **基因数据的家庭伦理**：23andMe 告诉小李他有某癌症基因高风险。小李的父母、妹妹在基因上都与他高度相关——但他们从未同意测试。小李是否有义务告诉他们？他是否有权利不告诉？基因测试公司的责任是什么？

4. **两层医疗的道德**：一家医院同时运营"AI 精准医疗 VIP 部"（基因定制、24 小时 AI 监护）和"普通门诊"。定价差 20 倍。从功利主义、义务论、德性伦理三个角度，这是道德的吗？（回顾 Topic 2 三大框架）

5. **医疗 AI 的"知情同意"升级**：传统知情同意书只需患者签字同意"做 CT 检查"。AI 时代，患者需要同意什么？同意 AI 诊断？同意数据用于训练？同意数据跨境？同意算法更新后无需重新同意？设计一份"AI 时代的知情同意书"。

6. **Liar's Dividend 的医疗版**：某医疗 AI 公司被曝数据泄露。CEO 回应："可能是对抗攻击伪造的证据。"（回顾 Topic 7 的 Liar's Dividend）——患者应该如何验证？监管机构应该如何应对？

---

# 📚 推荐阅读

- **Stahl et al. (2023)**: Chapter 4, Case 2（Monetization of health data）; Chapter 6, Case 3（Adversarial attacks in medical diagnosis）
- **WHO (2021)**: *Ethics and Governance of Artificial Intelligence for Health*
- **FDA (2021)**: *Artificial Intelligence/Machine Learning-Based Software as a Medical Device (SaMD) Action Plan*
- **Topol, E. (2019)**: *Deep Medicine: How Artificial Intelligence Can Make Healthcare Human Again*
- **Obermeyer et al. (2019)**: "Dissecting racial bias in an algorithm used to manage the health of populations." *Science*

---

# 🔚 教授结语

> 同学们，医疗 AI 是 AI 应用中 **最令人激动、也最令人恐惧** 的领域。
>
> - 激动：因为它能 **救命**——早期癌症检测多救 1% 的人，就意味着每年数十万人不死。
> - 恐惧：因为它能 **害命**——一个有偏见的算法漏诊 1% 的人，就意味着每年数十万人本可活下来却死了。
>
> 三句话的课堂总结：
>
> 1. **Healthcare AI is NOT about replacing doctors. It's about augmenting them.**（医疗 AI 不是取代医生，是增强医生。）
> 2. **The biggest risk in healthcare AI is NOT the algorithm—it's the blind trust in the algorithm.**（最大风险不是算法，是对算法的盲信。）
> 3. **Every healthcare AI decision has a patient on the other end. Never forget that.**（每个医疗 AI 决策的另一端都是一个患者。永远记住这一点。）
>
> 下一讲 Topic 10 我们将从"行业应用"回到"宏观治理"——讨论 **AI Governance and Regulation（AI 治理与监管）**：谁来监管 AI？如何监管？监管能跟上技术发展的速度吗？下课前我希望你们带着一个问题离开教室——**"If your family member's life depended on an AI diagnosis tomorrow, what would you need to know before you trusted it?"**（如果明天你的家人生命取决于一个 AI 诊断，你在信任它之前需要知道什么？）
