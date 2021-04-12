---
description: Obtient le type du jeton de point de terminaison, tel qu’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'IUpdateEndpointAuthToken :: TokenType, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526679"
---
# <a name="iupdateendpointauthtokentokentype-method"></a>IUpdateEndpointAuthToken :: TokenType, méthode

Obtient le type du jeton de point de terminaison, tel qu’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTokenType* \[ à\]
</dt> <dd>

Type du jeton de point de terminaison.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite. Sinon, retourne un code d’erreur COM ou Windows.

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

 

 




