# 👋 汤笛晴 · Diqing Tang

西交利物浦大学 · 人工智能(智能系统方向)· 2025 级本科 · 25-26 学年学术成就奖学金

> **"AI 会编造。我的工作是让它在不该编造的地方,编造不出来。"**
>
> 我做 AI 应用与后端工程,所有项目都围绕同一个问题:**怎么让 AI 的输出可以被核对、被复现、被审计**——在实验室里,也在生产线上。

## 🔬 我解决的问题

### LabNote Agent:让每一次实验都成为可复用的科研资产

**问题**:调研 52 份问卷,92% 的科研记录散落在纸质笔记、Excel 和聊天记录里,73% 的人复现不出论文实验——科研的"复现危机"就在每个课题组里。

**我的做法**:多模态大模型解析散乱文件 → 结构化实验卡片(逐字段置信度 + 来源标注)→ 自动生成分步复现协议与审计报告。

**结果**:已上线 [labnote.tech](https://labnote.tech),真实课题组内测走通全链路;2026 OPC 创新大赛二等奖、新锐木兰奖、Eazo 全球青年黑客松入围全球总决赛、智博会受邀展商。

源码:[github.com/DiqingTang25/labnote-agent](https://github.com/DiqingTang25/labnote-agent) · 技术:React 19 SSR · PostgreSQL + pgvector · RAG · MCP

### AI Agent 全自动化测评系统:用 Agent 给 Agent 打分

**问题**:AI 教学助手上线了,但没人能量化它教得好不好、会不会教错。

**我的做法**:10 维度三层级联评分(L1 规则 + L2 语义 + L3 跨模型 LLM Judge 投票);Playwright 零硬编码操控被测 Agent,四层自愈定位适配平台改版;评测证据 SHA-256 封存,LLM 根因分析自动产出改进方案——**一个会自我进化的评测器**。

**结果**:云端生产运行,CI 每 30 分钟自动巡检。

源码:[github.com/DiqingTang25/eval](https://github.com/DiqingTang25/eval)

<details>
<summary>点击展开:两个项目背后的技术细节与踩过的坑</summary>

- LabNote 的"置信度":用 logprobs 做 token 级校准,把 AI 的确定性分成四级(explicit / implied / inferred / unknown),用户核对数据时看的是"AI 有多确定",而不是"AI 说了什么"
- 评测系统的"自愈":被测平台改版是常态,我做了四层级联回退定位(规则 → 语义模糊匹配 → DOM 结构推断 → LLM 语义重定位),平台改版不再让评测崩溃
- 两个项目里我都自研了 MCP Server:把内部能力原子化成工具,让外部 Agent 可以直接"使用"我的系统,而不只是"访问"我的系统
- 踩过的坑:RLS 策略无限递归(42P17)、向量函数重载歧义(PGRST203)、AI 评测的"时间泄漏"(举报时间必须晚于停留时间,否则模型学到的是标签本身)

</details>

## 其他作品

- **SurfMate 智能科研助手** —— 三个科研场景 Agent 模块,两千余条结构化 QA 库,来源标注 + "不确定即明说"抑制科研幻觉
- **GPS 轨迹筛查举报系统** —— 纯 NumPy 双尺度 DBSCAN + LightGBM 嫌疑置信度,独立验证集 Top-1 95%
- **MaestroZoo** —— AR 手势指挥动物乐团的节奏游戏(Rokid 眼镜)
- **aromaX** —— AI 中药香薰配方系统

## 黑客档案

- ⚡ 交付速度:合规领航员 Agent 两周从零到全国一等奖;LabNote 两个月从零到上线(82 次提交)
- 🧰 日常装备:WSL + Linux、SSH、GitHub Actions CI、Docker、Playwright E2E
- 🤝 **正在找**:一起打黑客松、一起做 AI for Science 的伙伴。如果你也在做可信 AI、科研工具或 Agent 基础设施,直接邮件我

## 一些数字

独立验证集 Top-1 95%(Top-3 100%)· 14,000+ 条标注样本 · 8 个对外开放的 MCP 工具 · 两千余条结构化 QA 库

## 技术栈

![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/-Flask-000000?logo=flask&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/-MySQL-4479A1?logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?logo=redis&logoColor=white)
![React](https://img.shields.io/badge/-React_19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/-Linux-FCC624?logo=linux&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-2088FF?logo=githubactions&logoColor=white)

LLM / RAG / Agent:多模型接入(DeepSeek、GPT-4o、GLM、Qwen3-VL)· RAG(向量 + 全文混合检索 + 重排)· 多 Agent 编排 · LLM-as-a-Judge · MCP 工具开发

## 📫 找到我

- 邮箱:2662001087@qq.com
- 地点:中国 · 苏州
