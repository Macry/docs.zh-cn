---
title: ImportFileEx2 方法
ms.date: 03/30/2017
api_name:
- IALink2.ImportFileEx2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFileEx2
helpviewer_keywords:
- ImportFileEx2 method
ms.assetid: 02c789fd-16fc-48c6-9619-56e87e2a37ca
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: be6332c76b3dae9c02e1a939286b70438ee14cfb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33400674"
---
# <a name="importfileex2-method"></a>ImportFileEx2 方法
导入程序集和未绑定的模块。 此方法就像是[ImportFile 方法](../../../../docs/framework/unmanaged-api/alink/importfile-method.md)，但是如果即使正在导入的文件不存在磁盘上的工作。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT ImportFileEx2(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    IMetaDataAssemblyImport* pAssemblyScopeIn,  
    BOOL fSmartImport,  
    DWORD dwOpenFlags,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
#### <a name="parameters"></a>参数  
 `pszFilename`  
 要导入文件的名称。  
  
 `pszTargetName`  
 目标文件的可选名称。  
  
 `pAssemblyScopeIn`  
 可选的导入作用域[IMetaDataAssemblyImport 接口](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)接口。  
  
 `fSmartImport`  
 如果为 TRUE，则使用 ImportTypes，必须手动执行否则导入。  
  
 `dwOpenFlags`  
 要传递到标志[OpenScope 方法](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md)。  
  
 `pImportToken`  
 接收的程序集或文件的唯一 ID。  
  
 `ppAssemblyScope`  
 接收程序集导入作用域[IMetaDataAssemblyImport 接口](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)接口。 如果文件不是程序集，可以为 NULL。  
  
 `pdwCountOfScopes`  
 接收文件和/或导入的作用域的数。  
  
## <a name="return-value"></a>返回值  
 如果该方法成功，则返回，则为 S_OK。  
  
## <a name="requirements"></a>要求  
 需要 alink.h。  
  
## <a name="see-also"></a>请参阅  
 [IALink2 接口](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [IALink 接口](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [ALink API](../../../../docs/framework/unmanaged-api/alink/index.md)
