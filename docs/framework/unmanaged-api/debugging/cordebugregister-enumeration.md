---
title: "CorDebugRegister 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugRegister
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugRegister
helpviewer_keywords: CorDebugRegister enumeration [.NET Framework debugging]
ms.assetid: 003bb138-7960-4291-ac88-0d87e470ff70
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: aa9cbd0feaddf5c091bd1f724860cddbd5b11054
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="cordebugregister-enumeration"></a><span data-ttu-id="016fb-102">CorDebugRegister 枚举</span><span class="sxs-lookup"><span data-stu-id="016fb-102">CorDebugRegister Enumeration</span></span>
<span data-ttu-id="016fb-103">指定与给定处理器体系结构关联的寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-103">Specifies the registers associated with a given processor architecture.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="016fb-104">语法</span><span class="sxs-lookup"><span data-stu-id="016fb-104">Syntax</span></span>  
  
```  
typedef enum CorDebugRegister {  
  
    REGISTER_INSTRUCTION_POINTER = 0,  
    REGISTER_STACK_POINTER,  
    REGISTER_FRAME_POINTER,  
  
    REGISTER_X86_EIP = 0,  
    REGISTER_X86_ESP,  
    REGISTER_X86_EBP,  
  
    REGISTER_X86_EAX,  
    REGISTER_X86_ECX,  
    REGISTER_X86_EDX,  
    REGISTER_X86_EBX,  
  
    REGISTER_X86_ESI,  
    REGISTER_X86_EDI,  
  
    REGISTER_X86_FPSTACK_0,  
    REGISTER_X86_FPSTACK_1,  
    REGISTER_X86_FPSTACK_2,  
    REGISTER_X86_FPSTACK_3,  
    REGISTER_X86_FPSTACK_4,  
    REGISTER_X86_FPSTACK_5,  
    REGISTER_X86_FPSTACK_6,  
    REGISTER_X86_FPSTACK_7,  
  
    REGISTER_AMD64_RIP = 0,  
    REGISTER_AMD64_RSP,  
    REGISTER_AMD64_RBP,  
    REGISTER_AMD64_RAX,  
    REGISTER_AMD64_RCX,  
    REGISTER_AMD64_RDX,  
    REGISTER_AMD64_RBX,  
    REGISTER_AMD64_RSI,  
    REGISTER_AMD64_RDI,  
    REGISTER_AMD64_R8,  
    REGISTER_AMD64_R9,  
    REGISTER_AMD64_R10,  
    REGISTER_AMD64_R11,  
    REGISTER_AMD64_R12,  
    REGISTER_AMD64_R13,  
    REGISTER_AMD64_R14,  
    REGISTER_AMD64_R15,  
  
    REGISTER_AMD64_XMM0,  
    REGISTER_AMD64_XMM1,  
    REGISTER_AMD64_XMM2,  
    REGISTER_AMD64_XMM3,  
    REGISTER_AMD64_XMM4,  
    REGISTER_AMD64_XMM5,  
    REGISTER_AMD64_XMM6,  
    REGISTER_AMD64_XMM7,  
    REGISTER_AMD64_XMM8,  
    REGISTER_AMD64_XMM9,  
    REGISTER_AMD64_XMM10,  
    REGISTER_AMD64_XMM11,  
    REGISTER_AMD64_XMM12,  
    REGISTER_AMD64_XMM13,  
    REGISTER_AMD64_XMM14,  
    REGISTER_AMD64_XMM15,  
  
    REGISTER_IA64_BSP = REGISTER_FRAME_POINTER,  
    REGISTER_IA64_R0  = REGISTER_IA64_BSP + 1,  
    REGISTER_IA64_F0  = REGISTER_IA64_R0  + 128,  
    REGISTER_ARM_PC = 0,  
    REGISTER_ARM_SP,  
    REGISTER_ARM_R0,  
    REGISTER_ARM_R1,  
    REGISTER_ARM_R2,  
    REGISTER_ARM_R3,  
    REGISTER_ARM_R4,  
    REGISTER_ARM_R5,  
    REGISTER_ARM_R6,  
    REGISTER_ARM_R7,  
    REGISTER_ARM_R8,  
    REGISTER_ARM_R9,  
    REGISTER_ARM_R10,  
    REGISTER_ARM_R11,  
    REGISTER_ARM_R12,  
    REGISTER_ARM_LR,  
  
} CorDebugRegister;  
```  
  
## <a name="members"></a><span data-ttu-id="016fb-105">成员</span><span class="sxs-lookup"><span data-stu-id="016fb-105">Members</span></span>  
  
