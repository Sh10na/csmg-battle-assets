# csmg-battle-assets · 立绘图床

`assets/` 是脚本内置资源的备份（竞技场默认背景 + 默认敌人立绘）。

`characters/` 是**角色立绘**，放进去即可生效，不需要改脚本：

```
characters/<角色名>/idle.png     常态
characters/<角色名>/attack.png   攻击
characters/<角色名>/hurt.png     受击
characters/<角色名>/dodge.png    闪避
```

## 只有一张普通立绘的角色

不用建目录，也不用凑齐四个差分，任选一种：

```
characters/<角色名>/idle.png     ← 放这一个，四个状态都用它
characters/<角色名>.png          ← 或者直接丢一个单文件，也认
```

## 规则

- **文件名必须是 `.png`**，<角色名> 与游戏里显示的颜名完全一致（例如 `李汐子`）。
- 建议**透明背景**，否则会盖住战斗背景。画布比例尽量保持一致，四态切换时人物才不会跳动。
- 访问地址：`https://cdn.jsdelivr.net/gh/Sh10na/csmg-battle-assets@main/characters/...`
  jsDelivr 对分支引用有约 12 小时缓存，想立刻生效就给仓库打个 tag 并改用 `@v2` 之类的引用。
- 优先级：界面里手动设置过的立绘 > 图床立绘 > 角色卡自带立绘 / 立绘库 > 内置默认素材。
  图床里没有的角色会自动落到后面的来源，不会白屏。
