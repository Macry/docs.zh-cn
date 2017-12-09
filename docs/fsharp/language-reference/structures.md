---
title: "结构 (F#)"
description: "了解有关 F # 结构，紧凑对象类型通常比具有少量的数据和简单的行为的类型的类更有效。"
keywords: "visual f#, f#, 函数编程"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 50819506-3210-418f-9602-0ee1c9a52177
ms.openlocfilehash: 542b69a5aacb8fcfb0e8f6d6c943fe1954c4c59c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="structures"></a><span data-ttu-id="18554-104">结构</span><span class="sxs-lookup"><span data-stu-id="18554-104">Structures</span></span>

<span data-ttu-id="18554-105">A*结构*是一种紧凑对象类型，可能比具有少量数据且行为简单类型的类更有效。</span><span class="sxs-lookup"><span data-stu-id="18554-105">A *structure* is a compact object type that can be more efficient than a class for types that have a small amount of data and simple behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="18554-106">语法</span><span class="sxs-lookup"><span data-stu-id="18554-106">Syntax</span></span>

```fsharp
[ attributes ]
type [accessibility-modifier] type-name =
    struct
        type-definition-elements
    end
// or
[ attributes ]
[<StructAttribute>]
type [accessibility-modifier] type-name =
    type-definition-elements
```

## <a name="remarks"></a><span data-ttu-id="18554-107">备注</span><span class="sxs-lookup"><span data-stu-id="18554-107">Remarks</span></span>
<span data-ttu-id="18554-108">结构是*值类型*，这意味着它们存储在堆栈上直接中，或当它们用作字段或数组元素的父代中的内联键入。</span><span class="sxs-lookup"><span data-stu-id="18554-108">Structures are *value types*, which means that they are stored directly on the stack or, when they are used as fields or array elements, inline in the parent type.</span></span> <span data-ttu-id="18554-109">与类和记录不同，结构具有按值传递语义。</span><span class="sxs-lookup"><span data-stu-id="18554-109">Unlike classes and records, structures have pass-by-value semantics.</span></span> <span data-ttu-id="18554-110">这意味着它们主要用于经常访问和复制的少量聚合数据。</span><span class="sxs-lookup"><span data-stu-id="18554-110">This means that they are useful primarily for small aggregates of data that are accessed and copied frequently.</span></span>

<span data-ttu-id="18554-111">在前面的语法中，将显示两个窗体。</span><span class="sxs-lookup"><span data-stu-id="18554-111">In the previous syntax, two forms are shown.</span></span> <span data-ttu-id="18554-112">第一个窗体不是轻量级语法，但其仍然经常使用，因为当使用 `struct` 和 `end` 关键字时，你可以忽略第二个窗体中出现的 `StructAttribute` 特性。</span><span class="sxs-lookup"><span data-stu-id="18554-112">The first is not the lightweight syntax, but it is nevertheless frequently used because, when you use the `struct` and `end` keywords, you can omit the `StructAttribute` attribute, which appears in the second form.</span></span> <span data-ttu-id="18554-113">你可以将 `StructAttribute` 缩写为 `Struct`。</span><span class="sxs-lookup"><span data-stu-id="18554-113">You can abbreviate `StructAttribute` to just `Struct`.</span></span>

<span data-ttu-id="18554-114">*类型定义元素*在上述语法中表示成员声明和定义。</span><span class="sxs-lookup"><span data-stu-id="18554-114">The *type-definition-elements* in the previous syntax represents member declarations and definitions.</span></span> <span data-ttu-id="18554-115">结构可以具有构造函数以及可变和不可变字段，并且可以声明成员和接口实现。</span><span class="sxs-lookup"><span data-stu-id="18554-115">Structures can have constructors and mutable and immutable fields, and they can declare members and interface implementations.</span></span> <span data-ttu-id="18554-116">有关详细信息，请参阅[成员](members/index.md)。</span><span class="sxs-lookup"><span data-stu-id="18554-116">For more information, see [Members](members/index.md).</span></span>

<span data-ttu-id="18554-117">结构不能参与继承、不能包含 `let` 或 `do` 绑定、不能以递归方式包含其自身类型的字段（但可以包含引用其自身类型的引用单元格）。</span><span class="sxs-lookup"><span data-stu-id="18554-117">Structures cannot participate in inheritance, cannot contain `let` or `do` bindings, and cannot recursively contain fields of their own type (although they can contain reference cells that reference their own type).</span></span>

