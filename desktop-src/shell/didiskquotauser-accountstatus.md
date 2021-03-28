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
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972002"
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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




