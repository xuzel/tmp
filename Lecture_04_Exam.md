# Lecture 4 · Privacy and Data Protection — 考试冲刺包

> ⚠️ **本讲为考试重点**——PETs 六件套、法规三巨头、GDPR 两大权利全是高频考点。

---

## ① ⚡ 30 秒速记卡（Core Terms）

- **Data privacy** = 个体对其个人信息被收集/使用/分享的 **控制权**
- **Data protection** = 针对个人数据的 **法律、技术、组织层面的保障措施**
- **Privacy ≠ Protection**：Privacy 是权利，Protection 是手段
- **Data minimization principle** = 只收集与处理必要的个人数据
- **Informed consent** = 确保个体同意数据被 AI 收集与处理
- **Purpose limitation** = 数据只能用于取得同意的预定目的
- **Re-identification** = 用关联多数据源把匿名数据重新识别
- **Differential Privacy (DP)** = 加受控噪声，保持统计效用
- **Local Differential Privacy (LDP)** = 在客户端加噪声（更强但代价大）
- **Federated Learning (FL)** = 分散数据源训练，不直接访问个人信息
- **Homomorphic Encryption (HE)** = 在加密数据上直接计算
- **Secure Multi-Party Computation (SMC)** = 多方联合计算不泄露个体输入
- **Privacy-Preserving Record Linkage (PPRL)** = 跨数据集匹配记录不暴露身份
- **Data Masking / Tokenization** = 用非敏感等价物替换敏感数据
- **Zero-knowledge proofs** = 验证陈述不揭示数据
- **Trusted Execution Environment (TEE)** = 隔离执行环境
- **Privacy by Design** = 隐私从第一行代码开始的理念
- **Privacy Impact Assessment (PIA)** = 定期隐私影响评估
- **GDPR** = EU General Data Protection Regulation
- **PIPL** = China Personal Information Protection Law
- **HIPAA** = US Health Insurance Portability and Accountability Act
- **Right to be forgotten** = 被遗忘权（GDPR）
- **Right to Explanation** = 解释权（GDPR，推动 XAI 发展）
- **Privacy-utility tradeoff** = 数据保护 vs. 模型准确率/效率的平衡
- **PHI** = Protected Health Information（HIPAA 范畴）
- **PII** = Personally Identifiable Information

---

## ② 🔢 编号清单全收录

### 🔸 4 大核心概念
1. Data privacy · 2. Data protection · 3. Data minimization principle · 4. Informed consent

### 🔸 4 大数据收集与同意伦理原则（必背）
1. **Data minimization**（最小化）
2. **Informed consent**（知情同意）
3. **Purpose limitation**（目的限制）
4. **Transparency**（透明度）

记忆："**最小-同意-限制-透明**"

### 🔸 4 大数据泄露/滥用风险
1. 未授权访问 → 身份盗用/金融欺诈
2. 大规模监控 → 个人信息滥用
3. **Re-identification 匿名再识别**
4. 精密网络攻击与数据盗窃

### 🔸 6 种核心 PETs（必背！口诀：**DFHSPM**）
1. **Differential Privacy**（差分隐私）
2. **Federated Learning**（联邦学习）
3. **Homomorphic Encryption**（同态加密）
4. **Secure Multi-Party Computation**（安全多方计算）
5. **Privacy-Preserving Record Linkage**（隐私保护记录链接）
6. **Data Masking / Tokenization**（数据脱敏与令牌化）

### 🔸 5 大伦理与社会影响
1. 保护个体自主性与选择自由
2. 防止"数字档案"被用于操纵/控制
3. 技术进步与隐私权利的平衡
4. 通过公众信任培育创新
5. 防止非授权访问导致的权力滥用

### 🔸 5 大法律与经济动机
1. 避免合规罚款（GDPR 最高 **4% 全球年收入**；PIPL 最高 **5% 年收入**）
2. 维持竞争优势
3. 降低责任风险
4. 增强品牌声誉
5. 促进国际数据传输

### 🔸 7 大技术保障措施
1. Robust access control
2. Strong encryption（at rest + in transit）
3. **Trusted execution environments**（TEE）
4. Comprehensive audit trails
5. Privacy-preserving machine learning
6. Secure multiparty computation protocols
7. Data anonymization techniques

