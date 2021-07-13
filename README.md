# rime-philosophy-dict
用于朙月拼音的哲学专业词库

可能并不只限于哲学专业。

## dict说明

- guaxiang：卦象
  - 使得可以通过输入`guimeigua`得到`䷵`，以此类推
  - 双拼也可以通过配置双拼方案对应的`custom.yaml`使用，其他方案亦同
  - 在输入法界面中备选的卦象符号或显示为豆腐块，那么则需要在配置文件中修改字体，详询百度
- ctext
  - 这一dict主要内容来自ctext.org先秦两汉部分的标题（以经书、子书的书名和篇名为主，也有史书及其他）
  - 经手动复制，但基本没有校对读音（`噬嗑`除外，已给定`shi he`的读音）
- monarchies：帝王名諱、廟號及其他
  - 這個dict是這幾天陸陸續續校對的。
  - 資料來源：[中国历代皇帝列表](http://xh.5156edu.com/page/z2295m3375j18869.html)
  - 使用MS Word簡轉繁，然後人工校對（如后／後、寜／甯以及錯別字等等）
  - 校對以《王力古漢語字典》附錄爲準，不在其內的則參考ctext、維基百科
- philosophers：国内哲学工作者姓名
  - 来自cnki
  - 2010-2020年
  - 每年哲学类核心期刊（被引降序）前500篇论文
  - 筛选了发过三篇论文的学者（`羡慕`）
- philosophy
  - （2021-07-13更新部分）与`philosophers`来源相同
    - 筛选了这些期刊的一千多个关键词
    - 使用VOSviewer筛选，输出Pajek的net文件用python略微处理


## 在路上

- [ ] nianhao：年號
- [ ] scholars：中國歷史人物之人名
- [ ] literati： [西儒名姓资](https://alainalan.github.io/Aid-to-the-Names-and-Surnames-of-Western-Literati/)中的人名
- [ ] philosophes：哲學家姓名
- [x] philosophers: 國內哲學工作者姓名
- [ ] philosophy：哲學術語／概念／流派／著作等等（部分完成）


## 数据说明

- data：装文本的筐
  - journals：搜集期刊索引
     - 《中国哲学史》：该刊2010-2020的索引，来自cnki和CSSCI
     - 前500文献：2010-2020年cnki被引前500的哲学核心刊物文献，来自cnki
