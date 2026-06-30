# SimpleHmi_WEILI 规范索引

本索引用于帮助 AI 按阶段读取规范。不要一次性发散读取全部文件；先判断阶段，再读取对应规范和模板。

## 核心文件

| 文件 | 用途 |
| --- | --- |
| `../AGENTS.md` | AI 工作入口，定义阶段加载规则 |
| `../SIMPLE_HMI.md` | 总规范，最高优先级 |
| `../ENGINES.md` | 技术栈判定 |
| `../deployment_control/README.md` | deployment_control 标准能力规范 |

## 示例入口

| 示例 | 用途 |
| --- | --- |
| `../examples/industrial-workstation-demo/index.html` | 工业工位 HMI 静态视觉示例 |
| `../examples/industrial-workstation-demo/README.md` | 示例说明 |

## 阶段规范

| 阶段 | 规范 | 模板 |
| --- | --- | --- |
| 规划阶段 | `02_规划阶段规范.md` | `../templates/需求澄清模板.md` |
| 架构阶段 | `03_架构阶段规范.md` | `../templates/技术栈判定表.md`, `../templates/架构说明模板.md` |
| Demo 阶段 | `04_Demo阶段规范.md` | `../templates/Demo验收模板.md` |
| 开发阶段 | `05_开发阶段规范.md` | `../templates/接口契约模板.md` |
| 调试阶段 | `06_调试阶段规范.md` | `../templates/调试记录模板.md` |
| 部署阶段 | `07_部署阶段规范.md` | `../templates/部署检查清单.md` |
| 验收阶段 | `08_验收阶段规范.md` | `../templates/最终验收清单.md` |

## 横向规范

| 规范 | 何时读取 |
| --- | --- |
| `01_阶段流程规范.md` | 所有任务开始时，尤其是阶段不明确时 |
| `09_去Mock规范.md` | Demo、开发、调试、验收阶段必须读取 |
| `10_deployment_control规范.md` | 架构、部署、验收阶段必须读取 |
| `11_工程避坑清单.md` | 架构、调试、部署、验收阶段建议读取 |
| `12_项目目录结构规范.md` | 架构、Demo、开发阶段需要生成项目目录时读取 |

## 最小读取策略

如果用户只说“帮我做一个工业 HMI 项目”，AI 读取：

1. `../AGENTS.md`
2. `../SIMPLE_HMI.md`
3. `00_INDEX.md`
4. `02_规划阶段规范.md`
5. `../templates/需求澄清模板.md`

如果用户想把本规范交给另一个 AI 使用，优先复制：

1. `../templates/AI项目生成提示词.md`
2. `../AGENTS.md`
3. `../SIMPLE_HMI.md`

如果用户说“已经有需求，帮我定架构”，AI 读取：

1. `../AGENTS.md`
2. `../SIMPLE_HMI.md`
3. `../ENGINES.md`
4. `03_架构阶段规范.md`
5. `10_deployment_control规范.md`
6. `../templates/技术栈判定表.md`
7. `../templates/架构说明模板.md`

如果用户说“不要讨论，直接写 Demo”，AI 仍必须先读取规划和架构规范；缺失关键输入时先提问。
