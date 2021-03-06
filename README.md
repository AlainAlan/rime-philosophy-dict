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
- nianhao
  - 历代年号
  - 基于[China Biographical Database Project (CBDB)](https://projects.iq.harvard.edu/cbdb)
  - 假装引用了：[How to Cite CBDB | China Biographical Database Project (CBDB)](https://projects.iq.harvard.edu/cbdb/how-cite-cbdb)
  - License：[Creative Commons — 署名-非商业性使用-相同方式共享 4.0 国际 — CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh)
- temples
  - 寺庙与书院
  - ibid
- persons
  - 中国历史人物
  - ibid
- literati
  - [西儒名姓资](https://alainalan.github.io/Aid-to-the-Names-and-Surnames-of-Western-Literati/)
- ctext.titles
  - 来自https://api.ctext.org/gettexttitles?if=zh
  - https://ctext.org/
  - 建议为大佬捐款：https://ctext.org/help-us
- ctext.medicines
  - 为了方便个人输入西药名称，从[国家医保局 人力资源社会保障部关于印发《国家基本医疗保险、工伤保险和生育保险药品目录（2020年）》的通知](http://www.gov.cn/zhengce/zhengceku/2020-12/28/content_5574062.htm)下载了2020年的医保目录pdf
  - 将pdf转换为excel之后，简单整理后改为yaml词库
  - 这一词库没有列入extended（因为不属于哲学相关内容），可以手动加入
- ctext.TCM
  - 同上，是中药版本
  - 加入中成药乃至中药注射液不代表个人立场，仅代表这些药物在现实生活中被实际使用（实然），而不涉及对相关药物的药效和安全性的评价


## 繁简转换问题

有时候rime基于的opencc在转换人名的时候会出问题，例如汎->泛、旂->旗等。
需要在rime**程序文件夹**下data/opencc中添加`TSCharacters_custom.txt`：

```
徐乾學	徐乾学
王汎森	王汎森
薛應旂	薛应旂
```

如此自定义繁简转换（本词库主要基于繁体）

- [開放中文轉換 Open Chinese Convert (OpenCC)](https://opencc.byvoid.com/)
- [BYVoid/OpenCC: Conversion between Traditional and Simplified Chinese](https://github.com/BYVoid/OpenCC)

另：今天（2021-12-08）删掉了拼音重码太多的两字人名，同一拼音随机保留十个，避免翻页太累。

## 数据说明

- data：装文本的筐
  - journals：搜集期刊索引
     - 《中国哲学史》：该刊2010-2020的索引，来自cnki和CSSCI
     - 前500文献：2010-2020年cnki被引前500的哲学核心刊物文献，来自cnki
