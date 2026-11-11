# Glimmer 测试版下载

中文桌面转写、透明浮窗和学习/模拟面试辅助工具。本仓库仅提供安装包、校验值和使用说明，不提供应用源码或源码仓库历史。安装包包含运行所需的打包程序；公开二进制不等于无法被分析。

**[下载 Glimmer 0.2.2 测试版](https://github.com/nku-jiahui/glimmer-releases/releases/tag/v0.2.2)** · [详细使用说明](USAGE.md) · [稳定性测试与反馈](STABILITY.md)

这是公开下载入口，朋友下载不需要申请私有源码仓库权限，也不需要安装 Node.js。应用当前测试配置无需激活码，但 AI / 转写服务需自行配置并承担提供方费用。

## 下载哪个文件

- **Windows x64 安装器**：[Glimmer-0.2.2-win-x64-setup.exe](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.2/Glimmer-0.2.2-win-x64-setup.exe)
- **Windows x64 ZIP**：[Glimmer-0.2.2-win-x64.zip](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.2/Glimmer-0.2.2-win-x64.zip)
- **Mac Apple silicon DMG**：[Glimmer-0.2.2-arm64.dmg](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.2/Glimmer-0.2.2-arm64.dmg)
- **Mac Apple silicon ZIP**：[Glimmer-0.2.2-arm64-mac.zip](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.2/Glimmer-0.2.2-arm64-mac.zip)
- [SHA256 校验文件](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.2/Glimmer-0.2.2-SHA256SUMS.txt)

在 Release 页面展开 **Assets** 下载上述文件。`Source code (zip/tar.gz)` 是 GitHub 自动生成的本仓库说明文件快照，不是应用安装包。Windows ARM 与 Intel Mac 包本轮未提供/未验证。

## 安装与首次使用

1. 先退出旧版 Glimmer，避免两份应用抢占快捷键。Windows运行安装器，或把ZIP全部解压后运行其中的Glimmer.exe；不要只复制一个EXE。Mac打开DMG安装到应用程序，或解压Mac ZIP。
2. 可以先跳过引导，检查窗口、透明度、专注模式和本地功能。测试包未正式签名，Mac未公证，系统可能显示未知发布者/信任提示；确认来源和校验值，并遵守设备管理策略。
3. 设置自己的 AI 服务地址、模型和 Key，保存后先手工提问。语音另外配置百炼或兼容 ASR；默认localhost地址需要自己运行服务，不是内置模型。
4. 分别试麦克风和系统声音，再测双音源。开启自动回答后，双音源仅由系统声音最终转写触发，麦克风作为上下文。
5. 点击开始采集，保存面试方向，再明确点击开始采集。上下键滚动回答；填写本应用输入框、工具打开或隐藏/最小化时释放。Windows固定恢复键Ctrl+Alt+Esc，Mac为⌘⇧Esc；先确认恢复入口再开启鼠标穿透。
6. 结束后明确停止采集并等待保存。隐藏窗口不等于停止录音；恢复键在回答和采集同时运行时先停止回答，采集还需明确停止。

## 使用前注意

- 音频会发给自己配置的转写服务；问题与选用的历史、个人资料、知识库片段和截图会发给AI。录音本地保存不代表整个流程离线。请只在参与者知情、场景规则允许时使用。
- 裸↑/↓在浮窗可见时全局用于回答。需要在其它软件正常使用方向键时，隐藏/最小化浮窗或到桌面设置改绑组合键。
- 内容保护仅请求系统排除捕获，不能保证所有截图、会议共享都看不见；从接收端按实际模式核对。
- 本地资料检索不是训练模型；扫描PDF无OCR，真实经历不足时不应编造个人故事。行为面试准备见[使用说明](USAGE.md#行为面试题宝洁八大问等)。
- Windows包在Mac交叉生成，已检查架构、目标PDF原生模块、最终代码及压缩完整性，尚无Windows真机和长期稳定性验收。真实ASR、AI质量、耳机切换、休眠与共享表现仍需实测。
- 当前没有正式购买、售后或自动更新源；只从本仓库下载手动更新。安装包不包含使用者的服务密钥、个人会话或录音。

完整步骤、数据/费用边界和故障排查见[USAGE.md](USAGE.md)。请按[STABILITY.md](STABILITY.md)记录测试；如提交[问题反馈](https://github.com/nku-jiahui/glimmer-releases/issues/new)，不要附API Key、真实录音或完整用户目录。
