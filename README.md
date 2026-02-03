# GodForsaken Modding 示例

_《神弃之地》的 mod 示例说明。


## 工作原理概述

《神弃之地》的 Mod 系统会自动扫描并读取 GodForsaken_Data/StreamingAssets/Mod 文件夹，以及从 Steam 创意工坊中订阅的物品文件夹。当扫描发现这些文件夹中包含有特定的 xml 文件、info.ini 和 preview.png 文件，并在游戏的 Mods 菜单中管理并加载 mod。游戏暂时仅提供配置修改功能，资源及代码文件暂不支持开放。

游戏会读取 mod 文件夹的所有 xml 文件并覆写游戏的默认配置。
注意：xml 文件中的原配置项不要随意删除，否则可能导致游戏崩溃。
Mod制作和应用前请备份AppData\LocalLow\InsightStudio\GodForsakenRelease\game_save下的所有存档文件。

## 配置文件制作概述
使用Office的Excel打开官方提供的配置文件，修改/新增并导出xml 文件

 - 使用Excel时需要先打开开发工具选项（选项→自定义功能区→开发工具）
 - 修改或新增配置内容后通过开发工具→导出来导出 xml 文件
 - 导出的xml文件命名为excel表内左上角备注命名如:spell.xml

## Mod 文件夹结构

将准备好的 Mod 文件夹放到《神弃之地》本体的 GodForsaken_Data/StreamingAssets/Mods 中，即可在游戏主界面的 Mods 界面加载该 Mod。
以上面的 “ConfigMod” 为例，发布的文件结构应该如下：

  - ConfigMod（mod 的文件夹）
  - spell.xml（mod的自定义覆写的配置）
  - info.ini（重要，mod的配置文件）
  - preview.png（正方形的预览图，建议分辨率 `256*256`）

[Mod 文件夹示例](ReleaseExample/ConfigMod/)

### info.ini 格式

本配置文件应包含以下参数（不建议存放其他的额外数据）：

- name（mod 名称，主要用于加载 dll 文件。详情见上面的 _规则一_）
- displayName（显示的名称）
- description（显示的描述）
- publishedFileId（本 Mod 在 steam 创意工坊的 id）

**注意：在上传 Steam Workshop 的时候会覆写 info.ini。请不要在 info.ini 中存储除以上项目之外的任何信息。

## 神弃之地社区准则

为了神弃之地社区的长期健康与和谐发展，我们需要共同维护良好的创作环境。 因此，我们希望大家遵守以下规则：

1. 禁止利用 Mod 引导至广告、募捐等商业或非官方性质的外部链接，或引导他人付费的行为。
2. 禁止违反开发组以及 Steam平台所在地区法律的内容，禁止涉及政治、散布淫秽色情、宣扬暴力恐怖的内容。
3. 禁止对玩家正常游戏流程、存档安全或社区秩序存在损害的行为，或其他形式的恶意代码。
4. 禁止严重侮辱角色或者扭曲剧情、意图在玩家社群内容引起反感和制造对立的内容，或者涉及到热门时事与现实人物等容易引发现实争议的内容。
5. 禁止未经授权，使用受版权保护的游戏资源或其他第三方素材的内容。

对于在 Steam创意工坊发布的 Mod，如果违反上述规则，我们可能会在不事先通知的情况下直接删除，并可能封禁相关创作者的权限。
