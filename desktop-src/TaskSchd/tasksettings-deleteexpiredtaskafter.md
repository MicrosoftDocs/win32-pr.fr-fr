---
title: TaskSettings. DeleteExpiredTaskAfter, propriété
description: Pour les scripts, obtient ou définit la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Planificateur de tâches de la propriété DeleteExpiredTaskAfter
- Planificateur de tâches de la propriété DeleteExpiredTaskAfter, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464802"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>TaskSettings. DeleteExpiredTaskAfter, propriété

Pour les scripts, obtient ou définit la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration. Si aucune valeur n’est spécifiée pour cette propriété, le service Planificateur de tâches ne supprimera pas la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui obtient ou définit la durée d’attente de la Planificateur de tâches avant de supprimer la tâche après son expiration. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).

## <a name="remarks"></a>Notes

Une tâche expire une fois que la limite de fin a été dépassée pour tous les déclencheurs associés à la tâche. La limite de fin d’un déclencheur est spécifiée par la propriété [EndBoundary](trigger-endboundary.md) héritée par tous les objets déclencheurs.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