|<span data-ttu-id="016fb-106">成员</span><span class="sxs-lookup"><span data-stu-id="016fb-106">Member</span></span>|<span data-ttu-id="016fb-107">描述</span><span class="sxs-lookup"><span data-stu-id="016fb-107">Description</span></span>|  
|------------|-----------------|  
|`REGISTER_INSTRUCTION_POINTER`|<span data-ttu-id="016fb-108">任何处理器上的指令指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-108">An instruction pointer register on any processor.</span></span>|  
|`REGISTER_STACK_POINTER`|<span data-ttu-id="016fb-109">任何处理器上的堆栈指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-109">A stack pointer register on any processor.</span></span>|  
|`REGISTER_FRAME_POINTER`|<span data-ttu-id="016fb-110">任何处理器上的帧指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-110">A frame pointer register on any processor.</span></span>|  
|`REGISTER_X86_EIP`|<span data-ttu-id="016fb-111">x86 处理器上的指令指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-111">The instruction pointer register on the x86 processor.</span></span>|  
|`REGISTER_X86_ESP`|<span data-ttu-id="016fb-112">x86 处理器上的堆栈指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-112">The stack pointer register on the x86 processor.</span></span>|  
|`REGISTER_X86_EBP`|<span data-ttu-id="016fb-113">x86 处理器上的基指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-113">The base pointer register on the x86 processor.</span></span>|  
|`REGISTER_X86_EAX`|<span data-ttu-id="016fb-114">x86 处理器上的 A 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-114">The A data register on the x86 processor.</span></span>|  
|`REGISTER_X86_ECX`|<span data-ttu-id="016fb-115">x86 处理器上的 C 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-115">The C data register on the x86 processor.</span></span>|  
|`REGISTER_X86_EDX`|<span data-ttu-id="016fb-116">x86 处理器上的 D 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-116">The D data register on the x86 processor.</span></span>|  
|`REGISTER_X86_EBX`|<span data-ttu-id="016fb-117">x86 处理器上的 B 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-117">The B data register on the x86 processor.</span></span>|  
|`REGISTER_X86_ESI`|<span data-ttu-id="016fb-118">x86 处理器上的源索引寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-118">The source index register on the x86 processor.</span></span>|  
|`REGISTER_X86_EDI`|<span data-ttu-id="016fb-119">x86 处理器上的目标索引寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-119">The destination index register on the x86 processor.</span></span>|  
|`REGISTER_X86_FPSTACK_0`|<span data-ttu-id="016fb-120">x86 浮点 (FP) 处理器上的堆栈寄存器 0。</span><span class="sxs-lookup"><span data-stu-id="016fb-120">The stack register 0 on the x86 floating-point (FP) processor.</span></span>|  
|`REGISTER_X86_FPSTACK_1`|<span data-ttu-id="016fb-121">x86 FP 处理器上的 #1 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-121">The #1 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_2`|<span data-ttu-id="016fb-122">x86 FP 处理器上的 #2 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-122">The #2 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_3`|<span data-ttu-id="016fb-123">x86 FP 处理器上的 #3 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-123">The #3 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_4`|<span data-ttu-id="016fb-124">x86 FP 处理器上的 #4 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-124">The #4 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_5`|<span data-ttu-id="016fb-125">x86 FP 处理器上的 #5 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-125">The #5 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_6`|<span data-ttu-id="016fb-126">x86 FP 处理器上的 #6 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-126">The #6 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_7`|<span data-ttu-id="016fb-127">x86 FP 处理器上的 #7 堆栈寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-127">The #7 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_AMD64_RIP`|<span data-ttu-id="016fb-128">AMD64 处理器上的指令指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-128">The instruction pointer register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RSP`|<span data-ttu-id="016fb-129">AMD64 处理器上的堆栈指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-129">The stack pointer register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RBP`|<span data-ttu-id="016fb-130">AMD64 处理器上的基指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-130">The base pointer register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RAX`|<span data-ttu-id="016fb-131">AMD64 处理器上的 A 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-131">The A data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RCX`|<span data-ttu-id="016fb-132">AMD64 处理器上的 C 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-132">The C data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RDX`|<span data-ttu-id="016fb-133">AMD64 处理器上的 D 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-133">The D data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RBX`|<span data-ttu-id="016fb-134">AMD64 处理器上的 B 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-134">The B data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RSI`|<span data-ttu-id="016fb-135">AMD64 处理器上的源索引寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-135">The source index register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RDI`|<span data-ttu-id="016fb-136">AMD64 处理器上的目标索引寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-136">The destination index register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R8`|<span data-ttu-id="016fb-137">AMD64 处理器上的 #8 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-137">The #8 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R9`|<span data-ttu-id="016fb-138">AMD64 处理器上的 #9 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-138">The #9 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R10`|<span data-ttu-id="016fb-139">AMD64 处理器上的 #10 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-139">The #10 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R11`|<span data-ttu-id="016fb-140">AMD64 处理器上的 #11 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-140">The #11 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R12`|<span data-ttu-id="016fb-141">AMD64 处理器上的 #12 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-141">The #12 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R13`|<span data-ttu-id="016fb-142">AMD64 处理器上的 #13 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-142">The #13 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R14`|<span data-ttu-id="016fb-143">AMD64 处理器上的 #14 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-143">The #14 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R15`|<span data-ttu-id="016fb-144">AMD64 处理器上的 #15 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-144">The #15 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM0`|<span data-ttu-id="016fb-145">AMD64 处理器上的 #0 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-145">The #0 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM1`|<span data-ttu-id="016fb-146">AMD64 处理器上的 #1 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-146">The #1 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM2`|<span data-ttu-id="016fb-147">AMD64 处理器上的 #2 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-147">The #2 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM3`|<span data-ttu-id="016fb-148">AMD64 处理器上的 #3 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-148">The #3 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM4`|<span data-ttu-id="016fb-149">AMD64 处理器上的 #4 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-149">The #4 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM5`|<span data-ttu-id="016fb-150">AMD64 处理器上的 #5 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-150">The #5 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM6`|<span data-ttu-id="016fb-151">AMD64 处理器上的 #6 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-151">The #6 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM7`|<span data-ttu-id="016fb-152">AMD64 处理器上的 #7 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-152">The #7 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM8`|<span data-ttu-id="016fb-153">AMD64 处理器上的 #8 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-153">The #8 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM9`|<span data-ttu-id="016fb-154">AMD64 处理器上的 #9 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-154">The #9 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM10`|<span data-ttu-id="016fb-155">AMD64 处理器上的 #10 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-155">The #10 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM11`|<span data-ttu-id="016fb-156">AMD64 处理器上的 #11 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-156">The #11 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM12`|<span data-ttu-id="016fb-157">AMD64 处理器上的 #12 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-157">The #12 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM13`|<span data-ttu-id="016fb-158">AMD64 处理器上的 #13 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-158">The #13 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM14`|<span data-ttu-id="016fb-159">AMD64 处理器上的 #14 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-159">The #14 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM15`|<span data-ttu-id="016fb-160">AMD64 处理器上的 #15 多媒体寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-160">The #15 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_IA64_BSP`|<span data-ttu-id="016fb-161">IA-64 处理器上的堆栈指针寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-161">The stack pointer register on the IA-64 processor.</span></span>|  
|`REGISTER_IA64_R0`|<span data-ttu-id="016fb-162">IA-64 处理器上的 #0 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-162">The #0 data register on the IA-64 processor.</span></span>|  
|`REGISTER_IA64_F0`|<span data-ttu-id="016fb-163">IA-64 处理器上的 #0 FP 数据寄存器。</span><span class="sxs-lookup"><span data-stu-id="016fb-163">The #0 FP data register on the IA-64 processor.</span></span>|  
|`REGISTER_ARM_PC`|<span data-ttu-id="016fb-164">ARM 处理器上的程序计数器寄存器 (R15)。</span><span class="sxs-lookup"><span data-stu-id="016fb-164">The program counter register (R15) on the ARM processor.</span></span>|  
|`REGISTER_ARM_SP`|<span data-ttu-id="016fb-165">ARM 处理器上的堆栈指针寄存器 (R13)。</span><span class="sxs-lookup"><span data-stu-id="016fb-165">The stack pointer register (R13) on the ARM processor.</span></span>|  
|`REGISTER_ARM_R0`|<span data-ttu-id="016fb-166">ARM 处理器上的数据寄存器 R0。</span><span class="sxs-lookup"><span data-stu-id="016fb-166">Data register R0 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R1`|<span data-ttu-id="016fb-167">ARM 处理器上的数据寄存器 R1。</span><span class="sxs-lookup"><span data-stu-id="016fb-167">Data register R1 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R2`|<span data-ttu-id="016fb-168">ARM 处理器上的数据寄存器 R2。</span><span class="sxs-lookup"><span data-stu-id="016fb-168">Data register R2 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R3`|<span data-ttu-id="016fb-169">ARM 处理器上的数据寄存器 R3。</span><span class="sxs-lookup"><span data-stu-id="016fb-169">Data register R3 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R4`|<span data-ttu-id="016fb-170">ARM 处理器上的寄存器 R4。</span><span class="sxs-lookup"><span data-stu-id="016fb-170">Register R4 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R5`|<span data-ttu-id="016fb-171">ARM 处理器上的寄存器 R5。</span><span class="sxs-lookup"><span data-stu-id="016fb-171">Register R5 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R6`|<span data-ttu-id="016fb-172">ARM 处理器上的寄存器 R6。</span><span class="sxs-lookup"><span data-stu-id="016fb-172">Register R6 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R7`|<span data-ttu-id="016fb-173">ARM 处理器上的寄存器 R7（THUMB 帧指针）。</span><span class="sxs-lookup"><span data-stu-id="016fb-173">Register R7 (the THUMB frame pointer) on the ARM processor.</span></span>|  
|`REGISTER_ARM_R8`|<span data-ttu-id="016fb-174">ARM 处理器上的寄存器 R8。</span><span class="sxs-lookup"><span data-stu-id="016fb-174">Register R8 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R9`|<span data-ttu-id="016fb-175">ARM 处理器上的寄存器 R9。</span><span class="sxs-lookup"><span data-stu-id="016fb-175">Register R9 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R10`|<span data-ttu-id="016fb-176">ARM 处理器上的寄存器 R10。</span><span class="sxs-lookup"><span data-stu-id="016fb-176">Register R10 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R11`|<span data-ttu-id="016fb-177">ARM 处理器上的帧指针。</span><span class="sxs-lookup"><span data-stu-id="016fb-177">The frame pointer on the ARM processor.</span></span>|  
|`REGISTER_ARM_R12`|<span data-ttu-id="016fb-178">ARM 处理器上的寄存器 R12。</span><span class="sxs-lookup"><span data-stu-id="016fb-178">Register R12 on the ARM processor.</span></span>|  
|`REGISTER_ARM_LR`|<span data-ttu-id="016fb-179">ARM 处理器上的链接寄存器 (R14)。</span><span class="sxs-lookup"><span data-stu-id="016fb-179">The link register (R14) on the ARM processor.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="016fb-180">备注</span><span class="sxs-lookup"><span data-stu-id="016fb-180">Remarks</span></span>  
 <span data-ttu-id="016fb-181">IA-64 处理器上共有 128 种通用数据寄存器和 128 种浮点数据寄存器，但只提供了值 `REGISTER_IA64_R0` 和 `REGISTER_IA64_F0`。</span><span class="sxs-lookup"><span data-stu-id="016fb-181">There are 128 general-purpose data registers and 128 floating-point data registers on the IA-64 processor, but only values `REGISTER_IA64_R0` and `REGISTER_IA64_F0` are provided.</span></span> <span data-ttu-id="016fb-182">可按如下方式确定其他值：</span><span class="sxs-lookup"><span data-stu-id="016fb-182">The other values can be determined as follows:</span></span>  
  
