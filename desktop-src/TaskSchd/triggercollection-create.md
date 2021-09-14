---
title: TriggerCollection. Create, méthode
description: Pour les scripts, crée un nouveau déclencheur pour la tâche.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- déclenche Planificateur de tâches, création
- Créer une méthode Planificateur de tâches
- Create Method Planificateur de tâches, objet TriggerCollection
- Planificateur de tâches d’objets TriggerCollection, méthode Create
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857229"
---
# <a name="triggercollectioncreate-method"></a>TriggerCollection. Create, méthode

Pour les scripts, crée un nouveau déclencheur pour la tâche.

## <a name="syntax"></a>Syntaxe


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Ce paramètre est défini sur l’une des constantes d’énumération [**\_ \_ type2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) de la tâche suivante.



| Valeur                                                                                                                                                                                                                                                                                | Signification                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Tâche \_ DÉCLENCHER l' \_ événement**</dt> <dt>0</dt> </dl>                                                 | Déclenche la tâche lorsqu’un événement spécifique se produit.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Tâche \_ \_Heure du déclencheur**</dt> <dt>1</dt> </dl>                                                    | Déclenche la tâche à une heure spécifique de la journée.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ quotidien**</dt> <dt>2</dt> </dl>                                                 | Déclenche la tâche selon une planification quotidienne. Par exemple, la tâche commence à une heure spécifique tous les jours, tous les jours, tous les trois jours, et ainsi de suite.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ hebdomadaire**</dt> <dt>3</dt> </dl>                                              | Déclenche la tâche selon une planification hebdomadaire. Par exemple, la tâche commence à 8:00 AM pour un jour spécifique chaque semaine ou une autre semaine.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ mensuel**</dt> <dt>4</dt> </dl>                                           | Déclenche la tâche selon une planification mensuelle. Par exemple, la tâche démarre sur des jours spécifiques de mois spécifiques.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Déclenche la tâche selon une planification mensuelle de jour de semaine. Par exemple, la tâche démarre à des jours spécifiques de la semaine, des semaines du mois et des mois de l’année.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Tâche \_ DÉCLENCHEur \_ inactif**</dt> <dt>6</dt> </dl>                                                    | Déclenche la tâche lorsque l’ordinateur passe en état d’inactivité.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Tâche \_ \_Inscription du déclencheur**</dt> <dt>7</dt> </dl>                            | Déclenche la tâche lorsque la tâche est inscrite.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Tâche \_ DÉCLENCHER le \_ démarrage**</dt> <dt>8</dt> </dl>                                                    | Déclenche la tâche au démarrage de l’ordinateur.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Tâche \_ DÉCLENCHER l' \_ ouverture de session**</dt> <dt>9</dt> </dl>                                                 | Déclenche la tâche lorsqu’un utilisateur spécifique ouvre une session.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Tâche \_ \_Changement d' \_ état \_ de session du déclencheur**</dt> <dt>11</dt> </dl> | Déclenche la tâche lorsqu’un état de session spécifique change.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Objet de [**déclencheur**](trigger.md) qui représente le nouveau déclencheur.

## <a name="remarks"></a>Notes

Pour plus d’informations sur chaque type de déclencheur, consultez [types de déclencheurs](trigger-types.md).

## <a name="requirements"></a>Spécifications



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

[**Déclencheur**](trigger.md)
</dt> </dl>

 

 





