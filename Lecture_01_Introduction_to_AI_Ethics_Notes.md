# ARIN 5104 · Lecture 1 课堂笔记
# Introduction to AI Ethics（AI 伦理导论）

> 📚 **教授寄语**：这一讲是整门课的"开篇地图"。我们要回答三个根本问题——**AI 伦理是什么？为什么要谈？它从哪里来、要到哪里去？** 请把本笔记视为未来三个月的"导航坐标系"，每当你在后续主题中迷路时，回到这里找方向。

---

## 📍 本讲 Roadmap（四段式结构）

```
① Introduction（导论：什么是 AI 伦理）
        ↓
② Ethical Considerations in AI Development and Deployment（开发与部署中的伦理考量）
        ↓
③ Historical Context and Evolution of AI Ethics（历史脉络与演化）
        ↓
④ Case Studies（案例研究：招聘 AI & 预测性警务）
```

---

# 第一部分 · Introduction（导论）

## 1.1 什么是 AI Ethics（AI 伦理）？

AI 伦理 = 一门研究 **AI 系统在开发与部署中所引发的道德（moral）与伦理（ethical）影响** 的交叉学科。

### 核心关注议题（五大关键词）

| 议题 | 英文 | 含义 |
|------|------|------|
| 公平性 | **Fairness** | 避免歧视性结果 |
| 隐私 | **Privacy** | 保护个人数据与人格尊严 |
| 透明度 | **Transparency** | 决策过程可被理解 |
| 问责 | **Accountability** | 可追究、可承担责任 |
| 安全 | **Safety** | 系统不造成物理/心理伤害 |

### 核心目标

> 📌 **推动 AI 在各应用领域被"负责任（responsible）且有益（beneficial）"地使用，同时 minimizing potential harms（最大程度减少潜在伤害）。**

### 涉及的利益相关者（Stakeholders）

- **Computer scientists**（计算机科学家）
- **Ethicists**（伦理学家）
- **Policymakers**（政策制定者）
- **Users**（目标应用的终端用户）

> 🎓 **教授点评**：AI 伦理不是单一学科能解决的问题——它必然是 **跨学科（interdisciplinary）** 的，技术人不能把它丢给哲学家，哲学家也不能把它丢给工程师。

---

## 1.2 AI 的社会影响（Societal Impacts of AI）

AI 是一把"双刃剑"——既有正面赋能，也有负面冲击。

### ✅ 正面影响（Positive Impacts）

- **转型产业与商业模式**（Transforming industries and business models）
- **增强决策与问题解决能力**（Enhancing decision-making and problem-solving）
- **提升可及性与包容性**（Improving accessibility and inclusion）
- **应对全球性挑战**（Addressing global challenges，如气候、疾病）

### ⚠️ 负面影响（Negative Impacts）

- 引发 **隐私、安全、自主性**（privacy, security, autonomy）顾虑
- 加剧 **社会经济不平等**（exacerbating socioeconomic inequalities）
- 重塑 **工作与教育的未来**（shaping the future of work and education）——有机遇，也有冲击

> 🎓 **教授点评**：记住——每一项 AI 的"好处"，几乎都对应着一个伦理风险。二者不是对立，而是 **一枚硬币的两面**。

---

## 1.3 现实世界中的 AI 两难（Real-World AI Dilemmas）

七个典型场景（务必牢记，它们会反复出现在 essay 与 exam 中）：

1. **招聘与贷款中的算法偏见**（Algorithmic bias in hiring and lending）
2. **人脸识别**（Facial recognition）技术引发的隐私担忧
3. **自动驾驶汽车**（Autonomous vehicles）的道德抉择
4. **医疗 AI**（AI in healthcare）与患者隐私
5. **深度伪造**（Deepfakes）与虚假信息传播
6. **刑事司法中的算法决策**（Algorithmic decision-making in criminal justice）
7. **AI 自动化导致的岗位流失**（Job displacement due to AI automation）

> 🎓 **教授点评**：这 7 个场景不是孤立事件，而是 **整门课程后续 10 讲的"议题锚点"**。每学完一讲，请回到这张清单，把对应的理论工具对号入座。

---

# 第二部分 · AI 开发与部署中的伦理考量

## 2.1 六大核心伦理原则（Main Ethical Principles）

