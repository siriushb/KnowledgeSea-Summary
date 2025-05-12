# GitHub - 2977094657/BilibiliHistoryFetcher: 获取b站历史记录，批量下载视频，一键下载用户投稿视频，收藏夹所有视频，生成详细的年度总结，自动化任务，下面链接是对应前端
- URL: https://github.com/2977094657/BilibiliHistoryFetcher
- Added At: 2025-05-12 09:39:02
- [Link To Text](2025-05-12-github---2977094657-bilibilihistoryfetcher-获取b站历史记录，批量下载视频，一键下载用户投稿视频，收藏夹所有视频，生成详细的年度总结，自动化任务，下面链接是对应前端_raw.md)

## TL;DR
BilibiliHistoryFetcher是一个哔哩哔哩历史记录获取与分析工具，支持数据获取、下载、分析及自动化功能，提供完整的数据处理流程。项目采用Python+FastAPI技术栈，支持Docker部署，持续开发中，已有718 GitHub星标。

## Summary
1. **项目简介**：
   - **名称**：BilibiliHistoryFetcher
   - **功能**：哔哩哔哩历史记录获取与分析工具
   - **特点**：
     - 提供完整的数据处理流程（获取、处理、分析、可视化）
     - 支持自动化运行和邮件通知
     - 配套前端项目：[BiliHistoryFrontend](https://github.com/2977094657/BiliHistoryFrontend)

2. **主要功能**：
   - **数据获取**：
     - 获取历史记录
     - 获取用户评论
     - 获取收藏夹（含批量收藏和失效视频修复）
   - **下载功能**：
     - 视频和图片下载
     - 一键下载用户所有投稿视频
     - 一键下载收藏夹所有视频
   - **分析功能**：
     - 年度总结生成
     - 获取视频观看总时长
     - AI摘要
   - **自动化**：支持定时任务

3. **开发计划**：
   - 持续开发中，可通过[GitHub项目计划页面](https://github.com/users/2977094657/projects/2)查看路线图

4. **系统要求**：
   - **基础环境**：
     - Python 3.10+
     - SQLite 3
     - FFmpeg（视频下载依赖）
   - **依赖包**：详见requirements.txt

5. **部署方式**：
   - **Docker部署**（由[@eli-yip](https://github.com/eli-yip)实现）：
     - 支持NVIDIA显卡的镜像构建：
       ```shell
       docker build -t bilibili-api:dev -f docker/Dockerfile.cuda .
       ```

6. **社区支持**：
   - **交流群**：QQ群1030089634（提供问题解答和使用交流）
   - **群二维码**：项目内附Qun.png

7. **项目状态**：
   - **版本**：最新提交于2025年5月9日（fix #56）
   - **热度**：
     - GitHub Stars: 718
     - Forks: 31
   - **许可证**：MIT License

8. **技术架构**：
   - **后端技术栈**：
     - Python + FastAPI
     - SQLite数据库
   - **构建工具**：
     - 支持多平台构建（通过build.py）
     - 使用uv作为包管理器

9. **文件结构**：
   - 核心模块：
     - `/routers`：API路由
     - `/middleware`：中间件
     - `/config`：配置文件
   - 部署相关：
     - `/docker`：Docker配置
     - `docker-compose.yml`：容器编排
   - 辅助文件：
     - `app_launcher.py`：应用启动器
     - `uv.lock`：依赖锁定文件

10. **开发动态**：
    - 近期更新：
      - 增加内部调用支持（#56）
      - 添加API密钥验证功能（#53）
      - 重构日志系统（集成Loguru，#48）
    - 历史提交：
      - 134次提交记录
      - 10个标签版本
