# act1

```
SceneSetup.act1();
```

(...300)

n: 这位是人类的焦虑

n: _你_ 就是焦虑

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: 哦嘿！我们怎么又回来了？

`hong({eyes:"0_neutral"})`

n: 你的责任是保护人类不受到 *伤害*

`bb({eyes:"look", mouth:"small_lock"})`

n: 尤其是现在重玩这个游戏就非常的 *危险*

n: 快，警告他！

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: 人类！听好，我们有危险了！那个玩家...

[...又要再折磨我们了！](#act1_replay_torture)

[...不会找到另一个结局](#act1_replay_alternate)

[...会找到互相矛盾的对话！](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: 他会让我们缩成球大哭！
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: 他会让我们让你为给你带来焦虑的手机付出代价！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: 他会让我们 *不* 打开派对的！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: 他会让我们打同情我们的非反派一拳!
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: 虽然这次我们至少不会跳下屋顶--
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: *他会让我们跳下屋顶。*
{{/if}}

`bb({body:"fear"});`

b: 这些新的恐怖的事情都会发生，然后我们就会--

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: 对，故事 *基本上*，可是每一张都有两种结局，再加上他们都有不同的对话--

`bb({body:"fear"});`

b: 玩家会很失望，就会关掉浏览器，再删掉软件，然后我们就会--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: 互相什么？

`bb({eyes:"normal"});`

b: 故事想表达的是你可以 *选择* 怎么和你的恐惧建立良好的关系，
`bb({eyes:"normal_right"});`

b: 但是重玩游戏只会有一样的故事，这代表你的 *选择* 没有影响，

`bb({eyes:"narrow_eyebrow"});`

b: 然后就暴露了这个游戏在讯息和运作的矛盾，

`bb({eyes:"fear"});`

b: 这个故事宇宙的结构就会瓦解，

`bb({body:"fear"});`

b: 然后我们就会--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: 死！！！！！

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: 好了我们继续演吧。

```
Game.clearText();
```

n4: (让 _你的_ 焦虑吧啦吧啦 最像 _你的_ 焦虑吧啦吧啦你知道了的啦)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: 哦你看，我的狼回来了。实在太——————棒了。

`hong({eyes:"0_neutral"})`

n: 你的责任是保护人类不受到 *伤害*

`bb({eyes:"look", mouth:"small_lock"})`

n: 尤其是那个面包就非常的 *危险*

n: 快，警告他！

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: 人类！听好，我们有危险了！危险是……

`bb({body:"squeeze"})`

n4: (让 _你的_ 焦虑选择！选最像 _你_ 的恐惧的选择)

(#act1_normal_choice)

# act1_normal_choice

[我们又在孤零零的吃午餐了！](#act1a_alone) `bb({body:"squeeze_talk"})`

[我们吃午餐时没有产生价值！](#act1a_productive) `bb({body:"squeeze_talk"})`

[那个白面包有害！](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: 你知道孤独会减少的寿命跟一天抽15根烟一样多吗？-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: 呃，谢谢你提供的来源可是--

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: 这代表如果我们不 *马上* 和别人来往我们就会-

`bb({body:"panic"})`

b: 死！！！！！

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: 你使用了 *不被爱的恐惧*

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: 快点拿你的笔记本电脑做点什么啊！

`hong({eyes:"0_annoyed"})`

h: 可是我不想有面包屑在键盘--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 如果我们不为社会贡献我们就好比一个寄生虫！

b: 然后社会就会去想办法除掉寄生虫然后我们就会--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 死！！！！！

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: 你使用了 *成为坏人的恐惧*

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: 那些研究有被重现过--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 加工后的小麦会然我们高血糖！所以他们就得截掉四肢然后我们就会-

`bb({body:"panic"})`

b: 死！！！！！

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: 你使用了 *被伤害的恐惧*

(#act1b)

# act1b

n: 非常有效！

`bb({mouth:"smile", eyes:"smile"});`

b: 你看，人类！我就是你最忠诚的守护狼！

`bb({body:"pride_talk"});`

b: 相信你的直觉，你的感觉永远是对的！

`bb({body:"pride"});`

n: 让你人类的能力表降到零

n: 要确保他有 身体+社交+道德 上的需求，可以使用:

n: *被伤害* 的恐惧 #harm#

n: *不被爱* 的恐惧 #alone#

n: 以及 *成为坏人* 的恐惧 #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (提示: 选择那些最接近你内心的恐惧的对话！~)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: 嗯我觉得我看一下手机好了。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: 保护你的人类

n: 免受世界，其他人，他自己的伤害。

n: 祝你好运

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: 第一局: *FIGHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: 欸，脸书上写这个星期有派对。

`bb({eyes:"uncertain"});`

b: 那家伙不是 *每个* 星期都在开派对吗？

`bb({eyes:"uncertain_right"});`

b: 他们到底有多么空虚？他们内心深处一定亿团糟！

`hong({eyes:"surprise"});`

h: 而且，我也被邀请了？

`bb({eyes:"fear", mouth:"normal"});`

b: Well then!

[接受，不然我们会孤独到死！](#act1c_loner)

[拒绝，如果哪里有毒品的话怎么办！？](#act1c_drugs)

[无视，我们会毁掉派对的。](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: 一天十五根烟，人类！十五根。
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: 然后就没有人来我们的葬礼，他们会把我们的骨灰丢进海里, 我们被鲸鱼吃掉,
{{/if}}

{{if !_.fifteencigs}}
b: 然后我们就被消化成鲸鱼便便！
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: 所以我们应该去那场派对！
{{/if}}

{{if _.parasite}}
b: 不过记得带电脑去那工作，不然我们就是寄生虫。
{{/if}}

{{if _.whitebread}}
b: 只要他们没有白面包就好。
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: 天啊！好啦，你可以闭嘴了。

h: 我接受就是。

{{if _.whalepoop}}
b: 鲸鱼便便，人类！
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: 或者跟糟糕的……*白面包*
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: 我们会吸太多冰毒吃太多白面包直到我们进不了棺材！
{{/if}}

{{if !_.whitebread}}
b: 我们会吸太多毒品承办人会好奇我们怎么 *早就* 防腐了！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: 而且，派什么对，我们不工作的话就是社会的寄生虫！
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: 天啊！好啦，你可以闭嘴了。

h: 我拒绝就是。

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: 我们只会因为孤独和15根烟一样而哭在角落。
{{/if}}

{{if _.parasite}}
b: 我们在派对只会整天想着工作。
{{/if}}

{{if _.whitebread}}
b: 我们只会一直担心食物的危害性。
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: 呵，真奇怪啊。

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: 所以去派对他们会难过，不去他们也会难过！

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: *我们只会让他们伤心我们真是个大烂人*

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: 哎哟…… 好啦，你可以闭嘴了。

h: 我不管那个邀请了。

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: 算了， 脸书太够力了。我需要一些比较冷静，比较没有焦虑的。
`hong({eyes:"neutral"});`

h: 推特有什么？

`bb({eyes:"look"});`

[哦不，你看那个很惨的新闻！](#act1d_news)

[哦不，那一贴是在偷偷说 *我们* 吗？](#act1d_subtweet)

[嘿，一张猫喝牛奶的动图。](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: 天啊，感觉这个世界要毁灭了，对不对？

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: 感觉一切都快没了，我们每个人都要死了却无能为力。

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: 我们转发那个故事吧！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 好好好我转发就是了快给我闭嘴！

`hong({mouth:"neutral", eyes:"annoyed"});`

h: 不管了，我看看 Snapchat有什么。

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: 那是个子网！鬼鬼祟祟的子网。

`hong({eyes:"annoyed"});`

h: 怎么可能？

`bb({eyes:"narrow", mouth:"small"});`

b: 可是他们会不会在我们背后说坏话

h: 他们没--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: 在我们背后的前面！

`hong({eyes:"sad", mouth:"sad"});`

h: 我觉--

`bb({eyes:"narrow", mouth:"small"});`

b: 但是 *假如*

h: 但--

`bb({eyes:"narrow_eyebrow"});`

b: *如果……*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 好————， 我去看 Snapchat。

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: 好可爱啊，我转发一下，我觉--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: 猫是不能消化牛奶的我们竟然在享受虐待动物我们真坏！！

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 好————， 我去看 Snapchat。

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: 欸，这是昨天派对的照片。原来是 *这* 样的啊。

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: 哇，人真的多到我的焦虑会受不了。

h: 我不应该接受邀请的。

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[改变注意？那么坏？](#act1e_yes_dontchange)

[改变主意！太多人了！](#act1e_yes_changetono)

{{if _.subtweet}}
[他们果然是在偷偷讲我们。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[我们刚刚是不是还没验证就转发了？](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[你坐着的姿势很不好你知道吗？](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 他们这么期待我们的来临而我们现在要背叛他们？你想一个人死吗？

{{if _.fifteencigs}}
b: 十五。根烟。
{{/if}}

{{if _.whalepoop}}
b: 鲸鱼。便便。
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 够了够了我不会改的啦！

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 你提供过人类踩踏事故吗？

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 在2003年，罗得岛州有一间夜店着火了 全部人都挤在出口 结果100个人伤亡了。

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 你要那种事发生在我们吗！！-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: 拒绝拒绝拒绝拒绝拒绝拒绝拒绝拒绝拒绝-


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 够了够了我不会改的啦！靠！
(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: 嗯……好像很好玩。

h: 我不应该拒绝邀请的。

`bb({mouth:"normal", eyes:"normal"});`

[改变注意？那么坏？](#act1e_no_dontchange)

[改变注意！我们不想孤独到死！](#act1e_no_changetoyes)

{{if _.subtweet}}
[他们果然是在偷偷讲我们。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[我们刚刚是不是还没验证就转发了？](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[你坐着的姿势很不好你知道吗？](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: 他们都很指望我们！

b: ……不去干扰他们也不让他们看见你这个 {{if _.whitebread}}吃白面包的{{/if}} 怪胎--


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 够了够了我不会改的啦！

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 长期孤独会让我们的皮质醇更高 我们也更容易中风根有心血管的疾病！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: 十五。根烟。
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 够了够了我改成接受就对了！靠！
(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 我们那堆问题推文又回来捅我们一刀了！

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: 他们会毁掉我们的名声然后就再也没有人敢来跟我们说话了！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 你为什么要这样！

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 我们在传假新闻！我们在破坏对新闻自由的信任！

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 我们就是法西斯主义会从民主的废墟中出现的罪魁祸首！

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: 你为什么要这样！

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 你想要掰弯你的脊椎骨吗！？别再低头看手机了！

```
bb({body:"meta"});
```

b: 你也是。

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 你为什么要这样！

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: 嗯……好像很好玩。

h: 我不应该无视邀请的。

`bb({mouth:"normal", eyes:"normal"});`

[继续无视，我们还是会毁掉派对。](#act1e_ignore_continue)

[接受吧。](#act1e_ignore_changetoyes)

[拒绝吧。](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: 你不觉得不回应他们很没礼貌吗？

`bb({eyes:"normal_right"});`

b: 反正他们也一直无视 *我们*，所以

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: 我觉得很公平。

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: 你……要我去享受？

b: 呃，因为……孤独*可以*搞死我们。

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: 太多人了。 很多人=危险。

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 管他的，Tinder 有通知。

`bb({eyes:"uncertain"})`

b: 啥，那个约炮app？

`hong({eyes:"annoyed"})`

h: 这个不是约炮app啦，我只是用来认识新朋--

`bb({eyes:"narrow"})`

b: 它就是个约炮app。

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: 噢，找到配对了！长相不错！

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: 我拜托你别搞砸--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: *危险 危险 危险 危险 危险 危险 危险*

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[我们在 *被别人利用*。](#act1f_used_by_others)

[我们在 *利用别人*。](#act1f_using_others)

[*你的配对是连环杀人犯！*](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: 或许约炮可以填下面那个洞，

b: 但他们永远不可能填……

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: *这个* 洞.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 重点是*我们会孤独到死。*

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: 你以为别人的生殖器官是可以手机的精灵宝贝吗?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (宝可梦主题曲)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ 我要成为，最 ^变态^的-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ 无人能比的-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ 大腿 ^屁屁^, 性感大奶-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ 多汗的 ^屌^ 和蛋！-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ 变态-梦! 我要抓-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 重点是我们是控制狂。
```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: 他会把你困在水井里逼你吃白面包直到你肥到他们把你的皮当衣服穿！
{{/if}}

{{if _.parasite}}
b: 他们把你绑在一个定时炸弹然后说 "你应该更有贡献的你这个寄生虫"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: 他们会把你的肉撕成五彩纸屑，把你的内脏变成彩带，把你的血混合成潘趣酒！
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: *那*一种派对邀请怎么说？！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: 我受不了这个游戏了。
(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"孤独会杀死我们"... {{/if}}
{{if _.parasite}}"我们是社会的寄生虫"... {{/if}}
{{if _.whitebread}}"不要吃，会死的"... {{/if}}
{{if _.subtweet}}"他在背后说坏话"... {{/if}}
{{if _.badnews}}"世界要毁灭了"... {{/if}}
{{if _.hookuphole}}"我们会孤零零的死"... {{/if}}
{{if _.serialkiller}}"他是连环杀人犯"... {{/if}}
{{if _.catmilk}}"猫不能消化牛奶"... {{/if}}
{{if _.pokemon}}那个 ^垃圾的^ 歌词改篇... {{/if}}

h: 我只想好好的活下去。

h: 我只想要在这种痛苦中……获得自由。

`bb({eyes:"look_sad"});`

b: 嘿……人类……

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: 会没事的。
(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: 身为你忠诚的守护狼，我会一直注意危险，确保你的安全。

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: 我保证。

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: 最后一个。 Instagram。有什么东西？

`hong({eyes:"sad"});`

h: 这是……更多派对的照片

`hong({mouth:"sad"});`

h: 大家看起来都好开心。没有担心。没有焦虑。

`hong({mouth:"anger"});`

h: 老天，为什么我就不能向他们一样？为什么我就不能 *正常* 一点？

`bb({eyes:"normal_right"});`

b: 说到派对，关于这星期的派对，我的最终决定是……

`bb({eyes:"normal"});`

[我们去吧。](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[我们别去。](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: 我们--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^FUCK^.*

`hong({body:"2_you"});`

h: YOU.

(...500)

b: 什

(...1500)

`bb({eyes:"wat_2"});`

b: 什么？
`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: 我会接受那个派对的邀请，

{{if _.act1g=="go"}}
h: 不是因为你要我去，而是因为*我*要去。
{{/if}}

{{if _.act1g=="dont"}}
h: 就是因为*你*不要我去。
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: *你不能操控我。*

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: 现在请^TM^让我安静一个人吃我的三明治。

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[啊啊啊我们要死了](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[啊啊啊大家讨厌我们](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[啊啊啊我们太坏了](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: 啊啊啊我们要死了 啊啊啊啊啊

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: 啊啊啊大家讨厌我们 啊啊啊啊啊

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: 啊啊啊我们太坏了 啊啊啊啊啊

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: 恭喜你

(...500)

n: 你成功的确保了你人类的 身体+社交+道德需求

n: 你看他多么感激你啊！

(...500)

n: 现在他们的能量条降到零了，你可以直接操控他们

`bb({mouth:"smile", eyes:"normal"});`

n: 选择你的结束方法

`bb({mouth:"small_lock", eyes:"fear"});`

n: *结束他*

[{战斗: 惩罚你的手机！}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{自卫: 缩成球哭起来！}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: 你的手机给你造成了很多焦虑！

`bb({eyes:"anger"})`

b: 扎克伯格和他的公司正在为风险资本家的钱劫持你的心理健康！
```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 惩罚你的手机！摧毁掉它！杀了它！

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: 杀了它杀了它杀了它杀了它杀了它杀了它杀了它杀了它杀了它--

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: 这个世界太危险了！

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 缩成球自卫！像穿山甲一样！

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: 缩成球哭缩成球哭缩成球哭缩成球哭缩成球哭缩成球哭缩成球哭缩成球哭-- 

(#act1j)

# act1j

`SceneSetup.act1_outro()`
