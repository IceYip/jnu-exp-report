# 暨南大学本科实验报告 LaTeX 模版（包含中文版和英文版）

## Overview

暨南大学本科实验报告 LaTeX 模版 / Jinan University Experiment Report LaTeX Template

这是一份暨南大学本科实验报告的 LaTeX 模版，和 Word 版高度一致，包含中英双语版本。

点击这里**预览**：[中文版](https://github.com/IceYip/jnu-exp-report/blob/main/Problem.pdf) 
[英文版](https://github.com/IceYip/jnu-exp-report/blob/main/ProblemEng.pdf)

有了这个 LaTeX 模版：

- 可以在没有 Office 的情况下写实验报告了
- 编辑实验名称的时候，再也不用煞心费神地对齐下划线了
- 不用手动添加附页页眉
- 不需要操心代码高亮的问题
- 轻松插入复杂公式，远离 Word 的阴间公式编辑器

## Usage

中文版：复制 `ExpReport.cls` `Problem.tex` 到另一个目录，在 `Problem.tex` 的基础上编写你的实验报告即可。

英文版：复制 `ExpReport.cls` `ProblemEng.tex` 到另一个目录，用法同上。

本模版已经在 TeX Live 2020/Arch Linux，以及 Tex Live 2017/Debian 环境下测试通过。

注意：请使用 **XeLaTeX** 编译。

### 中文版和英文版的区别

实验报告正文为英文的情况下，建议使用英文版，因为它的排版更符合英文习惯。

|          | 中文版   | 英文版       |
|----------|----------|--------------|
| 行间距   | 1.3      | 1.0          |
| 首段的首行缩进 | 有       | 无           |
| 节序号   | 中文序号 | 罗马数字序号 |

### 定制标题区

可以根据自己的需要更改这些项目。

```LaTeX
\course{模拟电子技术实验} %课程名称
\director{赵钱孙，李周吴} %指导老师
\author{学生A，学生B} %学生姓名
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

**注意：** 温度、湿度等用不到的项目可以留空，但请不要删掉，否则 LaTeX 会报错。

唯一能删除的是 `\date` 选项。若删除 `\date`， LaTeX 将自动填入今天的日期。

### 插入代码

本模版为 `lstlisting` 环境定义了语法高亮，你可以用 `lstlisting` 在报告中插入代码，通过 `language` 选项可以指定高亮语言。下面是插入 C 语言代码的示例：

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
