---
description: Fonction proxy pour la méthode GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536166"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a>\_Fonction de \_ proxy IWICBitmapDecoder GetColorContexts

Fonction proxy pour la méthode [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

Pointeur vers cet objet [_ *IWICBitmapDecoder* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*ompte* \[ dans\]
</dt> <dd>

Type : **uint**

Nombre de contextes de couleur à récupérer.

Cette valeur doit être inférieure ou égale à la taille disponible pour *ppIColorContexts*.

</dd> <dt>

*ppIColorContexts* \[ in, out\]
</dt> <dd>

Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Pointeur qui reçoit un pointeur vers [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).

</dd> <dt>

*pcActualCount* \[ à\]
</dt> <dd>

Type : **uint \** _

Pointeur qui reçoit le nombre de contextes de couleur contenus dans l’image.

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



 

 




