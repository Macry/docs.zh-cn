---
title: "StackOverflowInfo 结构"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StackOverflowInfo
api_location: mscoree.dll
api_type: COM
f1_keywords: StackOverflowInfo
helpviewer_keywords: StackOverflowInfo structure [.NET Framework hosting]
ms.assetid: 519389f2-0217-436c-99d4-93a76ebce5b5
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 102f744ecc769a10161cd20767e8e49c838252a7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="stackoverflowinfo-structure"></a><span data-ttu-id="8d166-102">StackOverflowInfo 结构</span><span class="sxs-lookup"><span data-stu-id="8d166-102">StackOverflowInfo Structure</span></span>
<span data-ttu-id="8d166-103">由于溢出时引发的异常上存储的溢出发生和信息的类型。</span><span class="sxs-lookup"><span data-stu-id="8d166-103">Stores the type of overflow that occurred and information on the exception that was thrown due to the overflow.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d166-104">语法</span><span class="sxs-lookup"><span data-stu-id="8d166-104">Syntax</span></span>  
  
```  
typedef struct _StackOverflowInfo {  
    StackOverflowType   soType;  
    EXCEPTION_POINTERS  *pExceptionInfo;  
} StackOverflowInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="8d166-105">成员</span><span class="sxs-lookup"><span data-stu-id="8d166-105">Members</span></span>  
  
|<span data-ttu-id="8d166-106">成员</span><span class="sxs-lookup"><span data-stu-id="8d166-106">Member</span></span>|<span data-ttu-id="8d166-107">描述</span><span class="sxs-lookup"><span data-stu-id="8d166-107">Description</span></span>|  
|------------|-----------------|  
|`soType`|<span data-ttu-id="8d166-108">值为[StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md)指定溢出的类型的枚举。</span><span class="sxs-lookup"><span data-stu-id="8d166-108">A value of the [StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md) enumeration that specifies the type of overflow.</span></span>|  
|`pExceptionInfo`|<span data-ttu-id="8d166-109">一个指向 Win32`EXCEPTION_POINTERS`对象，其中包含一个异常记录异常的独立于计算机的说明和在异常发生时的处理器上下文依赖于计算机的说明的上下文记录。</span><span class="sxs-lookup"><span data-stu-id="8d166-109">A pointer to a Win32 `EXCEPTION_POINTERS` object, which contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8d166-110">备注</span><span class="sxs-lookup"><span data-stu-id="8d166-110">Remarks</span></span>  
 <span data-ttu-id="8d166-111">A`StackOverflowInfo`对象传递给[iactiononclrevent:: Onevent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)方法`Event_StackOverflow`事件。</span><span class="sxs-lookup"><span data-stu-id="8d166-111">A `StackOverflowInfo` object is passed to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method for `Event_StackOverflow` events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d166-112">要求</span><span class="sxs-lookup"><span data-stu-id="8d166-112">Requirements</span></span>  
 <span data-ttu-id="8d166-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8d166-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d166-114">**标头：** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="8d166-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="8d166-115">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8d166-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8d166-116">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d166-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d166-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d166-117">See Also</span></span>  
 [<span data-ttu-id="8d166-118">承载结构</span><span class="sxs-lookup"><span data-stu-id="8d166-118">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)