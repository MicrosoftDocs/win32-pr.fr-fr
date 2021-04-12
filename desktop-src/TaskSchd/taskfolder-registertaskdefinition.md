---
title: Méthode TaskFolder. RegisterTaskDefinition
description: Pour les scripts, inscrit (crée) une tâche à un emplacement spécifié à l’aide de l’objet TaskDefinition pour définir une tâche.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- Planificateur de tâches de la méthode RegisterTaskDefinition
- Méthode RegisterTaskDefinition Planificateur de tâches, objet TaskFolder
- Planificateur de tâches objet TaskFolder, méthode RegisterTaskDefinition
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384916"
---
# <a name="taskfolderregistertaskdefinition-method"></a><span data-ttu-id="7523e-106">Méthode TaskFolder. RegisterTaskDefinition</span><span class="sxs-lookup"><span data-stu-id="7523e-106">TaskFolder.RegisterTaskDefinition method</span></span>

<span data-ttu-id="7523e-107">Pour les scripts, inscrit (crée) une tâche à un emplacement spécifié à l’aide de l’objet [**TaskDefinition**](taskdefinition.md) pour définir une tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-107">For scripting, registers (creates) a task in a specified location using the [**TaskDefinition**](taskdefinition.md) object to define a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="7523e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7523e-108">Syntax</span></span>


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a><span data-ttu-id="7523e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7523e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7523e-110">*chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7523e-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-111">Nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-111">The name of the task.</span></span> <span data-ttu-id="7523e-112">Si cette valeur est **Nothing**, la tâche est inscrite dans le dossier racine de la tâche et le nom de la tâche est une valeur Guid créée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7523e-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="7523e-113">Un nom de tâche ne peut pas commencer ou se terminer par un espace.</span><span class="sxs-lookup"><span data-stu-id="7523e-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="7523e-114">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="7523e-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="7523e-115">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7523e-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="7523e-116">*définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="7523e-116">*definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-117">Définition de la tâche qui est inscrite.</span><span class="sxs-lookup"><span data-stu-id="7523e-117">The definition of the task that is registered.</span></span>

</dd> <dt>

