---
description: Obtient les données XML (envoyées sur le réseau) qui représentent le jeton.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'IUpdateEndpointAuthToken :: TokenData, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512992"
---
# <a name="iupdateendpointauthtokentokendata-method"></a>IUpdateEndpointAuthToken :: TokenData, méthode

Obtient les données XML (envoyées sur le réseau) qui représentent le jeton.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszTokenData* \[ à\]
</dt> <dd>

Données XML (envoyées sur le réseau) qui représentent le jeton. Par exemple, les données d’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1 est le code SAML qui est ajouté à la requête.

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

 

 