### 🔸 7 大组织最佳实践
1. Regular **Privacy Impact Assessments（PIAs）**
2. **Privacy by Design**（核心理念！）
3. Comprehensive privacy training
4. Data retention and deletion policies
5. Detailed data inventories and data flow maps
6. Robust incident response plan
7. Responsible data sharing practices

### 🔸 3 大伦理责任（数据质量与安全）
1. Data accuracy and quality
2. Data security and protection
3. Ethical data retention policies（含 Right to be forgotten）

### 🔸 4 大伦理框架应用于 AI 数据（与 Topic 2 联动）
1. **Consequentialist**（Utilitarianism + Social Contract Theory）
2. **Deontological + Rights-based**
3. **Virtue Ethics + Care Ethics**

### 🔸 3 大隐私法规（必背）
| 法规 | 全称 | 地区 | 特点 |
|---|---|---|---|
| **GDPR** | General Data Protection Regulation | **EU**（2018 生效） | 权利导向，最高罚 4% 年收入 |
| **PIPL** | Personal Information Protection Law | **China**（2021 生效） | 国家主权 + 数据本地化，最高罚 5% 年收入 |
| **HIPAA** | Health Insurance Portability and Accountability Act | **USA**（医疗专项） | 规范 **PHI 受保护健康信息** |

### 🔸 7 大隐私-效用冲突根源
1. 数据最小化 ↔ 大数据需求
2. 匿名化降效用
3. 加密增加开销（computational overhead）
4. 透明度 ↔ 专有保护
5. DP 的隐私预算（privacy budget）最优化
6. 跨境数据传输 + 各国法规冲突
7. 动态威胁演进 → 需持续重评估

### 🔸 高级 PETs（第二层深度）
**数学/密码学**：Local DP · SMC · Zero-Knowledge Proofs
**系统/架构**：TEE · Blockchain · Privacy-Preserving FL · Advanced Anonymization

### 🔸 自适应隐私-效用框架（7 项）
1. Context-aware privacy protection
2. Privacy budget allocation strategies
3. Hybrid approaches
4. Privacy-utility frontiers
5. User-centric privacy controls
6. Dynamic privacy protection mechanisms
7. Privacy-preserving transfer learning

### 🔸 主教材 5 大隐私案例（Stahl et al. 2023）
1. **Genetic privacy**（Ch.3, Case 2）
2. **Biometric surveillance**（Ch.3, Case 3）
3. **Data appropriation**（Ch.4, Case 1）
4. **Unfair commercial practices**（Ch.4, Case 3）
5. **Smart home hubs security vulnerabilities**（Ch.6, Case 2）

### 🔸 隐私防御"5 层"（Defense in Depth）
1. **Data Layer**：minimization, anonymization, masking
2. **Transmission Layer**：encryption, TLS/SSL
3. **Computation Layer**：DP, HE, SMC, ZKP
4. **Architecture Layer**：FL, TEE, Blockchain
5. **Organizational Layer**：Privacy by Design, PIA, audit

---

## ③ ⚠️ 易混概念对比表

### A. Privacy vs. Protection
| | Privacy | Protection |
|---|---|---|
| 性质 | **权利** | **手段** |
| 主体 | 个体 | 机构 |
| 问法 | "我有什么权？" | "如何实现？" |

### B. 6 种 PETs 机制区分（超高频！）
| 技术 | 核心机制 | 特色 |
|---|---|---|
| **DP** | 数据/查询加受控噪声 | 保持统计效用 |
| **FL** | 分散训练，不集中数据 | 数据不出本地 |
| **HE** | 在加密数据上直接计算 | 不用解密就能算 |
| **SMC** | 多方联合计算不泄露输入 | 协作但互不信 |
| **PPRL** | 跨数据集匹配记录不暴露身份 | 链接但匿名 |
| **Masking** | 用非敏感等价物替换 | 数据可用但不识别 |

### C. GDPR vs. PIPL vs. HIPAA
| | GDPR | PIPL | HIPAA |
|---|---|---|---|
| 地区 | EU | China | USA |
| 生效 | 2018 | 2021 | 1996 |
| 哲学 | 权利导向 | 国家主权/数据本地化 | 行业专项（医疗） |
| 罚款 | 最高 4% 年收入 | 最高 5% 年收入 | 行业专项罚则 |
| 覆盖 | 所有行业 | 所有行业 | **仅医疗（PHI）** |
| 域外效力 | 有 | 有（对中国公民境外） | 较弱 |