<span data-ttu-id="7523e-118">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7523e-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-119">Constante [**de \_ création de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="7523e-119">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="7523e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7523e-120">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="7523e-121">Signification</span><span class="sxs-lookup"><span data-stu-id="7523e-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="7523e-122"><dt>**Tâche \_ VALIDER \_ uniquement**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-122"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="7523e-123">Le Planificateur de tâches vérifie la syntaxe du code XML qui décrit la tâche, mais n’inscrit pas la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-123">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="7523e-124">Cette constante ne peut pas être combinée **avec \_ la création**, la **\_ mise à jour** de tâches ou la **\_ création \_ ou la \_ mise à jour** de tâches.</span><span class="sxs-lookup"><span data-stu-id="7523e-124">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="7523e-125"><dt>**Tâche \_ CRÉER**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-125"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="7523e-126">L’Planificateur de tâches inscrit la tâche en tant que nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-126">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="7523e-127"><dt>**Tâche \_ METTRE à jour**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-127"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="7523e-128">L’Planificateur de tâches inscrit la tâche en tant que version mise à jour d’une tâche existante.</span><span class="sxs-lookup"><span data-stu-id="7523e-128">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="7523e-129">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="7523e-129">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="7523e-130"><dt>**Tâche \_ CRÉER \_ ou \_ mettre à jour**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-130"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="7523e-131">La Planificateur de tâches inscrit la tâche en tant que nouvelle tâche ou version mise à jour si la tâche existe déjà.</span><span class="sxs-lookup"><span data-stu-id="7523e-131">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="7523e-132">Équivaut à la \_ \| mise à jour des tâches de création de tâche \_ .</span><span class="sxs-lookup"><span data-stu-id="7523e-132">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="7523e-133"><dt>**Tâche \_ DÉSACTIVER**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-133"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="7523e-134">Le Planificateur de tâches désactive la tâche existante.</span><span class="sxs-lookup"><span data-stu-id="7523e-134">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="7523e-135"><dt>**Tâche \_ Ne pas \_ Ajouter le \_ principal \_ ACE**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-135"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="7523e-136">L’Planificateur de tâches ne peut pas ajouter l’entrée de contrôle d’accès (ACE) allow pour le principal de contexte.</span><span class="sxs-lookup"><span data-stu-id="7523e-136">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="7523e-137">Lorsque la fonction **TaskFolder. RegisterTaskDefinition** est appelée avec cet indicateur pour mettre à jour une tâche, le service Planificateur de tâches n’ajoute pas l’entrée du contrôle d’accès pour le nouveau contexte principal et ne supprime pas l’entrée du contrôle d’accès de l’ancien principal de contexte.</span><span class="sxs-lookup"><span data-stu-id="7523e-137">When the **TaskFolder.RegisterTaskDefinition** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="7523e-138"><dt>**Tâche \_ IGNORER \_ les \_ déclencheurs d’inscription**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-138"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="7523e-139">L’Planificateur de tâches crée la tâche, mais ignore les déclencheurs d’inscription dans la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-139">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="7523e-140">En ignorant les déclencheurs d’inscription, la tâche ne s’exécute pas lors de son inscription, sauf si un déclencheur basé sur la durée l’exécute lors de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="7523e-140">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="7523e-141">*userid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7523e-141">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-142">Informations d’identification de l’utilisateur utilisées pour inscrire la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-142">The user credentials that are used to register the task.</span></span> <span data-ttu-id="7523e-143">S’ils sont présents, ces informations d’identification sont prioritaires par rapport aux informations d’identification spécifiées dans l’objet de définition de tâche vers lequel pointe le paramètre de *définition* .</span><span class="sxs-lookup"><span data-stu-id="7523e-143">If present, these credentials take priority over the credentials specified in the task definition object pointed to by the *definition* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="7523e-144">Si la tâche est définie en tant que tâche Planificateur de tâches 1,0, n’utilisez pas de nom de groupe (au lieu d’un nom d’utilisateur spécifique) dans ce paramètre userId.</span><span class="sxs-lookup"><span data-stu-id="7523e-144">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="7523e-145">Une tâche est définie comme une tâche Planificateur de tâches 1,0 lorsque la propriété de [**compatibilité**](tasksettings-compatibility.md) est définie sur 1 dans les paramètres de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-145">A task is defined as a Task Scheduler 1.0 task when the [**Compatibility**](tasksettings-compatibility.md) property is set to 1 in the task's settings.</span></span>

 

</dd> <dt>

