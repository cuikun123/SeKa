# OpenSpec Index

本文件是当前仓库 OpenSpec 资产索引。

<!-- opsx-init:rules:start —— 由 sdflow-init 维护，勿手改本区块 -->
## OpenSpec 工作流规则（sdflow-init 维护）

> 本区块由 `sdflow-init` 维护——`openspec/workflow/` bundle 的规则索引。
> 新增/删 workflow 规则后重跑 `sdflow-init update`，或手动同步本表。

> **本表不是本仓目录**：下列规则文件在消费仓**不存在**，不随 `sdflow-init` 铺设。
> 解析只有一条路径：`$SDFLOW_HOME/workflow/`（缺省 `~/.sdflow/workflow/`），或 `$SDFLOW_HOME/workflow-path` 指针文件的首行所指目录。
> 取到的目录须通过健全性检查；**目录存在但不健全时不会再试指针**，`resolve-workflow.sh` 直接以 exit 2 显式降级（修复：在运行 checkout 跑 `bash setup.sh`）。
> 本仓 `openspec/workflow/` 内的本地副本一律忽略。下表按文件名查阅，**一律不可点**。

| 名称 | 文件 | 作用 |
|---|---|---|
| `workflow` | `workflow.md` | 端到端流程总览（三阶段连续化）：/sdflow-spec 生成→设计审(sdflow-spec-review 编排器)→设计 GATE→实现(sdflow-implement)+代码审(sdflow-code-review)+收尾(sdflow-done)；阶段内部不用 /clear，仅两处阶段交界用（G1），连续跑到 merge |
| `trigger-catalog` | `trigger-catalog.md` | 「按内容条件触发」单一权威源 TG-NN，驱动 约束/领域清单/画图/必填槽 四层 |
| `ff-generation-constraints` | `ff-generation-constraints.md` | 生成起手强制：FF-0 开分支 + 生成硬约束 D-1~D-6 + 切片建议（`/sdflow-spec` 调用，或 `opsx:propose` 直呼） |
| `generation-process` | `generation-process.md` | 生成过程：发散(explore) + `/sdflow-spec`（澄清→拷问→生成三相位） |
| `design-diagrams` | `design-diagrams.md` | 设计/spec 阶段画哪些图、何时画、什么形态（C4 + 行为图，触发条件化） |
| `spec-review` | `spec-review.md` | spec 评审（Detection 层）：只做 prevention 残差，trigger 驱动 + 独立 + 读码核验 |
| `model-tiers` | `model-tiers.md` | 模型档位映射（强/中/弱职责 + canonical 缺省 + config 覆盖语义） |
| `subagent-dispatch-contract` | `subagent-dispatch-contract.md` | 已决定派发后的完整任务清单、容量分批、effort 回退、终态与本轮结果双门 |

设计审规则集（`/sdflow-spec-review` 用）：`spec-checklists/`（base BASE-NN + domains，含 devex、frontend(+frontend-react)）。
代码审规则集（`/sdflow-code-review` 用）：`code-checklists/`（base CR-NN + domains，含 frontend(+frontend-react)）。
多为说明类（可删不影响执行），另含 change 拆分标准单一源（`change-decomposition-standard.md`，被
三处 SKILL 引为执行必需的规范文本）：`reference/`（**消费仓不铺设该目录，勿按此路径查找**）。
人读概念指南（原理 / 设计思想 / 实战用法）：`~/.sdflow/workflow/sdflow-guide.html`（自包含 HTML，浏览器直接打开；随 bundle 全局分发，不入消费仓）。
>
> 本表只列**规则资产**。本仓的变更记录、ADR、issue 台账**不在本表**，见 `openspec/INDEX.md`（init 生成的人读入口）与各目录本身。
<!-- opsx-init:rules:end -->
