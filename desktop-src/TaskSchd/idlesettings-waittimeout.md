---
title: IdleSettings. WaitTimeout, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Planificateur de tâches de la propriété WaitTimeout
- Planificateur de tâches de la propriété WaitTimeout, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032962"
---
# <a name="idlesettingswaittimeout-property"></a>IdleSettings. WaitTimeout, propriété

Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise. Si aucune valeur n’est spécifiée pour cette propriété, le service Planificateur de tâches attend indéfiniment qu’une condition d’inactivité se produise.

## <a name="syntax"></a>Syntaxe


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). La durée minimale autorisée est de 1 minute. Si cette valeur est **null**, le délai prend la valeur par défaut de 1 heure.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) du schéma planificateur de tâches.

Si une tâche est déclenchée par un déclencheur inactif, la propriété **IdleSettings. WaitTimeout** est ignorée.

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

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





