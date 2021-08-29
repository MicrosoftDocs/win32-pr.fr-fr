---
description: Obtient l’état du compte de l’utilisateur.
title: DIDiskQuotaUser. AccountStatus, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: 06339659333a18334dae2e0604f0ad456699cef7f8343fd6dc00043bf782e01f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090759"
---
# <a name="didiskquotauseraccountstatus-property"></a>DIDiskQuotaUser. AccountStatus, propriété

Obtient l’état du compte de l’utilisateur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété peut prendre l’une des valeurs suivantes.



| Statut            | Valeur | Description                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | Les informations de compte sont résolues.    |
| dqAcctUnavailable | 1     | Les informations de compte ne sont pas disponibles. |
| dqAcctDeleted     | 2     | Le compte a été supprimé.           |
| dqAcctInvalid     | 3     | Le compte n’est pas valide.                 |
| dqAcctUnknown     | 4     | Le compte est introuvable.            |
| dqAcctUnresolved  | 5     | Les informations de compte ne sont pas résolues.  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




