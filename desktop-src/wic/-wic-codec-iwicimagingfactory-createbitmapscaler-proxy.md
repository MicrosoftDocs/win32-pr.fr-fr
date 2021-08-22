---
description: Fonction proxy pour la méthode CreateBitmapScaler.
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: IWICImagingFactory_CreateBitmapScaler_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dd72049f72d14be41f1ef3601d04fd692af54271011849486ae72c1cce0e0e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711432"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateBitmapScaler

Fonction proxy pour la méthode [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Type : **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIBitmapScaler* \[ à\]
</dt> <dd>

Type : **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***

Pointeur qui reçoit un pointeur vers un nouveau [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).

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



 

 




