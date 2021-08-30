---
description: Fonction proxy pour la méthode DoesSupportLossless.
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: IWICBitmapCodecInfo_DoesSupportLossless_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f102a487e76667cc3a1cfb9c3bf0c2153d661199b36cbef86fec3f7f111d2f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090059"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a>IWICBitmapCodecInfo \_ \_ fonction proxy DoesSupportLossless

Fonction proxy pour la méthode [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Pointeur vers cet objet [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*pfSupportLossless* \[ à\]
</dt> <dd>

Type : **bool \***

Pointeur qui reçoit la **valeur true** si le codec prend en charge les formats sans perte ; Sinon, **false**.

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



 

 




