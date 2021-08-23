---
description: Obtient le format XML d’une référence jointe au jeton.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'IUpdateEndpointAuthToken :: TokenReferenceAttached, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: eae5e616e8583e2a1da8f8aa0882ea25160faad3f064734620466a0353736efe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793859"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>IUpdateEndpointAuthToken :: TokenReferenceAttached, méthode

Obtient le format XML d’une référence jointe au jeton.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszTokenReference* \[ à\]
</dt> <dd>

Pointeur vers la référence du jeton attaché.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite. sinon, retourne un code d’erreur COM ou Windows.

## <a name="remarks"></a>Remarques

Une référence jointe fait référence à un referece (tel que le signature qui utilise le jeton) qui se trouve dans le même message que celui où se trouve le jeton.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




