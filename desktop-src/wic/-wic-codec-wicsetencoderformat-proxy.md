---
description: Fonction proxy pour négocier le format de pixel et la palette pour l’encodeur.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: WICSetEncoderFormat_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541820"
---
# <a name="wicsetencoderformat_proxy-function"></a>\_Fonction proxy WICSetEncoderFormat

Fonction proxy pour négocier le format de pixel et la palette pour l’encodeur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceIn* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Pointeur vers la bitmap source.

</dd> <dt>

_pIPalette * \[ dans\]
</dt> <dd>

Tapez : **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Pointeur vers la palette à utiliser pour l’encodage.

</dd> <dt>

_pIFrameEncode * \[ dans\]
</dt> <dd>

Type : **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _

Pointeur vers l’objet de codage de frame.

</dd> <dt>

_ppSourceOut * \[ out\]
</dt> <dd>

Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Pointeur qui reçoit un pointeur vers la source de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




