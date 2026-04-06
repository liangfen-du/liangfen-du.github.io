# 计划：在 Activities 中新增 2026 年 3 月的讲座活动

## 目标与背景 (Summary & Current State Analysis)
根据您的要求，我们需要在 `_data/activities.yml` 中新增一条 2026 年 3 月的活动记录：Prof. Du 受邀在香港工程师学会和建筑环境及能源工程学系联合举办的 BS One-Day Seminar 上发表演讲。同时您附上了一张现场照片，该照片也需要展示在活动记录中。

目前 `_data/activities.yml` 中的记录是按照时间倒序排列的，最新的记录是 `02/2026`。因此，这条 `03/2026` 的新记录应该被添加在文件最顶端。

## 提议的更改 (Proposed Changes)

**目标文件:** `_data/activities.yml`

1. **新增活动记录 (Add new activity entry):**
   在文件最开始的位置（紧挨着现有第一条记录之上），插入以下 YAML 内容：
   ```yaml
   - date: "03/2026"
     images:
       - src: "/images/2026-03-BS-Seminar.jpg"
         alt: "BS One-Day Seminar 2026"
     description: "Prof. Du was invited to give a talk at the BS One-Day Seminar, jointly organized by The Hong Kong Institution of Engineers and the Department of Building Environment and Energy Engineering."
   ```

## 假设与决定 (Assumptions & Decisions)
- **图片路径和命名：** 由于聊天中上传的图片无法自动保存到项目目录，我假设我们将使用 `/images/2026-03-BS-Seminar.jpg` 作为该图片的路径。**请您在计划执行后，将上传的图片手动保存为 `images/2026-03-BS-Seminar.jpg`，或者如果您希望使用其他名称，请在执行前告诉我修改。**
- **排序顺序：** 新记录的时间为 "03/2026"，所以被放置在文件的第一位，符合当前文件的时间倒序规则。

## 验证步骤 (Verification steps)
- 使用 Ruby 验证修改后的 `_data/activities.yml` 文件格式是否正确，无缩进错误。
- 确认新的活动项被放置在了文件顶部。