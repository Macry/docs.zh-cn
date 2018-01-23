---
title: "使用 .NET Compiler Platform SDK 语义模型"
description: "此概述介绍了用于理解和操作代码的语义节点的类型。"
author: billwagner
ms.author: wiwagn
ms.date: 10/15/2017
ms.topic: conceptual
ms.prod: .net
ms.devlang: devlang-csharp
ms.custom: mvc
ms.openlocfilehash: 28366093c516f5367d82c0bdfc53749e764361ef
ms.sourcegitcommit: d095094e942eedf09530ea5636fbaf9029853027
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2017
---
# <a name="work-with-semantics"></a>使用语义

[语法树](work-with-syntax.md)表示源代码的词法和语法结构。 尽管此信息已足以描述源中的所有声明和逻辑，但不足以识别正在引用的内容。 一个名称可能表示：

- 一种类型
- 一个字段
- 一种方法
- 一个局部变量

尽管以上每一项都各不相同，但要确定标识符实际上引用哪一项，通常需要深入了解语言规则。 

源代码中还表示了程序元素，并且程序也可引用以前编译的库，这些库打包在程序集文件中。 尽管没有任何可用于程序集的源代码（因此没有任何可用于程序集的语法节点或语法树），程序仍可引用其中的元素。

对于这些任务，需要语义模型。

除了源代码的语法模型外，语义模型还封装了语言规则，提供了一种将标识符与正在引用的正确程序元素正确匹配的简单办法。

## <a name="compilation"></a>编译

编译是编译 C# 或 Visual Basic 程序所需的所有内容的表示形式，其中包括所有程序集引用、编译器选项和源文件。 

由于所有这些信息都存储在一个位置，因此可以更详细地描述源代码中包含的元素。 编译以符号的形式表示每个声明的类型、成员或变量。 编译包含多种方法，可帮助查找和关联在源代码中声明的符号或作为元数据从程序集中导出的符号。

与语法树类似，编译是不可变的。 创建编译后，创建者或可能与之共享该编译的任何其他用户均不可进行更改。 但是，可以从现有编译创建新编译，指定进行的更改。 例如，可以创建与现有编译各方面均相同、但可能包含其他源文件或程序集引用的编译。

## <a name="symbols"></a>符号

符号表示源代码声明的不同元素，或作为元数据从程序集中导出。 每个命名空间、类型、方法、属性、字段、事件、参数或局部变量都由符号表示。 

<xref:Microsoft.CodeAnalysis.Compilation> 类型的各种方法和属性可帮助查找符号。 例如，可以通过声明的类型的通用元数据名称来查找该类型的符号。 还可以访问整个符号表，该表是以全局命名空间为根的符号树。

符号还包含编译器根据源或元数据（如其他引用的符号）确定的其他信息。 每种类型的符号都由派生自 <xref:Microsoft.CodeAnalysis.ISymbol> 的单独接口表示，每种符号都有其自己的方法和属性，详细说明了编译器收集的信息。 其中许多属性直接引用了其他符号。 例如，可通过 <xref:Microsoft.CodeAnalysis.IMethodSymbol.ReturnType?displayProperty=nameWithType> 属性得知方法声明引用的实际类型符号。

符号提供了源代码与元数据之间命名空间、类型和成员的共同表示形式。 例如，在源代码中声明的方法以及从元数据导入的方法均由具有相同属性的 <xref:Microsoft.CodeAnalysis.IMethodSymbol> 表示。

符号在概念上类似于 <xref:System.Reflection> API 表示的 CLR 类型系统，但前者更丰富，因为它们不仅仅可以对类型建模。 命名空间、局部变量和标签都是符号。 此外，符号是语言概念，而不是 CLR 概念的表示形式。 存在很多重叠，但也有许多有意义的区别。 例如，在 C# 或 Visual Basic 中，迭代器方法是单个符号。 但是，当迭代器方法转换为 CLR 元数据时，它是一种类型和多个方法。

## <a name="semantic-model"></a>语义模型

语义模型表示单个源文件的所有语义信息。 可使用语义模型发现以下内容： 

* 在源中特定位置引用的符号。
* 任何表达式的结果类型。
* 所有诊断（错误和警告）。
* 变量流入和流出源区域的方式。
* 更多推理问题的答案。