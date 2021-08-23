---
description: Fonction proxy pour la méthode SetColorContexts.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: IWICBitmapFrameEncode_SetColorContexts_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8f939c3ea5836c152e65f1fe0f5aff5ccf5941e1811691a41a6d8f44bc8ade3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812379"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a>\_ \_ Fonction proxy SetColorContexts IWICBitmapFrameEncode

Fonction proxy pour la méthode [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Pointeur vers cet objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .

</dd> <dt>

*ompte* \[ dans\]
</dt> <dd>

Type : **uint**

Nombre de profils [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) à définir.

</dd> <dt>

*ppIColorContext* \[ dans\]
</dt> <dd>

Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Pointeur vers un pointeur [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) contenant les profils de contextes de couleur à définir sur le frame.

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



 

 




