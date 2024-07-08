3Dmigoto-Armor额外特性列表及使用说明
-ReleaseX64Dev				开发版，制作Mod和测试使用
-ReleaseX64Play				游玩版，仅用于使用Mod，无绿字					（集成了MMT-ACP）
-ReleaseX64PlayNoWarning   	游玩版，仅用于使用Mod，无绿字，无任何警告文字版本	（集成了MMT-ACP）

- 设置track_texture_updates=1时，F8 dump出来的已经打了Mod被替换的Buffer也会拥有Hash值，原版3Dmigoto没有这个hash值，
这个hash值无法在Hunting界面查询，但是可以通过手动查看log.txt来获取hunting界面IB的hash值对应的Dump出来的IB的hash值，
从而实现逆向提取模型，即直接提取打了Mod的模型的功能，从而实现最直接最简单的模型逆向提取。
(Dev版本独占)

- Store CommandList (Same as GIMI's store feature)
使用案例：store = $health, cs-cb0, 33
含义：将cs-cb0中的索引为33的float类型数据存储到变量$health中供后续使用(索引从0开始)
(Dev版、Play版都支持)

- CSReplace CommandList (Constant Slot Replace)
使用案例: csreplace = cs-cb0, 3, 2533, 4000
含义：读取cs-cb0中的索引为3的数据，如果值为2533，则把值改为4000并放回此cs-cb0供后续使用(索引从0开始)
(Dev版本独占)

- 在GI启动时加再多Mod也不会闪退
(Dev版、Play版都支持)




