# iso21434-audit-kit

> **定位**：ISO 21434 / UN R155-R156 / GB 44495-96 审计模板与规划集（WIP）
> **技能**：合规条款拆解、审计报告模板、证据包规范
> **证据**：审计报告模板（示例受审方为虚构对象，已声明）；差距分析/映射/45 条清单未产出
> **复现**：复制 `templates/report-template.md` 开始填写
> **边界**：学习/研究；示例为虚构对象
> **维护**：WIP（P3 补交付物）


面向 ISO/SAE 21434 / UN R155 & R156 / GB 44495-2024 / GB 44496-2024 合规审计的**模板与规划集**（WIP）——把"读过标准"变成"能按审核员视角产出可判定的审计交付物"。

> 声明：本仓库用于**学习与研究**。模板内示例受审方为声明的虚构对象（模拟审计，非真实企业），不针对、也不适用于任何真实企业、车型或产品。

## 解决什么问题

合规验证岗的核心能力不是渗透，而是把标准条款拆成**可验证的检查项**，并给出可追溯、抗质询的判定。本仓库规划提供：

- **差距分析表**：ISO/SAE 21434 Clause 5~15 逐条款与受审现状对撞，输出差距等级（Conform / Minor / Major / Missing）与整改优先级（规划 ≥28 行）；
- **条款映射表**：GB 44495-2024 / GB 44496-2024 与 ISO 21434（及 UN R155 §7 / R156 SUMS）的"条款 → 测试项 → 证据"三向映射；
- **审计检查清单**：五类 45 条（组织治理 / 流程文档 / 技术措施 / 供应链 / 运维事件），每条含检查方法、判定标准与抽样建议；
- **证据包目录规范**：`EV-<类别>-<序号>` 编号规则、SHA-256 哈希清单、只读归档与保留期限；
- **审计报告**：用 `templates/report-template.md` 产出，强制"覆盖率、成熟度评分、不符合项分级"三口径一致。

## 快速开始

纯 Markdown 模板，无需安装依赖：

```bash
# 1) 复制模板开始填写
cp templates/report-template.md my-audit-report.md   # Windows: copy templates\report-template.md my-audit-report.md
# 2) 对照下方规划交付物清单逐项产出
```

## 目录结构

```text
iso21434-audit-kit/
├── README.md
├── LICENSE
├── templates/
│   └── report-template.md     # 完整审计报告模板（含示例数据；示例受审方为虚构对象）
└── （规划中，尚未产出）
    ├── data/gap-analysis.csv          # 差距分析原始数据
    ├── data/clause-map.csv            # 条款→检查项→证据
    ├── scripts/clause_coverage.py     # 条款覆盖率统计
    ├── checklist/                     # 45 条检查清单（五类）
    └── evidence-spec/                 # 证据包目录规范（编号/哈希/保留期）
```

## Status（WIP，诚实声明）

- **已完成**：审计报告模板 `templates/report-template.md`——含不符合项五要素、条款覆盖统计、CSMS 成熟度评分、抽样与访谈附录等完整结构，并附带模拟审计示例数据（示例受审方已显式声明为虚构）。
- **未完成**：差距分析、GB 44495/44496 与 ISO 21434 映射表、45 条检查清单、证据包目录规范、覆盖率脚本——以上均为规划交付物，尚未产出。
- 模板中的覆盖率（20.7%）/成熟度（1.3/5）等数字为**虚构示例**，仅演示结构与口径一致性，不代表任何真实评估结论。

## License

MIT（见 LICENSE）。

---

**English TL;DR:** A WIP template-and-planning repo for ISO/SAE 21434 / UN R155-R156 / GB 44495-44496 compliance audits. Ships a full audit-report template (with example data from a declared fictional OEM); gap analysis, clause mapping tables, a 45-item checklist, and the evidence-package spec are planned but not yet produced. For study and research only — not applicable to real companies or vehicles.
