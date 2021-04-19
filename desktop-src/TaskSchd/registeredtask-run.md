---
title: RegisteredTask. Run, méthode
description: Pour les scripts, exécute la tâche inscrite immédiatement.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Planificateur de tâches de la méthode Run
- Méthode Run Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches de l’objet RegisteredTask, méthode Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512598"
---
# <a name="registeredtaskrun-method"></a>RegisteredTask. Run, méthode

Pour les scripts, exécute la tâche inscrite immédiatement.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*paramètres* \[ dans\]
</dt> <dd>

Paramètres utilisés comme valeurs dans les actions de tâche. Pour ne pas spécifier de valeurs de paramètre pour les actions de tâche, attribuez la valeur **Nothing** à ce paramètre. Dans le cas contraire, vous pouvez spécifier une valeur de chaîne unique ou un tableau de valeurs de chaîne.

Les valeurs de chaîne que vous spécifiez sont associées à des noms et stockées en tant que paires nom-valeur. Si vous spécifiez une valeur de chaîne unique, arg0 sera le nom affecté à la valeur. La valeur peut être utilisée dans l’action de tâche où la variable $ (arg0) est utilisée dans les propriétés de l’action.

Si vous transmettez des valeurs telles que « 0 », « 100 » et « 250 » en tant que tableau de valeurs de chaîne, « 0 » remplace les variables $ (arg0), « 100 » remplace les variables $ (Arg1) et « 250 » remplace les variables $ (Arg2) utilisées dans les propriétés d’action.

Vous pouvez spécifier au maximum 32 valeurs de chaîne.

Pour plus d’informations et pour obtenir la liste des propriétés d’action qui peuvent utiliser les variables $ (arg0), $ (Arg1),..., $ (Arg32) dans leurs valeurs, consultez [actions de tâche](task-actions.md).

</dd> <dt>

*ppRunningTask* \[ à\]
</dt> <dd>

Objet [**RunningTask**](runningtask.md) qui définit la nouvelle instance de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **RegisteredTask. Run** est équivalente à la fonction [**RegisteredTask. RunEx**](registeredtask-runex.md) avec le paramètre flags égal à 0 et rien n’est spécifié pour le paramètre User.

Cette méthode retournera sans erreur, mais la tâche ne s’exécutera pas si la propriété [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) est définie sur false pour la tâche inscrite.

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