-   <span data-ttu-id="016fb-183">将寄存器号与 `REGISTER_IA64_R0` 相加，获得值 `REGISTER_IA64_R1` 到 `REGISTER_IA64_R127`（对应于 IA-64 处理器上的 #1 数据寄存器到 #127 数据寄存器）。</span><span class="sxs-lookup"><span data-stu-id="016fb-183">Add the register number to `REGISTER_IA64_R0` for values `REGISTER_IA64_R1` through `REGISTER_IA64_R127`, which correspond to the #1 data register through the #127 data register on the IA-64 processor.</span></span>  
  
-   <span data-ttu-id="016fb-184">将寄存器号与 `REGISTER_IA64_F0` 相加，获得值 `REGISTER_IA64_F1` 到 `REGISTER_IA64_F127`（对应于 IA-64 处理器上的 #1 FP 数据寄存器到 #127 FP 数据寄存器）。</span><span class="sxs-lookup"><span data-stu-id="016fb-184">Add the register number to `REGISTER_IA64_F0` for values `REGISTER_IA64_F1` through `REGISTER_IA64_F127`, which correspond to the #1 FP data register through the #127 FP data register on the IA-64 processor.</span></span>  
  
 <span data-ttu-id="016fb-185">例如，如果需要指定 IA-64 处理器上的 #83 数据寄存器，请使用 `REGISTER_IA64_R0` + 83。</span><span class="sxs-lookup"><span data-stu-id="016fb-185">For example, if you need to specify the #83 data register on the IA-64 processor, use `REGISTER_IA64_R0` + 83.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="016fb-186">要求</span><span class="sxs-lookup"><span data-stu-id="016fb-186">Requirements</span></span>  
 <span data-ttu-id="016fb-187">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="016fb-187">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="016fb-188">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="016fb-188">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="016fb-189">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="016fb-189">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="016fb-190">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="016fb-190">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="016fb-191">另请参阅</span><span class="sxs-lookup"><span data-stu-id="016fb-191">See Also</span></span>  
 [<span data-ttu-id="016fb-192">调试枚举</span><span class="sxs-lookup"><span data-stu-id="016fb-192">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)