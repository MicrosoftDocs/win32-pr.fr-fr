---
title: WeeklyTrigger. WeeksInterval, propriété
description: Pour les scripts, obtient ou définit l’intervalle entre les semaines de la planification.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Planificateur de tâches de la propriété WeeksInterval
- Planificateur de tâches de la propriété WeeksInterval, objet WeeklyTrigger
- Planificateur de tâches objet WeeklyTrigger, propriété WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509510"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger. WeeksInterval, propriété

Pour les scripts, obtient ou définit l’intervalle entre les semaines de la planification.

## <a name="syntax"></a>Syntaxe


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valeur de la propriété

Intervalle entre les semaines de la planification.

## <a name="remarks"></a>Notes

Un intervalle de 1 produit une planification hebdomadaire. Un intervalle de 2 produit une planification chaque semaine.

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, l’intervalle d’une planification hebdomadaire est spécifié à l’aide de l’élément [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) du schéma planificateur de tâches.

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

 

 





