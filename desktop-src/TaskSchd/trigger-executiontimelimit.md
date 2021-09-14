---
title: Propriété Trigger. ExecutionTimeLimit
description: Pour les scripts, obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Planificateur de tâches de la propriété ExecutionTimeLimit
- Propriété ExecutionTimeLimit Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233009"
---
# <a name="triggerexecutiontimelimit-property"></a>Propriété Trigger. ExecutionTimeLimit

Pour les scripts, obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.

## <a name="syntax"></a>Syntaxe


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valeur de la propriété

Durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, la limite de temps d’exécution est spécifiée dans l’élément [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) du schéma planificateur de tâches.

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
</dt> </dl>

 

 





