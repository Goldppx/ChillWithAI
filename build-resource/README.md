这里存放构建 Mod 需要用到的资源文件，主要用于在线构建（本地构建可直接引用游戏所在目录）。

## 文件说明
- `buildenv` 中的文件用于构建 `AIChat.dll`（随后将其放入 `assets` 中进行打包）。
  - `mokgamedir` 与游戏目录结构保持一致，但仅保留构建所需的部分（参见 [qzrs777/AIChat 仓库中的 AIChat/AIChat.csproj](https://github.com/qzrs777/AIChat/blob/main/AIChat/AIChat.csproj) 所引用的文件）来减小体积（注：`BepInEx` 采用软链接，不需要移除其中的任何文件）。
- `assets` 中的文件用于直接打包。
