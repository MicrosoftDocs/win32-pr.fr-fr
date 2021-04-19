---
title: Objet SessionStateChangeTrigger
description: Objet de script qui déclenche des tâches pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Objet SessionStateChangeTrigger Planificateur de tâches
- Planificateur de tâches d’objets SessionStateChangeTrigger, Description
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511545"
---
# <a name="sessionstatechangetrigger-object"></a>Objet SessionStateChangeTrigger

Objet de script qui déclenche des tâches pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail.

## <a name="members"></a>Membres

L’objet **SessionStateChangeTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **SessionStateChangeTrigger** a ces propriétés.



| Propriété                                                                | Type d’accès           | Description                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retard**](sessionstatechangetrigger-delay.md)<br/>             | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique la durée d’un délai avant le démarrage d’une tâche après la détection d’un changement d’état de session Terminal Server.<br/>                                         |
| [**Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                              |
| [**EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/>               |
| [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.<br/>                                                 |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                                             |
| [**Répétition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | Lecture/écriture<br/> | Obtient ou définit le type de Terminal Server modification de session qui déclenche un lancement de tâche.<br/>                                                                                                      |
| [**Entrer**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                                            |
| [**IDutilisateur**](sessionstatechangetrigger-userid.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’utilisateur pour la session de Terminal Server. Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.<br/>                                                               |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, un déclencheur de changement d’état de session est spécifié à l’aide de l’élément [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





