# csmg-battle-assets · 立绘图床

`assets/` 是脚本内置资源的备份（竞技场默认背景 + 默认敌人立绘）。

`characters/` 是**角色立绘**，放进去即可生效，不需要改脚本。

## 目录约定

```
characters/<角色名>/idle.png     常态
characters/<角色名>/attack.png   攻击
characters/<角色名>/hurt.png     受击
characters/<角色名>/dodge.png    闪避
```

**只有一张普通立绘的角色**，任选一种：

```
characters/<角色名>/idle.png     ← 放这一个，四个状态都用它
characters/<角色名>.png          ← 或者直接丢个单文件，也认
```

## 文件格式

- **`.png` 和 `.jpg` 都支持**，探测顺序是 `.png` 优先、`.jpg` 兜底。
- 想要**透明背景**就必须用 **PNG**。JPEG 格式本身没有 alpha 通道，
  且剪贴板 / 聊天软件传图会把透明底压成白底 —— 那样贴到战斗界面上就是一个白方块。
- 建议四个差分的画布比例保持一致（脚本的立绘 `<img>` 是拉伸填充，不看宽高比）。

## 规则

- `<角色名>` 与游戏里显示的颜名完全一致（例如 `李汐子`），中文直接写，会自动 URL 编码。
- 访问地址：`https://cdn.jsdelivr.net/gh/Sh10na/csmg-battle-assets@main/characters/...`
  jsDelivr 对分支引用有约 12 小时缓存；想立刻生效就给仓库打 tag 并改用 `@v2`。
- 优先级：界面里手动设置过的立绘 > 图床立绘 > 角色卡自带立绘 / 立绘库 > 内置默认素材。
  图床里没有的角色会自动落到后面的来源，不会白屏。
