---
title: Élément StopAtDurationEnd (repetitionType)
description: Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Élément StopAtDurationEnd Planificateur de tâches
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538614"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Élément StopAtDurationEnd (repetitionType)

Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition. Cela s’applique uniquement si des répétitions sont définies.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

L’élément **StopAtDurationEnd** est défini par le type complexe [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Élément parent

| Élément | Dérivé de | Description |
|-|-|-|
| [**Répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/> |

## <a name="remarks"></a>Notes

Pour le développement de script, ce paramètre est spécifié à l’aide de la propriété [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .

Pour le développement C++, ce paramètre est spécifié à l’aide de la propriété [**IRepetitionPattern :: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |

## <a name="see-also"></a>Voir aussi

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)

[Planificateur de tâches](task-scheduler-start-page.md)
