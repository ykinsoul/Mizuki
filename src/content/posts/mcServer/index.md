---
title: FTAS服务器更新日志
published: 2026-07-30
pinned: true
description: 随缘更新
tags: [MCServer]
category: updateLog
author: 河动力牛马
draft: false
---

# FTAS服务器我也不知道第几周目更新日志

---

## 2026/08/14 更新

依旧生活质量更新：

- 再一次，更新了 [机械动力：附魔工业](https://www.mcmod.cn/class/7892.html) Mod；
  - 现在，附魔模板和超越附魔模板会显示其包含的附魔魔咒了。
- 调整了 [Collector's Reap](https://www.mcmod.cn/class/8808.html) Mod；
  - 之前未汉化的部分已添加汉化，让我们说中文！
    - 是的，这个 Mod 甚至没有一个官方译名。
  - 现在，青柠树和石榴树<b><span style="color:red;">不再</span></b>需要蜜蜂授粉，即可结果了。
- 调整了 [机械动力：喷气背包](https://www.mcmod.cn/class/7338.html) Mod。
  - 现在，喷气背包悬浮模式下<b><span style="color:red;">不再</span></b>缓慢下落了。

:::grid{columns="1"}
![你在等什么，每次结尾都会有的表情包吗？](/images/mcServer/meiyou.jpg)
:::

---

## 2026/08/12 更新

本次更新仍为生活质量更新，无实际新增内容，修复了一些 Bug，并尝试改善游戏体验：

- 新增与更新内容：
  - 更新了 [机械动力：附魔工业](https://www.mcmod.cn/class/7892.html) Mod 及其前置 Mod：[机械动力：龙+](https://www.mcmod.cn/class/19299.html);
    - 现在，锻造模板的名字恢复正常显示了。
  - 终于更新了 [TrueUUID](https://www.mcmod.cn/class/21953.html)，可喜可贺可喜可贺；
    - <del>我们还没有实际测试过，因为有问题的玩家暂时都不在线。</del>
    - <del>不过，据 issue 内其他有相同问题的用户反馈，新版本已解决问题。耶拉冈德与欧姆弥赛亚在上，可千万别再出什么乱子了。</del>问题终于解决了，真他民主的爽！
  - 加入了 [Blueprint Texture Issue Fix](https://www.mcmod.cn/class/17831.html) Mod 和 [Constancy](https://www.mcmod.cn/class/25474.html) Mod。
    - 这两个 Mod 有什么用，请见下文。
      <br>
- 移除内容：
  - 移除了 [Collective](https://www.mcmod.cn/class/2652.html) Mod；
    - 这个 Mod 是一个依赖库，本身不具备任何功能，经过检查发现我们目前使用的 Mod 并未依赖此库，故而删除。
  - 移除了 [信雅互联](https://www.mcmod.cn/class/11627.html)、[Continuity](https://www.mcmod.cn/class/4906.html)、和 [Forgified Fabric API](https://www.mcmod.cn/class/11464.html) Mod。
    - 同上，移除原因请见下文。
      <br>

为什么要删除这些 Mod？新增的 Mod 又有什么用？
我要告诉你一些事情...请仔细听好，保持镇静...<br>
<b>Minecraft 原版中的玻璃，从来都不会自动连接材质，它们本来应该长这个样子：</b>
:::grid{columns="2"}
![玻璃原本的样子，不难注意到玻璃方块之间是有边框的](/images/mcServer/originalGlass.jpg)
![我们看到的玻璃，同色玻璃之间不再有边框](/images/mcServer/newGlass.webp)
:::
那么，为什么会有这样的区别呢？<br>
在 Minecraft 低版本的时代，想必都听说过 `高清修复(OptiFine)` ，它的主要功能是为 Minecraft 提供光影支持、更详细的画面设置、增加高清纹理和自定义纹理支持等等，其中就包括<b>为玻璃加入自动连接材质</b>功能。<br>
然而，随着时间流逝<del>史山堆积</del>，高清修复已不再能满足玩家们的需求，其愈发臃肿的体量也对游戏性能造成了负面影响。在这一背景下，以 [钠](https://www.mcmod.cn/class/2785.html) 为代表的全新渲染模组逐渐取代了高清修复的地位。但钠并不具备自动连接玻璃材质的功能，因此需要 [Continuity](https://www.mcmod.cn/class/4906.html) 这种 Mod 来让玻璃再次连接。<br>
不过，Continuity 仅支持 Fabric 模组加载器，而我们所使用的是 Forge 模组加载器，二者的 Mod 并不互通。为此，就需要使用 [信雅互联](https://www.mcmod.cn/class/11627.html) 和 [Forgified Fabric API](https://www.mcmod.cn/class/11464.html) 来让 Fabric 的模组可以在 Forge 上运行。此举势必造成一定性能和稳定性影响，但也别无他法。直至 [Constancy](https://www.mcmod.cn/class/25474.html) 出现了，它其实是上文提到的 Continuity 的一个分支，但它可以在 Forge 加载器上原生运行，这意味着我们可以摆脱掉 Fabric 带来的一系列沉重包袱了。<b>经体感测试，删除这几个模组后游戏加载速度又得到了大幅提升。</b><br>
与此同时一并加入的 [Blueprint Texture Issue Fix](https://www.mcmod.cn/class/17831.html) 则修复了一个玻璃有时无法连接纹理的 Bug，现在，玻璃可以完美互相连接而不必保留边框了。<br>
:::grid{columns="1"}
![如何快速理解模组加载器之间的区别](/images/mcServer/forge.png)
:::

---

## 2026/08/11 更新

本次更新内容主要为玩法方面拓展，增强挑战性，并修复了一些存在的 Bug：<br>

- 新增与更新内容：
  - 加入了 [机械动力](https://www.mcmod.cn/class/2021.html) Mod 的附属 Mod： [机械动力：创想附加](https://www.mcmod.cn/class/3437.html) 与 [机械动力：物品附加](https://www.mcmod.cn/class/3779.html)；
    - 创想附加新增了与沉浸工程联动的元件，可实现应力与FE之间的转换；物品附加则新增了一些工具。
      <br/>
  - 加入了 <del>恐虐</del>[冠军/强敌再续](https://www.mcmod.cn/class/15862.html) Mod;
    - 现在，怪物刷新时有一定概率生成为精英怪，具有更强的属性和特殊能力。
      <br>
  - 加入了 [永恒之门](https://www.mcmod.cn/class/7522.html) Mod，及其前置 Mod：[Apothic Attributes](https://www.mcmod.cn/class/12036.html) 和 [Placebo](https://www.mcmod.cn/class/1023.html)。
    - 永恒之门 Mod 允许合成生成大量怪物的传送门，完成挑战并获取奖励。
    - 也包含一个无尽挑战传送门。
    - <b>原 Mod 的汉化并不完全，因此本次更新亦附带了一个补充汉化资源包，使用方式请见下文。</b>
      <br>
  - 更新了 [机械动力：附魔工业](https://www.mcmod.cn/class/7892.html) Mod。
    - 修复了烈焰人锻造台不接受装备作为附魔模板的 Bug。
      <br>
- <b>汉化资源包使用方法</b>
  1. 资源包会随着更新自动下载，只需启动游戏。
  2. 在主菜单界面，点击`选项`-`资源包...`。
  3. 在资源包界面找到`GatewaysToEternity-1.20.1-4.2.6补充汉化...`，将鼠标移至其左侧的蓝色 logo 上，可见一个向右的箭头，点击该箭头，确保补充包被移动至`已选`列表中。
  4. 点击完成即可。
     :::grid{columns="4"}
     ![点击左侧的“选项”按钮](/images/mcServer/tutorial/1.png)

     ![然后点击“资源包...”](/images/mcServer/tutorial/2.png)

     ![将滑鼠移动至该资源包的logo之上，单击箭头](/images/mcServer/tutorial/3.png)

     ![确保其在“已选”列表中，大功告成！可以游玩伺服器了](/images/mcServer/tutorial/4.png)
     :::

    <br>

  今日晚间或许还会有一次更新，`TrueUUID` 的作者已初步完成 Bug 修复，目前尚在测试中，暂未发布新版本，等待，并心怀希望吧。
  :::grid{columns="1" aspect="1/1"}

  ![等待作者更新的我 be like:](/images/mcServer/kuaisu.jpg)

  :::

---

## 2026/08/10 更新

本次更新主题为生活质量更新，旨在通过更新已安装 Mod 版本修复一些旧有 Bug，同时优化加载速度：<br>

- 修复 Bug 更新列表：
  - [超越维度](https://www.mcmod.cn/class/19045.html)
  - [FTB 连锁破坏](https://www.mcmod.cn/class/3004.html)
  - [沉浸式奏乐](https://www.mcmod.cn/class/11850.html)
  - [精妙背包](https://www.mcmod.cn/class/3739.html)及其前置 Mod [精妙核心](https://www.mcmod.cn/class/6324.html)
  - 以上 Mod 在新版本中修复的 Bug 我们未必触发过，但既然作者修了我们就顺手更一下（  
    <br>
- 增加新特性的已安装 Mod：
  - [机械动力：附魔工业](https://www.mcmod.cn/class/7892.html)
    - 该 Mod 的更新幅度较大，具体更新内容请见[这里](https://www.mcmod.cn/post/5420.html)。
      <br>
- 新增 Mod：
  - [LightSpeedRe](https://www.mcmod.cn/class/23346.html)
    - 该 Mod 极大幅度地加快了游戏加载速度，现在进游戏的加载体验更加丝滑了。
  - [机械动力：龙+](https://www.mcmod.cn/class/19299.html)
    - 该 Mod 为 机械动力：附魔工业 新版本的前置 Mod，但也包含一些实际功能：
      - 例如：新增各色燃料的液体形态，并且这些液体接触到岩浆会变为对应颜色的混凝土方块；
      - 鼓风机可以通过液态染料方块、细雪方块、液态龙息或龙首、流沙为物品进行染色、冷冻、终结、喷砂等加工处理；
      - 增加了流体舱口，可直接向流体容器手动存取流体。
  - [通用拼音搜索](https://www.mcmod.cn/class/840.html)
    - 现在可以在 JEI 界面里直接用简拼甚至全拼搜索物品了，耶！
      - 顺带一提，其实超越维度（也就是云盘）界面一直都是支持这个功能的。
        <br>
- 不知道更新了什么的：
  - [森罗酒馆：世界名酒](https://www.mcmod.cn/class/25477.html)
    - 为什么说不知道更新了什么呢，因为作者更新并没有写更新日志，甚至 Github 上也没有体现，不过还是那句话，既然作者更了我们也顺手更一下（
      <br>
- 改善性更新：
  - 经过民主训练营的奖励性惩罚式再教育，现在，酒狐们不会在<b>工作中</b>偷吃背包里的[烘焙坊](https://www.mcmod.cn/class/18100.html) Mod 食物了；
    - 不过，经过批准，酒狐们依然会在摸鱼时和需要回血时享用这些美味的面包。
  - 对于没有装备披风的玩家，其背后不会再显示黄色一串英文的申必披风了。

<br>另外，还有一个好消息：`TrueUUID` 的作者已对 issue 作出反馈，不出意外的话，近期应该就可以让正版软件受害者们解脱了...吧？
![求放过](/images/mcServer/qiufangguo.jpg)

---

## 2026/08/08 更新

依旧小更新：

- 加入了 [永无止境：载具](https://www.mcmod.cn/class/24495.html) Mod 的附属包：[龙之崛起](https://www.curseforge.com/minecraft/customization/limitless-vehicle-dragonrise)。
  - 该整合包大部分内容仍处于开发状态中，仅数辆载具可实际合成。
  - 好消息是，开发中载具已有模型，可由创造模式调出，似乎也能正常驾驶。
  - 坏消息是，这个载具 Mod 的所有附属都加上了（是的，就 2 个），让我们默哀一普朗克时间。
    <br>
- 更新了 [永恒枪械工坊：零（TAC:Z)](https://www.mcmod.cn/class/14980.html) Mod 的附属包： [42 Labs](https://www.bilibili.com/video/BV1dGuJ6MEsZ) 。
  - 为大狗新增了几个弱智配件，更适合 FTAS 的平均智商！
    - 尽管官方在新版本为大狗新增了合成途径，但鉴于狼刷怪蛋在生存模式无法获得，故合成公式仍沿用先前手搓的自研合成配方。
  - 其余更新内容请见视频，反正也不是饺子醋。
    - 你知道吗，蓝字都是可以点的，视频链接就在其中。
      <br>
- 没了。又混完一期更新，耶！

---

## 2026/08/07 更新

_"早上好夜之城！昨天的 UUID 乐透，最后结果是满打满算的整整三十个！..."_

本次更新带来了全新载具<del>和更多的键位冲突灾难</del>：

- 加入了 [永无止境：载具](https://www.mcmod.cn/class/24495.html) Mod 及其附属包：[TankAssault](https://www.curseforge.com/minecraft/customization/limitless-vehicle-tankassault)。

- 没了。

:::grid{columns="2" aspect="1/1"}
![总而言之先放四包神秘零食在这](/images/mcServer/greenGuaiguai.jpg)

![然后赞美万机之神欧姆弥赛亚](/images/mcServer/guaiguai.gif)
:::

---

## 2026/08/06 回滚

服务器存档已回滚至 <code>2026/08/05 05:01 AM</code> 状态，由此带来的损失肥肠煲芡，，，<br>
<del>尽管只有我和日本人受到了损失</del><br>
本次回滚起因为 <code>2026/08/04 约 09:00 PM</code> 时，未知原因导致 <code>TrueUUID</code> Mod 无法正常处理登陆请求，造成线程堵塞进而造成服务器持续崩溃。当时第一时间处理方案为更新 <code>TrueUUID</code> Mod 至最新的 `V1.2.0`版本。<br>
该 Mod 更新之后，线程堵塞问题确已解决，然而`该名称已绑定正版 UUID，鉴权失败时不允许以离线模式进入。请检查网络后重试。` 问题更加严重，<del>唯三的</del>正版<del>受害者</del>用户几乎无法正常登入服务器。<br>
为解决此问题，尝试在互联网搜索相关内容后得知，`TrueUUID V1.1.2` 版本相比最新版本似乎更为稳定，可缓解上述鉴权失败问题。然而，在更换 `TrueUUID V1.1.2`后，鉴权失败问题仍然存在。<br>
安装`TureUUID` 的初衷是考虑到服务器玩家并非全部使用正版账户，因此服务器需要关闭正版验证，但关闭正版验证将面临扫端口 bot 的恶意攻击潜在危险。为了安全起见，安装了 `TrueUUID` 来防范未经许可的登入。然而，在鉴权失败问题频发后，我们选择两害相权取其轻，承担遭受攻击的潜在风险来保障正版玩家的游戏体验。故后续尝试彻底删除 `TrueUUID` 。<br>
哭笑不得的是，在 `2026/08/05 10:00 PM` 彻底删除 `TrueUUID` 之后，所有用户的UUID（唯一身份凭证）均发生改变，导致所有玩家变成空白新号。尽管仍可以通过手动迁移 `playerdata` 文件夹内数据的方式恢复玩家数据，但由于该操作需要玩家首先登陆一次获取新UUID后才可针对性迁移，我们认为可行性不高，故再次安装 `TrueUUID` ,并修改其配置文件，将其行为修改为鉴权失败的正版账户仍可以离线账户登入服务器。<br>
而后进一步出现问题，该操作实际使得所有用户，毋论正版账户、皮肤站账户亦或离线账户均出现了 UUID 混乱情况，玩家数据仍然丢失。但在该时间段，仅有正版账户用户在线，且配置文件的行为修改亦仅针对正版账户，我们当时认为离线账户和皮肤站账户没有受到影响。为尽可能减小混乱，我们选择了手动迁移正版账户的数据。<br>
然而在 `2026/08/06` 问题再次爆发，我们发现连离线账户和皮肤站账户也受到了此次 UUID 混乱影响，出现了鉴权失败问题。为遏制混乱，彻底平息风波，我们不得已将服务器数据回滚至 `2026/08/05 05:01 AM`。目前服务器已恢复平稳运行，皮肤站用户和离线用户应该可以正常游玩，仅正版用户的鉴权失败问题仍然存在，我们已向 `TrueUUID` 的作者提交了 issue，期望尽快修复这一问题。<br>
针对此次风波，我们得到的唯一心得是，<span style="color:red;font-size:30px">永远不要再安装 TrueUUID 了</span><br>
:::grid{columns="1" aspect="1/1"}
![红豆泥私密马赛](/images/mcServer/ketou.gif)
:::

---

## 2026/08/05 更新

本次依然是小更新：

- 加入了刷新交易 Mod。
  - 现在，无需再反复拆放村民交易方块，可以用快捷键快速刷新村民交易了。（默认 `T` 键，可在设置中调整）
    - 使用快捷键刷新交易时，若交易刷出JEI界面内鼠标指着的物品，则交易项不会被再次刷新，可利用此功能快速刷新自己所需交易项。
    - 原版机制仍然存在，**已交易过的村民不可被刷新交易项**。
  - 附魔书的详情栏现在会显示该附魔是否可从附魔台/交易中获取。
  - <del>我才不会说加这个 Mod 的起因是我刷荆棘III刷破防了</del>

---

## 2026/08/04 更新

不知道是微软服务器炸了还是登陆 Mod 用的端口炸了，总之不得不更新。

- 更新了 TrueUUID Mod，以修复线程堵塞导致炸服的问题。
  - <del>尽管炸服修好了，但对于正版玩家来说，可能会导致更频繁地出现`该名称已绑定正版 UUID，鉴权失败时不允许以离线模式进入。请检查网络后重试。`问题，该问题是由沟槽的微软服务器导致的，您可能是正版软件受害者（摊手）。对于这种情况，只能反复尝试进入服务器解决，或许使用加速服务会有所改善？</del><br>似乎微软服务器修好了，我们安全了，暂时。
    <br>

:::grid{columns="2" aspect="1/1"}
![修炸服我就这样](/images/mcServer/guaiguai.jpg)

![骗你的没这么慢](/images/mcServer/guaiguai.gif)
:::

---

## 2026/07/31 更新

<del>不出意外这应该是本月最后一次更新</del>

- 更新了 [绝地潜兵2枪包](https://www.curseforge.com/minecraft/customization/tacz-helldivers-escalation-of-freedom)；
  - 武器追加：

    > 国防部已经批准，为绝地潜兵新增一批全新武器:
    >
    > - MGX-42子弹风暴，
    > - EAT-411荡平者，
    > - DBS-2双重自由，
    > - SG-97扫荡者，
    > - flam-66火炬手
    > - TED-63炸药
    > - G-12高爆手雷
    > - G-48千兆级榴弹
    > - G-23眩晕弹
    > - 以及K-2飞刀！

  - 此外，佩玛丘拉™为在异乡的绝地潜兵提供了治疗针！

  - 机制更新：

    > - 科学部重置了一部分蓄力式武器的机制，使其与原世界的武器效果相符....
    > - 追加了flam-66,ar-2和plas-1，plas-101的特殊配件

  - 武器改动：
    > - P-4参议员，P-113裁决的全自动模式已被移除，它们是科学部用来测试的:(
    > - plas-101的全自动模式被移除，改为sup-8回响配件作为特色；
    > - 为las-5长柄镰，las-16镰刀，las-98激光大炮增加了充能开火系统，现在开火需要充能；
    > - 为m1000添加了开火充能；
    > - 为变数全弹发射模式添加了自我伤害功能；
    > - 现在，法令手枪在锁定模式下未识别到目标无法开火，当且仅当有目标时才会允许射击，避免弹药浪费。

<br>

- 加入了 [绿葡萄战术工坊](https://www.curseforge.com/minecraft/mc-mods/tacz-lesraisins-tactical-equipements)枪包及其附属，[42LABs](https://www.bilibili.com/video/BV19b376iEHS)；
  - 加入这两个附属枪包主要是为绝地潜兵2的枪包服务，有一些特性不可避免地使用到了它们。
  - 这些枪包本身也加入了一些新物品。
    - 当然，还有一把整活很好用的武器，欢迎探索(
      <br>
- 加入了 [烘焙坊](https://www.mcmod.cn/class/18100.html) Mod 及其附属的 [女仆的烘焙坊](https://www.mcmod.cn/class/21890.html) Mod；
  - 现在可以烘焙大量面包、蛋糕、甜品和饮品了，游戏内有专门的书籍介绍烘焙教程。
  - 聪明的读者看到附属 Mod 的名字应该就猜到了，女仆现在也可以做烘焙啦！
    <br>
- 加入了 [沉浸式奏乐](https://www.mcmod.cn/class/11850.html) Mod，现在可以在MC里用乐器演奏木柜子乐曲了（捏鼻
  :::grid{columns="1" aspect="1/1"}
  ![真正的音乐！](/images/mcServer/trueMusic.jpg)
  :::

---

## 2026/07/30 更新

- 整合了之前的版本更新内容；
- 现在整合包支持自动在线更新了，**不再需要每次从群文件更新**，好耶！
  - _更新服务器有效期三个月，到期了再想办法（_
  - 因为找到了无痛更新的方法，后续更新可能会频繁一些了。
    （求你们了快回来玩吧）
    <br>
- 加入了机械动力：附魔工业 Mod；
  - 现在，机械动力的机械手可以正常使用经验修补的工具击杀生物并用掉落的经验修复手中的工具了。
    - 多余的经验会变成经验块掉落。
      <br>
- 加入了展示乐事 Mod。
  - 几乎所有农夫乐事及附属 Mod 的食物都可以放进新增的餐盘中以 3D 模型展示。
    - 对于我们没加的附属 Mod 食物，流浪商人也会卖，但只能看不能吃。
      - 如果有心仪的附属 Mod 想加大大方方反馈，反正现在无痛更新了。

---
