# 王辅助系 RVC 语音模型

小王音色的 RVC 语音转换模型。准备一段去伴奏的纯人声输入音频，通过 RVC 将其转换为目标音色。本项目提供模型文件及使用说明。

## 内容

完整 ZIP 包含全部 7 个推理模型，用户可自由选择。包内另附目录，供使用同款 RVC 环境的用户测试。该目录包含训练资料和检查点。

完整模型包：[夸克网盘下载](https://pan.quark.cn/s/d92ede45c0a3?pwd=13AF)，提取码：`13AF`。版本说明见本仓库的 Releases 页面。

## 选择模型

**一般直接选 `wanghongwen_e150_s10500.pth`。** e150 是本次最后训练出的结果，但训练轮数更多可能出现过拟合，不保证对所有输入都最好。可以使用相同输入音频比较其他轮次，选择更适合自己的版本。

全部模型均为 **RVC v2、40 kHz、带音高引导**。

## 如何使用

以下步骤以训练时使用的 Windows 整合环境 **RVC20260718Nvidia50x0** 为例。RVC 根目录是 `go-webui.bat` 所在目录。

1. 下载并解压 `whw_rvc_model_v1.0.zip`，打开包内的 `whw_rvc_model_v1.0` 文件夹。将需要的 `.pth` 模型复制到 RVC 的 `assets/weights/`。
2. 如需测试随包附带的目录，将包内 `wanghongwen/` 完整复制到 RVC 的 `logs/`，形成 `logs/wanghongwen/`。
3. 运行 `go-webui.bat`，进入模型推理页面，刷新模型列表，选择一个小王模型。建议先选择 e150 。
4. 按照软件提供的一般流程推理即可。

## 使用说明

- 模型由 RTX 50 系环境训练。应使用适合自己的 RVC 运行环境；跨设备实际运行情况欢迎反馈。
- 输出是 AI 转换音频，不代表辅助系本人真实说过相应内容；公开分享生成音频时请注明 AI 合成。

## 来源与致谢

本模型使用 [RVC-Project / Retrieval-based-Voice-Conversion-WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) 作为训练与推理框架。感谢 RVC-Project 团队及项目贡献者。

本仓库维护者负责小王音色模型的训练、整理和发布。本发布不附带 RVC 环境程序代码。RVC 软件的许可请参阅上游 [MIT LICENSE](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI/blob/main/LICENSE)。
