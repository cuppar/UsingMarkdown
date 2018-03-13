> Teacher: Liu Qing  
E-mail: liuqing@ynu.edu.cn

## Week 1
---
### 1.1 What is a compiling program?
#### Programming language
- program: a set of instructions
- machine language: consists of 0 and 1
- assembly language: pseudo code with symbols
- high-level language: natural-like language and mathematical formula
> FORTRAN: **For**mula **Tran**slation, the first high-level language

#### Compiling Terminology
- Compiler: translate high-level program to target program
- Running System: sub-programs required when target program is running
- Compiling System: __Compiler__ + __Running System__
- Interpretor: compiling while running

#### Translator
Language A --> Translator --> equivalent Language B

#### Compiler
high-level language A --> Compiler --> equivalent assembly language or machine language

### 1.2 Compiling Process
#### 6阶段（8部分）
1. 词法分析
   - 这个阶段的任务是从左到右读入源程序，对构成源程序的字符流进行扫描和分解，从而识别出一个个单词（也称单词符号和TOKEN）
1. 语法分析
   - 语法分析的任务是在语法分析的基础上将单词序列分解成各类语法短语（也称语法单位、语法成分、语法范畴），如“程序”，“语句”，“表达式”等等。
   - 语法分析所依据的是语言的语法规则，即描述程序结构的规则。通过语法分析确定整个输入串是否构成一个语法上正确的程序。
1. 语义分析
   - 依据语言的语义规则，对语法分析得到的语法结构分析其含义以及应进行的运算，审查源程序中有无语义错误，为代码生成阶段收集类型信息。
1. 中间代码生成
   - 某些编译程序将源程序转变成一种内部表示形式，叫做中间代码。
   - 所谓“中间代码”是一种结构简单，含义明确的记号系统，可以设计为多种多样的形式。
   - 中间代码设计原则：容易生成、容易翻译成目标代码（举例：四元式）
1. 代码优化
   - 对前阶段产生的中间代码序列进行变换或改造。目的是使生成的目标代码更高效，即省时间省空间。
1. 目标代码生成
   - 将中间代码变换成特定机器上的绝对指令代码或可重定位的指令代码或汇编指令代码。它的工作与硬件系统结构和指令含义有关。

#### 另外两个重要的工作：
1. 表格管理
   - 编译过程中源程序的各种信息被保留在种种不同的表格里，各阶段工作都涉及到构造、查找或更新有关的表格，因此需要表格管理。
1. 出错处理
   - 错误产生时，编译程序应报告错误的性质和发生地点，并且将错误所造成的影响限制在尽可能小的范围内，使得源程序的其余部分能继续被编译下去。
   - 有些编译程序还能自动校正错误，这些工作被称为错误处理。

### 1.3 编译阶段的组合
#### 前端和后端
- 前端：其工作依赖于源程序而与目标机无关
- 后端：其工作依赖于目标机

#### 遍（Pass）
- 遍（Pass），指对源程序或源程序的中间形式从头到尾扫视并完成规定任务的过程。
- 每一遍扫视可完成一个阶段或多个阶段的功能。
- 一个编译程序需要分成几遍，应视**语言要求**和**机器情况**而定。

### 1.4 编译技术和软件工具
- 语言的结构化编辑器
- 语言程序的调试工具
- 语言程序的测试工具
- 高级语言之间的转换工具
- 并行编译技术

### 1.5 程序设计语言范型
- 强制式语言
- 函数式语言
- 基于规则
