---
description: Permet aux pages côté serveur hébergées dans un assistant de vérifier que l’utilisateur a été authentifié par le biais d’un compte Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Méthode NewWDEvents. PassportAuthenticate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235241"
---
# <a name="newwdeventspassportauthenticate-method"></a>Méthode NewWDEvents. PassportAuthenticate

Permet aux pages côté serveur hébergées dans un assistant de vérifier que l’utilisateur a été authentifié par le biais d’un compte Microsoft.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrSignInUrl* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Chaîne contenant l’URL d’une page Web qui redirige vers l’interface utilisateur de connexion compte Microsoft.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **booléen**

A la valeur **true** si l’authentification est réussie ; sinon, **false** .

## <a name="remarks"></a>Notes

Cette méthode peut être appelée même si un utilisateur est déjà connecté à un compte Microsoft. Dans ce cas, la méthode retourne la **valeur true** sans afficher l’interface utilisateur de connexion compte Microsoft.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

 
