# 示例技能名称 SOP

**触发**：当用户请求 XXX 时 | **禁用**：YYY 场景不适用

## 一、核心规则

- ⚠️ **必须先确认**：执行前必须检查 ZZZ
- ⛔ **禁止**：不得在 AAA 情况下执行
- ✅ **推荐**：优先使用 BBB 方法

## 二、快速用法

```python
from example_module import example_function

# 基本用法
result = example_function(param1, param2)

# 高级选项
result = example_function(param1, param2, option=True)
```

## 三、工作流程

1. 确认前置条件满足
2. 准备输入数据
3. 调用核心函数
4. 验证输出结果
5. 清理临时资源

## 四、避坑指南

- ⚠️ **超时问题**：大数据量时增加 `timeout` 参数
- ⚠️ **编码问题**：使用 `file_read` 而非 `cat/type` 处理中文
- ⚠️ **路径问题**：始终使用相对路径或绝对路径，避免歧义

---

**依赖**：`example_module.py`（位于 memory/ 目录）