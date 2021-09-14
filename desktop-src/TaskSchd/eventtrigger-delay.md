---
title: EventTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet EventTrigger
- Objet EventTrigger Planificateur de tâches, propriété Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008665"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger. Delay, propriété

Pour les scripts, obtient ou définit une valeur qui indique la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).

## <a name="syntax"></a>Syntaxe


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique la durée écoulée entre le moment où l’événement se produit et le moment où la tâche est démarrée.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de votre propre code XML pour une tâche, le délai d’événement est spécifié à l’aide de l’élément [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) du schéma planificateur de tâches.

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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





