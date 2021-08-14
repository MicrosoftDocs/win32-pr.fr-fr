---
description: Fonction proxy pour la méthode GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b693c78ba3a3d7c68c33f68ec1494997536ffb10272cc384d89d9e94ded7145b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206745"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>\_ \_ Fonction proxy IWICBitmapLock GetDataPointer STA \_

Fonction proxy pour la méthode [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\***

Pointeur vers cet objet [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

</dd> <dt>

*pcbBufferSize* \[ à\]
</dt> <dd>

Type : **uint \***

Pointeur qui reçoit la taille de la mémoire tampon.

</dd> <dt>

*ppbData* \[ à\]
</dt> <dd>

Type : **Byte \* \***

Pointeur qui reçoit un pointeur vers le pixel supérieur gauche dans le rectangle verrouillé.

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



 

 




