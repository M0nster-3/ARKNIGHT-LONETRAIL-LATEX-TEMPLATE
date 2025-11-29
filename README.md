# 明日方舟孤星Latex模板
## 0.特别声明
仓库内美术素材版权归明日方舟所有，仅供学习交流使用，本人无任何盈利行为；严禁商业用途，否则后果自负  

仓库里附上了AI源文件，不过个人接触AI不到一个月，水平很有限，里面的素材还是挺粗糙的...  

其余的请博士们随意(如自用或拼团)，也可以根据个人喜好修改里面素材，本人不会有任何意见  

XHS:Mikukawaii2
## 1.封面相关设置
(PS:封面代码有点麻烦，想要实现原本排版但是元素对齐代码我个人实现不了，  

就改了现在的这一版，简单但是和我原本的排版思路有差别)  

<div style="display: flex; gap: 10px; flex-wrap: wrap;">
  <img width="200" alt="封面草稿图" src="https://github.com/user-attachments/assets/07af5237-7f33-47db-886e-c5e92e9533b7" style="object-fit: contain;">
  <img width="200" alt="封面" src="https://github.com/user-attachments/assets/ede1a88c-0c20-4229-afdc-ba3266bcc4ee" style="object-fit: contain;">
</div>  

如左图所示，在封面有三个地方需要进行设置，提醒一下需要根据内容自行调整...   

封面标题

```tex
\newcommand{\TitleText}{
	\fontsize{36}{12}\selectfont\color{qiancheng}\XeTeXinterchartokenstate=0
	\AvantGarde\addfontfeatures{LetterSpace=-5} Measure Theory 
	\SSS \\[8pt] 
	\SiYuan 测度论
}


 \node[
   anchor=north west,
   minimum width=280pt,
   minimum height=100pt,
   text width=280pt,
   inner sep=0pt,
   outer sep=0pt,
   align=left,
   %align=center,
   ] at ($(current page.north west) + (10.096cm,-5.4467cm)$) {\TitleText};


%=====================================代码说明================================
在代码\fontsize{36}{12}\selectfont\color{qiancheng}\XeTeXinterchartokenstate=0中  
\fontsize{36}{12}是调整标题字体大小(目前36pt)  
\selectfont\color{qiancheng}让字体是橙色  
\XeTeXinterchartokenstate=0这个是解除宏包冲突的  

在代码\AvantGarde\addfontfeatures{LetterSpace=-5} Measure Theory里面的  
\AvantGarde\addfontfeatures{LetterSpace=-5}应用AvantGarde字体并且让字距缩小

代码\SSS \\[8pt] 是对标题进行分割线，然后上下文本间距扩大的(8pt)，也可以不使用

代码\SiYuan 测度论 是对[测度论]应用思源黑体的

最后下面的代码只需要注意align=left是让标题左对齐，你也可以用align=center让标题居中对齐

%===================================注意事项==============================
标题的排版只能说看你习惯了，能够拆为两行最好(长标题直接拆，短标题可以加标题的中文翻译等等)
默认左对齐和加入分割线\SSS，你可以删除分割线以及让标题居中
有时候需要手动调整标题字体大小，还是挺麻烦的
追求版面则可以加一些小元素让标题长短对齐(如最后一行加:到行尾等等)...
```

作者

```tex
\newcommand{\AuthorText}{
	\fontsize{15}{16}\selectfont\color{qiancheng}\XeTeXinterchartokenstate=0
	\AvantGarde\addfontfeatures{LetterSpace=-5} @Mikukawaii
}

%===================================注意事项==============================
相关代码和标题里面的差不多，默认了居中
如果名字过长可以修改字体大小
```

参考部分

```tex
\newcommand{\ReferenceText}{
	\FFF \\[14pt]
	\fontsize{9}{7}\selectfont\color{qiancheng}\AvantGarde\XeTeXinterchartokenstate=0 Reference: \\
	\fontsize{6}{7}\selectfont\color{heise}\AvantGarde\XeTeXinterchartokenstate=0 1.Jech."Set Theory".3rd ed,Springer,2003 \\
	\fontsize{6}{7}\selectfont\color{heise}\AvantGarde\XeTeXinterchartokenstate=0 2.Kechris."Classical Descriptive Set Theory".Springer,1995 \\
	\fontsize{6}{7}\selectfont\color{heise}\AvantGarde\XeTeXinterchartokenstate=0 3.Engelking."General Topology".Heldermann Veriag,1989 \\[12pt]
	\fontsize{9}{7}\selectfont\color{qiancheng}\AvantGarde\XeTeXinterchartokenstate=0 Acknowledgements: \\
	\fontsize{6}{7}\selectfont\color{heise}\AvantGarde\XeTeXinterchartokenstate=0 \#.Rhine Lab Pioneer Project \\
	}

%===================================注意事项==============================
相关代码结构也和标题里面的差不多，默认了左对齐，字体大小应该这样就可以
然后让标题是橙色的，而正文是黑色的
这里我觉得参考可以写多一点，让整个封面的左下角有点内容，看着就不会空
可以加一些莫名其妙的东西，把老师名字放进去也没有问题...
```
