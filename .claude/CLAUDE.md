# GPT 学术优化 (GPT Academic) 配置

> **项目**: gpt_academic
> **仓库**: https://github.com/binary-husky/gpt_academic
> **作者**: binary-husky

## 项目概述

GPT 学术优化 - 一个为学术工作设计的 AI 助手，具有论文翻译、代码解释、文档润色等功能。

**核心功能**:
- **论文处理**: Arxiv 论文翻译、PDF 全文翻译、Latex 校对
- **代码功能**: 程序剖析、批量注释生成、代码解释
- **写作辅助**: 润色、翻译、语法纠错
- **多模型支持**: GPT、通义千问、智谱 GLM、DeepseekCoder 等
- **插件系统**: 模块化设计，支持自定义插件热更新

## 技术栈

| 技术 | 用途 |
|------|------|
| Python | 主要语言 |
| Gradio | Web UI |
| LangChain | LLM 集成 |
| Transformers | 本地模型支持 |
| Docker | 容器化部署 |

## 项目结构

```
gpt_academic/
├── main.py                 # 入口文件
├── config.py              # 配置文件
├── core_functional.py     # 核心功能
├── crazy_functional.py    # 高级功能
├── crazy_functions/       # 插件目录
├── request_llms/          # LLM 请求处理
├── shared_utils/          # 共享工具
├── themes/                # UI 主题
├── docs/                  # 文档
├── tests/                 # 测试
├── Dockerfile             # Docker 配置
└── requirements.txt       # Python 依赖
```

## 开发规范

### 安装依赖
```bash
pip install -r requirements.txt
```

### 运行
```bash
python main.py
```

### Docker 部署
```bash
docker-compose up
```

## 配置文件

主要配置在 `config.py`:
- `API_KEY`: OpenAI/其他 API 密钥（支持多个，逗号分隔）
- `LAYOUT`: 界面布局（"左右布局" 或 "上下布局"）
- `DEFAULT_WORKING_NUM`: 线程数

## 支持的模型

| 类型 | 模型 |
|------|------|
| OpenAI | GPT-3.5, GPT-4, GPT-4-turbo |
| 国内 | 通义千问、智谱 GLM、文心一言、讯飞星火 |
| 开源 | LLaMA2、ChatGLM2、DeepseekCoder |

## 主要插件

| 插件 | 功能 |
|------|------|
| Arxiv 翻译 | 高质量翻译 arxiv 论文 |
| 语音对话 | 实时语音输入 |
| 虚空终端 | 自然语言调度其他插件 |
| 程序剖析 | 一键剖析 Python/C/C++/Java 项目 |
| 批量注释 | 一键批量生成函数注释 |
| 谷歌学术助手 | 写 related work |

## 特色功能

- **Mermaid 图表渲染**: 流程图、状态转移图、甘特图等
- **公式/图片/表格显示**: 同时显示 Tex 形式和渲染形式
- **暗色主题**: URL 后添加 `/?__theme=dark`
- **多语言界面**: 支持中英日韩俄法等多种语言

## 相关文档

- [README](./README.md) - 完整文档
- [Wiki](https://github.com/binary-husky/gpt_academic/wiki) - 项目文档
- [自译解报告](https://github.com/binary-husky/gpt_academic/wiki/GPT‐Academic项目自译解报告) - `self_analysis.md`

---

## 资源索引

详见 `.claude/index.json`

## 历史记录

详见 `.claude/completed.md`

## 当前任务

详见 `.claude/in-progress.md`
