---
title: RegistrationTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet RegistrationTrigger
- Planificateur de tâches objet RegistrationTrigger, propriété Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122829"
---
# <a name="registrationtriggerdelay-property"></a>RegistrationTrigger. Delay, propriété

Pour les scripts, obtient ou définit la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).

## <a name="syntax"></a>Syntaxe


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Valeur de la propriété

Intervalle de temps entre le moment où le système est inscrit et le moment où la tâche est démarrée.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, le délai de démarrage est spécifié à l’aide de l’élément [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) du schéma planificateur de tâches.

Si une tâche avec un déclencheur d’inscription différé est inscrite et que l’ordinateur sur lequel la tâche est inscrite est arrêté ou redémarré pendant le délai, avant l’exécution de la tâche, la tâche ne s’exécutera pas et le délai sera perdu.

## <a name="requirements"></a>Spécifications



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

 

 





