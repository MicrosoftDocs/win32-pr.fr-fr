---
title: Objet IdleTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’une condition d’inactivité se produit.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Planificateur de tâches de déclencheur inactif, objet
- Objet IdleTrigger Planificateur de tâches
- Planificateur de tâches d’objets IdleTrigger, Description
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a3c538dbd04f3eb20a86f495fcf4a8b027b51fbe5cd6443cd8ff3a69ac6ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621139"
---
# <a name="idletrigger-object"></a>Objet IdleTrigger

Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’une condition d’inactivité se produit. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).

## <a name="members"></a>Membres

L’objet **IdleTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **IdleTrigger** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**activé**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.<br/>                                                 |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                                             |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                                            |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                                            |



 

## <a name="remarks"></a>Remarques

Un déclencheur inactif déclenche une action de tâche uniquement si l’ordinateur passe en état d’inactivité après la limite de démarrage du déclencheur.

Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur inactif est spécifié à l’aide de l’élément [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) du schéma planificateur de tâches.

Si une tâche est déclenchée par un déclencheur inactif, la propriété [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) est ignorée.

Si l’instance initiale d’une tâche avec un déclencheur inactif est toujours en cours d’exécution, la tâche est lancée une seule fois sans répétitions, même si plusieurs répétitions sont définies dans la propriété [**répétition**](trigger-repetition.md) . Ce comportement ne se produit pas si la tâche s’arrête de lui-même.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Déclencheur**](trigger.md)
</dt> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





