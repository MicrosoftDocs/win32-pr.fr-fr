---
title: Déclencheur. rerépétition, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Planificateur de tâches de la propriété de répétition
- Propriété de répétition Planificateur de tâches, objet déclencheur
- Planificateur de tâches de l’objet de déclencheur, propriété à répétition
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e14b8dc23b329d9646647fdcc1c5bcb3166c5bf885886a5308c329e186dc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002107"
---
# <a name="triggerrepetition-property"></a>Déclencheur. rerépétition, propriété

Pour les scripts, obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**RepetitionPattern**](repetitionpattern.md) qui définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, le modèle de répétition d’un déclencheur est spécifié dans l’élément de [**répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) du schéma planificateur de tâches.

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

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





