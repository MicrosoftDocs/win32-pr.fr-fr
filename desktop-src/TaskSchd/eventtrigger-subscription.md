---
title: Propriété EventTrigger. subscription
description: Pour les scripts, obtient ou définit une chaîne de requête qui identifie l’événement qui déclenche le déclencheur.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Planificateur de tâches de propriété d’abonnement
- Planificateur de tâches de propriété d’abonnement, objet EventTrigger
- Objet EventTrigger Planificateur de tâches, propriété Subscription
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008662"
---
# <a name="eventtriggersubscription-property"></a>Propriété EventTrigger. subscription

Pour les scripts, obtient ou définit une chaîne de requête qui identifie l’événement qui déclenche le déclencheur.

## <a name="syntax"></a>Syntaxe


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne de requête qui identifie l’événement qui déclenche le déclencheur.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, l’abonnement aux événements est spécifié à l’aide de l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) du schéma planificateur de tâches.

Pour plus d’informations sur l’écriture d’une chaîne de requête pour certains événements, consultez [sélection d’événements](/previous-versions//aa385231(v=vs.85)) et [abonnement à des événements](../wes/subscribing-to-events.md).

## <a name="examples"></a>Exemples

La chaîne de requête suivante définit un abonnement à tous les événements de niveau 2 dans le canal système :


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

