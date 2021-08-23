---
description: Fonction proxy pour la méthode GetFriendlyName.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5af41c00945550fc9e833b9324e22f522aa7a5e73dacd109d76159d5dd0173db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965248"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>IWICComponentInfo \_ \_ fonction proxy GetFriendlyName

Fonction proxy pour la méthode [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Pointeur vers cet objet [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchFriendlyName* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon *wzFriendlyName* .

</dd> <dt>

*wzFriendlyName* \[ in, out\]
</dt> <dd>

Type : **WCHAR \***

Pointeur qui reçoit le nom convivial du composant.

La chaîne retournée est spécifique aux paramètres régionaux, 1033 par défaut.

</dd> <dt>

*pcchActual* \[ à\]
</dt> <dd>

Type : **uint \***

Pointeur qui reçoit la longueur réelle du nom convivial du composant.

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



 

 




