---
title: "ICLRErrorReportingManager::GetBucketParametersForCurrentException 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRErrorReportingManager.GetBucketParametersForCurrentException
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRErrorReportingManager::GetBucketParametersForCurrentException
helpviewer_keywords:
- ICLRErrorReportingManager::GetBucketParametersForCurrentException method [.NET Framework hosting]
- GetBucketParametersForCurrentException method [.NET Framework hosting]
ms.assetid: a13ec8a6-8e18-4acb-8054-77f5b1a0e0b9
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 80bf3e9b1cee9f19534f985dccf4508467dbe26e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="iclrerrorreportingmanagergetbucketparametersforcurrentexception-method"></a><span data-ttu-id="6fb4a-102">ICLRErrorReportingManager::GetBucketParametersForCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="6fb4a-102">ICLRErrorReportingManager::GetBucketParametersForCurrentException Method</span></span>
<span data-ttu-id="6fb4a-103">获取在调用线程上的当前异常的 Watson bucket。</span><span class="sxs-lookup"><span data-stu-id="6fb4a-103">Gets the Watson bucket for the current exception on the calling thread.</span></span>  
  
 <span data-ttu-id="6fb4a-104">A*存储桶*是与相同的代码缺陷相关的错误数据的集合。</span><span class="sxs-lookup"><span data-stu-id="6fb4a-104">A *bucket* is a collection of error data that is related to the same code defect.</span></span> <span data-ttu-id="6fb4a-105">*Watson*指一套用于收集和分析与异常关联的数据的技术。</span><span class="sxs-lookup"><span data-stu-id="6fb4a-105">*Watson* refers to a set of technologies for collecting and analyzing data that is associated with an exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6fb4a-106">语法</span><span class="sxs-lookup"><span data-stu-id="6fb4a-106">Syntax</span></span>  
  
```  
HRESULT GetBucketParametersForCurrentException(  
    [out] BucketParameters *pParams  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6fb4a-107">参数</span><span class="sxs-lookup"><span data-stu-id="6fb4a-107">Parameters</span></span>  
 `pParams`  
 <span data-ttu-id="6fb4a-108">[out]指向的指针[BucketParameters](../../../../docs/framework/unmanaged-api/hosting/bucketparameters-structure.md)包含异常的错误数据的结构。</span><span class="sxs-lookup"><span data-stu-id="6fb4a-108">[out] A pointer to a [BucketParameters](../../../../docs/framework/unmanaged-api/hosting/bucketparameters-structure.md) structure that contains error data for the exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6fb4a-109">要求</span><span class="sxs-lookup"><span data-stu-id="6fb4a-109">Requirements</span></span>  
 <span data-ttu-id="6fb4a-110">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6fb4a-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6fb4a-111">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6fb4a-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6fb4a-112">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="6fb4a-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6fb4a-113">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6fb4a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fb4a-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6fb4a-114">See Also</span></span>  
 [<span data-ttu-id="6fb4a-115">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="6fb4a-115">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)