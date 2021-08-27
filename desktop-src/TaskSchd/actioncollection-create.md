---
title: ActionCollection. Create, méthode
description: Pour les scripts, crée et ajoute une nouvelle action à la collection.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Créer une méthode Planificateur de tâches
- Create Method Planificateur de tâches, objet ActionCollection
- Planificateur de tâches d’objets ActionCollection, méthode Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce517ae33681fcb106e83720fc5ddd7685f26f673c466e24162ce95e9ca442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072699"
---
# <a name="actioncollectioncreate-method"></a>ActionCollection. Create, méthode

Pour les scripts, crée et ajoute une nouvelle action à la collection.

## <a name="syntax"></a>Syntaxe


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Ce paramètre est défini sur l’une des constantes d’énumération de [**\_ \_ type d’action de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) suivantes.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Tâche \_ ACTION \_ Exec**</dt> <dt>0</dt> </dl>                          | L’action effectue une opération de ligne de commande. Par exemple, l’action peut exécuter un script, lancer un exécutable ou, si le nom d’un document est fourni, Rechercher l’application associée et lancer l’application avec le document.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Tâche \_ \_ \_ Gestionnaire com d’action**</dt> <dt>5</dt> </dl>    | L’action déclenche un gestionnaire.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Tâche \_ ACTION \_ Envoyer un \_ e-mail**</dt> <dt>6</dt> </dl>       | Cette action envoie un message électronique.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Tâche \_ ACTION \_ afficher le \_ message**</dt> <dt>7</dt> </dl> | Cette action affiche une boîte de message.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet d' [**action**](action.md) qui représente la nouvelle action.

## <a name="remarks"></a>Remarques

Vous ne pouvez pas ajouter plus de 32 actions à la collection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type d’action de tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> <dt>

[**Action**](action.md)
</dt> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