<span data-ttu-id="18554-118">由于结构不允许 `let` 绑定，你必须通过使用 `val` 关键字在结构中声明字段。</span><span class="sxs-lookup"><span data-stu-id="18554-118">Because structures do not allow `let` bindings, you must declare fields in structures by using the `val` keyword.</span></span> <span data-ttu-id="18554-119">`val` 关键字定义字段及其类型，但不允许初始化。</span><span class="sxs-lookup"><span data-stu-id="18554-119">The `val` keyword defines a field and its type but does not allow initialization.</span></span> <span data-ttu-id="18554-120">相反，`val` 声明会初始化零或 null。</span><span class="sxs-lookup"><span data-stu-id="18554-120">Instead, `val` declarations are initialized to zero or null.</span></span> <span data-ttu-id="18554-121">因此，具有隐式构造函数（即，在声明中的结构名称后直接给定参数）的结构要求使用 `val` 特性批注 `DefaultValue` 声明。</span><span class="sxs-lookup"><span data-stu-id="18554-121">For this reason, structures that have an implicit constructor (that is, parameters that are given immediately after the structure name in the declaration) require that `val` declarations be annotated with the `DefaultValue` attribute.</span></span> <span data-ttu-id="18554-122">具有定义构造函数的结构仍支持零初始化。</span><span class="sxs-lookup"><span data-stu-id="18554-122">Structures that have a defined constructor still support zero-initialization.</span></span> <span data-ttu-id="18554-123">因此，`DefaultValue` 特性是此类零值对字段有效的声明。</span><span class="sxs-lookup"><span data-stu-id="18554-123">Therefore, the `DefaultValue` attribute is a declaration that such a zero value is valid for the field.</span></span> <span data-ttu-id="18554-124">由于此类型上不允许 `let` 和 `do` 绑定，结构的隐式构造函数不执行任何操作，但所传入的隐式构造函数参数值作为私有字段提供。</span><span class="sxs-lookup"><span data-stu-id="18554-124">Implicit constructors for structures do not perform any actions because `let` and `do` bindings aren’t allowed on the type, but the implicit constructor parameter values passed in are available as private fields.</span></span>

<span data-ttu-id="18554-125">显式构造函数可能涉及字段值的初始化。</span><span class="sxs-lookup"><span data-stu-id="18554-125">Explicit constructors might involve initialization of field values.</span></span> <span data-ttu-id="18554-126">当你的结构具有显式构造函数时，它仍支持零初始化；但是，由于它与显式构造函数冲突，请勿在 `DefaultValue` 声明上使用 `val` 特性。</span><span class="sxs-lookup"><span data-stu-id="18554-126">When you have a structure that has an explicit constructor, it still supports zero-initialization; however, you do not use the `DefaultValue` attribute on the `val` declarations because it conflicts with the explicit constructor.</span></span> <span data-ttu-id="18554-127">有关详细信息`val`声明，请参阅[显式字段：`val`关键字](members/explicit-fields-the-val-keyword.md)。</span><span class="sxs-lookup"><span data-stu-id="18554-127">For more information about `val` declarations, see [Explicit Fields: The `val` Keyword](members/explicit-fields-the-val-keyword.md).</span></span>

<span data-ttu-id="18554-128">结构上允许特性和可访问性修饰符，并遵循与其他类型相同的规则。</span><span class="sxs-lookup"><span data-stu-id="18554-128">Attributes and accessibility modifiers are allowed on structures, and follow the same rules as those for other types.</span></span> <span data-ttu-id="18554-129">有关详细信息，请参阅[属性](attributes.md)和[访问控制](access-control.md)。</span><span class="sxs-lookup"><span data-stu-id="18554-129">For more information, see [Attributes](attributes.md) and [Access Control](access-control.md).</span></span>

<span data-ttu-id="18554-130">以下代码示例说明结构定义。</span><span class="sxs-lookup"><span data-stu-id="18554-130">The following code examples illustrate structure definitions.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2501.fs)]

## <a name="struct-records-and-discriminated-unions"></a><span data-ttu-id="18554-131">结构记录和可区分的联合</span><span class="sxs-lookup"><span data-stu-id="18554-131">Struct Records and Discriminated Unions</span></span>

<span data-ttu-id="18554-132">F # 4.1 开始，您可以表示[记录](records.md)和[可区分联合](discriminated-unions.md)为与结构`[<Struct>]`属性。</span><span class="sxs-lookup"><span data-stu-id="18554-132">Starting with F# 4.1, you can represent [Records](records.md) and [Discriminated Unions](discriminated-unions.md) as structs with the `[<Struct>]` attribute.</span></span>  <span data-ttu-id="18554-133">请查看每个文章以了解详细信息。</span><span class="sxs-lookup"><span data-stu-id="18554-133">See each article to learn more.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18554-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18554-134">See Also</span></span>
[<span data-ttu-id="18554-135">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="18554-135">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="18554-136">类</span><span class="sxs-lookup"><span data-stu-id="18554-136">Classes</span></span>](classes.md)

[<span data-ttu-id="18554-137">记录</span><span class="sxs-lookup"><span data-stu-id="18554-137">Records</span></span>](records.md)

[<span data-ttu-id="18554-138">成员</span><span class="sxs-lookup"><span data-stu-id="18554-138">Members</span></span>](members/index.md)