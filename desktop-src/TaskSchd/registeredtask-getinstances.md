---
title: Méthode RegisteredTask. GetInstances
description: Pour les scripts, retourne toutes les instances en cours d’exécution de la tâche inscrite.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Planificateur de tâches de la méthode GetInstances
- Méthode GetInstances Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122953"
---
# <a name="registeredtaskgetinstances-method"></a>Méthode RegisteredTask. GetInstances

Pour les scripts, retourne toutes les instances en cours d’exécution de la tâche inscrite.

> [!Note]  
> **RegisteredTask. GetInstances** retourne uniquement les instances de la tâche inscrite en cours d’exécution qui s’exécutent au-dessous ou au-dessous du contexte de sécurité d’un utilisateur. Par exemple, pour les membres du groupe administrateurs, **GetInstances** retourne toutes les instances de la tâche inscrite en cours d’exécution, mais pour les membres du groupe utilisateurs, **GetInstances** renvoie uniquement les instances de la tâche inscrite en cours d’exécution qui s’exécutent dans le contexte de sécurité du groupe utilisateurs.

 

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*flags* 
</dt> <dd>

Ce paramètre est réservé pour une utilisation ultérieure et doit avoir la valeur 0.

</dd> <dt>

*runningTasks* \[ à\]
</dt> <dd>

Objet [**RunningTaskCollection**](runningtaskcollection.md) qui contient toutes les instances en cours d’exécution de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





