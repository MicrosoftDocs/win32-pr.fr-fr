---
title: LogonTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet LogonTrigger
- Planificateur de tâches objet LogonTrigger, propriété Delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013431"
---
# <a name="logontriggerdelay-property"></a>LogonTrigger. Delay, propriété

Pour les scripts, obtient ou définit une valeur qui indique la durée entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique le laps de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, le délai de déclenchement de connexion est spécifié à l’aide de l’élément [**delay**](taskschedulerschema-delay-logontriggertype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





