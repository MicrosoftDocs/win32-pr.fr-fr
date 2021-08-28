---
title: IdleSettings. IdleDuration, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche soit exécutée.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Planificateur de tâches de la propriété IdleDuration
- Planificateur de tâches de la propriété IdleDuration, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a78210202579d517410a2d82f1c5566d947f1ceb76cbd92538a0266b7b81ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002437"
---
# <a name="idlesettingsidleduration-property"></a>IdleSettings. IdleDuration, propriété

Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche soit exécutée.

## <a name="syntax"></a>Syntaxe


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). La valeur minimale est d’une minute. Si cette valeur est **null**, le délai est défini sur la valeur par défaut de 10 minutes.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) du schéma planificateur de tâches.

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

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





