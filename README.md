# 自动化 ROUGE 部署与使用

为你的 NLP 任务提供方便

## docker-rouge155

我们尽力压缩了镜像的大小，提供了一个已经配置好的 ROUGE1.5.5 的 ubuntu [镜像](https://hub.docker.com/repository/docker/willqvq/rouge155)。
熟悉 docker 的同行可以拿去二次开发，不熟悉的可以等 fastNLP-rouge 的代码整理出来。

### 使用方法

从 docker hub 获取镜像， `docker pull willqvq/rouge155` 。 启动容器，把待测试的文件映射到容器内测试即可。

### 性能

与系统分给 docker 的算力和文件映射的效率（使用 NFS 会导致文件映射变慢）相关。 经多次实验统计，使用 docker 耗时约为使用原生的 1.5 倍 - 2 倍。

## fastNLP-rouge

代码还在整理中

## reference

[ROUGE-RELEASE-1.5.5](https://github.com/summanlp/evaluation/tree/master/ROUGE-RELEASE-1.5.5)
[fastNLP](https://github.com/fastnlp/fastNLP)

