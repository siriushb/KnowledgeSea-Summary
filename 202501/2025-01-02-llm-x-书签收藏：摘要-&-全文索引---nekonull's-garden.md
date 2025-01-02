# LLM x 书签收藏：摘要 & 全文索引 - Nekonull's Garden
- URL: https://nekonull.me/posts/llm_x_bookmark/
- Added At: 2025-01-02 09:48:26
- [Link To Text](2025-01-02-llm-x-书签收藏：摘要-&-全文索引---nekonull's-garden_raw.md)

## TL;DR
作者使用`osmos::memo`插件将书签记录到Github存储库，但面临死链接、查找困难和内容遗忘等问题。为此，作者创建了`bookmark-summary`存储库，通过Github Actions自动化生成书签摘要，并利用LLM提升效率。未来计划优化摘要质量、数据结构化、代码重构等，并已实现自动生成周报功能。

## Summary
1. **背景**：
   - 作者在浏览网页时经常收藏有趣的文章或网站，但发现单独收藏效率不高。
   - 自2021年5月起，使用名为`osmos::memo`的书签插件，将收藏记录到公开的Github存储库中。
   - 插件通过Github token实现自动提交和推送，近三年半积累了800+条目。

2. **问题**：
   - **死链接问题**：书签指向的URL可能失效，导致无法访问。
   - **查找困难**：记录项仅包含URL、标题和标签，查找时效率低下。
   - **内容遗忘**：书签中的长文章时间久了容易忘记内容，重新阅读耗时。

3. **解决方案**：
   - 创建新的存储库`bookmark-summary`，作为现有书签存储库的辅助数据。
   - 通过Github Actions实现自动化流程：
     - 新增书签条目后，触发`summarize`工作流。
     - 使用`jina reader` API获取Markdown格式的全文。
     - 使用LLM生成列表摘要和一句话总结。
     - 将摘要和总结保存到`YYYYMM/{title}.md`，并更新README.md。
   - 主要代码由Claude和GPT4o编写，LLM显著提升了生产力。

4. **未来优化方向**：
   - **列表摘要质量**：优化prompt或更换模型，解决摘要过于简略的问题。
   - **数据结构化**：考虑在Markdown之外维护JSON格式，便于程序查询。
   - **代码整理和重构**：将逻辑拆分为多个模块，改进测试和存储库交互方式。
   - **向量搜索**：引入embedding模型，实现更高效的搜索功能。
   - **自动生成周报**：已完成，每周新增书签自动生成摘要并发布到Github Releases。
   - **工具链升级**：考虑使用更现代的工具链，如uv和PEP 723。

5. **部署指南**：
   - 初始化书签存储库并安装`osmos::memo`插件。
   - 创建摘要存储库并添加`process_changes.py`文件。
   - 在书签存储库中添加`bookmark_summary.yml`工作流文件。
   - 生成并配置Github Personal Access Token。
   - 添加必要的环境变量，如API key和模型名称。
   - 完成配置后，测试书签添加和摘要生成流程。

6. **勘误**：
   - 感谢读者指出部署指南中的部分步骤错误，已在文中修复。
