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
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519944"
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

## <a name="remarks"></a>Notes

Cette fonction est une application auxiliaire pour la création d’une fabrique WIC pour la liaison de DLL explicite, qui était nécessaire pour Windows XP. Dans un usage normal, vous pouvez utiliser [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) à la place (consultez [fabriques de classes d’API WIC](./-wic-api.md#class-factories)), car cela est toujours inclus dans toutes les versions plus récentes de Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>windowscodecs. lib</dt> </dl> |



 

