<!--
此文件的全部内容（除注释外）将作为 Release 说明。
开头这几行注释不会被写入到 Release 说明，请始终保留。

发布（Release）稳定版的方法：
- 使得本地**最新**的提交（commit）信息为“[Release]版本号”，例如“[Release]1.0.0”。
- 推送到 main 分支，GitHub 将自动构建并发布。
- 发布完成之后，请清空非注释的部分，再加一行“更新内容：”作为初始模板。

注意：
- tag 会自动创建，不需要在本地打 git tag。
- 若有相同 tag 的 Release，原 Release 将被删除。
- BepInEx 对插件版本号有格式要求，所以 V1.0.0 这种是不可以的，将会无法加载。
-->
基础设施更新：
- 解耦 LLM 构建逻辑、LLM 请求逻辑、Logger 逻辑（by @GarfieldGod ）
  - 分离 LLM 请求体构建逻辑
  - 分离 LLM 发送请求逻辑
  - 分离 BepInEx 和 Logger
  - 增加 Console 调试模式，可用 `dotnet build -c Console` 构建 `exe` 可执行程序，不必开启游戏就能调试。

