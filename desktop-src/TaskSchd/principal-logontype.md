---
title: Propriété principal. LogonType
description: Pour les scripts, obtient ou définit la méthode de connexion à la sécurité requise pour exécuter les tâches associées au principal.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Planificateur de tâches de la propriété LogonType
- Planificateur de tâches de la propriété LogonType, objet principal
- Planificateur de tâches de l’objet principal, propriété LogonType
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465630"
---
# <a name="principallogontype-property"></a>Propriété principal. LogonType

Pour les scripts, obtient ou définit la méthode de connexion à la sécurité requise pour exécuter les tâches associées au principal.

## <a name="syntax"></a>Syntaxe


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valeur de la propriété

Définissez l’une des constantes d’énumération de [**\_ type d’ouverture de session des tâches**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) suivantes.



| Valeur                                                                                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Tâche \_ Ouverture de session \_ None**</dt> <dt>0</dt> </dl>                                                                               | La méthode d’ouverture de session n’est pas spécifiée. Utilisé pour les informations d’identification non-NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Tâche \_ \_Mot de passe de connexion**</dt> <dt>1</dt> </dl>                                                                   | Utilisez un mot de passe pour la journalisation de l’utilisateur. Le mot de passe doit être fourni au moment de l’inscription.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Tâche \_ CONNEXION \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Utilisez un jeton interactif existant pour exécuter une tâche. L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user). Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a aucun accès au réseau ou aux fichiers chiffrés.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Tâche \_ Ouverture de session \_ interactive \_ Token**</dt> <dt>3</dt> </dl>                                       | L’utilisateur doit déjà avoir ouvert une session. La tâche est exécutée uniquement dans une session interactive existante.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Tâche \_ \_Groupe d’ouverture de session**</dt> <dt>4</dt> </dl>                                                                            | Activation du groupe. Le champ userId spécifie le groupe.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Tâche \_ \_ \_ Compte de service d’ouverture de session**</dt> <dt>5</dt> </dl>                                             | Indique qu’un compte système local, service local ou service réseau est utilisé comme contexte de sécurité pour exécuter la tâche.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Tâche \_ Jeton interactif d’ouverture de session \_ \_ \_ ou \_ mot de passe**</dt> <dt>6</dt> </dl> | Utilisez d’abord le jeton interactif. Si l’utilisateur n’est pas connecté (aucun jeton interactif n’est disponible), le mot de passe est utilisé. Le mot de passe doit être spécifié lors de l’inscription d’une tâche. Cet indicateur n’est pas recommandé pour les nouvelles tâches, car il est moins fiable que le \_ \_ mot de passe de connexion à la tâche.<br/> |



 

## <a name="remarks"></a>Notes

Cette propriété est valide uniquement lorsqu’un identificateur d’utilisateur est spécifié par la propriété [**userid**](principal-userid.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, le type de connexion est spécifié dans l' [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) élément du schéma planificateur de tâches.

Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive. Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété **LogonType** du principal de la tâche, ou dans le paramètre *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

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

[**Directeur**](principal.md)
</dt> </dl>

 

 