<span data-ttu-id="7523e-146">*mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7523e-146">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-147">Mot de passe de l’ID utilisateur utilisé pour inscrire la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-147">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="7523e-148">Lorsque le \_ type d’ouverture de session du compte de service d’ouverture de session \_ \_ est utilisé, le mot de passe doit être une valeur **Variant** vide telle que **VT \_ null** ou **VT \_ vide**.</span><span class="sxs-lookup"><span data-stu-id="7523e-148">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="7523e-149">*LogonType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7523e-149">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-150">Définit la technique d’ouverture de session utilisée pour exécuter la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="7523e-150">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="7523e-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7523e-151">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="7523e-152">Signification</span><span class="sxs-lookup"><span data-stu-id="7523e-152">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="7523e-153"><dt>**Tâche \_ Ouverture de session \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-153"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="7523e-154">La méthode d’ouverture de session n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7523e-154">The logon method is not specified.</span></span> <span data-ttu-id="7523e-155">Utilisé pour les informations d’identification non-NT.</span><span class="sxs-lookup"><span data-stu-id="7523e-155">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="7523e-156"><dt>**Tâche \_ \_Mot de passe de connexion**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-156"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="7523e-157">Utilisez un mot de passe pour la journalisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7523e-157">Use a password for logging on the user.</span></span> <span data-ttu-id="7523e-158">Le mot de passe doit être fourni au moment de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="7523e-158">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="7523e-159"><dt>**Tâche \_ CONNEXION \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-159"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="7523e-160">Utilisez un jeton interactif existant pour exécuter une tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-160">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="7523e-161">L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user).</span><span class="sxs-lookup"><span data-stu-id="7523e-161">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="7523e-162">Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a pas d’accès au réseau ou aux fichiers chiffrés.</span><span class="sxs-lookup"><span data-stu-id="7523e-162">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="7523e-163"><dt>**Tâche \_ Ouverture de session \_ interactive \_ Token**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-163"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="7523e-164">L’utilisateur doit déjà avoir ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="7523e-164">User must already be logged on.</span></span> <span data-ttu-id="7523e-165">La tâche est exécutée uniquement dans une session interactive existante.</span><span class="sxs-lookup"><span data-stu-id="7523e-165">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="7523e-166"><dt>**Tâche \_ \_Groupe d’ouverture de session**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-166"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="7523e-167">Activation du groupe.</span><span class="sxs-lookup"><span data-stu-id="7523e-167">Group activation.</span></span> <span data-ttu-id="7523e-168">Le champ **GroupID** spécifie le groupe.</span><span class="sxs-lookup"><span data-stu-id="7523e-168">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="7523e-169"><dt>**Tâche \_ \_ \_ Compte de service d’ouverture de session**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-169"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="7523e-170">Indique qu’un compte système local, service local ou service réseau est utilisé comme contexte de sécurité pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-170">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="7523e-171"><dt>**Tâche \_ Jeton interactif d’ouverture de session \_ \_ \_ ou \_ mot de passe**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-171"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="7523e-172">Utilisez d’abord le jeton interactif.</span><span class="sxs-lookup"><span data-stu-id="7523e-172">First use the interactive token.</span></span> <span data-ttu-id="7523e-173">Si l’utilisateur n’est pas connecté (aucun jeton interactif n’est disponible), le mot de passe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7523e-173">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="7523e-174">Le mot de passe doit être spécifié lors de l’inscription d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-174">The password must be specified when a task is registered.</span></span> <span data-ttu-id="7523e-175">Cet indicateur n’est pas recommandé pour les nouvelles tâches, car il est moins fiable que le \_ \_ mot de passe de connexion à la tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-175">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7523e-176">*langage SDDL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7523e-176">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-177">Descripteur de sécurité associé à la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="7523e-177">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="7523e-178">Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’une tâche afin d’autoriser ou de refuser l’accès à une tâche à certains utilisateurs et groupes.</span><span class="sxs-lookup"><span data-stu-id="7523e-178">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="7523e-179">Si l’accès à une tâche est refusé au compte système local, le service Planificateur de tâches peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="7523e-179">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="7523e-180">*tâche* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7523e-180">*task* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7523e-181">Objet [**RegisteredTask**](registeredtask.md) qui représente la nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="7523e-181">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7523e-182">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7523e-182">Return value</span></span>

<span data-ttu-id="7523e-183">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7523e-183">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7523e-184">Notes</span><span class="sxs-lookup"><span data-stu-id="7523e-184">Remarks</span></span>

<span data-ttu-id="7523e-185">Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="7523e-185">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="7523e-186">Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété [**LogonType**](principal-logontype.md) du principal de la tâche, ou dans le paramètre *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou **TaskFolder. RegisterTaskDefinition**.</span><span class="sxs-lookup"><span data-stu-id="7523e-186">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**.</span></span>

<span data-ttu-id="7523e-187">Seul un membre du groupe administrateurs peut créer une tâche avec un déclencheur de démarrage.</span><span class="sxs-lookup"><span data-stu-id="7523e-187">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="7523e-188">Vous pouvez inscrire correctement une tâche avec un groupe spécifié dans le paramètre *userid* et 3 (**\_ \_ \_ jeton interactif d’ouverture de session de tâche**) spécifiés dans le paramètre *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou **TaskFolder. RegisterTaskDefinition**, mais la tâche ne s’exécutera pas.</span><span class="sxs-lookup"><span data-stu-id="7523e-188">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**, but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="7523e-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7523e-189">Requirements</span></span>



| <span data-ttu-id="7523e-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7523e-190">Requirement</span></span> | <span data-ttu-id="7523e-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="7523e-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7523e-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7523e-192">Minimum supported client</span></span><br/> | <span data-ttu-id="7523e-193">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7523e-193">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7523e-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7523e-194">Minimum supported server</span></span><br/> | <span data-ttu-id="7523e-195">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7523e-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7523e-196">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7523e-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="7523e-197"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-197"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7523e-198">DLL</span><span class="sxs-lookup"><span data-stu-id="7523e-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7523e-199"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-199"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7523e-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7523e-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7523e-201">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7523e-201">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="7523e-202">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="7523e-202">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="7523e-203">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="7523e-203">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

 





