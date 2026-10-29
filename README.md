# Dynamic Key Prompts 0.1.4 — Dark Souls III 1.15.0

Shows the **keyboard / mouse key you actually bound** instead of the gamepad button in prompts.

An unofficial port of Dynamic Key Prompts 0.1.4 to the 1.15.0 executable: upstream version 0.1.4, rebuilt for game version 1.15.0. **1.15.0 only.**

The install-ready build is in **Releases** ([`DynamicKeyPrompts-0.1.4-ds3-1.15.0.zip`](../../releases/latest)); this repository holds the description and the licences.

## Install

Download `DynamicKeyPrompts-0.1.4-ds3-1.15.0.zip` from Releases, extract it, then copy both items next to `DarkSoulsIII.exe` (`...\DARK SOULS III\Game\`), and start the game from Steam:

```
Game\xinput1_3.dll
Game\DynamicKeyPrompts\DynamicKeyPrompts.dll
Game\DynamicKeyPrompts\DynamicKeyPrompts.ini
```

**Uninstall:** delete `xinput1_3.dll` and the `DynamicKeyPrompts` folder.
If another mod already occupies `xinput1_3.dll`, the two cannot be installed together.

## Settings

`DynamicKeyPrompts\DynamicKeyPrompts.ini`:

| Key | Values |
|---|---|
| `Enabled` | `0` = the mod does nothing |
| `Style` | `text` = key names as text, e.g. `[E]` · `icons` = key icons (cached in `DynamicKeyPrompts\cache\ds3`) |
| `IconTheme` | icon look: `dark` / `minimal` / `silver` |
| `Labels` | when an action has both a key and a mouse button: `auto` / `keyboard` / `mouse` / `both` |
| `Format` | text only; `{0}` is the key name, e.g. `[{0}]` → `[E]` |
| `Separator` | between the keys of a stick / d-pad prompt |
| `Color` | key label colour `RRGGBB`, empty = normal text colour |
| `Diagnostics` | `1` = more detailed `DynamicKeyPrompts.log` |

## About this port

Two changes to 0.1.4: the loader detects the 1.15.0 executable and skips the upstream entry-point blocking (it used 1.15.2 addresses and crashed 1.15.0); and the keycap atlas moved to the always-loaded `menu/01_common.tpf.dcx`, so the centred prompt ("Rest at bonfire", "Talk") shows the keycap too.

## Credits

Dynamic Key Prompts 0.1.4 by HappyEntity — MIT, see [LICENSE](LICENSE). MinHook and the Hacker Disassembler Engine are BSD 2-Clause — see [LICENSE-MinHook.txt](LICENSE-MinHook.txt). This port is unofficial and not affiliated with the author.

## 中文

把提示里的手柄按键换成你实际绑定的键鼠按键。这是 Dynamic Key Prompts 0.1.4 针对《黑暗之魂3》1.15.0 重新编译的版本，**仅支持 1.15.0**。

安装：从 Releases 下载 `DynamicKeyPrompts-0.1.4-ds3-1.15.0.zip` 解压，把 `xinput1_3.dll` 和 `DynamicKeyPrompts` 文件夹放进 `...\DARK SOULS III\Game\`（与 `DarkSoulsIII.exe` 同级），从 Steam 正常启动即可。卸载就是删掉这两样。若别的 mod 已占用 `xinput1_3.dll`，两者不能共存。

设置看 `DynamicKeyPrompts\DynamicKeyPrompts.ini`：`Style=text` 显示 `[E]` 这样的文字，`icons` 显示按键图标；`Labels` 控制同时有键鼠绑定时显示哪一个；`Color` 是文字颜色。

代码与美术版权归原作者 HappyEntity（MIT）。
