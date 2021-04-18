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
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210287"
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

Tapez : **[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

Pointeur vers cet objet [_ *IWICPixelFormatInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

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

Type : **Byte \** _

Pointeur vers la mémoire tampon du masque.

</dd> <dt>

_pcbActual * \[ out\]
</dt> <dd>

Type : **uint \** _

Taille réelle de la mémoire tampon nécessaire pour obtenir le masque de canal.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




