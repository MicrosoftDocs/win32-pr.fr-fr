---
title: TaskSettings.Exepropriété cutionTimeLimit
description: Pour les scripts, obtient ou définit la durée autorisée pour terminer la tâche.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Planificateur de tâches de la propriété ExecutionTimeLimit
- Planificateur de tâches de la propriété ExecutionTimeLimit, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509343"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>TaskSettings.Exepropriété cutionTimeLimit

Pour les scripts, obtient ou définit la durée autorisée pour terminer la tâche. Par défaut, une tâche sera arrêtée 72 heures après son démarrage. Vous pouvez modifier ce paramètre en modifiant ce paramètre.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valeur de la propriété

Durée autorisée pour terminer la tâche. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). La valeur PT0S permet à la tâche de s’exécuter indéfiniment. Lorsque ce paramètre a la valeur Nothing, la limite de durée d’exécution est infinie.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





