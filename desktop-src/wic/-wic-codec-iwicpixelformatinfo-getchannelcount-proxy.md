---
description: Fonction proxy pour la méthode GetChannelCount.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eaaf0abc2c32e7a5a4469a3959875e28bb29d840f9da43f9bbbcc88fe56df788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812119"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a>IWICPixelFormatInfo \_ \_ fonction proxy GetChannelCount

Fonction proxy pour la méthode [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Pointeur vers cet objet [**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

</dd> <dt>

*puiChannelCount* \[ à\]
</dt> <dd>

Type : **uint \***

Pointeur qui reçoit le nombre de canaux.

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



 

 




