---
description: Fonction proxy pour la méthode GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: IWICPalette_GetType_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1c4b9c0d17b37be8ff2d5db85f112e528b0d9e447856e387c63a5f436d59376a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668171"
---
# <a name="iwicpalette_gettype_proxy-function"></a>IWICPalette \_ \_ fonction proxy GetType

Fonction proxy pour la méthode [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Pointeur vers cet objet [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*pePaletteType* \[ à\]
</dt> <dd>

Type : **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\***

Pointeur qui reçoit le type de palette du bimtap.

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



 

 




