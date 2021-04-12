---
title: TaskService. TargetServer, propriété
description: Pour les scripts, obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Propriété TargetServer Planificateur de tâches
- Propriété TargetServer Planificateur de tâches, objet TaskService
- Objet TaskService Planificateur de tâches, propriété TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519097"
---
# <a name="taskservicetargetserver-property"></a>TaskService. TargetServer, propriété

Pour les scripts, obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.

## <a name="syntax"></a>Syntaxe


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.

## <a name="remarks"></a>Notes

Cette propriété retourne une chaîne vide lorsque l’utilisateur passe une adresse IP, localhost ou'. 'en tant que paramètre, et retourne le nom de l’ordinateur qui exécute le service Planificateur de tâches lorsque l’utilisateur ne passe aucune valeur de paramètre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





