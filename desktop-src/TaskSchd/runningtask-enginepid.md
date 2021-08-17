---
title: RunningTask. EnginePID, propriété
description: Pour les scripts, obtient l’ID de processus du moteur (processus) qui exécute la tâche.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Planificateur de tâches de la propriété EnginePID
- Planificateur de tâches de la propriété EnginePID, objet RunningTask
- Planificateur de tâches objet RunningTask, propriété EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed259ccc92e954ae1acde076f0cc09167d15071ea71a33039e7298479875b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759072"
---
# <a name="runningtaskenginepid-property"></a>RunningTask. EnginePID, propriété

Pour les scripts, obtient l’ID de processus du moteur (processus) qui exécute la tâche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valeur de la propriété

ID de processus du moteur qui exécute la tâche.

## <a name="remarks"></a>Remarques

L’ID de processus retourné par cette propriété ne peut pas être ajouté directement à une chaîne. La valeur retournée doit être convertie en une valeur entière en appelant la fonction [CInt](/previous-versions//fctcwhw9(v=vs.85)) sur la valeur retournée.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

