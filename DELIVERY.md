# Windows 下载和测试步骤

这是技术验证程序，不是完整网页工具。本分支只交付程序 ZIP 和说明，没有真实业务 PDF、二维码图片或生成标签。

## 下载程序

1. 在 GitHub 打开本分支的 `distribution/offline-probe.zip` 文件。
2. 点击文件页面中的下载按钮（Download raw file）；也可点击 View raw / Raw 下载。不要保存整个 GitHub 网页。
3. Windows 下载目录中应出现 `offline-probe.zip`。
4. 用鼠标右键点击 ZIP，选择“全部解压”。不要在 ZIP 内直接运行。
5. 打开解压后的 `offline-probe` 文件夹，里面应有 index.html、vendor、licenses 和 README.txt。

如果找不到单个文件的下载按钮，在本分支仓库主页点击绿色 Code → Download ZIP，解压整个仓库，再找到 distribution/offline-probe.zip，继续“全部解压”。

## 在本地生成三页测试 PDF

1. 准备你电脑上原有的固定产品标签 PDF 和平台箱唛 PDF。不需要上传到 GitHub。
2. 断开 Wi-Fi 或网线。
3. 右键 index.html → 打开方式 → Microsoft Edge 或 Google Chrome。
4. 点击第一个“选择文件”，选固定产品标签 PDF 1。
5. 点击第二个“选择文件”，选平台箱唛 PDF 2。
6. 点击“运行技术测试”，等待读取完成。
7. 成功时应显示 203 页输入、405 个箱唛、3 页输出，序号为 282、283、284，并显示首张预览。
8. 点击“下载三页测试 PDF”。浏览器会保存 test-282-284.pdf，通常在“下载”文件夹；可按 Ctrl+J 查看下载记录。
9. 用 Edge/Chrome 打开下载的 PDF，确认三页序号；再与参考 PDF 的前三页比较。

请分别在 Edge 和 Chrome 测试。若按钮没有反应、提示错误或无法下载，告诉我们操作步骤、浏览器版本和错误文字；这意味着该 Windows 环境尚未验证通过，不能用启动服务器替代此验收。

## 已验证与未验证

- Linux Chromium 断网状态下，通过本地脚本内嵌文档，成功解析、合成、预览及下载；零网络请求。
- 三页输出与参考前三页在 144 DPI 下逐像素一致，原始图像数据保留，二维码软件解码一致。
- 云浏览器管理员策略阻止 file:// 导航，未验证外部脚本的双击加载。
- Windows 10/11 的 Edge/Chrome 双击运行和实物打印扫码未验证。下载此程序并不代表这些检查已经通过。
- 使用预加载解析器在主线程处理，可能短暂卡顿；本测试只支持本次样本版式和 282–284。
- 裁剪只控制可见区域，并不保证删除隐藏内容，不能用作隐私脱敏。

完整分析见 VALIDATION.md。三页业务测试 PDF 不会发布到 GitHub，请按上述步骤在本地生成。
