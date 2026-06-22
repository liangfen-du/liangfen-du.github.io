# 计划：新增 06/2026 最佳论文奖活动记录

## 1. 摘要 (Summary)
为项目首页的活动列表 (`_data/activities.yml`) 新增一条 06/2026 关于获得最佳论文奖 (Best Paper Award) 的记录。同时，将本地下载目录中的两张相关原图处理为适合网页展示的缩略图，并放入项目的 `images` 目录中。

## 2. 当前状态分析 (Current State Analysis)
- 待添加的内容：06/2026 的 Best Paper Award 获奖记录，包含文字描述和两张照片（颁奖合影和证书）。
- 原图位置：
  - `/Users/zhenglilei/Downloads/Image_20260622203829_822_48.jpg`
  - `/Users/zhenglilei/Downloads/Image_20260622203832_823_48.jpg`
- 目标数据文件：`/Users/zhenglilei/Documents/2_dlf_homepage/liangfen-du.github.io/_data/activities.yml`，该文件记录按时间倒序排列。

## 3. 提议的更改 (Proposed Changes)

### 3.1 处理并保存图片
- **操作**：使用 `sips` 命令对两张原图进行尺寸缩放和格式优化（限制最大尺寸为 1280px 宽/高，输出高质量 JPEG）。
- **输出**：
  - `images/2026-06-Best-Paper-Award-1.jpg` （对应第一张图）
  - `images/2026-06-Best-Paper-Award-2.jpg` （对应第二张图）

### 3.2 更新 `_data/activities.yml`
- **操作**：在文件最顶部的列表前插入新的活动项。
- **YAML 结构**：
```yaml
- date: "06/2026"
  images:
    - src: "/images/2026-06-Best-Paper-Award-1.jpg"
      alt: "Best Paper Award Group Photo"
      style: "display: inline-block; width: 100%; margin-bottom: 2%; vertical-align: top;"
    - src: "/images/2026-06-Best-Paper-Award-2.jpg"
      alt: "Best Paper Award Certificate"
      style: "display: inline-block; width: 100%; vertical-align: top;"
  description: "Our paper, “Directional Control of Noise Transmission via Ultracompact Acoustic Metagrating Barriers,” received the Best Paper Award from the committee of the 35th International Conference on Adaptive Structures and Technologies. Congratulations to Mr. Liangzhou Wang and Dr. Wenkai Dong!"
```
*(注：参考之前多图的排版，添加适当的 style 属性确保页面显示整齐)*

## 4. 假设与决策 (Assumptions & Decisions)
- 图片最大尺寸定为 1280px，既能保持足够的清晰度，又能有效减小网页加载时的文件体积。
- 考虑到有两张图片，在 `images` 数组中顺次排列。

## 5. 验证步骤 (Verification Steps)
- 运行 `ls -l images/2026-06-Best-Paper-Award-*.jpg` 确保两张图片生成成功且文件大小合理。
- 检查 `_data/activities.yml` 文件的内容，确保 YAML 语法有效，且新记录被正确添加到文件首位。