| # | 原则 | 英文 | 核心含义 |
|---|------|------|---------|
| 1 | 公平与非歧视 | **Fairness and non-discrimination** | 不让模型复制/放大社会偏见 |
| 2 | 隐私与数据保护 | **Privacy and data protection** | 保障个人信息安全 |
| 3 | 透明度与可解释性 | **Transparency and explainability** | 决策过程可审视、可理解 |
| 4 | 问责与责任 | **Accountability and responsibility** | 出了问题有人负责 |
| 5 | 安全与稳健 | **Safety and robustness** | 面对异常/攻击仍可靠 |
| 6 | 有益与不伤害 | **Beneficence and non-maleficence** | 既要做好事，也要不作恶 |

> 📌 **记忆法（F-P-T-A-S-B）**：Fairness → Privacy → Transparency → Accountability → Safety → Beneficence。这是整门课的"六芒星"，每一讲都在围绕其中某一角深挖。

---

## 2.2 三大伦理学理论框架（Main Ethical Frameworks）

| 框架         | 英文                   | 核心主张              | 应用于 AI          |
| ---------- | -------------------- | ----------------- | --------------- |
| **功利主义伦理** | Utilitarian ethics   | **最大化整体福祉、最小化伤害** | 看结果：算法带来的总效用    |
| **义务论伦理**  | Deontological ethics | **遵守道德规则与义务**     | 看规则：是否违反基本权利    |
| **德性伦理**   | Virtue ethics        | **培养道德品格与美德**     | 看品格：开发者/使用者是否有德 |

> 🎓 **教授点评**：这是 **下一讲（Topic 2: Philosophical Foundations）** 的预告。记住：**没有单一的"正确伦理观"**，真实世界的 AI 决策往往需要三种视角的综合判断。

---
## 2.3 AI 系统的伦理影响（Ethical Implications）

负面影响六大类：

1. **偏见与歧视** → 延续既有的 **societal biases（社会偏见）**
2. **隐私与监控** → 侵犯 **personal privacy（个人隐私）**
3. **岗位流失与经济不平等** → 加剧 **disparities（差距）**
4. **关键领域的自主决策与问责问题**（Autonomous decision-making & accountability in critical domains）
5. **操纵与虚假信息**（Manipulation and misinformation）通过 AI 生成内容扩散
6. **对 AI 的依赖**导致 **human skills（人类技能）流失**

---

## 2.4 长期考量（Long-Term Considerations）

- **存在性风险**（Existential risks）：高级 AI 系统可能带来的长期威胁
- **AI 研究与开发中的伦理考量**（Ethical considerations in R&D）
- **伦理框架的持续演化**（Evolving ethical frameworks）以应对新兴 AI 技术

> 🎓 **教授点评**：不要只想短期 bug，还要想 **10 年、20 年、50 年后的 AI 将是什么？** 现在的决策会在那时形成怎样的路径依赖？这是 Topic 11（Future of AI Ethics）的核心议题。

---

## 2.5 伦理 AI 实践的利益相关者（Stakeholders）

三大阵营、六类角色：

### 🔧 开发与实施（Development and implementation）
- **开发者与研究者**（Developers and researchers）
- **公司与组织**（Companies and organizations）

### 🏛️ 治理与监督（Governance and oversight）
- **政府与政策制定者**（Governments and policymakers）
- **伦理委员会与咨询委员会**（Ethics boards and advisory committees）

### 👥 公众参与与教育（Public engagement and education）
- **终端用户与消费者**（End-users and consumers）
- **公民社会组织与倡导团体**（Civil society organizations and advocacy groups）
- **教育机构**（Educational institutions）

> 🎓 **教授点评**：伦理 AI 不是任何单一角色的责任。**工程师必须理解自己身处的生态位**——你不是伦理的唯一守门人，但你绝对是守门链条中不可缺位的一环。

---

# 第三部分 · AI 伦理的历史脉络与演化

## 3.1 从古代神话到 AI 早期（Ancient Myths → Early Years of AI）

| 时期 | 关键事件 | 伦理议题的出现 |
|------|---------|--------------|
| 古代 | 早期 AI 概念源于 **ancient myths and legends**（神话与传说） | 人造智能体的想象由来已久 |
| **1956** | **Dartmouth Summer Research Project**（达特茅斯夏季研究项目）正式命名 "Artificial Intelligence" | AI 作为学科诞生 |
| 早期研究 | 聚焦 **symbolic reasoning**（符号推理） | 引发关于 **机器决策** 与 **人类自主性（human autonomy）** 的初步担忧 |
| **1970s–1980s** | **AI winter**（AI 寒冬） | 伦理讨论暂时放缓 |

---

## 3.2 AI 复兴带来的伦理挑战（Ethical Challenges from AI Resurgence）

