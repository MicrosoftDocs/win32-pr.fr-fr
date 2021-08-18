---
title: DailyTrigger. DaysInterval, propriété
description: Pour les scripts, obtient ou définit l’intervalle entre les jours de la planification.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Planificateur de tâches de la propriété DaysInterval
- Planificateur de tâches de la propriété DaysInterval, objet DailyTrigger
- Planificateur de tâches objet DailyTrigger, propriété DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139492"
---
# <a name="dailytriggerdaysinterval-property"></a>DailyTrigger. DaysInterval, propriété

Pour les scripts, obtient ou définit l’intervalle entre les jours de la planification.

## <a name="syntax"></a>Syntaxe


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valeur de la propriété

Intervalle entre les jours de la planification.

## <a name="remarks"></a>Remarques

Un intervalle de 1 produit une planification quotidienne. Un intervalle de 2 produit une planification tous les jours.

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, l’intervalle d’une planification quotidienne est spécifié à l’aide de l’élément [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) du schéma planificateur de tâches.

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

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