### D. DP vs. Local DP
| | DP | Local DP |
|---|---|---|
| 加噪时点 | 服务端处理时 | **客户端上传前** |
| 隐私强度 | 较弱 | **更强** |
| 效用代价 | 较小 | **更大** |
| 典型应用 | 统计发布 | **Apple/Google 键盘统计** |

### E. Anonymization vs. Pseudonymization
- **Anonymization（匿名化）**：完全不可识别 → 不可还原
- **Pseudonymization（假名化）**：用 token 替换 → 理论上可还原（持有映射表的一方）

### F. 4 大数据收集伦理原则 vs. 7 大技术保障
- 伦理原则 = **应该做什么**（What）
- 技术保障 = **如何做到**（How）

---

## ④ 📌 案例 → 概念速查

| 案例 | 涉及议题 | 关键概念 |
|---|---|---|
| **Netflix 2006 匿名数据集** | 再识别风险 | Re-identification + Anonymization 的局限 |
| **Cambridge Analytica** | 数据挪用/操纵 | Purpose limitation 违反 + 数字档案 |
| **Apple 键盘统计** | 本地差分隐私应用 | Local DP 典型 |
| **Google Federated Learning（键盘）** | 联邦学习商业应用 | FL 经典 |
| **Genetic privacy 案例** | 基因数据保护 | 高敏感数据 + 家庭延伸影响 |
| **Biometric surveillance** | 公共安全 vs. 隐私 | Privacy-utility tradeoff 经典 |
| **Smart home hubs** | IoT 安全漏洞 | 架构层安全失败 |
| **Data appropriation** | 数据未经同意被商用 | Purpose limitation + Consent 违反 |
| **Unfair commercial practices** | 数据驱动的歧视性营销 | 数据保护 + 消费者权益 |

---

## ⑤ 🧠 缩写 / 法规 / 年份速查

| 缩写 | 全称 | 关键点 |
|---|---|---|
| **GDPR** | General Data Protection Regulation | **EU**, 2018 生效, **4% 罚款** |
| **PIPL** | Personal Information Protection Law | **China**, 2021 生效, **5% 罚款**, 数据本地化 |
| **HIPAA** | Health Insurance Portability and Accountability Act | **USA 医疗**, 1996, **PHI** |
| **PHI** | Protected Health Information | HIPAA 核心范畴 |
| **PII** | Personally Identifiable Information | 通用个人可识别信息 |
| **DP** | Differential Privacy | Dwork 2006 |
| **LDP** | Local Differential Privacy | 客户端加噪 |
| **FL** | Federated Learning | McMahan et al. 2017 |
| **HE** | Homomorphic Encryption | 加密数据可计算 |
| **SMC / MPC** | Secure Multi-Party Computation | 多方协作 |
| **PPRL** | Privacy-Preserving Record Linkage | 跨库匹配 |
| **ZKP** | Zero-Knowledge Proofs | 证而不露 |
| **TEE** | Trusted Execution Environment | 隔离计算 |
| **PIA** | Privacy Impact Assessment | 定期评估 |
| **DPO** | Data Protection Officer | GDPR 下设 |
| **TLS/SSL** | 传输层加密协议 | 传输层防御 |

### GDPR 两大衍生权利
- **Right to be Forgotten**（被遗忘权）
- **Right to Explanation**（解释权）→ 推动 Explainable AI

### 两大奠基论文
- **Dwork (2006)**：*Differential Privacy* 奠基
- **McMahan et al. (2017)**：*Communication-Efficient Learning of Deep Networks from Decentralized Data*（FL 奠基）
- **Narayanan & Shmatikov (2008)**：Netflix 再识别实证

---

## ⑥ 🕳️ 常见出题陷阱

