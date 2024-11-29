自用华科研究生报告 LaTeX 模板，基于 [HUSTLatexTemplate](https://github.com/ywang-wnlo/HUSTLatexTemplate) 修改制作。

# Overleaf 使用方法

1. 修改overleaf项目的编译器为XeLaTeX
![](./assets/overleaf1.png)

# 使用参考
## 章节

一级标题：`\section{}`
二级标题：`\subsection{}`
三级标题：`\subsubsection{}`

## 交叉引用

```latex
\subsection{交叉引用}\label{subsec:crossref}

\autoref{subsec:crossref}
```

## 参考文献

```latex
这是一个参考文献引用的范例\cite{Stone_1998}，你可以随时使用两种不同的样式\normalcite{Stone_1998}或者\supercite{Stone_1998}
	
这样可以添加一个不标注的参考文献引用\nocite{9787508342894}
	
这样可以添加所有bib文件中的参考文献\nocite{*}
```

## 字体

```latex

{\songti \bfseries 宋体加粗}
	
{\songti \itshape 宋体斜体}
	
{\songti \bfseries \itshape 宋体粗斜体}

{\bfseries 加粗后变为黑体}
	
{\itshape 斜体后变为楷体}
```

## 图片

引用：`\autoref{fig:data}`
```latex
\begin{generalfig}[htb]{大数据信息处理框架}{fig:data}
    \includegraphics[width=\textwidth]{Figures/data.png}
\end{generalfig}
```

## 表格

引用：`\autoref{tab:heightweight}`
```latex
\begin{generaltab}{某校学生升高体重样本}{tab:heightweight}
    \begin{tabularx}{\textwidth}{lCCC}
        \toprule
        序号&年龄&身高&体重\\
        \midrule
        1&14&156&42\\
        2&16&158&45\\
        3&14&162&48\\
        4&15&163&50\\
        \cmidrule{2-4} %添加2-4列的中线
        平均&15&159.75&46.25\\
        \bottomrule
    \end{tabularx}
\end{generaltab}
```

## 公式

引用：`\autoref{eq:pingfanghe}`
```latex
在文中引用公式可以这么写：$a^2+b^2=c^2$这是勾股定理，他还可以表示为$c=\sqrt{a^2+b^2}$，还可以让公式单独一段并且加上编号

\begin{equation}
	\sin^2{\theta}+\cos^2{\theta}=1 
    \label{eq:pingfanghe}
\end{equation}
```

## 列表

计数列表
```latex
\begin{enumerate}
    \item 第一项
        \begin{enumerate}
            \item 第一项中的第一项
            \item 第一项中的第二项
        \end{enumerate}
    \item 第二项
    \item 第三项
\end{enumerate}
```

不计数列表
```latex
\begin{itemize}
    \item 第一项
    \begin{itemize}
        \item 第一项中的第一项
        \item 第一项中的第二项
    \end{itemize}
    \item 第二项
    \item 第三项
\end{itemize}
```