# Glimmer 测试版下载

Glimmer 是一款中文桌面学习与模拟面试辅助工具：将声音转成文字，结合上下文识别问题，并在透明浮窗中显示回答。也可以直接打字提问、参考自己的资料，以及回看会话和录音。

**[下载 Glimmer 0.2.3 测试版](https://github.com/nku-jiahui/glimmer-releases/releases/tag/v0.2.3)** · [首次安装与配置](SETUP.md) · [详细使用说明](USAGE.md) · [稳定性测试与反馈](STABILITY.md)

从这里下载安装包，再按教程完成服务配置即可开始使用，不需要源码、开发环境或 GitHub 账号。当前测试配置无需激活码；AI / 转写服务需要使用自己的账号，调用费用由对应服务商收取。

0.2.3 新增技术 / 行为自动混合回答、可编辑默认故事模板，以及按简历一键生成初稿。Windows x64 和 Mac Apple silicon 均提供测试包；Windows 真机效果仍需反馈。完整改动与试用步骤见 [版本说明](https://github.com/nku-jiahui/glimmer-releases/releases/tag/v0.2.3)。

## 下载哪个文件

- **Windows x64 安装器**：[Glimmer-0.2.3-win-x64-setup.exe](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.3/Glimmer-0.2.3-win-x64-setup.exe)
- **Windows x64 ZIP**：[Glimmer-0.2.3-win-x64.zip](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.3/Glimmer-0.2.3-win-x64.zip)
- **Mac Apple silicon DMG**：[Glimmer-0.2.3-arm64.dmg](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.3/Glimmer-0.2.3-arm64.dmg)
- **Mac Apple silicon ZIP**：[Glimmer-0.2.3-arm64-mac.zip](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.3/Glimmer-0.2.3-arm64-mac.zip)
- [SHA256 校验文件](https://github.com/nku-jiahui/glimmer-releases/releases/download/v0.2.3/Glimmer-0.2.3-SHA256SUMS.txt)

在 Release 页面展开 **Assets** 下载上述文件。`Source code (zip/tar.gz)` 是 GitHub 自动生成的本仓库说明文件快照，不是应用安装包。Windows ARM 与 Intel Mac 包本轮未提供/未验证。

## 安装与首次使用

**第一次用，直接打开 [从安装到第一次回答：完整配置教程](SETUP.md)。** 包含服务商网站入口、每个字段填什么、语音识别的两种选项和故障排查，不需要懂编程。

### 第一次安装：没有旧版

Windows 下载 EXE 安装器按向导安装；ZIP 版先“全部解压”，再打开完整文件夹里的 `Glimmer.exe`。Mac M 系列芯片打开 arm64 DMG，将应用拖到“应用程序”再启动。不需要先卸载或退出“旧版”，也不需要安装 Node.js。

### 已有旧版：先备份，再升级

旧版先停止任务、等待保存，重要会话导出、录音另行备份，再完全退出。Windows 运行新版安装器，或把 ZIP 完整解压到新目录；Mac 替换“应用程序”里的旧应用。不要同时启动两份程序，不混用新旧资源。[升级详细步骤](SETUP.md#从旧版升级已经装过-glimmer)。

### 安装时系统提醒，是什么意思

测试包还没有正式发行者签名，Mac 也没有提交 Apple 公证检查，所以系统可能无法确认发布者。这不等于已经发现病毒，也不表示文件一定安全。先核实下载来源与 SHA256 文件指纹，再按对应提示处理。公司 / 学校管理的电脑不允许安装时，联系管理员。[不同提示及具体操作](SETUP.md#系统拦截安装是什么意思)。

### 第一次配置，按这个顺序

1. **先配 AI**：到 [DeepSeek 开放平台](https://platform.deepseek.com/) 申请 API Key。Glimmer“设置 → DeepSeek 回答”中，服务地址填 `https://api.deepseek.com`，模型填 `deepseek-flash`，API Key 填自己的完整密钥；保存成功后手工提问。[逐项教程](SETUP.md#配置-ai-回答deepseek)。
2. **再选转写**：没有自建服务，建议选“阿里云百炼（实时）”，申请北京地域百炼 Key。“本机 / 兼容服务（需自行部署）”是**需自行部署的高级选项，普通安装后不可直接使用**；没有可用服务器时请跳过，不要保留默认 localhost 地址开始试音。两种转写二选一，DeepSeek Key 和百炼 Key 不能混用。[如何选择](SETUP.md#语音识别两个选项应该选哪个) · [百炼配置](SETUP.md#方案-a配置阿里云百炼实时转写)。
3. **先试音，再自动回答**：仅麦克风短测成功后，再开启自动回答；最后按需测试系统声音与双音源。双音源只有系统声音定稿触发，麦克风补充上下文。[逐步试用](SETUP.md#第一次采集和自动回答)。
4. 结束后明确停止采集，等待保存；如果答案还在输出，另外停止生成。隐藏窗口不等于停止录音。

## 使用前注意

- 音频会发给自己配置的转写服务；问题与选用的历史、个人资料、知识库片段和截图会发给AI。录音本地保存不代表整个流程离线。请只在参与者知情、场景规则允许时使用。
- 裸↑/↓在浮窗可见时全局用于回答。需要在其它软件正常使用方向键时，隐藏/最小化浮窗或到桌面设置改绑组合键。
- 内容保护仅请求系统排除捕获，不能保证所有截图、会议共享都看不见；从接收端按实际模式核对。
- 本地资料检索不是训练模型；扫描 PDF 暂无 OCR。行为面试可先用一份核心经历和通用结构练习，操作见[使用说明](USAGE.md#行为面试题宝洁八大问等)。
- Windows包在Mac交叉生成，已检查架构、目标PDF原生模块、最终代码及压缩完整性，尚无Windows真机和长期稳定性验收。真实ASR、AI质量、耳机切换、休眠与共享表现仍需实测。
- 当前没有正式购买、售后或自动更新源；只从本仓库下载手动更新。安装包不包含使用者的服务密钥、个人会话或录音。

完整步骤、数据/费用边界和故障排查见[USAGE.md](USAGE.md)。请按[STABILITY.md](STABILITY.md)记录测试；如提交[问题反馈](https://github.com/nku-jiahui/glimmer-releases/issues/new)，不要附API Key、真实录音或完整用户目录。
