---
title: Propriété Trigger. EndBoundary
description: Pour les scripts, obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Planificateur de tâches de la propriété EndBoundary
- Propriété EndBoundary Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032642"
---
# <a name="triggerendboundary-property"></a>Propriété Trigger. EndBoundary

Pour les scripts, obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.

## <a name="syntax"></a>Syntaxe


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valeur de la propriété

Date et heure de désactivation du déclencheur. La date et l’heure doivent être au format suivant : AAAA-MM-JJThh : MM : SS (+-) HH : MM. Par exemple, la date du 11 octobre 2005 à 1:21:17 dans le fuseau horaire Pacifique serait écrite sous la forme 2005-10-11T13:21:17-08:00. La section (+-) HH : MM du format décrit le fuseau horaire comme un certain nombre d’heures avant ou après le temps universel coordonné (heure de Greenwich).

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, la propriété Enabled est spécifiée à l’aide de l’élément [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) du schéma planificateur de tâches.

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

 

 





