# 你将学到什么

## EC2 简介：

什么是 EC2，为什么它很重要？

```
- Amazon Elastic Compute Cloud (Amazon EC2) 是一种 Web 服务，可在云中提供安全、可调整大小的计算能力。
- 按需访问可靠、可扩展的基础设施。在几分钟内扩展容量，SLA 承诺 99.99% 的可用性。
- 为您的应用程序提供安全的计算服务。安全性已内置到 Amazon EC2 的基础架构中，采用 AWS Nitro 系统。
- 通过灵活的选项优化性能和成本，如 AWS Graviton 实例、Amazon EC2 Spot 实例和 AWS Savings Plans。
```

EC2 使用场景

```
提供安全、可靠、高性能且具有成本效益的计算基础设施，以满足苛刻的业务需求。
按需访问运行高性能计算 (HPC) 应用程序所需的基础设施和容量，更快、更经济高效。
在几分钟内访问环境，根据需要动态扩展容量，并享受 AWS 按需付费定价的优势。
提供最广泛的计算、网络（高达 400 Gbps）和存储服务选择，专为优化机器学习项目的性价比而打造。
```

EC2 实例类型

建议参考[此页面](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html)获取详细且最新的信息。

通用型

```
通用型实例旨在提供计算、内存和网络资源的平衡。它们适用于广泛的应用程序，包括 Web 服务器、小型数据库、开发和测试环境等。
```

计算优化型

```
计算优化型实例提供更高的计算能力与内存比。它们在需要高性能处理的工作负载中表现出色，如批处理、科学建模、游戏服务器和高性能 Web 服务器。
```

内存优化型

```
内存优化型实例专为处理内存密集型工作负载而设计。它们适用于需要大量内存的应用程序，如内存数据库、实时大数据分析和高性能计算。
```

存储优化型

```
存储优化型实例针对需要对大型数据集进行高顺序读写访问的应用程序进行了优化。它们非常适合数据仓库、日志处理和分布式文件系统等任务。
```

加速计算型

```
加速计算型实例通常配备一个或多个加速器，如图形处理单元 (GPU)、现场可编程门阵列 (FPGA) 或专用集成电路 (ASIC)。
这些加速器从主 CPU 卸载计算密集型任务，为特定工作负载实现更快、更高效的处理。
```

![image](https://github.com/iam-veeramalla/aws-devops-zero-to-hero/assets/43399466/fc8e083c-dba5-41a6-94b9-14ebef0255c1)

实例家族

```
    C – 计算 (Compute)

    D – 密集存储 (Dense storage)

    F – FPGA

    G – GPU

    Hpc – 高性能计算 (High performance computing)

    I – I/O

    Inf – AWS Inferentia

    M – 大多数场景 (Most scenarios)

    P – GPU

    R – 随机存取内存 (Random access memory)

    T – 涡轮 (Turbo)

    Trn – AWS Trainium

    U – 超高内存 (Ultra-high memory)

    VT – 视频转码 (Video transcoding)

    X – 超大内存 (Extra-large memory)
```

附加能力标识

```
    a – AMD 处理器

    g – AWS Graviton 处理器

    i – Intel 处理器

    d – 实例存储卷 (Instance store volumes)

    n – 网络和 EBS 优化 (Network and EBS optimized)

    e – 额外存储或内存 (Extra storage or memory)

    z – 高性能 (High performance)
```

## EC2 实例基础：

理解虚拟服务器和实例的概念。
EC2 实例的关键组件：AMI (Amazon Machine Image)、实例类型和实例状态。
区分按需实例、预留实例和 Spot 实例。

## 启动 EC2 实例：

- 使用 AWS 管理控制台启动 EC2 实例的分步指南。
- 配置实例详细信息，如实例类型、网络设置和存储选项。
- 理解安全组和密钥对以保护实例安全。

## 管理 EC2 实例：

- 启动、停止和终止实例。
- 监控实例性能和利用率。
- 基本故障排除和使用 SSH (Secure Shell) 访问实例。