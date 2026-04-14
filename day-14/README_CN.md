# AWS 持续集成演示

## 设置 GitHub 仓库

我们 CI 旅程的第一步是设置一个 GitHub 仓库来存储 Python 应用程序的源代码。如果你已经有仓库，可以跳过此步骤。否则，让我们按照以下步骤在 GitHub 上创建新仓库：

- 访问 github.com 并登录你的账户。
- 点击右上角的 "+" 按钮，选择 "New repository"。
- 为你的仓库命名并添加可选描述。
- 根据你的需求选择适当的可见性选项。
- 使用 README 文件初始化仓库。
- 点击 "Create repository" 按钮创建你的新 GitHub 仓库。

太好了！现在我们的仓库已设置好，可以继续下一步。

## 创建 AWS CodePipeline

在此步骤中，我们将创建 AWS CodePipeline 来自动化 Python 应用程序的持续集成流程。AWS CodePipeline 将编排从 GitHub 仓库到应用程序部署的变更流。让我们开始设置：

- 访问 AWS 管理控制台并导航到 AWS CodePipeline 服务。
- 点击 "Create pipeline" 按钮。
- 为你的管道提供名称并点击 "Next" 按钮。
- 对于源阶段，选择 "GitHub" 作为源提供商。
- 将你的 GitHub 账户连接到 AWS CodePipeline 并选择你的仓库。
- 选择你要用于管道的分支。
- 在构建阶段，选择 "AWS CodeBuild" 作为构建提供商。
- 点击 "Create project" 按钮创建新的 CodeBuild 项目。
- 为你的 Python 应用程序配置 CodeBuild 项目必要的设置，如构建环境、构建命令和构件。
- 保存 CodeBuild 项目并返回 CodePipeline。
- 继续配置管道阶段，如使用 AWS Elastic Beanstalk 或其他合适的部署选项部署应用程序。
- 查看管道配置并点击 "Create pipeline" 按钮创建你的 AWS CodePipeline。

太棒了！现在我们的管道已准备就绪。让我们继续下一步设置 AWS CodeBuild。

## 配置 AWS CodeBuild

在此步骤中，我们将配置 AWS CodeBuild 根据我们定义的规范构建 Python 应用程序。CodeBuild 将负责构建和打包应用程序以进行部署。按照以下步骤：

- 在 AWS 管理控制台中，导航到 AWS CodeBuild 服务。
- 点击 "Create build project" 按钮。
- 为你的构建项目提供名称。
- 对于源提供商，选择 "AWS CodePipeline"。
- 选择你在上一步创建的管道。
- 配置构建环境，如 Python 应用程序所需的操作系统、运行时和计算资源。
- 指定构建命令，如安装依赖和运行测试。根据应用程序的需求自定义。
- 设置构件配置以生成部署所需的构建输出。
- 查看构建项目设置并点击 "Create build project" 按钮创建你的 AWS CodeBuild 项目。

太好了！AWS CodeBuild 已设置完成，现在我们可以见证持续集成魔术的运作。

## 触发 CI 流程

在最后一步中，我们将通过更改 GitHub 仓库来触发 CI 流程。让我们看看它是如何工作的：

- 访问你的 GitHub 仓库并对 Python 应用程序的源代码进行更改。可以是 bug 修复、新功能或你想引入的任何其他更改。
- 将更改提交并推送到 AWS CodePipeline 中配置的分支。
- 进入 AWS CodePipeline 控制台并导航到你的管道。
- 你应该看到管道在检测到仓库变更后自动启动。
- 坐下来放松，AWS CodePipeline 会处理其余工作。它将获取最新代码，使用 AWS CodeBuild 触发构建过程，并在你配置了部署阶段的情况下部署应用程序。