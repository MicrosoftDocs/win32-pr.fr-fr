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
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543712"
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

Tapez : **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Pointeur vers cet objet [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*puiWidth* \[ à\]
</dt> <dd>

Type : **uint \** _

Pointeur qui reçoit la largeur en pixels de l’image bitmap.

</dd> <dt>

_puiHeight * \[ out\]
</dt> <dd>

Type : **uint \** _

Pointeur qui reçoit la hauteur en pixels de la bitmap.

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



 

 




