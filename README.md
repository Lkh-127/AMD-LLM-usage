新手必看！AMD显卡本地运行 DeepSeek-R1 全流程指南（超详细！）
哈喽大家好！我是九九吐，今天带来一篇超级实用的教程，手把手教你如何在 AMD 显卡上本地运行 DeepSeek-R1！

如果你一直在找方法让 AMD 显卡 也能流畅运行 LLM，本教程绝对适合你！💡

第一步：环境准备（Alpha 环节）
1️⃣ 下载 Ollama for AMD 
https://github.com/likelovewant/ollama-for-amd
👉 访问 Ollama for AMD
👉 进入 Releases 页面
👉 找到 .exe 文件并下载

2️⃣ 下载运行库（ROCmLibs）
https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.6.1.2
👉 打开 ROCmLibs for AMD 
👉 下载适配自己 AMD 显卡的 着色器（shader） 版本
📌 Tip： 不确定显卡的 shader 代号？可以去 TechPowerUp 查询

第二步：安装与配置
1️⃣ 安装 Ollama
✅ 运行刚刚下载的 ollama.exe，完成安装

2️⃣ 配置 ROCm 运行库
✅ 解压 ROCmLibs 下载的 .rar 文件
✅ 例如：rocm.gfx1031.for.hip.sdk.6.1.2.7z（适用于 6750 GRE）

🔹 拷贝 rocblas.dll 文件：
📂 路径： C:\Users\你的用户名\AppData\Local\Programs\Ollama\lib\ollama

🔹 删除原有 library 文件夹，并替换为解压出的 library 文件夹

📌 这样就完成了 Ollama 对 AMD 显卡的适配！

第三步：运行 DeepSeek-R1 🚀
👉 访问 Ollama 官网，找到自己喜欢的模型
👉 在 CMD 运行命令 ，如：
ollama run deepseek-r1

✅ 如果对话成功，就说明一切 OK！ 🎉
✅ 快捷键： Ctrl + D 退出对话，ollama ps 查看当前运行情况（CPU or GPU）

📌 如果 Ollama 仍然运行在 CPU
🔹 解决方法：下载 AMD 适配的 Ollama for CPU 版本
🔹 链接：AMD Ollama CPU Installer 
https://github.com/ByronLeeeee/Ollama-For-AMD-Installer
运行exe试试看

第四步：Web UI 操作（更方便！）
📌 推荐使用 Page Assist（A W 扩展）
✅ 打开 右上角齿轮 ⚙️ 设置语言
✅ 进入 RAG Settings 选择 Ollama 模型并保存
✅ 享受流畅的 Web 交互体验！

总结 & 资源 🔗
🎯 至此，你已经成功在 AMD 显卡上本地运行 DeepSeek-R1！
🎯 不再依赖昂贵的 NVIDIA 显卡，AMD 用户也能玩转大模型！

🔹 Github 资源
👉 DeepSeek-R1 官方 https://github.com/deepseek-ai/DeepSeek-R1
👉 DeepSeek-R1 详细性能论文

💬 如果本教程对你有帮助，欢迎点赞 + 关注！
📢 我是九九吐，祝大家玩得开心，我们下期再见！ 🚀
