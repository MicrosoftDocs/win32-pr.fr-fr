---
title: RepetitionPattern. Duration, propriété
description: Pour les scripts, obtient ou définit la durée de répétition du modèle.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Propriété Duration Planificateur de tâches
- Propriété Duration Planificateur de tâches, objet RepetitionPattern
- Planificateur de tâches objet RepetitionPattern, propriété Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510154"
---
# <a name="repetitionpatternduration-property"></a>RepetitionPattern. Duration, propriété

Pour les scripts, obtient ou définit la durée de répétition du modèle.

## <a name="syntax"></a>Syntaxe


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>Valeur de la propriété

Durée de répétition du modèle. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). La durée minimale autorisée est d’une minute.

Si aucune valeur n’est spécifiée pour la durée, le modèle est répété indéfiniment.

## <a name="remarks"></a>Notes

Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.

Lors de la lecture ou de l’écriture de données XML pour une tâche, la durée de répétition est spécifiée dans l’élément [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) du schéma planificateur de tâches.

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

 

 





