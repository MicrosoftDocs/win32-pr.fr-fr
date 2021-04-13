---
title: Action. type, propriété
description: Pour les scripts, obtient le type de l’action.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Planificateur de tâches de propriété de type
- Planificateur de tâches de propriété de type, objet d’action
- Planificateur de tâches de l’objet action, propriété type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466038"
---
# <a name="actiontype-property"></a>Action. type, propriété

Pour les scripts, obtient le type de l’action.

## <a name="syntax"></a>Syntaxe


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété retourne l’une des constantes d’énumération de [**\_ \_ type d’action de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) suivantes.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Tâche \_ ACTION \_ Exec**</dt> <dt>0</dt> </dl>                          | Cette action effectue une opération de ligne de commande. Par exemple, l’action peut exécuter un script, lancer un exécutable ou, si le nom d’un document est fourni, Rechercher l’application associée et lancer l’application avec le document.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Tâche \_ \_ \_ Gestionnaire com d’action**</dt> <dt>5</dt> </dl>    | Cette action déclenche un gestionnaire.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Tâche \_ ACTION \_ Envoyer un \_ e-mail**</dt> <dt>6</dt> </dl>       | Cette action envoie un message électronique.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Tâche \_ ACTION \_ afficher le \_ message**</dt> <dt>7</dt> </dl> | Cette action affiche une boîte de message.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Notes

Le type d’action est défini lors de la création de l’action et ne peut pas être modifié ultérieurement. Pour plus d’informations sur la création d’une action, consultez [**ActionCollection. Create**](actioncollection-create.md).

Pour plus d’informations sur la façon dont les actions et les tâches fonctionnent ensemble, consultez [actions des tâches](task-actions.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type d’action de tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**Action**](action.md)
</dt> </dl>

 

 





