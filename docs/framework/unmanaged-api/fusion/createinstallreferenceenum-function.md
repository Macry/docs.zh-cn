---
title: "CreateInstallReferenceEnum 函数"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type: DLLExport
f1_keywords: CreateInstallReference
helpviewer_keywords: CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 07c7ec72a66b37798e6e2af523bb024e9dd63d9a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="createinstallreferenceenum-function"></a><span data-ttu-id="00329-102">CreateInstallReferenceEnum 函数</span><span class="sxs-lookup"><span data-stu-id="00329-102">CreateInstallReferenceEnum Function</span></span>
<span data-ttu-id="00329-103">获取一个指向[IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)表示的指定程序集的应用程序的引用列表的实例。</span><span class="sxs-lookup"><span data-stu-id="00329-103">Gets a pointer to an [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instance that represents a list of an application's references to the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00329-104">语法</span><span class="sxs-lookup"><span data-stu-id="00329-104">Syntax</span></span>  
  
```  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="00329-105">参数</span><span class="sxs-lookup"><span data-stu-id="00329-105">Parameters</span></span>  
 `ppRefEnum`  
 <span data-ttu-id="00329-106">[out]返回`IInstallReferenceEnum`指针。</span><span class="sxs-lookup"><span data-stu-id="00329-106">[out] The returned `IInstallReferenceEnum` pointer.</span></span>  
  
 `pName`  
 <span data-ttu-id="00329-107">[in][IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) ，它标识要枚举引用的程序集。</span><span class="sxs-lookup"><span data-stu-id="00329-107">[in] The [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) that identifies the assembly for which to enumerate references.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="00329-108">[in]影响枚举器的行为的标志。</span><span class="sxs-lookup"><span data-stu-id="00329-108">[in] Flags that influence the enumerator's behavior.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="00329-109">[in]留待将来扩展。</span><span class="sxs-lookup"><span data-stu-id="00329-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="00329-110">`pvReserved`必须是 null 引用。</span><span class="sxs-lookup"><span data-stu-id="00329-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00329-111">要求</span><span class="sxs-lookup"><span data-stu-id="00329-111">Requirements</span></span>  
 <span data-ttu-id="00329-112">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="00329-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00329-113">**标头：** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="00329-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="00329-114">**库：**为 Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="00329-114">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="00329-115">使用而不是 Mscorwks.dll 为 Fusion.dll 来确保面向.NET Framework 的正确版本。</span><span class="sxs-lookup"><span data-stu-id="00329-115">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="00329-116">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00329-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00329-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00329-117">See Also</span></span>  
 [<span data-ttu-id="00329-118">IInstallReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="00329-118">IInstallReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)  
 [<span data-ttu-id="00329-119">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="00329-119">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="00329-120">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="00329-120">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)