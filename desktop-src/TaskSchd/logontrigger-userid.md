---
title: LogonTrigger. UserId, propriété
description: Pour les scripts, obtient ou définit l’identificateur de l’utilisateur.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserId, propriété Planificateur de tâches
- UserId, propriété Planificateur de tâches, objet LogonTrigger
- Objet LogonTrigger Planificateur de tâches, UserId, propriété
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384107"
---
# <a name="logontriggeruserid-property"></a>LogonTrigger. UserId, propriété

Pour les scripts, obtient ou définit l’identificateur de l’utilisateur.

## <a name="syntax"></a>Syntaxe


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur de l’utilisateur. Par exemple, « MyDomain \\ myname » ou pour un compte local, « administrateur ».

Cette propriété peut être dans l’un des formats suivants :

-   Nom d’utilisateur ou SID : la tâche est démarrée lorsque l’utilisateur ouvre une session sur l’ordinateur.
-   NULL : la tâche est démarrée quand un utilisateur ouvre une session sur l’ordinateur.

## <a name="remarks"></a>Notes

Si vous souhaitez qu’une tâche soit déclenchée lorsqu’un membre d’un groupe se connecte à l’ordinateur plutôt qu’à un utilisateur spécifique, n’affectez pas de valeur à la propriété **LogonTrigger. UserID** . Au lieu de cela, créez un déclencheur LOGON avec une propriété **LogonTrigger. UserID** vide et attribuez une valeur au principal pour la tâche à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur d’utilisateur d’ouverture de session est spécifié à l’aide de l’élément [**userid**](taskschedulerschema-userid-logontriggertype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





