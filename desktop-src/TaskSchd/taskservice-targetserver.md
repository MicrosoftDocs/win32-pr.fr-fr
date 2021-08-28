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
ms.openlocfilehash: 79f68dfaf5d6000ad88dca9001102056eb349601630364105526ea0d29a8bf46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080289"
---
# <a name="taskservicetargetserver-property"></a>TaskService. TargetServer, propriété

Pour les scripts, obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.

## <a name="syntax"></a>Syntaxe


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.

## <a name="remarks"></a>Remarques

Cette propriété retourne une chaîne vide lorsque l’utilisateur passe une adresse IP, localhost ou'. 'en tant que paramètre, et retourne le nom de l’ordinateur qui exécute le service Planificateur de tâches lorsque l’utilisateur ne passe aucune valeur de paramètre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





