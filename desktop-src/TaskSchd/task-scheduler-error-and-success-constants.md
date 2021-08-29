---
title: Planificateur de tâches les constantes d’erreur et de réussite (WinError. h)
description: Si une erreur se produit, les API Planificateur de tâches peuvent retourner l’un des codes d’erreur suivants sous la forme d’une valeur HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Planificateur de tâches Planificateur de tâches, références, erreurs et constantes de réussite
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: d9633282fd6a504a48db81ce852fad7a2aca16a4ee26a1d14ce4f052b6447ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080389"
---
# <a name="task-scheduler-error-and-success-constants"></a>Planificateur de tâches les constantes d’erreur et de réussite

Si une erreur se produit, les API Planificateur de tâches peuvent retourner l’un des codes d’erreur suivants sous la forme d’une valeur **HRESULT** .

Les constantes qui commencent par SCHED \_ S \_ sont des constantes de réussite et les constantes qui commencent par sched \_ E \_ sont des constantes d’erreur.

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

Exemple de [code C/C++ : récupération](c-c-code-example-retrieving-task-status.md)de l’état de la tâche.

> [!Note]  
> Certaines API Planificateur de tâches peuvent renvoyer des codes d’erreur système et réseau (64, par exemple). Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes. Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.

 

Pour plus d’informations sur les événements et les messages d’erreur, consultez [Centre de messages d’erreurs et](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx)d’événements.

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**\_tâche sched \_ S \_ prête**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



La tâche est prête à s’exécuter à la prochaine heure planifiée.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**\_tâche sched \_ S \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



La tâche est en cours d'exécution.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**\_tâche sched \_ S \_ désactivée**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



La tâche ne s’exécutera pas aux heures planifiées, car elle a été désactivée.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**la \_ tâche sched S \_ \_ \_ n’a pas été \_ exécutée**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



La tâche n’a pas encore été exécutée.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**PLANIFICATION \_ \_ des tâches \_ \_ S \_**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



Il n’y a plus d’exécutions planifiées pour cette tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_tâche sched \_ S \_ non \_ planifiée**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



Une ou plusieurs des propriétés nécessaires pour exécuter cette tâche sur une planification n’ont pas été définies.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**\_tâche sched \_ S \_ terminée**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



La dernière exécution de la tâche a été arrêtée par l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**PLANIFICATION \_ des \_ tâches \_ S \_ aucun \_ déclencheur valide**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



Soit la tâche n’a aucun déclencheur, soit les déclencheurs existants sont désactivés ou non définis.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_ \_ déclencheur d’événement sched S \_**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



Les déclencheurs d’événements n’ont pas de durée d’exécution définie.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ déclencheur sched \_ E \_ introuvable**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



Le déclencheur d’une tâche est introuvable.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**\_tâche sched \_ E \_ non \_ prête**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



Une ou plusieurs des propriétés requises pour exécuter cette tâche n’ont pas été définies.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_tâche sched \_ E \_ non \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



Il n’y a aucune instance en cours d’exécution de la tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**\_service sched \_ E \_ non \_ installé**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



Le service Planificateur de tâches n’est pas installé sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**la grille \_ E \_ ne peut pas \_ ouvrir la \_ tâche**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



Impossible d’ouvrir l’objet de tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**PLANIFICATION \_ E \_ tâche non valide \_**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



L’objet est un objet de tâche non valide ou n’est pas un objet de tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_ \_ informations sur le compte sched E \_ \_ non \_ définies**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



Aucune information de compte n’a été trouvée dans la base de données de sécurité Planificateur de tâches pour la tâche indiquée.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_nom du compte sched E \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



Impossible d’établir l’existence du compte spécifié.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**le \_ compte sched E \_ \_ dBASE est \_ endommagé**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



Une altération a été détectée dans la base de données de sécurité Planificateur de tâches ; la base de données a été réinitialisée.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ aucun \_ service de sécurité \_**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



Les services de sécurité Planificateur de tâches sont disponibles uniquement sur Windows NT.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**PLANIFICATION d’une \_ \_ version d’objet inconnue \_ \_**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



La version de l’objet de tâche n’est pas prise en charge ou n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_option de compte sched E \_ non prise en charge \_ \_**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



La tâche a été configurée avec une combinaison non prise en charge de paramètres de compte et d’options d’exécution.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**le \_ service sched E \_ \_ n’est pas \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



Le service Planificateur de tâches n’est pas en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**PLANIFICATION \_ E \_ UNEXPECTEDNODE**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



Le code XML de la tâche contient un nœud inattendu.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_espace de \_ noms sched E**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



Le code XML de la tâche contient un élément ou un attribut d’un espace de noms inattendu.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**PLANIFICATION \_ E \_ INVALIDVALUE**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



Le fichier XML de la tâche contient une valeur qui n’est pas correctement mise en forme ou en dehors de la plage.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**PLANIFICATION \_ E \_ MISSINGNODE**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



L’élément ou l’attribut requis est manquant dans le fichier XML de la tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**PLANIFICATION \_ E \_ MALFORMEDXML**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



Le code XML de la tâche est incorrect.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**échec de la planification de \_ \_ certains \_ déclencheurs \_**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



La tâche est inscrite, mais tous les déclencheurs spécifiés ne démarrent pas la tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problème de \_ connexion par lot de sched S \_ \_**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



La tâche est inscrite, mais peut ne pas démarrer. Le privilège de connexion par lot doit être activé pour le principal de tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**PLANIFICATION \_ d' \_ \_ un trop grand nombre de \_ nœuds**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



Le code XML de la tâche contient un trop grand nombre de nœuds du même type.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**\_ \_ \_ délimiteur de fin \_ de la grille**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



La tâche ne peut pas être démarrée après la limite de fin du déclencheur.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E \_ déjà \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



Une instance de cette tâche est déjà en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_utilisateur sched \_ E \_ non \_ connecté \_**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



La tâche ne s’exécute pas, car l’utilisateur n’est pas connecté.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**\_ligne de \_ \_ hachage de tâche non valide \_**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



L’image de tâche est endommagée ou a été falsifiée.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**\_service sched \_ E \_ non \_ disponible**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



Le service Planificateur de tâches n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**\_service sched \_ E \_ trop \_ occupé**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



Le service Planificateur de tâches est trop occupé pour traiter votre demande. Veuillez réessayer plus tard.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**\_tâche sched \_ E \_ tentée**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



Le service de Planificateur de tâches a tenté d’exécuter la tâche, mais la tâche n’a pas été exécutée en raison de l’une des contraintes dans la définition de la tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**\_tâche sched S en \_ \_ attente**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



Le service de Planificateur de tâches a demandé l’exécution de la tâche.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**\_tâche sched \_ E \_ désactivée**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



La tâche est désactivée.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Compatibilité de la \_ tâche sched E \_ \_ non \_ v1 \_**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



La tâche a des propriétés qui ne sont pas compatibles avec les versions antérieures de Windows.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**PLANIFICATION \_ \_ d’un démarrage \_ à \_ la demande**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



Les paramètres de tâche n’autorisent pas le démarrage de la tâche à la demande.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





