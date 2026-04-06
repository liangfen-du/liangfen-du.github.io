# 计划：将 周桐（Zhou Tong）移至 Alumni（校友）板块

## 目标与背景 (Summary & Current State Analysis)
目前在 `_data/team.yml` 文件中，**ZHOU Tong (周桐)** 被列在 `postdocs` 板块下（第 15-28 行）。根据您的要求，我们需要将他的信息从博士后板块移除，并将他添加到 `alumni` 板块，同时更新其介绍文案，祝贺他前往宁波诺丁汉大学就职。

## 提议的更改 (Proposed Changes)

**目标文件:** `_data/team.yml`

1. **移除现有的博士后信息 (Delete from postdocs):**
   删除第 15 至 28 行的内容：
   ```yaml
     - name: "ZHOU Tong (周桐)"
       image: "/images/zhou_tong.jpeg"
       ...
       contact:
         - type: "email"
           url: "mailto:tong-beee.zhou@polyu.edu.hk"
   ```

2. **添加至校友板块 (Add to alumni):**
   在 `alumni:` 节点下（作为最新添加的校友，置于列表顶部或现有列表后），增加如下内容：
   ```yaml
     - name: "Zhou Tong (周桐)"
       title: "Postdoctoral Fellow (2024.10 ~ 2026.03). Dr. Zhou will begin his new journey at the University of Nottingham Ningbo China. Congratulations to him, and we wish him all the best and continued success in his future career."
   ```

## 假设与决定 (Assumptions & Decisions)
- 根据 `_pages/team.md` 中的渲染逻辑，校友列表使用 `<li>{{ member.name }}, {{ member.title }}</li>` 格式，因此我们将新的文案分配为 `title`，以完全匹配页面展示效果并符合现有的数据结构规范。

## 验证步骤 (Verification steps)
- 检查 `_data/team.yml` 格式是否合法，无缩进错误。
- 确认 Jekyll 页面（Team 页面的 Alumni 部分）正确渲染了修改后的 Zhou Tong 校友信息。