| 时期 | 驱动技术 | 新伦理议题 |
|------|---------|---------|
| **1990s–2000s** | **机器学习**（Machine Learning）推动 AI 复兴 | 关于 AI 系统的伦理争论重新点燃 |
| **2010s** | **深度学习 + 大数据分析**的进步 | 引出 **privacy（隐私）、bias（偏见）** 新挑战；并引发对 **superhuman capabilities（超人能力）** 的担忧 |

---

## 3.3 当代 AI 伦理讨论（Contemporary Discussions）

- 当代讨论覆盖议题广泛
- 新增议题：**Transparency（透明度）** 与 **Accountability（问责）**
- 引发关于 **AGI（通用人工智能）与 ASI（超级人工智能）** 长期影响的讨论

---

## 3.4 新兴伦理挑战（Emerging Ethical Challenges）

四大新兴议题：

1. **生成式 AI（GenAI）** → 虚假信息、深度伪造、人类行为操纵
2. **自主系统（Autonomous systems）** → 自动驾驶、军事应用的伦理争论
3. **社会影响（Societal impact）** → 岗位流失、经济不平等加剧
4. **长期考量** → 与 **AGI** 相关的长期风险

---

## 3.5 塑造当代 AI 伦理的近期事件（Recent Events Shaping AI Ethics）

| 事件 | 启示 |
|------|------|
| **2008 金融危机** | 算法系统的系统性风险 |
| **高调数据泄露与隐私丑闻** | 数据保护刻不容缓 |
| **2016 美国大选 + 社交媒体操纵调查** | AI/算法对民主的冲击 |
| **近期 AI 生成内容的突破** | 信息真实性危机 |

> 📎 延伸阅读：https://www.rand.org/pubs/perspectives/PEA2679-1.html

> 🎓 **教授点评**：AI 伦理不是"纯理论"，而是被 **真实世界的重大事件不断倒逼演化** 的实践学科。理解"为什么现在要谈"——就必须理解这些事件。

---

# 第四部分 · 案例研究（Case Studies）

## 📁 Case Study 1：AI in Hiring Practices（招聘 AI · TechCorp）

### 背景（Background）
- **TechCorp**：一家领先的软件公司，部署 AI 驱动的招聘工具。
- 工具使用 **机器学习算法** 分析简历，并基于 **qualifications（资质）、experiences（经验）、skills（技能）** 对候选人排序。
- 目标：**减少招聘偏见** + **提升初筛效率**。

### 暴露的问题
- 运行数月后，HR 发现"troubling patterns（令人不安的模式）"：
  - 系统偏向 **某些大学与背景** 的候选人 → 造成申请池缺乏多样性
  - 部分合格候选人因 AI 依赖 **特定关键词** 而被忽略

### 四大关键问题（Key Issues）

| # | 问题 | 解析 |
|---|------|------|
| 1 | **Algorithmic bias（算法偏见）** | AI 延续既有偏见，偏袒特定画像，导致对少数群体的歧视 |
| 2 | **Transparency（透明度）** | 候选人不了解简历如何被评估、用了什么标准 |
| 3 | **Accountability（问责）** | 责任归属模糊——开发者？HR？公司？ |
| 4 | **Impact on diversity（对多样性的影响）** | 损害公司对 D&I（多样性与包容性）的承诺 |

### 讨论问题（Discussion Questions）

1. **Bias and fairness**：AI 招聘工具偏见的潜在来源？TechCorp 如何应对以确保公平？
2. **Transparency**：是否应向候选人披露 AI 标准与算法？披露对双方意味着什么？
3. **Accountability**：若 AI 导致歧视，应由谁负责——开发者、HR、还是公司领导？为什么？
4. **Diversity and inclusion**：如何在 AI 效率与 D&I 承诺之间取得平衡？
5. **Alternative solutions**：有哪些替代方法？
6. **Long-term implications**：长期依赖 AI 招聘对公司文化、员工士气、D&I 的长期影响？

---

## 📁 Case Study 2：AI in Predictive Policing（预测性警务 · CitySafe）

### 背景（Background）
- **CitySafe**：某大都会警察局部署 AI 驱动的预测性警务系统。
- 系统目标：**预测犯罪热点、优化警力配置**。
- 数据源：**历史犯罪数据 + 人口统计信息 + 社交媒体活动**。

### 暴露的问题
- 尽管目标是提升公共安全，社区担忧 **种族画像（racial profiling）** 与 **公民自由（civil liberties）受侵蚀**。
- 报告显示系统 **不成比例地针对少数族裔聚居区** → 加剧警方存在感与社区紧张关系。

