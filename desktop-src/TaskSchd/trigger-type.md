---
title: Propriété Trigger. type
description: Pour les scripts, obtient le type du déclencheur.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Planificateur de tâches de propriété de type
- Propriété type Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857248"
---
# <a name="triggertype-property"></a>Propriété Trigger. type

Pour les scripts, obtient le type du déclencheur. Le type de déclencheur est défini lors de la création du déclencheur et ne peut pas être modifié ultérieurement. Pour plus d’informations sur la création d’un déclencheur, consultez [**TriggerCollection. Create**](triggercollection-create.md).

## <a name="syntax"></a>Syntaxe


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valeur de la propriété

L’une des [**tâches suivantes \_ déclenchent \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) des valeurs d’énumération type2.



| Valeur                                                                                                                                                                                                                                                                                | Signification                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Tâche \_ DÉCLENCHER l' \_ événement**</dt> <dt>0</dt> </dl>                                                 | Démarre la tâche lorsqu’un événement spécifique se produit.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Tâche \_ \_Heure du déclencheur**</dt> <dt>1</dt> </dl>                                                    | Démarre la tâche à une heure spécifique de la journée.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ quotidien**</dt> <dt>2</dt> </dl>                                                 | Démarre la tâche quotidiennement.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ hebdomadaire**</dt> <dt>3</dt> </dl>                                              | Démarre la tâche toutes les semaines.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ mensuel**</dt> <dt>4</dt> </dl>                                           | Démarre la tâche tous les mois.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Démarre la tâche chaque mois à un jour spécifique de la semaine.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ inactif**</dt> <dt>6</dt> </dl>                                                    | Démarre la tâche lorsque l’ordinateur passe en état d’inactivité.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Tâche \_ \_Inscription du déclencheur**</dt> <dt>7</dt> </dl>                            | Démarre la tâche lorsque la tâche est inscrite.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Tâche \_ DÉCLENCHER le \_ démarrage**</dt> <dt>8</dt> </dl>                                                    | Démarre la tâche au démarrage de l’ordinateur.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Tâche \_ DÉCLENCHER l' \_ ouverture de session**</dt> <dt>9</dt> </dl>                                                 | Démarre la tâche lorsqu’un utilisateur spécifique ouvre une session.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Tâche \_ \_Changement d' \_ état \_ de session du déclencheur**</dt> <dt>11</dt> </dl> | Déclenche la tâche lorsqu’un état de session spécifique change.<br/>   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> <dt>

[**\_Déclencheur de tâche \_ type2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





