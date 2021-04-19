---
description: Obtient le format XML d’une référence non attachée au jeton.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'IUpdateEndpointAuthToken :: TokenReferenceUnattached, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513435"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>IUpdateEndpointAuthToken :: TokenReferenceUnattached, méthode

Obtient le format XML d’une référence non attachée au jeton.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszTokenReference* \[ à\]
</dt> <dd>

Pointeur vers la référence du jeton non attaché.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite. Sinon, retourne un code d’erreur COM ou Windows.

## <a name="remarks"></a>Notes

Une référence non attachée fait référence à un referece (tel que le signature qui utilise le jeton) qui n’est pas dans le message où réside le jeton.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




