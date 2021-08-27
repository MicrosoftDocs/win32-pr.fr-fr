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
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080259"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger. WeeksInterval, propriété

Pour les scripts, obtient ou définit l’intervalle entre les semaines de la planification.

## <a name="syntax"></a>Syntaxe


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valeur de la propriété

Intervalle entre les semaines de la planification.

## <a name="remarks"></a>Remarques

Un intervalle de 1 produit une planification hebdomadaire. Un intervalle de 2 produit une planification chaque semaine.

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, l’intervalle d’une planification hebdomadaire est spécifié à l’aide de l’élément [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) du schéma planificateur de tâches.

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
</dt> </dl>

 

 





