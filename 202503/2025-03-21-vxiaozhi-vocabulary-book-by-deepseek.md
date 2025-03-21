# vxiaozhi/vocabulary-book-by-deepseek
- URL: https://github.com/vxiaozhi/vocabulary-book-by-deepseek
- Added At: 2025-03-21 05:42:51
- [Link To Text](2025-03-21-vxiaozhi-vocabulary-book-by-deepseek_raw.md)

## TL;DR
该项目名为“vocabulary-book-by-deepseek”，是一个基于DeepSeek开发的英语词汇库，涵盖四六级、考研、托福等词库，提供词义、例句、助记图像等功能。项目已完成初高中、四六级、考研、托福词库，计划增加单词搜索、生成Anki卡片等功能。运行方式包括处理单词数据、生成助记图像等，代码主要由Cline和DeepSeek-R1-16b自动生成。项目采用Apache-2.0许可证，支持捐赠和交流群讨论。

## Summary
1. **项目简介**：
   - **项目名称**：vocabulary-book-by-deepseek
   - **功能**：使用 DeepSeek 开发实现的四六级、考研、托福单词词汇库，提供单词的词义、词根、例句、辅助记忆、助记图像等信息。
   - **项目链接**：[小智晖的AI单词库](https://word.vxiaozhi.com/)

2. **项目结构**：
   - **主要目录**：
     - `.github/workflows`：GitHub Actions 工作流配置
     - `data`：存储原始单词数据
     - `docs`：项目文档
     - `imgs`：存储助记图像
     - `result`：生成的结果文件
     - `scripts`：脚本文件
     - `web`：Web 相关文件
   - **主要文件**：
     - `.env.example`：环境变量示例
     - `.gitignore`：Git 忽略文件
     - `LICENSE`：Apache-2.0 许可证
     - `README.md`：项目说明文件
     - `gen_articles.py`：生成文章脚本
     - `gen_words_img.py`：生成单词助记图像脚本
     - `process_words.py`：处理单词脚本
     - `provider_aliyun.py`：阿里云图像生成提供者
     - `provider_bytedance.py`：字节跳动图像生成提供者
     - `provider_ollama.py`：Ollama 图像生成提供者
     - `provider_replicate.py`：Replicate 图像生成提供者
     - `provider_siliconflow.py`：SiliconFlow 图像生成提供者
     - `prun.sh`：运行脚本
     - `requirements.txt`：Python 依赖文件

3. **功能规划**：
   - **已完成**：
     - 初高中词库
     - 英语四级词库
     - 英语六级词库
     - 考研词库
     - 托福词库
   - **计划中**：
     - 单词搜索
     - 生成 Anki 卡片
     - 生成 PDF
     - 自定义单词本

4. **运行方式**：
   - **处理单词数据**：
     - 串行处理：`./prun.sh process_words.py`
     - 处理单个文件：`./prun.sh process_words.py a`
     - 并发处理所有文件：`for letter in {a..z}; do ./prun.sh process_words.py ${letter} & sleep 10; done`
   - **生成助记图像**：`./prun.sh gen_words_img.py`
   - **生成文章**：`./prun.sh gen_articles.py`
   - **本地启动**：`./scripts/run_local.sh` 和 `./start.sh`

5. **Cline 任务**：
   - **代码生成**：80% 以上代码采用 Cline + DeepSeek-R1-16b（本地部署）自动编码完成。
   - **提示词记录**：[Cline 任务提示词记录](https://github.com/vxiaozhi/vocabulary-book-by-deepseek/blob/main/docs/cline_tasks.md)

6. **数据来源**：
   - **四级单词库**：[Vocabulary-of-CET-4](https://github.com/cuttlin/Vocabulary-of-CET-4)
   - **六级单词库**：[english-vocabulary](https://github.com/KyleBing/english-vocabulary)

7. **赞赏与支持**：
   - **捐赠支持**：项目运行成本由个人承担，欢迎捐赠支持。
   - **交流群**：通过扫码加入讨论社群，探讨英语学习和 AI 应用。

8. **项目统计**：
   - **Stars**：360
   - **Forks**：22
   - **Watchers**：3
   - **Contributors**：2
   - **Languages**：
     - HTML 26.2%
     - CSS 21.4%
     - Less 20.0%
     - JavaScript 16.8%
     - Python 14.2%
     - Ruby 1.0%
     - Shell 0.4%

9. **许可证**：
   - **许可证类型**：Apache-2.0 许可证

10. **项目活动**：
    - **最新提交**：支持搜索功能（2025年3月16日）
    - **提交历史**：73 次提交

11. **项目导航**：
    - **主要导航选项**：
      - Code
      - Issues
      - Pull requests
      - Actions
      - Projects
      - Security
      - Insights

12. **项目资源**：
    - **Readme**：[项目说明文件](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#readme-ov-file)
    - **许可证**：[Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#Apache-2.0-1-ov-file)

13. **项目贡献者**：
    - **主要贡献者**：
      - [erikluo](https://github.com/erikluo)
      - [vxiaozhi](https://github.com/vxiaozhi)

14. **项目语言**：
    - **主要语言**：
      - HTML
      - CSS
      - Less
      - JavaScript
      - Python
      - Ruby
      - Shell

15. **项目发布**：
    - **发布状态**：暂无发布版本

16. **项目包**：
    - **包状态**：暂无发布包

17. **项目统计**：
    - **活动**：[项目活动](https://github.com/vxiaozhi/vocabulary-book-by-deepseek/activity)

18. **项目导航**：
    - **文件导航**：
      - [README](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)
      - [Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)

19. **项目功能**：
    - **功能规划**：
      - 初高中词库
      - 英语四级词库
      - 英语六级词库
      - 考研词库
      - 托福词库
      - 单词搜索
      - 生成 Anki 卡片
      - 生成 PDF
      - 自定义单词本

20. **项目运行**：
    - **运行方式**：
      - 处理单词数据
      - 生成助记图像
      - 生成文章
      - 本地启动

21. **项目数据**：
    - **数据来源**：
      - 四级单词库
      - 六级单词库

22. **项目支持**：
    - **赞赏与支持**：
      - 捐赠支持
      - 交流群

23. **项目统计**：
    - **项目统计**：
      - Stars
      - Forks
      - Watchers
      - Contributors
      - Languages

24. **项目许可证**：
    - **许可证类型**：Apache-2.0 许可证

25. **项目活动**：
    - **最新提交**：支持搜索功能（2025年3月16日）
    - **提交历史**：73 次提交

26. **项目导航**：
    - **主要导航选项**：
      - Code
      - Issues
      - Pull requests
      - Actions
      - Projects
      - Security
      - Insights

27. **项目资源**：
    - **Readme**：[项目说明文件](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#readme-ov-file)
    - **许可证**：[Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#Apache-2.0-1-ov-file)

28. **项目贡献者**：
    - **主要贡献者**：
      - [erikluo](https://github.com/erikluo)
      - [vxiaozhi](https://github.com/vxiaozhi)

29. **项目语言**：
    - **主要语言**：
      - HTML
      - CSS
      - Less
      - JavaScript
      - Python
      - Ruby
      - Shell

30. **项目发布**：
    - **发布状态**：暂无发布版本

31. **项目包**：
    - **包状态**：暂无发布包

32. **项目统计**：
    - **活动**：[项目活动](https://github.com/vxiaozhi/vocabulary-book-by-deepseek/activity)

33. **项目导航**：
    - **文件导航**：
      - [README](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)
      - [Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)

34. **项目功能**：
    - **功能规划**：
      - 初高中词库
      - 英语四级词库
      - 英语六级词库
      - 考研词库
      - 托福词库
      - 单词搜索
      - 生成 Anki 卡片
      - 生成 PDF
      - 自定义单词本

35. **项目运行**：
    - **运行方式**：
      - 处理单词数据
      - 生成助记图像
      - 生成文章
      - 本地启动

36. **项目数据**：
    - **数据来源**：
      - 四级单词库
      - 六级单词库

37. **项目支持**：
    - **赞赏与支持**：
      - 捐赠支持
      - 交流群

38. **项目统计**：
    - **项目统计**：
      - Stars
      - Forks
      - Watchers
      - Contributors
      - Languages

39. **项目许可证**：
    - **许可证类型**：Apache-2.0 许可证

40. **项目活动**：
    - **最新提交**：支持搜索功能（2025年3月16日）
    - **提交历史**：73 次提交

41. **项目导航**：
    - **主要导航选项**：
      - Code
      - Issues
      - Pull requests
      - Actions
      - Projects
      - Security
      - Insights

42. **项目资源**：
    - **Readme**：[项目说明文件](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#readme-ov-file)
    - **许可证**：[Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#Apache-2.0-1-ov-file)

43. **项目贡献者**：
    - **主要贡献者**：
      - [erikluo](https://github.com/erikluo)
      - [vxiaozhi](https://github.com/vxiaozhi)

44. **项目语言**：
    - **主要语言**：
      - HTML
      - CSS
      - Less
      - JavaScript
      - Python
      - Ruby
      - Shell

45. **项目发布**：
    - **发布状态**：暂无发布版本

46. **项目包**：
    - **包状态**：暂无发布包

47. **项目统计**：
    - **活动**：[项目活动](https://github.com/vxiaozhi/vocabulary-book-by-deepseek/activity)

48. **项目导航**：
    - **文件导航**：
      - [README](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)
      - [Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)

49. **项目功能**：
    - **功能规划**：
      - 初高中词库
      - 英语四级词库
      - 英语六级词库
      - 考研词库
      - 托福词库
      - 单词搜索
      - 生成 Anki 卡片
      - 生成 PDF
      - 自定义单词本

50. **项目运行**：
    - **运行方式**：
      - 处理单词数据
      - 生成助记图像
      - 生成文章
      - 本地启动

51. **项目数据**：
    - **数据来源**：
      - 四级单词库
      - 六级单词库

52. **项目支持**：
    - **赞赏与支持**：
      - 捐赠支持
      - 交流群

53. **项目统计**：
    - **项目统计**：
      - Stars
      - Forks
      - Watchers
      - Contributors
      - Languages

54. **项目许可证**：
    - **许可证类型**：Apache-2.0 许可证

55. **项目活动**：
    - **最新提交**：支持搜索功能（2025年3月16日）
    - **提交历史**：73 次提交

56. **项目导航**：
    - **主要导航选项**：
      - Code
      - Issues
      - Pull requests
      - Actions
      - Projects
      - Security
      - Insights

57. **项目资源**：
    - **Readme**：[项目说明文件](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#readme-ov-file)
    - **许可证**：[Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#Apache-2.0-1-ov-file)

58. **项目贡献者**：
    - **主要贡献者**：
      - [erikluo](https://github.com/erikluo)
      - [vxiaozhi](https://github.com/vxiaozhi)

59. **项目语言**：
    - **主要语言**：
      - HTML
      - CSS
      - Less
      - JavaScript
      - Python
      - Ruby
      - Shell

60. **项目发布**：
    - **发布状态**：暂无发布版本

61. **项目包**：
    - **包状态**：暂无发布包

62. **项目统计**：
    - **活动**：[项目活动](https://github.com/vxiaozhi/vocabulary-book-by-deepseek/activity)

63. **项目导航**：
    - **文件导航**：
      - [README](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)
      - [Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)

64. **项目功能**：
    - **功能规划**：
      - 初高中词库
      - 英语四级词库
      - 英语六级词库
      - 考研词库
      - 托福词库
      - 单词搜索
      - 生成 Anki 卡片
      - 生成 PDF
      - 自定义单词本

65. **项目运行**：
    - **运行方式**：
      - 处理单词数据
      - 生成助记图像
      - 生成文章
      - 本地启动

66. **项目数据**：
    - **数据来源**：
      - 四级单词库
      - 六级单词库

67. **项目支持**：
    - **赞赏与支持**：
      - 捐赠支持
      - 交流群

68. **项目统计**：
    - **项目统计**：
      - Stars
      - Forks
      - Watchers
      - Contributors
      - Languages

69. **项目许可证**：
    - **许可证类型**：Apache-2.0 许可证

70. **项目活动**：
    - **最新提交**：支持搜索功能（2025年3月16日）
    - **提交历史**：73 次提交

71. **项目导航**：
    - **主要导航选项**：
      - Code
      - Issues
      - Pull requests
      - Actions
      - Projects
      - Security
      - Insights

72. **项目资源**：
    - **Readme**：[项目说明文件](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#readme-ov-file)
    - **许可证**：[Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#Apache-2.0-1-ov-file)

73. **项目贡献者**：
    - **主要贡献者**：
      - [erikluo](https://github.com/erikluo)
      - [vxiaozhi](https://github.com/vxiaozhi)

74. **项目语言**：
    - **主要语言**：
      - HTML
      - CSS
      - Less
      - JavaScript
      - Python
      - Ruby
      - Shell

75. **项目发布**：
    - **发布状态**：暂无发布版本

76. **项目包**：
    - **包状态**：暂无发布包

77. **项目统计**：
    - **活动**：[项目活动](https://github.com/vxiaozhi/vocabulary-book-by-deepseek/activity)

78. **项目导航**：
    - **文件导航**：
      - [README](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)
      - [Apache-2.0 license](https://github.com/vxiaozhi/vocabulary-book-by-deepseek#)

79. **项目功能**：
    - **功能规划**：
      - 初高中词库
      - 英语四级词库
      - 英语六级词库
      - 考研词库
      - 托福词库
      - 单词搜索
      - 生成 Anki 卡片
      - 生成 PDF
      - 自定义单词本

80. **项目运行**：
    - **运行方式**：
      - 处理单词数据
      - 生成助记图像
      - 生成文章
      - 本地启动

81. **项目数据**：
    - **数据来源**：
      - 四级单词库
      - 六级单词库

82. **项目支持**：
    - **赞赏与支持**：
      - 捐赠支持
      - 交流群

83. **项目统计**：
    - **项目统计**：
      - Stars
      - Forks
      - Watchers
      - Contributors
      - Languages

84. **项目许可证**：
    - **许可证类型**：Apache-2.0 许可证

85. **项目活动**：
    - **最新提交**：支持搜索功能（2025年3月16日）

