---
title: Méthode RegisteredTask. RunEx
description: Pour les scripts, exécute la tâche inscrite immédiatement à l’aide d’indicateurs spécifiés et d’un identificateur de session.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Planificateur de tâches de la méthode RunEx
- Méthode RunEx Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122921"
---
# <a name="registeredtaskrunex-method"></a>Méthode RegisteredTask. RunEx

Pour les scripts, exécute la tâche inscrite immédiatement à l’aide d’indicateurs spécifiés et d’un identificateur de session.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
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

*indicateurs* \[ dans\]
</dt> <dd>

Constante [d' \_ exécution \_ de tâche indicateurs](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) qui définit le mode d’exécution de la tâche.

</dd> <dt>

*SessionID* \[ dans\]
</dt> <dd>

Session Terminal Server dans laquelle vous souhaitez lancer la tâche.

Si l’exécution de la tâche \_ \_ utiliser une \_ \_ constante d’ID de session (0x4) n’est pas passée dans le paramètre *Flags* , la valeur spécifiée dans ce paramètre est ignorée. Si la \_ constante exécuter la tâche \_ utiliser \_ \_ l’ID de session est passée dans le paramètre *Flags* et que la valeur SessionID est inférieure ou égale à 0, une erreur d’argument non valide est retournée.

Si la tâche \_ exécuter la tâche \_ utiliser l’ID de \_ session \_ est passée dans le paramètre *Flags* et que la valeur SessionID est un ID de session valide supérieur à 0 et si aucune valeur n’est spécifiée pour le paramètre *User* , le service Planificateur de tâches tente de lancer la tâche de manière interactive en tant qu’utilisateur connecté à la session spécifiée.

Si la tâche \_ exécuter la tâche \_ utiliser l’ID de \_ session \_ est passée dans le paramètre *Flags* et que la valeur SessionID est un ID de session valide supérieur à 0 et si un utilisateur est spécifié dans le paramètre *User* , le service Planificateur de tâches essaiera de lancer la tâche de manière interactive en tant qu’utilisateur spécifié dans le paramètre *User* .

</dd> <dt>

*runningTask* \[ à\]
</dt> <dd>

Objet [**RunningTask**](runningtask.md) qui définit la nouvelle instance de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode retournera sans erreur, mais la tâche ne s’exécutera pas si la propriété [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) est définie sur false pour la tâche inscrite.

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

 

 





