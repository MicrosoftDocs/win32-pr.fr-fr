---
description: Fonction proxy pour la méthode CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8391b7ce90e99d03e53951afa64a53de87f464e88a906444e0b379545c37fc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033642"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateComponentInfo

Fonction proxy pour la méthode [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Type : **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*clsidComponent* \[ dans\]
</dt> <dd>

Type : **REFCLSID**

CLSID du composant souhaité.

</dd> <dt>

*ppIInfo* \[ à\]
</dt> <dd>

Type : **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***

Pointeur qui reçoit un pointeur vers un nouveau [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, Windows les \[ applications de bureau Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




