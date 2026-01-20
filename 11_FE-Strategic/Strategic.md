<h1 align="center">📈 经营战略与商业模式 (Strategy & Business)</h1>

<p align="center">
  <strong>Strategic Management & Business Models</strong><br>
  <i>経営戦略とビジネスモデル</i>
</p>

---

你好！我是你的基础情报讲师。在 FE 考试的 **“策略 (Strategy / ストラテジ)”** 部分，术语多且易混淆，但只要掌握了背后的商业逻辑和计算模型，这一部分就是你的“拿分区”。本手册将严格基于最新大纲，为你拆解最核心的考点。

---

## 1. ☁️ IT 解决方案业务 (Solution Business)

解决方案业务的核心是解决客户课题。首先我们要区分系统“住”在哪里的三种传统形态与现代云服务。

### 1.1 部署形态：从自建到租赁

> [!CAUTION]
> **考试高频对比**
> 不仅要分清本地和云端，还要区分“托管”的细微差别。

<div align="center">

| 部署形态 | 定义与特征 | 🔑 指挥命令与管理责任 |
| :--- | :--- | :--- |
| **传统本地部署**<br>(On-Premises / オンプレミス) | 企业在自有机房内自行购置硬件、软件并管理。 | **完全自主**：管理负担最重，自由度最高。 |
| **住房服务**<br>(Housing / ハウジング) | 客户将 **自有** 的服务器存放在服务商的数据中心。 | **租位置**：由服务商提供电力和空调，服务器仍是你的。 |
| **托管服务**<br>(Hosting / ホスティング) | 客户直接租赁服务商 **已经准备好** 的服务器。 | **租设备**：服务器和位置都是租的。 |
| **云端**<br>(Cloud / クラウド) | 不保有资源，通过网络按需利用服务。 | **按需付费**：完全无需触碰硬件。 |

</div>

### 1.2 云服务模型：盖房类比法

<div align="center">

| 模型 | 全称 | 🏠 房屋建造类比 | 考试要点 |
| :--- | :--- | :--- | :--- |
| **IaaS** | Infrastructure as a Service | **只租土地** | 提供基础设施（硬件、网络）。你需要自己盖房（装 OS、装软件）。自由度最高，难度也大。 |
| **PaaS** | Platform as a Service | **租土地 + 房屋框架** | 提供开发环境（OS、中间件）。你只需要搬进家具（编写代码）。 |
| **SaaS** | Software as a Service | **拎包入住的精装房** | 软件全套提供，如 Gmail、Zoom。上手最快，但无法定制功能。 |

</div>

### 1.3 核心技术与应用

* **SOA (Service Oriented Architecture / サービス指向アーキテクチャ)**：将功能拆解为像“乐高零件”一样的独立服务，通过组合零件构建系统。**关键词：组件化**。
* **数字鸿沟 (Digital Divide / デジタルデバイド)**：指因 IT 利用能力或环境差异导致的信息格差。
* **BYOD (Bring Your Own Device)**：员工用私人设备办公。
  * ✅ 优点：成本低、效率高。
  * ⚠️ 缺点：**安全风险** (Security Risk)。
* **RPA (Robotic Process Automation)**：软件机器人，处理“重复性、定型化”的录入工作。
* **BI (Business Intelligence)**：利用统计学方法分析大数据，辅助经营者做决策。

---

## 2. 🛒 电子商务与现代商业 (E-Business)

### 2.1 EC 取引形态

* **B2C** (Business to Consumer)：如 Amazon。
* **C2C** (Consumer to Consumer)：如 Mercari、雅虎拍卖。**考试常客！**
* **G2B** (Government to Business)：电子投标、政府采购。
* **B2E** (Business to Employee)：企业面向员工提供的福利。

### 2.2 电子数据交换 (EDI)

**EDI (Electronic Data Interchange)** 的精髓在于 **标准化**。它让不同公司间的订单、发票能通过统一格式直接进行系统互联，彻底告别传真和手动输入。

### 2.3 虚拟货币与区块链

* **区块链 (Blockchain / ブロックチェーン)**：核心是 **“去中心化”** 和 **“分布式账本”**。
* **挖矿 (Mining / マイニング)**：通过参与交易数据的验证与记录（计算过程）来换取报酬。
  * *注意*：它是对验证工作的补偿，而非简单的“寻找金矿”。

### 2.4 网络营销与关键指标

* **SEO**：优化搜索排名。
* **联盟营销 (Affiliate / アフィリエイト)**：**成果报酬型** 广告（有人买才有钱拿）。
* **CGM (Consumer Generated Media)**：口碑网、论坛（内容由消费者产生）。
* **转化率 (Conversion Rate / コンバージョン率)**：
    $$ \text{CVR} = \frac{\text{成果件数（购买人数）}}{\text{访问总人数}} \times 100\% $$

### 2.5 趋势分析

* **全渠道营销 (Omni-Channel / オムニチャネル)**：模糊线上线下界限。
* **O2O (Online to Offline)**：线上领券，线下消费。
* **长尾理论 (Long Tail / ロングテール)**：互联网让“冷门商品”的总销量汇聚成超过“爆款商品”的利润。

---

## 3. 🏭 工程系统与生产管理 (Engineering System)

### 3.1 消除浪费：JIT 与 看板

* **JIT (Just In Time / ジャストインタイム)**：在“需要的时候”，生产“需要量”的“需要产品”。
* **看板方式 (Kanban / かんばん方式)**：JIT 的实现手段。核心是 **后工序领取 (Pull System)**，从而将中间库存降到零。

### 3.2 灵活生产：细胞 vs 流水线

<div align="center">

