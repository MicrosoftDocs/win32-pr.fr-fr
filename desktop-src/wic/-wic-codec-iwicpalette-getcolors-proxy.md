---
description: Fonction proxy pour la méthode GetColors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203809"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>IWICPalette \_ \_ fonction proxy GetColors

Fonction proxy pour la méthode [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Pointeur vers cet objet [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*colorCount* \[ dans\]
</dt> <dd>

Type : **uint**

Taille du tableau *pColors* .

</dd> <dt>

*pColors* \[ à\]
</dt> <dd>

Tapez : **WICColor \** _

Pointeur qui reçoit les couleurs de la palette.

</dd> <dt>

_pcActualColors * \[ out\]
</dt> <dd>

Type : **uint \** _

Taille réelle nécessaire pour obtenir les couleurs de la palette.

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



 

 




