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
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508666"
---
# <a name="dailytriggerdaysinterval-property"></a>DailyTrigger. DaysInterval, propriété

Pour les scripts, obtient ou définit l’intervalle entre les jours de la planification.

## <a name="syntax"></a>Syntaxe


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valeur de la propriété

Intervalle entre les jours de la planification.

## <a name="remarks"></a>Notes

Un intervalle de 1 produit une planification quotidienne. Un intervalle de 2 produit une planification tous les jours.

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, l’intervalle d’une planification quotidienne est spécifié à l’aide de l’élément [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) du schéma planificateur de tâches.

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
</dt> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