| 方式 | 描述 | 特点 |
| :--- | :--- | :--- |
| **细胞生产**<br>(Cell Production / セル生産) | 一个工人或小组负责全流程。 | 灵活应对 **多品种少量** 生产，提升员工积极性。 |
| **流水线生产**<br>(Line Production / ライン生産) | 传送带机械化重复。 | 适合 **单品种大批量**。 |

</div>

### 3.3 关键术语

* **MRP (Material Requirements Planning / 資材要件計画)**：根据生产计划精准计算“什么时候需要多少料”。
* **IoT 应用**：
  * **HEMS**：家庭能源管理。
  * **电子看板 (Digital Signage / デジタルサイネージ)**：街头广告屏。

---

## 4. ♟️ 经营与事业战略 (Corporate Strategy)

### 4.1 战略工具

* **核心竞争力 (Core Competence / コアコンピタンス)**：他司无法模仿的绝活。
* **标杆管理 (Benchmarking / ベンチマーク)**：对比行业 **“最佳实践”** (Best Practice)。

### 4.2 PPM 矩阵：资源怎么分？

根据 **市场增长率** 和 **市场占有率**，将业务分为四类：

1. 🌟 **明星 (Star / 花形)**：双高。有前途，但需持续砸钱。
2. 💰 **金牛 (Cash Cow / 金のなる木)**：低增长、高占有。摇钱树，产生稳定现金流。
3. 👶 **问题儿 (Problem Child / 問題児)**：高增长、低占有。不砸钱变瘦狗，砸钱变明星。
4. 🐶 **瘦狗 (Dog / 負け犬)**：双低。撤退信号。

### 4.3 SWOT 与 价值链

* **SWOT 分析**：
  * **内部**：Strengths (强项), Weaknesses (弱项)
  * **外部**：Opportunities (机会), Threats (威胁)
* **价值链 (Value Chain / バリューチェーン)**：区分 **主活动**（制造、物流）与 **支援活动**（人事、财务），找出利润源泉。

---

## 5. 🏢 经营管理系统 (Management Systems)

### 5.1 系统一体化

* **SCM (Supply Chain Mgmt)**：供应链全局最优化（从原料到消费者）。
* **CRM (Customer Relationship Mgmt)**：提升客户满意度 (LTV)。
* **ERP (Enterprise Resource Planning)**：人/财/物/信息集成，实时决策。
* **KM (Knowledge Mgmt)**：将 **隐性知识** (Tacit) 转化为 **显性知识** (Explicit)。

### 5.2 绩效评价：BSC

**平衡计分卡 (Balanced Scorecard)** 四维度：财务、客户、内部流程、学习与成长。

> [!NOTE]
> **指标层级**
>
> 1. **KGI** (Key Goal Indicator / 最终目标)：结果（如销售额翻倍）。
> 2. **CSF** (Critical Success Factor / 成功要因)：手段（如增加进店人数）。
> 3. **KPI** (Key Performance Indicator / 关键绩效指标)：量化过程（如每天新增50客）。

---

## 6. ⚖️ 组织、财务与法律 (Org/Fin/Law)

### 6.1 组织形态

* **职能别**：专业分工。
* **事业部制**：按产品划分，独立核算。
* **矩阵式**：一人有两个老板。
* **项目型**：任务驱动，搞完解散。

### 6.2 线性规划法 (Linear Programming)

> [!TIP]
> **解题思路**
>
> 1. **设方程**：$X, Y$ 为产品数量。
> 2. **列限制**：$\text{资源消耗} \le \text{库存上限}$。
> 3. **求交点**：解联立方程组。
> 4. **算利润**：代入目标函数 $P = aX + bY$。

### 6.3 财务会计重点

* **盈亏平衡点 (Break-Even Point / 損益分岐点)**：
    $$ \text{BEP Sales} = \frac{\text{固定费}}{1 - \text{变动费率}} $$
    *(其中 变动费率 = 变动费 ÷ 销售额)*
* **折旧 (Depreciation)**：
    $$ \text{年折旧费} = \frac{\text{取得价格} - \text{残值}}{\text{耐用年数}} $$

### 6.4 法律与合规 (Legal)

* **著作权法**：
  * 🛡️ **保护**：代码、网页。
  * ❌ **不保护**：编程语言、算法、规约。
  * **归属**：委外开发默认归 **受托方**（创作者）。
* **劳动法**：
  * **派遣**：指挥权在 **用人单位**。
  * **承包 (請負)**：指挥权在 **承包单位**。（发包方直接指挥是违法的“伪装请负”！）

---

## 📚 备考核心词汇表 (Glossary)

<div align="center">

| 中文词汇 | 假名标注 | 英文参考 |
| :--- | :--- | :--- |
| **本地部署** | オンプレミス | On-Premises |
| **住房服务** | ハウジング | Housing |
| **托管服务** | ホスティング | Hosting |
| **云端** | クラウド | Cloud |
| **数字鸿沟** | デジタルデバイド | Digital Divide |
| **联盟营销** | アフィリエイト | Affiliate |
| **转化率** | コンバージョン率 | Conversion Rate |
| **核心竞争力** | コアコンピタンス | Core Competence |
| **标杆管理** | ベンチマーク | Benchmarking |
| **供应链管理** | SCM (Supply Chain Mgmt) | Supply Chain Management |
| **关键绩效指标** | KPI | Key Performance Indicator |
| **盈亏平衡点** | 損益分岐点（そんえきぶんきてん） | Break-Even Point |
| **承包** | 請負（うけおい） | Contracting |

</div>

---

<p align="center">
  <em>"战略是洞察未来的望远镜，数据是丈量现实的刻度尺。"</em><br>
  <strong>Strategy is the telescope to foresee the future; Data is the ruler to measure reality.</strong>
</p>