1. **Privacy ≠ Protection**：前者是权利，后者是手段——题目问定义要分清。
2. **Data minimization 不是"完全不收集"**，而是"只收集**必要的**数据"。
3. **GDPR 最高罚 4% 年收入；PIPL 最高罚 5% 年收入**——别搞反。
4. **HIPAA 仅覆盖医疗（PHI）**，不是通用数据保护法。
5. **DP 加噪声在服务端；LDP 加噪声在客户端**。Apple/Google 用 LDP。
6. **Federated Learning 数据不出本地**，但 **模型更新仍有泄露风险**（需配合 DP）。
7. **Homomorphic Encryption 是"在加密数据上计算"**，不是"加密后的数据解密"。
8. **Anonymization 不能完全防 Re-identification**——这正是本讲强调的陷阱。
9. **Purpose limitation 违反**：用"优化产品"为由收集的数据用于"广告投放"。
10. **Right to Explanation 是 GDPR 的**，不是 HIPAA 或 PIPL 的。
11. **7 条保障 vs. 7 条最佳实践**：前者是技术层面，后者是组织层面，题目问哪层要看清。
12. **"Privacy by Design" 是原则/理念**，不是某种具体技术。
13. **Zero-Knowledge Proofs 是"验证但不揭示"**，不是"加密"——别和 HE 混。
14. **4 条伦理原则不包含 Beneficence**——那是 Topic 1 的 6 原则之一。

---

## ⑦ 🎯 本讲练习题（10 道 MCQ）

**Q1.** Which of the following is NOT one of the four ethical principles of AI data collection and consent?
- A. Data minimization
- B. Informed consent
- C. Purpose limitation
- D. Data maximization

**Q2.** **Federated Learning** primarily addresses privacy by:
- A. Encrypting data mathematically
- B. Training models on distributed data sources without directly accessing personal information
- C. Adding noise to aggregated statistics
- D. Using tokens to replace sensitive fields

**Q3.** The **GDPR** is enforced in which jurisdiction?
- A. United States (healthcare only)
- B. China
- C. European Union
- D. United Kingdom only

**Q4.** Which technique allows computation to be performed **directly on encrypted data**?
- A. Differential privacy
- B. Federated learning
- C. Homomorphic encryption
- D. Data masking

**Q5.** **Re-identification** of anonymized data is a risk primarily because:
- A. Encryption is reversible
- B. AI can link multiple data sources
- C. Consent forms are often unclear
- D. GDPR prohibits anonymization

**Q6.** The **"Right to Explanation"** originates from which regulation?
- A. HIPAA
- B. PIPL
- C. GDPR
- D. PCI-DSS

**Q7.** **HIPAA** primarily regulates:
- A. Social media platforms in the EU
- B. Cross-border data transfer in China
- C. Protected Health Information (PHI) in the US
- D. General consumer data globally

**Q8.** **"Privacy by Design"** is best understood as:
- A. A final-stage legal review
- B. An approach that embeds privacy throughout the AI development lifecycle
- C. A type of encryption
- D. A GDPR penalty formula

**Q9.** Which of the following is the **correct pairing**?
- A. Local DP — server-side noise
- B. Federated Learning — client-side noise before upload
- C. Zero-Knowledge Proof — verifying a claim without revealing data
- D. Homomorphic Encryption — removing sensitive fields

**Q10.** Which of the following is NOT one of the six core PETs discussed?
- A. Differential Privacy
- B. Federated Learning
- C. Blockchain consensus
- D. Privacy-Preserving Record Linkage

---

## 📎 Appendix · 答案与解析

| Q | Ans | 解析 |
|---|---|---|
| 1 | **D** | 四原则是 Minimization/Consent/Purpose Limitation/Transparency，没有"Maximization"。 |
| 2 | **B** | FL 核心 = 分散训练不集中数据。 |
| 3 | **C** | GDPR = European Union 的通用数据保护法。 |
| 4 | **C** | HE = 加密数据上直接计算。 |
| 5 | **B** | AI 关联多数据源是再识别的核心原因。 |
| 6 | **C** | GDPR 的 Right to Explanation 推动 XAI 发展。 |
| 7 | **C** | HIPAA 是美国医疗专项，管 PHI。 |
| 8 | **B** | Privacy by Design = 嵌入全生命周期的理念。 |
| 9 | **C** | ZKP 的定义正确；A/B/D 都是错误配对（LDP 是客户端、FL 不加噪、HE 不是删字段）。 |
| 10 | **C** | 六大 PETs 是 DP/FL/HE/SMC/PPRL/Masking，不含 Blockchain consensus。 |
