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
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122781"
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

## <a name="remarks"></a>Notes

L’ID de processus retourné par cette propriété ne peut pas être ajouté directement à une chaîne. La valeur retournée doit être convertie en une valeur entière en appelant la fonction [CInt](/previous-versions//fctcwhw9(v=vs.85)) sur la valeur retournée.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

