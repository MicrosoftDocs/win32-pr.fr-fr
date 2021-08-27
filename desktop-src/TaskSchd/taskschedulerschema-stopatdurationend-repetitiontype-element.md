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
ms.openlocfilehash: 896aa6db4ce5bf2c0dddf666024c143754afc97ec76bfb557e6431f593689857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010539"
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

## <a name="remarks"></a>Remarques

Pour le développement de script, ce paramètre est spécifié à l’aide de la propriété [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .

Pour le développement C++, ce paramètre est spécifié à l’aide de la propriété [**IRepetitionPattern :: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |

## <a name="see-also"></a>Voir aussi

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)

[Planificateur de tâches](task-scheduler-start-page.md)
