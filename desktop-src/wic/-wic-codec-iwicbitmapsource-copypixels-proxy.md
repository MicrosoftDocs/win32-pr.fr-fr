---
description: Fonction proxy pour la méthode CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e9c847680a93cb245b0e5d4247cb60b82629ea82eba12313dbcff7303dcce707
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772339"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a>\_ \_ Fonction Proxy copyPixels IWICBitmapSource

Fonction proxy pour la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Pointeur vers cet objet [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*PRC* \[ dans\]
</dt> <dd>

Type : **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***

Rectangle à copier. Une valeur NULL spécifie la bitmap entière.

</dd> <dt>

*cbStride* \[ dans\]
</dt> <dd>

Type : **uint**

STRIDE de la bitmap

</dd> <dt>

*cbBufferSize* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon.

</dd> <dt>

*pbBuffer* \[ à\]
</dt> <dd>

Type : **Byte \***

Pointeur vers la mémoire tampon.

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



 

 




