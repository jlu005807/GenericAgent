---
name: 示例技能名称
version: 1.0.0
description: 一句话描述此技能的功能和用途
author: GenericAgent Community
created: 2026-05-01
updated: 2026-05-01
tags: [示例, 模板, 基础]
trigger: 当用户请求 XXX 或系统检测到 YYY 条件时触发
input: 描述输入格式和来源（如用户指令、系统状态、文件路径等）
output: 描述输出格式和去向（如文件、控制台、返回值等）
---

# 示例技能名称 SOP

**触发**：<触发条件> | **禁用**：<不适用场景>
**核心原则**：<一句话概括执行准则>

## 前置条件

- 环境要求（如 Python 3.10+、特定 OS）
- 依赖工具（如 `pip install xxx`）
- 权限需求（如文件读写、网络访问）

## 工作流程

### Step 1: 准备阶段

- 检查环境和依赖是否就绪
- 验证输入数据的完整性

```python
# 示例：检查依赖
import importlib
assert importlib.import_module("required_pkg"), "缺少依赖: required_pkg"
```

### Step 2: 执行核心操作

- 具体操作指令
- 操作过程中需要记录关键数据

```python
# 示例：核心操作
result = perform_main_task(input_data)
```

### Step 3: 验证结果

- 检查输出是否符合预期
- 记录执行日志

```python
# 示例：验证
assert result.is_valid(), f"结果验证失败: {result.error}"
print(f"执行完成，结果: {result.summary}")
```

### Step 4: 收尾与清理

- 保存结果
- 清理临时资源
- 更新工作状态

## 常见错误与处理

| 错误场景 | 处理方式 |
|----------|----------|
| 依赖缺失 | 自动安装或提示用户 |
| 输入格式错误 | 返回格式说明并请求修正 |
| 执行超时 | 记录状态，支持断点续传 |

## 权限边界

- 无需批准：只读探测、临时文件操作
- 需要批准：修改系统配置、网络请求、安装软件
- 绝对禁止：删除用户数据、读取密钥文件

## 配置参数

| 参数 | 默认值 | 说明 |
|------|--------|------|
| `max_retries` | 3 | 最大重试次数 |
| `timeout` | 60 | 超时时间（秒） |
| `verbose` | false | 是否输出详细日志 |

## 依赖

- 无外部 SOP 依赖
- 可选：`ocr_utils.py`（用于图像识别场景）

## 版本历史

| 版本 | 日期 | 变更 |
|------|------|------|
| 1.0.0 | 2026-05-01 | 初始版本 |

## 参考

- [SOP 格式规范](./SOP_FORMAT_SPEC.md)
- 相关文档链接