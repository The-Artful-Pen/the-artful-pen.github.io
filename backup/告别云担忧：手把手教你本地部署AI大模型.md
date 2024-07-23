## 前言
当我们想跟AI对话时，把一些文件发送到云端可能会不安全，这时候，就需要本地部署了。本地部署指的是AI会调用电脑本地的算力进行计算，所以，电脑的性能不可以太差。下面是本地部署大模型的教程。
> [!IMPORTANT]
> 请务必**看完全文后再进行操作**
> [!IMPORTANT]
>本教程使用Win10，如果您是Mac用户，请参考[Mac本地部署教程](https://www.bilibili.com/video/BV18E421N7d4/?vd_source=4d615fafe7d9dfc43c90bfcb3b9fdcbb)
## 教程
### 准备
下载[Ollama](https://ollama.com/),进入主页点击Download，选择自己的操作系统，点击下载
> [!NOTE]
> 您无需点击下方的注册按钮
### 下载大模型
1.下载完成后点击Win+R，“打开”栏输入cmd，回车
2.打开 [Ollama官网](https://ollama.com/)，点击右上角的 `Search models`，输入你想下载的开源模型名称。找到模型后，复制页面中提供的下载命令到CMD窗口，回车开始下载。
![屏幕截图 2024-07-23 102305](https://github.com/user-attachments/assets/22fdeeeb-6382-4051-8164-e4b800d99b62)
![屏幕截图 2024-07-23 103510](https://github.com/user-attachments/assets/45c070d8-c8e4-4d37-8712-442505c366ed)
> [!Warning]
> 每个模型的代码不一样，上图使用Qwen2-72b演示，请根据电脑性能选择下载的模型。一般来说，7b左右的模型适合大部分的电脑，我2016年的显卡都带的动。72b左右的模型则需要强大性能的电脑，它的安装包就足有40GB！

> [!TIP]
> 建议选择qwen2，因为它是迄今为止**最强大的开源大模型**，具体可以看[🤗 Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard)，您也可以选择自己喜欢的大模型，方法相同
![屏幕截图 2024-07-23 104504](https://github.com/user-attachments/assets/bdd3cc45-c8e0-4c89-afa9-9e57c6ed8773)

### 使用大模型
完成下载后，你将看到类似以下界面，这意味着一切准备就绪！
![屏幕截图 2024-07-23 105346](https://github.com/user-attachments/assets/6e1cccf9-3def-48e2-97a3-270844a1e946)
测试一下
![屏幕截图 2024-07-23 110142](https://github.com/user-attachments/assets/4ab8d016-3abe-4c05-a826-e37cdb8a3596)
> [!TIP]
> 要再次使用模型，重复上述**下载大模型的第1-2步**，但这次回车后将启动而不是重新下载模型。请确保Ollama程序正在运行。
由于Ollama位于国外，国内用户可能会遇到下载速度缓慢的问题。为此，我已将下载链接上传至网盘，你可以直接从那里下载，无需注册。
[123网盘下载](https://www.123pan.com/s/hoPKVv-DxB63.html)
请忽略下载页的广告

## 其他
什么，界面不好看？下期博客教大家获得更好地UI界面