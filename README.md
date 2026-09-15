# 移动交互设计 实验1 实验报告
**姓名**：沈大为
**班级**：2024级软件工程
**实验名称**：Android开发基础实验
**实验日期**：2026年X月X日
**实验环境**：Windows11，Android Studio，Git Bash，GitHub

## 一、实验目的
1. 掌握Android Studio开发环境的安装与基础配置，熟悉Android开发工具界面。
2. 学会新建Android空白工程，理解Android项目基础目录结构。
3. 掌握Git工具基础命令，学会使用GitHub远程仓库管理代码。
4. 能够将本地Android项目提交、上传至GitHub仓库，完成代码版本托管。

## 二、实验原理
1. Android Studio是Android官方集成开发环境，用于Android应用开发，项目包含`app`、`gradle`等核心目录。
2. Git是分布式版本控制系统，可以记录代码修改、保存多个版本；GitHub提供远程仓库，实现代码云端存储与分享。
3. 基本Git工作流程：初始化仓库→添加文件到暂存区→本地提交commit→推送到远程仓库push。

## 三、实验内容与步骤
1. **环境安装**
   下载并安装Android Studio，配置SDK，等待组件下载完成；安装Git工具，配置Git用户名与邮箱。

2. **创建Android项目**
   打开Android Studio，选择新建Empty Activity项目，选择Kotlin语言，创建初始空白Android工程，等待项目同步构建，验证项目可正常编译。查看项目目录，认识`app/src/main`源代码目录、gradle构建配置文件。

3. **GitHub仓库准备**
   登录GitHub网页，新建公开仓库`Android-lab1`，不勾选自动生成README。生成个人访问令牌Token，勾选repo仓库读写权限，用于Git身份验证。

4. **本地Git管理项目**
   在项目根目录打开Git Bash，执行Git命令初始化版本库，将Android项目文件加入暂存区，本地提交代码。绑定本地仓库与GitHub远程仓库origin。

5. **代码上传至远程仓库**
   尝试使用`git push`上传代码，过程中遇到403权限拒绝、网络443端口连接超时、本地代理弹窗等问题。最终采用GitHub网页上传方式，将项目`app`、`gradle`文件夹以及build.gradle、settings.gradle、.gitignore等文件上传至仓库根目录。

6. **验证结果**
   刷新GitHub仓库网页，查看仓库根目录，确认Android项目全部目录与文件成功上传。

## 四、实验结果
成功创建Android空白工程，并将完整工程上传到GitHub仓库。仓库链接：https://github.com/0110wabisabi/Android-lab1
仓库中包含`app`文件夹、`gradle`文件夹、项目配置文件、`.gitignore`文件，代码可在线查看。实验1任务完成。

## 五、遇到的问题及解决方法
1. **问题1：git push返回403 Permission denied**
   原因：Token权限不足，Windows凭据管理器缓存旧的失效Token。
   解决：删除Windows凭据管理器中github旧凭证，重新生成带repo权限的Token。

2. **问题2：Failed to connect to github.com port443，连接超时**
   原因：当前网络环境访问GitHub HTTPS服务器超时，同时本机开启代理导致代理身份验证弹窗。
   解决：取消Git全局代理配置；网络依旧无法连通，改用GitHub网页拖拽上传文件，绕过Git推送网络问题。

3. **问题3：提示nothing to commit, working tree clean**
   原因：本地代码已经完成commit提交，本地无新修改。
   解决：无需重复执行git add、git commit，直接尝试推送或者网页上传。

## 六、实验总结
本次实验完成Android开发环境搭建，了解Android项目基础结构；学习Git版本控制基础命令与GitHub代码托管。本次踩坑主要集中在网络访问与身份认证问题，校园网络直连GitHub不稳定，使用网页上传是更简单的作业提交方案。
后续实验2可以继续在这个仓库内增加多个实验页面，实现一个项目存放全部课程实验代码，继续使用该仓库进行版本管理。
