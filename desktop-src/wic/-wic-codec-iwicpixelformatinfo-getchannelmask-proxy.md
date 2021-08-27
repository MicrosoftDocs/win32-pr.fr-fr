---
description: Fonction proxy pour la méthode GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee200dddf0b2cd736ca2ad435b63e774076465ad3d1f6215f1c558f1abb6c194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056599"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>IWICPixelFormatInfo \_ \_ fonction proxy GetChannelMask

Fonction proxy pour la méthode [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Pointeur vers cet objet [**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

</dd> <dt>

*uiChannelIndex* \[ dans\]
</dt> <dd>

Type : **uint**

Index du masque de canal à récupérer.

</dd> <dt>

*cbMaskBuffer* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon *pbMaskBuffer* .

</dd> <dt>

*pbMaskBuffer* \[ in, out\]
</dt> <dd>

Type : **Byte \***

Pointeur vers la mémoire tampon du masque.

</dd> <dt>

*pcbActual* \[ à\]
</dt> <dd>

Type : **uint \***

Taille réelle de la mémoire tampon nécessaire pour obtenir le masque de canal.

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



 

 




