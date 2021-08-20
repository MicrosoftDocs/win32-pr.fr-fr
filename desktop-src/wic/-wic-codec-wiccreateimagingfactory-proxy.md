---
description: Fonction proxy pour la création du IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: c26ba9fbe1f230a4269fb6b71f15a39d00a80b4a3e1f19c3e5d8681e5008c5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033403"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>\_Fonction proxy WICCreateImagingFactory

Fonction proxy pour la création du [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*SDKVersion* \[ dans\]
</dt> <dd>

Type : **uint**

</dd> <dt>

*ppIImagingFactory* \[ à\]
</dt> <dd>

Type : **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

cette fonction est une application auxiliaire pour la création d’une fabrique WIC pour la liaison de DLL explicite, qui était nécessaire pour Windows XP. Dans un usage normal, vous pouvez utiliser [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) à la place (consultez [fabriques de classes d’API WIC](./-wic-api.md#class-factories)), car cela est toujours inclus dans toutes les versions plus récentes de Windows.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, Windows les \[ applications de bureau Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>windowscodecs. lib</dt> </dl> |



 

