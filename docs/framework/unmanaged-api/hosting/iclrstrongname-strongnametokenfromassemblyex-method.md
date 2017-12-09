---
title: "ICLRStrongName::StrongNameTokenFromAssemblyEx 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRStrongName.StrongNameTokenFromAssemblyEx
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRStrongName::StrongNameTokenFromAssemblyEx
helpviewer_keywords:
- StrongNameTokenFromAssemblyEx method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameTokenFromAssemblyEx method [.NET Framework hosting]
ms.assetid: 648ea90e-5e60-40a0-a56a-3e61bf2fba7c
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e46216f9e64d76188d60dbfcfc8e5113f2409b07
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="iclrstrongnamestrongnametokenfromassemblyex-method"></a><span data-ttu-id="08c1d-102">ICLRStrongName::StrongNameTokenFromAssemblyEx 方法</span><span class="sxs-lookup"><span data-stu-id="08c1d-102">ICLRStrongName::StrongNameTokenFromAssemblyEx Method</span></span>
<span data-ttu-id="08c1d-103">从指定的程序集文件中，创建强名称标记并返回标记表示的公钥。</span><span class="sxs-lookup"><span data-stu-id="08c1d-103">Creates a strong name token from the specified assembly file, and returns the public key that the token represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08c1d-104">语法</span><span class="sxs-lookup"><span data-stu-id="08c1d-104">Syntax</span></span>  
  
```  
HRESULT StrongNameTokenFromAssemblyEx (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="08c1d-105">参数</span><span class="sxs-lookup"><span data-stu-id="08c1d-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="08c1d-106">[in]程序集可移植可执行 (PE) 文件的路径。</span><span class="sxs-lookup"><span data-stu-id="08c1d-106">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="08c1d-107">[out]返回强名称标记。</span><span class="sxs-lookup"><span data-stu-id="08c1d-107">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="08c1d-108">[out]以字节为单位，强名称标记的大小。</span><span class="sxs-lookup"><span data-stu-id="08c1d-108">[out] The size, in bytes, of the strong name token.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="08c1d-109">[out]返回的公钥。</span><span class="sxs-lookup"><span data-stu-id="08c1d-109">[out] The returned public key.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="08c1d-110">[out]以字节为单位的公钥大小。</span><span class="sxs-lookup"><span data-stu-id="08c1d-110">[out] The size, in bytes, of the public key.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="08c1d-111">返回值</span><span class="sxs-lookup"><span data-stu-id="08c1d-111">Return Value</span></span>  
 <span data-ttu-id="08c1d-112">`S_OK`如果成功，则完成的方法否则为该值指示失败的 HRESULT 值 (请参阅[常见的 HRESULT 值](http://go.microsoft.com/fwlink/?LinkId=213878)有关的列表)。</span><span class="sxs-lookup"><span data-stu-id="08c1d-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="08c1d-113">备注</span><span class="sxs-lookup"><span data-stu-id="08c1d-113">Remarks</span></span>  
 <span data-ttu-id="08c1d-114">强名称标记是公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="08c1d-114">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="08c1d-115">令牌是从用于对程序集进行签名的公钥创建一个 64 位哈希。</span><span class="sxs-lookup"><span data-stu-id="08c1d-115">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="08c1d-116">该令牌属于的强名称的程序集，且可从程序集元数据中读取。</span><span class="sxs-lookup"><span data-stu-id="08c1d-116">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="08c1d-117">检索到密钥，并创建令牌后，应调用[iclrstrongname:: Strongnamefreebuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md)方法来释放分配的内存。</span><span class="sxs-lookup"><span data-stu-id="08c1d-117">After the key is retrieved and the token is created, you should call the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08c1d-118">要求</span><span class="sxs-lookup"><span data-stu-id="08c1d-118">Requirements</span></span>  
 <span data-ttu-id="08c1d-119">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08c1d-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08c1d-120">**标头：** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="08c1d-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="08c1d-121">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="08c1d-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="08c1d-122">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08c1d-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08c1d-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="08c1d-123">See Also</span></span>  
 [<span data-ttu-id="08c1d-124">StrongNameTokenFromAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="08c1d-124">StrongNameTokenFromAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md)  
 [<span data-ttu-id="08c1d-125">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="08c1d-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)