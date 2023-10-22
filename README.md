# OpenPAI-HENU

⚠️ 本服务没有任何技术支持，请自行参考文档和相关说明使用

⚠️ 公用数据存储需要你在openpai文件夹中创建一个与你用户名相同的文件夹，之后，参考官方文档，这个文件夹的文件将自动挂载到容器中。

| 相关资源： | [官方文档](https://openpai.readthedocs.io/zh_CN/latest/manual/cluster-user/index.html) | [交流讨论区](https://github.com/yurhett/OpenPAI-HENU/issues) | [数据区挂载教程](https://kb.synology.cn/zh-cn/DSM/tutorial/How_to_access_files_on_Synology_NAS_with_WebDAV) | 🔥🔥🔥[多卡训练教程（很简单）](https://pytorch.org/tutorials/beginner/blitz/data_parallel_tutorial.html) |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |

### Q&A:

Q：部署一次需要多长时间呢？

A：分情况。如果你需要的镜像服务器没有，就需要通过网络拉取，通常需要10分钟或更久（取决于镜像大小）。如果使用你（或别人）以前用过的镜像，则不需要很长时间。

Q：为什么能在Jobs页面看到别人的项目？

A：这是正常的，作为一款内部协作工具，不必过多担心。

Q：怎么切换服务器？

A：每个Virtual Cluster有不同的服务器，请在首页查看占用情况选择具有合适资源的机器。

Q：每个人限制多少资源？

A：在资源能够满足的情况下，目前限制每人最高调用3个SKU，注意，三个SKU是三张显卡，并不代表你的代码支持多卡并行计算，请检查代码。

Q：对软件的支持情况？

A：需要特别说明的以下两配置：

|          | K80  | K40  |
| -------- | ---- | ---- |
| CUDA     | 11.8 | 11.8 |
| Pytorch  | 最新 | 1.2  |
| 算力等级 | 3.7  | 3.5  |


### 20231021

服务上线

