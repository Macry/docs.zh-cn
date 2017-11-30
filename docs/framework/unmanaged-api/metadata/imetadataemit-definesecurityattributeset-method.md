---
title: "IMetaDataEmit::DefineSecurityAttributeSet 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DefineSecurityAttributeSet
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DefineSecurityAttributeSet
helpviewer_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet method [.NET Framework metadata]
- DefineSecurityAttributeSet method [.NET Framework metadata]
ms.assetid: 27064ca2-4186-4433-90a7-3b297785e891
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 79d5bb7240305d06d916e969765606ddc2ddf9b0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitdefinesecurityattributeset-method"></a><span data-ttu-id="1a7d6-102">IMetaDataEmit::DefineSecurityAttributeSet 方法</span><span class="sxs-lookup"><span data-stu-id="1a7d6-102">IMetaDataEmit::DefineSecurityAttributeSet Method</span></span>
<span data-ttu-id="1a7d6-103">创建一组安全权限才能将附加到指定的标记所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-103">Creates a set of security permissions to attach to the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1a7d6-104">语法</span><span class="sxs-lookup"><span data-stu-id="1a7d6-104">Syntax</span></span>  
  
```  
HRESULT DefineSecurityAttributeSet (   
    [in]  mdToken       tkObj,   
    [in]  COR_SECATTR   rSecAttrs[],   
    [in]  ULONG         cSecAttrs,   
    [out] ULONG         *pulErrorAttr   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1a7d6-105">参数</span><span class="sxs-lookup"><span data-stu-id="1a7d6-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="1a7d6-106">[in]向其附加的安全信息的令牌。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-106">[in] The token to which the security information is attached.</span></span>  
  
 `rSecAttrs`  
 <span data-ttu-id="1a7d6-107">[in]数组`COR_SECATTR`结构。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-107">[in] An array of `COR_SECATTR` structures.</span></span>  
  
 `cSecAttrs`  
 <span data-ttu-id="1a7d6-108">[in]中的元素数`rSecAttrs`。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-108">[in] The number of elements in `rSecAttrs`.</span></span>  
  
 `pulErrorAttr`  
 <span data-ttu-id="1a7d6-109">[out]如果此方法失败，指定在索引`rSecAttrs`引起问题的原因的元素。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-109">[out] If the method fails, specifies the index in `rSecAttrs` of the element that caused the problem.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a7d6-110">要求</span><span class="sxs-lookup"><span data-stu-id="1a7d6-110">Requirements</span></span>  
 <span data-ttu-id="1a7d6-111">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1a7d6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a7d6-112">**标头：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1a7d6-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1a7d6-113">**库：**用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1a7d6-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1a7d6-114">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a7d6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a7d6-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1a7d6-115">See Also</span></span>  
 [<span data-ttu-id="1a7d6-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="1a7d6-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="1a7d6-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="1a7d6-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)