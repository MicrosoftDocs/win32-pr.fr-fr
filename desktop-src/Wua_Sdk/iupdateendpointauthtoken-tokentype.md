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
ms.openlocfilehash: a4479adc05eba8160098bd60c349645c4e30853abc693396f18f69ec722a06d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815290"
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

Retourne **S \_ OK** en cas de réussite. sinon, retourne un code d’erreur COM ou Windows.

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

 

 




