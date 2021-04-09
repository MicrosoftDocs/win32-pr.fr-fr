---
title: SessionStateChangeTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée d’un délai avant le démarrage d’une tâche après la détection d’un changement d’état de session Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet SessionStateChangeTrigger
- Planificateur de tâches objet SessionStateChangeTrigger, propriété Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103189"
---
# <a name="sessionstatechangetriggerdelay-property"></a>SessionStateChangeTrigger. Delay, propriété

Pour les scripts, obtient ou définit une valeur qui indique la durée d’un délai avant le démarrage d’une tâche après la détection d’un changement d’état de session Terminal Server. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).

## <a name="syntax"></a>Syntaxe


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Valeur de la propriété

Délai qui s’écoule avant le démarrage d’une tâche après la détection d’une modification d’état de session Terminal Server.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





