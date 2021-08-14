---
description: Fonction proxy pour la méthode de traitement.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1a0892fea469180a0d06eded30e4459667513acbf66d56161d81788c1a17820f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711642"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a>IWICBitmapSource \_ obtient la \_ fonction proxy

Fonction proxy [**pour la méthode de traitement**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Pointeur vers cet objet [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*puiWidth* \[ à\]
</dt> <dd>

Type : **uint \***

Pointeur qui reçoit la largeur en pixels de l’image bitmap.

</dd> <dt>

*puiHeight* \[ à\]
</dt> <dd>

Type : **uint \***

Pointeur qui reçoit la hauteur en pixels de la bitmap.

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



 

 




