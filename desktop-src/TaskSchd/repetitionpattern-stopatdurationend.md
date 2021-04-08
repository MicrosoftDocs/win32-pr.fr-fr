---
title: RepetitionPattern. StopAtDurationEnd, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique si une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- Planificateur de tâches de la propriété StopAtDurationEnd
- Planificateur de tâches de la propriété StopAtDurationEnd, objet RepetitionPattern
- Planificateur de tâches objet RepetitionPattern, propriété StopAtDurationEnd
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742437"
---
# <a name="repetitionpatternstopatdurationend-property"></a>RepetitionPattern. StopAtDurationEnd, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique si une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.

## <a name="syntax"></a>Syntaxe


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique si une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ces informations sont spécifiées dans l’élément [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) du schéma planificateur de tâches.

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

 

 





