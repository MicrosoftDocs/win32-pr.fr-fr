---
title: RunningTask. InstanceGuid, propriété
description: Pour les scripts, obtient l’identificateur GUID pour cette instance de la tâche.
ms.assetid: 35be538f-5223-4c61-9491-677953b4135a
keywords:
- Planificateur de tâches de la propriété InstanceGuid
- Planificateur de tâches de la propriété InstanceGuid, objet RunningTask
- Planificateur de tâches objet RunningTask, propriété InstanceGuid
topic_type:
- apiref
api_name:
- RunningTask.InstanceGuid
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f3ad40eb7c8799d12ca3b4a6aaeb0b968a9229
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509127"
---
# <a name="runningtaskinstanceguid-property"></a>RunningTask. InstanceGuid, propriété

Pour les scripts, obtient l’identificateur GUID pour cette instance de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
RunningTask.InstanceGuid As string
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur GUID de cette instance de la tâche. Un identificateur est généré par le service Planificateur de tâches chaque fois que la tâche est exécutée.

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

 

 