### 四大关键问题（Key Issues）

| # | 问题 | 解析 |
|---|------|------|
| 1 | **Algorithmic bias（算法偏见）** | 强化历史犯罪数据中的偏见，对边缘社区造成不成比例的影响，导致种族画像 |
| 2 | **Transparency（透明度）** | 算法运作机制与数据源不清，动摇问责与公民权利 |
| 3 | **Civil liberties（公民自由）** | 特定社区警力增多 → 隐私权与免于不当监控的权利受侵 |
| 4 | **Community trust（社区信任）** | AI 警务可能侵蚀执法与社区间信任 |

### 讨论问题（Discussion Questions）

1. **Bias and fairness**：CitySafe 如何识别并缓解偏见，以公平对待所有社区？
2. **Transparency**：是否应公开算法与数据源？利弊何在？
3. **Accountability**：出现负面结果时，谁应负责——开发者、警方、城市官员？为什么？
4. **Balancing safety and rights**：如何在公共安全与公民自由、社区信任之间取得平衡？
5. **Alternative approaches**：有哪些不依赖 AI、可改善社区关系的替代方案？
6. **Long-term societal impacts**：AI 在警务中的长期社会影响？

> 🎓 **教授点评**：这两个案例看似不同，实则结构相同——**Bias + Transparency + Accountability + 社会代价**。请把这个四元结构内化为你的"案例分析模板"。

---

# 🎯 本讲重点提炼（复习口诀）

## 🔑 核心定义
**AI 伦理 = 研究 AI 开发与部署中的道德影响，平衡 responsible + beneficial vs. harms。**

## 🔑 五大关注议题
**Fairness · Privacy · Transparency · Accountability · Safety**

## 🔑 六大伦理原则（记忆："F-P-T-A-S-B"）
**Fairness → Privacy → Transparency → Accountability → Safety → Beneficence**

## 🔑 三大伦理框架
**Utilitarianism（结果）· Deontology（规则）· Virtue Ethics（品格）**

## 🔑 七大现实两难
**Hiring · Facial Recognition · Autonomous Vehicles · Healthcare · Deepfakes · Criminal Justice · Job Displacement**

## 🔑 历史四阶段
**神话 → 1956 Dartmouth → AI Winter (1970s–80s) → ML 复兴 (1990s–2010s) → GenAI/AGI 时代**

## 🔑 三大利益相关者阵营
**Development · Governance · Public Engagement**

## 🔑 案例分析四元结构
**Bias + Transparency + Accountability + 社会代价（Diversity / Civil Liberties / Community Trust）**

---

# 📝 课后思考题（供 Essay 与 Exam 备战）

1. 结合 **Utilitarian、Deontological、Virtue** 三种伦理框架，分别分析 TechCorp 招聘 AI 案例，三种视角给出的结论是否一致？如不一致，应如何调和？
2. 为什么 **Transparency** 与 **Accountability** 在 2010s 后才成为突出议题？这与机器学习技术的哪些特性有关？
3. 在 CitySafe 预测性警务案例中，如果你是项目技术负责人，你会如何从"模型训练"与"部署监控"两个环节降低偏见？请列出至少 3 条可落地措施。
4. AGI 的伦理问题与当下 ML 模型的伦理问题，**本质相同还是根本不同**？请论证你的观点。
5. 选取七大现实两难中的任一个，追溯它的 **技术根源 + 社会根源 + 制度空白**，并提出初步的治理建议。

---

# 📖 延伸学习建议

- **主教材** Ch.1：Stahl et al. (2023). *Ethics of Artificial Intelligence*. Springer.
- **案例库**：Princeton AI Ethics Case Studies, Santa Clara University Technology Ethics Cases, AIethicist.org Incident Registries
- **持续关注**：近期真实 AI 事件（如大模型幻觉、自动驾驶事故、生成式 AI 版权诉讼）——它们是你 Essay 和 Project 最好的素材。

---

> 📌 **教授结语**：
> 这一讲只是"导言"，但已经埋下了整门课的所有伏笔。请记住——
> **AI 伦理不是让你"变得谨慎"，而是让你"变得清醒"。**
> 清醒地知道你写的每一行代码背后连接着多少人的真实生活，清醒地知道你优化的每一个指标可能在哪里变形为对某些群体的伤害。
>
> 这种清醒，才是本门课给你的最大礼物。
>
> —— 下一讲我们进入 **Topic 2: Philosophical Foundations of AI Ethics**，为大家铺开本讲中只做简介的三大伦理学理论。请提前预习主教材对应章节。
