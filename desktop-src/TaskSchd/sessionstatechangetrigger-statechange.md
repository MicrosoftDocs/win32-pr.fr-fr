---
title: SessionStateChangeTrigger. StateChange, propriété
description: Pour les scripts, obtient ou définit le type de Terminal Server modification de session qui déclencherait un lancement de tâche.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange, propriété Planificateur de tâches
- StateChange, propriété Planificateur de tâches, objet SessionStateChangeTrigger
- Objet SessionStateChangeTrigger Planificateur de tâches, propriété StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740613"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>SessionStateChangeTrigger. StateChange, propriété

Pour les scripts, obtient ou définit le type de Terminal Server modification de session qui déclencherait un lancement de tâche.

## <a name="syntax"></a>Syntaxe


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valeur de la propriété

Type de Terminal Server modification de session qui déclenche l’exécution d’une tâche.

Les valeurs possibles proviennent de l’énumération des [**types de changement d’état de session de tâche \_ \_ \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .



| Valeur                                                                                                                                                                                                                                               | Signification                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**Tâche \_ \_Connexion**</dt> de la console <dt>1</dt> </dl>          | Modification de l’état de la connexion à la console Terminal Server. Par exemple, lorsque vous vous connectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**Tâche \_ \_Déconnexion**</dt> de la console <dt>2</dt> </dl> | Modification de l’état de déconnexion de la console Terminal Server. Par exemple, lorsque vous vous déconnectez à une session utilisateur sur l’ordinateur local en basculant les utilisateurs sur l’ordinateur.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**Tâche \_ \_Connexion à distance**</dt> <dt>3</dt> </dl>             | Terminal Server modification de l’état de la connexion à distance. Par exemple, lorsqu’un utilisateur se connecte à une session utilisateur à l’aide du programme Connexion Bureau à distance à partir d’un ordinateur distant.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**Tâche \_ \_Déconnexion à distance**</dt> <dt>4</dt> </dl>    | Terminal Server modification de l’état de la déconnexion distante. Par exemple, lorsqu’un utilisateur se déconnecte d’une session utilisateur lors de l’utilisation du programme Connexion Bureau à distance à partir d’un ordinateur distant.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**Tâche \_ \_Verrou de session**</dt> <dt>7</dt> </dl>                   | Terminal Server modification de l’état verrouillé de la session. Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est verrouillé. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**Tâche \_ \_Déverrouillage de session**</dt> <dt>8</dt> </dl>             | Modification de l’état de déverrouillage de la session Terminal Server. Par exemple, ce changement d’État provoque l’exécution de la tâche lorsque l’ordinateur est déverrouillé.<br/>                                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





