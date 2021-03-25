# 暨南大学本科实验报告 LaTeX 模版

## Overview

这是一份暨南大学本科实验报告的 LaTeX 模版。本模版在 TeX Live 2020/Arch Linux 环境下测试通过。

本实验报告和 Word 版高度一致，[点击这里预览](https://github.com/IceYip/jnu-exp-report/blob/main/Problem.pdf)。

有了这个 LaTeX 模版：

- 可以在没有 Office 的情况下写实验报告了
- 不用手动添加附页页眉
- 不需要操心代码高亮的问题
- 轻松插入复杂公式，远离 Word 的阴间公式编辑器
- 编辑实验名称的时候，再也不用煞心费神地对齐下划线了

## Usage

按需求修改示例文档 Problem.tex 即可。

### 英文实验报告

本模版引用了`ctexart`类，适用于中文实验报告，故`\section`皆为中文序号（例如 `一、`）。如果要写**英文实验报告**，请注释掉`ExpReport.cls`中的这几行：

```LaTeX
% 设置章节编号
\renewcommand\thesection{\chinese{section}、}
\renewcommand\thesubsection{\arabic{subsection}.}
\renewcommand\thesubsubsection{\alph{subsubsection})}
```

注释掉这几行后，章节序号会恢复默认样式。

### 定制标题区

可以根据自己的需要更改这些项目。

```LaTeX
\course{模拟电子技术实验} %课程名称
\director{赵钱孙，李周吴} %指导老师
\author{郑王冯，陈禇卫} %学生姓名
\classroom{南海楼} %实验地点
\title{晶体管共射极单管放大器} %实验名称
\expno{080812345601} %实验编号
\exptype{} %实验项目类型，没有要求的话请留空
\authorno{2020101234，2019051234} %学号
\college{信息科学技术学院} %学院
\department{电子} %系
\major{电子科学与技术} %专业

\date{2021年3月1日 $\sim$ 2021年3月1日} %时间，可删掉

\temp{} %温度，可留空
\humid{} %湿度，可留空
```

**注意：** 有些项目，例如温度、湿度，你可能用不上。可以留空但请不要删掉，否则 LaTeX 会报错。

唯一能删除的是`\date`选项。若删除`\date`， LaTeX 将自动填入今天的日期。

### 插入代码

你可以用`lstlisting`在报告中插入代码，通过`language`选项可以指定高亮语言。下面是插入 C 语言代码的示例：

```LaTeX
\subsection{Problem.c}
\begin{lstlisting}[language=c]
#include <stdio.h>
int main(){
    printf("Hello world");
    // This is a comment.
}
\end{lstlisting}
```

`lstlisting` 支持的语言请参见[Code listing - Supported languages](https://pt.overleaf.com/learn/latex/Code_listing#Supported_languages)