# FC25

## 游戏设置

### AI滑块

射门失误：`1/99`

传球失误：`1/99`

门将：`50/99`

盯人：`1/99`

触球：`1/99`

### AI战术

逼抢：`99`

花式：`1`

### 镜头

视角：`合作`

高度：`20`

其余：`0`

大力射门放大：`关`

## 改年龄

1. 导出player.txt

2. 找到：BF列  `birthdate`

3. 改成：`155135`  （亚马尔的年龄）

亚马尔 id：`277643`

## 改鞋（ 解决黑白鞋问题）

1. 导出player.txt

2. 找到：BE列  `shoetypecode`

3. 套公式 ( 123 改 71 , 124 改 71 , 125 改 71 ，127 改 45 ，389 改 45 )

```excel-formula
=IF(BE2=123, 71, IF(BE2=124, 71, IF(BE2=125, 71, IF(BE2=127, 45, IF(BE2=389, 45, BE2)))))
```

or

```excel-formula
=SWITCH(BE2, 123, 71, 124, 71, 125, 71, 127, 45, 389, 45, BE2)
```
