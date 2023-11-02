# OpenPAI-HENU

⚠️ 本服务没有任何技术支持，请自行参考文档和相关说明使用

⚠️ 公用数据存储需要你在openpai文件夹中创建一个与你用户名相同的文件夹，之后，参考官方文档，这个文件夹的文件将自动挂载到容器中。

⚠️ Pytorch推荐镜像，除官方镜像外，推荐以下两款镜像：
  - yulonger/pytorch:1.13.1-py3.9.12-cuda11.7.1-ubuntu20.04-pai-sm35（最合适的版本，所有Virtual Cluster都兼容）
  - yulonger/pytorch:2.0.1-py3.9.17-cuda11.8.0-ubuntu20.04-pai-sm37（Pytorch2版本，除K40以外的集群可用）

| 相关资源： | [官方文档](https://openpai.readthedocs.io/zh_CN/latest/manual/cluster-user/index.html) | [交流讨论区](https://github.com/yurhett/OpenPAI-HENU/issues) | [数据区挂载教程（暂未使用）](https://kb.synology.cn/zh-cn/DSM/tutorial/How_to_access_files_on_Synology_NAS_with_WebDAV) | 🔥🔥🔥[多卡训练教程（很简单）](https://pytorch.org/tutorials/beginner/blitz/data_parallel_tutorial.html) |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |

### Q&A:
Q：有没有快速入门指南？

A：
1. 登陆文件存储，上传你的代码，我这里上传的是代码+数据的压缩包，在线解压即可。
<img width="705" alt="image" src="https://github.com/yurhett/OpenPAI-HENU/assets/46419702/16b599bc-63fa-46e0-9b5f-8875423f248c">
2. 登陆OpenPAI新建Job，选你合适的环境，用Pytorch的按照我的填。
![WX20231102-164010@2x](https://github.com/yurhett/OpenPAI-HENU/assets/46419702/9fe687c5-7f65-454c-a96d-02569df2e800)

Q：部署一次需要多长时间呢？

A：分情况。如果服务器没有你需要的镜像，就需要通过网络拉取，通常需要15分钟或更久（取决于镜像大小）。如果使用你（或别人）以前用过的镜像，则不需要很长时间。

Q：为什么能在Jobs页面看到别人的项目？在公用数据存储能看到别人的文件夹？

A：这是正常的，作为一款内部协作工具，不必过多担心。害人之心不可有，防人之心不可无。保留副本的同时，别乱动别人的文件！

Q：怎么切换服务器？

A：每个Virtual Cluster有不同的服务器，请在首页查看占用情况选择具有合适资源的机器。

Q：每个人限制多少资源？

A：在资源能够满足的情况下，目前限制每人最高调用3个SKU，注意，三个SKU是三张显卡，并不代表你的代码支持多卡并行计算，请检查代码。

Q：对软件的支持情况？

A：需要特别说明的以下两配置（注意你所使用的镜像是否兼容）：

|          | K80  | K40  |
| -------- | ---- | ---- |
| CUDA     | 11.8 | 11.8 |
| Pytorch  | 最新 | 1.2  |
| 算力等级 | 3.7  | 3.5  |


### 20231021

服务上线

