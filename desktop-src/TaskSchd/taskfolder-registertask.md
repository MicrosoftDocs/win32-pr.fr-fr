---
title: Méthode TaskFolder. RegisterTask
description: Pour les scripts, inscrit (crée) une nouvelle tâche dans le dossier à l’aide de XML pour définir la tâche.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- Planificateur de tâches de la méthode RegisterTask
- Méthode RegisterTask Planificateur de tâches, objet TaskFolder
- Planificateur de tâches objet TaskFolder, méthode RegisterTask
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942585"
---
# <a name="taskfolderregistertask-method"></a>Méthode TaskFolder. RegisterTask

Pour les scripts, inscrit (crée) une nouvelle tâche dans le dossier à l’aide de XML pour définir la tâche.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*chemin d’accès* \[ dans\]
</dt> <dd>

Nom de la tâche. Si cette valeur est **Nothing**, la tâche est inscrite dans le dossier racine de la tâche et le nom de la tâche est une valeur Guid créée par le service Planificateur de tâches.

Un nom de tâche ne peut pas commencer ou se terminer par un espace. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

</dd> <dt>

*XmlText* \[ dans\]
</dt> <dd>

Description de la tâche au format XML.

Les rubriques suivantes contiennent des tâches définies à l’aide de XML.

-   [Exemple de déclencheur de temps (XML)](time-trigger-example--xml-.md)
-   [Exemple de déclencheur d’événement (XML)](/previous-versions//aa446889(v=vs.85))
-   [Exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md)
-   [Exemple de déclencheur d’inscription (XML)](registration-trigger-example--xml-.md)
-   [Exemple de déclencheur hebdomadaire (XML)](weekly-trigger-example--xml-.md)
-   [Exemple de déclencheur LOGON (XML)](logon-trigger-example--xml-.md)
-   [Exemple de déclencheur de démarrage (XML)](boot-trigger-example--xml-.md)

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Constante [**de \_ création de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .



| Valeur                                                                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**Tâche \_ VALIDER \_ uniquement**</dt> <dt>0x1</dt> </dl>                                                | Le Planificateur de tâches vérifie la syntaxe du code XML qui décrit la tâche, mais n’inscrit pas la tâche. Cette constante ne peut pas être combinée **avec \_ la création**, la **\_ mise à jour** de tâches ou la **\_ création \_ ou la \_ mise à jour** de tâches.<br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**Tâche \_ CRÉER**</dt> <dt>0X2</dt> </dl>                                                                      | L’Planificateur de tâches inscrit la tâche en tant que nouvelle tâche.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**Tâche \_ METTRE à jour**</dt> <dt>0x4</dt> </dl>                                                                      | L’Planificateur de tâches inscrit la tâche en tant que version mise à jour d’une tâche existante. Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.<br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**Tâche \_ CRÉER \_ ou \_ mettre à jour**</dt> <dt>0x6</dt> </dl>                                      | La Planificateur de tâches inscrit la tâche en tant que nouvelle tâche ou version mise à jour si la tâche existe déjà. Équivaut à la \_ \| mise à jour des tâches de création de tâche \_ .<br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**Tâche \_ DÉSACTIVER**</dt> <dt>0x8</dt> </dl>                                                                   | Le Planificateur de tâches désactive la tâche existante.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**Tâche \_ Ne pas \_ Ajouter le \_ principal \_ ACE**</dt> <dt>0x10</dt> </dl>                  | L’Planificateur de tâches ne peut pas ajouter l’entrée de contrôle d’accès (ACE) allow pour le principal de contexte. Lorsque la fonction **TaskFolder. RegisterTask** est appelée avec cet indicateur pour mettre à jour une tâche, le service Planificateur de tâches n’ajoute pas l’entrée du contrôle d’accès pour le nouveau contexte principal et ne supprime pas l’entrée du contrôle d’accès de l’ancien principal de contexte.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**Tâche \_ IGNORER \_ les \_ déclencheurs d’inscription**</dt> <dt>0x20</dt> </dl> | L’Planificateur de tâches crée la tâche, mais ignore les déclencheurs d’inscription dans la tâche. En ignorant les déclencheurs d’inscription, la tâche ne s’exécute pas lors de son inscription, sauf si un déclencheur basé sur la durée l’exécute lors de l’inscription.<br/>                                                                                               |



 

</dd> <dt>

*userid* \[ dans\]
</dt> <dd>

Informations d’identification de l’utilisateur utilisées pour inscrire la tâche.

> [!Note]  
> Si la tâche est définie en tant que tâche Planificateur de tâches 1,0, n’utilisez pas de nom de groupe (au lieu d’un nom d’utilisateur spécifique) dans ce paramètre userId. Une tâche est définie comme une tâche Planificateur de tâches 1,0 lorsque l’attribut version de l’élément Task dans le code XML de la tâche est défini sur 1,1.

 

</dd> <dt>

*mot de passe* \[ dans\]
</dt> <dd>

Mot de passe de l’ID utilisateur utilisé pour inscrire la tâche. Lorsque le \_ type d’ouverture de session du compte de service d’ouverture de session \_ \_ est utilisé, le mot de passe doit être une valeur **Variant** vide telle que **VT \_ null** ou **VT \_ vide**.

</dd> <dt>

*LogonType* \[ dans\]
</dt> <dd>

Définit la technique d’ouverture de session utilisée pour exécuter la tâche inscrite.



| Valeur                                                                                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Tâche \_ Ouverture de session \_ None**</dt> <dt>0</dt> </dl>                                                                               | La méthode d’ouverture de session n’est pas spécifiée. Utilisé pour les informations d’identification non-NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Tâche \_ \_Mot de passe de connexion**</dt> <dt>1</dt> </dl>                                                                   | Utilisez un mot de passe pour la journalisation de l’utilisateur. Le mot de passe doit être fourni au moment de l’inscription.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Tâche \_ CONNEXION \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Utilisez un jeton interactif existant pour exécuter une tâche. L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user). Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a pas d’accès au réseau ou aux fichiers chiffrés.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Tâche \_ Ouverture de session \_ interactive \_ Token**</dt> <dt>3</dt> </dl>                                       | L’utilisateur doit déjà avoir ouvert une session. La tâche est exécutée uniquement dans une session interactive existante.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Tâche \_ \_Groupe d’ouverture de session**</dt> <dt>4</dt> </dl>                                                                            | Activation du groupe. Le champ **GroupID** spécifie le groupe.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Tâche \_ \_ \_ Compte de service d’ouverture de session**</dt> <dt>5</dt> </dl>                                             | Indique qu’un compte système local, service local ou service réseau est utilisé comme contexte de sécurité pour exécuter la tâche.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Tâche \_ Jeton interactif d’ouverture de session \_ \_ \_ ou \_ mot de passe**</dt> <dt>6</dt> </dl> | Utilisez d’abord le jeton interactif. Si l’utilisateur n’est pas connecté (aucun jeton interactif n’est disponible), le mot de passe est utilisé. Le mot de passe doit être spécifié lors de l’inscription d’une tâche. Cet indicateur n’est pas recommandé pour les nouvelles tâches, car il est moins fiable que le \_ \_ mot de passe de connexion à la tâche.<br/> |



 

</dd> <dt>

*langage SDDL* \[ dans, facultatif\]
</dt> <dd>

Descripteur de sécurité associé à la tâche inscrite. Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’une tâche afin d’autoriser ou de refuser l’accès à une tâche à certains utilisateurs et groupes.

> [!Note]  
> Si l’accès à une tâche est refusé au compte système local, le service Planificateur de tâches peut produire des résultats inattendus.

 

</dd> <dt>

*ptask* \[ à\]
</dt> <dd>

Objet [**RegisteredTask**](registeredtask.md) qui représente la nouvelle tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive. Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété [**LogonType**](principal-logontype.md) du principal de la tâche, ou dans le paramètre *LogonType* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Seul un membre du groupe administrateurs peut créer une tâche avec un déclencheur de démarrage.

Vous pouvez inscrire correctement une tâche avec un groupe spécifié dans le paramètre *userid* et 3 (**\_ \_ \_ jeton interactif d’ouverture de session de tâche**) spécifiés dans le paramètre *LogonType* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), mais la tâche ne s’exécutera pas.

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
</dt> <dt>

[**TaskFolder**](taskfolder.md)
</dt> </dl>

 

