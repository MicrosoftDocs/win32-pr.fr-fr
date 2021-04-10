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
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="903f9-106">Méthode TaskFolder. RegisterTask</span><span class="sxs-lookup"><span data-stu-id="903f9-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="903f9-107">Pour les scripts, inscrit (crée) une nouvelle tâche dans le dossier à l’aide de XML pour définir la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="903f9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="903f9-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="903f9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="903f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="903f9-110">*chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-111">Nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-111">The name of the task.</span></span> <span data-ttu-id="903f9-112">Si cette valeur est **Nothing**, la tâche est inscrite dans le dossier racine de la tâche et le nom de la tâche est une valeur Guid créée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="903f9-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="903f9-113">Un nom de tâche ne peut pas commencer ou se terminer par un espace.</span><span class="sxs-lookup"><span data-stu-id="903f9-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="903f9-114">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="903f9-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="903f9-115">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="903f9-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="903f9-116">*XmlText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-117">Description de la tâche au format XML.</span><span class="sxs-lookup"><span data-stu-id="903f9-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="903f9-118">Les rubriques suivantes contiennent des tâches définies à l’aide de XML.</span><span class="sxs-lookup"><span data-stu-id="903f9-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="903f9-119">Exemple de déclencheur de temps (XML)</span><span class="sxs-lookup"><span data-stu-id="903f9-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="903f9-120">[Exemple de déclencheur d’événement (XML)](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="903f9-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="903f9-121">Exemple de déclencheur quotidien (XML)</span><span class="sxs-lookup"><span data-stu-id="903f9-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="903f9-122">Exemple de déclencheur d’inscription (XML)</span><span class="sxs-lookup"><span data-stu-id="903f9-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="903f9-123">Exemple de déclencheur hebdomadaire (XML)</span><span class="sxs-lookup"><span data-stu-id="903f9-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="903f9-124">Exemple de déclencheur LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="903f9-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="903f9-125">Exemple de déclencheur de démarrage (XML)</span><span class="sxs-lookup"><span data-stu-id="903f9-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="903f9-126">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-127">Constante [**de \_ création de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="903f9-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="903f9-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="903f9-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="903f9-129">Signification</span><span class="sxs-lookup"><span data-stu-id="903f9-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="903f9-130"><dt>**Tâche \_ VALIDER \_ uniquement**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="903f9-131">Le Planificateur de tâches vérifie la syntaxe du code XML qui décrit la tâche, mais n’inscrit pas la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="903f9-132">Cette constante ne peut pas être combinée **avec \_ la création**, la **\_ mise à jour** de tâches ou la **\_ création \_ ou la \_ mise à jour** de tâches.</span><span class="sxs-lookup"><span data-stu-id="903f9-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="903f9-133"><dt>**Tâche \_ CRÉER**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="903f9-134">L’Planificateur de tâches inscrit la tâche en tant que nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="903f9-135"><dt>**Tâche \_ METTRE à jour**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="903f9-136">L’Planificateur de tâches inscrit la tâche en tant que version mise à jour d’une tâche existante.</span><span class="sxs-lookup"><span data-stu-id="903f9-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="903f9-137">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="903f9-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="903f9-138"><dt>**Tâche \_ CRÉER \_ ou \_ mettre à jour**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="903f9-139">La Planificateur de tâches inscrit la tâche en tant que nouvelle tâche ou version mise à jour si la tâche existe déjà.</span><span class="sxs-lookup"><span data-stu-id="903f9-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="903f9-140">Équivaut à la \_ \| mise à jour des tâches de création de tâche \_ .</span><span class="sxs-lookup"><span data-stu-id="903f9-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="903f9-141"><dt>**Tâche \_ DÉSACTIVER**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="903f9-142">Le Planificateur de tâches désactive la tâche existante.</span><span class="sxs-lookup"><span data-stu-id="903f9-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="903f9-143"><dt>**Tâche \_ Ne pas \_ Ajouter le \_ principal \_ ACE**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="903f9-144">L’Planificateur de tâches ne peut pas ajouter l’entrée de contrôle d’accès (ACE) allow pour le principal de contexte.</span><span class="sxs-lookup"><span data-stu-id="903f9-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="903f9-145">Lorsque la fonction **TaskFolder. RegisterTask** est appelée avec cet indicateur pour mettre à jour une tâche, le service Planificateur de tâches n’ajoute pas l’entrée du contrôle d’accès pour le nouveau contexte principal et ne supprime pas l’entrée du contrôle d’accès de l’ancien principal de contexte.</span><span class="sxs-lookup"><span data-stu-id="903f9-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="903f9-146"><dt>**Tâche \_ IGNORER \_ les \_ déclencheurs d’inscription**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="903f9-147">L’Planificateur de tâches crée la tâche, mais ignore les déclencheurs d’inscription dans la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="903f9-148">En ignorant les déclencheurs d’inscription, la tâche ne s’exécute pas lors de son inscription, sauf si un déclencheur basé sur la durée l’exécute lors de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="903f9-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="903f9-149">*userid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-150">Informations d’identification de l’utilisateur utilisées pour inscrire la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="903f9-151">Si la tâche est définie en tant que tâche Planificateur de tâches 1,0, n’utilisez pas de nom de groupe (au lieu d’un nom d’utilisateur spécifique) dans ce paramètre userId.</span><span class="sxs-lookup"><span data-stu-id="903f9-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="903f9-152">Une tâche est définie comme une tâche Planificateur de tâches 1,0 lorsque l’attribut version de l’élément Task dans le code XML de la tâche est défini sur 1,1.</span><span class="sxs-lookup"><span data-stu-id="903f9-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="903f9-153">*mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-154">Mot de passe de l’ID utilisateur utilisé pour inscrire la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="903f9-155">Lorsque le \_ type d’ouverture de session du compte de service d’ouverture de session \_ \_ est utilisé, le mot de passe doit être une valeur **Variant** vide telle que **VT \_ null** ou **VT \_ vide**.</span><span class="sxs-lookup"><span data-stu-id="903f9-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="903f9-156">*LogonType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-157">Définit la technique d’ouverture de session utilisée pour exécuter la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="903f9-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="903f9-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="903f9-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="903f9-159">Signification</span><span class="sxs-lookup"><span data-stu-id="903f9-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="903f9-160"><dt>**Tâche \_ Ouverture de session \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="903f9-161">La méthode d’ouverture de session n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="903f9-161">The logon method is not specified.</span></span> <span data-ttu-id="903f9-162">Utilisé pour les informations d’identification non-NT.</span><span class="sxs-lookup"><span data-stu-id="903f9-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="903f9-163"><dt>**Tâche \_ \_Mot de passe de connexion**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="903f9-164">Utilisez un mot de passe pour la journalisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="903f9-164">Use a password for logging on the user.</span></span> <span data-ttu-id="903f9-165">Le mot de passe doit être fourni au moment de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="903f9-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="903f9-166"><dt>**Tâche \_ CONNEXION \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="903f9-167">Utilisez un jeton interactif existant pour exécuter une tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="903f9-168">L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user).</span><span class="sxs-lookup"><span data-stu-id="903f9-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="903f9-169">Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a pas d’accès au réseau ou aux fichiers chiffrés.</span><span class="sxs-lookup"><span data-stu-id="903f9-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="903f9-170"><dt>**Tâche \_ Ouverture de session \_ interactive \_ Token**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="903f9-171">L’utilisateur doit déjà avoir ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="903f9-171">User must already be logged on.</span></span> <span data-ttu-id="903f9-172">La tâche est exécutée uniquement dans une session interactive existante.</span><span class="sxs-lookup"><span data-stu-id="903f9-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="903f9-173"><dt>**Tâche \_ \_Groupe d’ouverture de session**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="903f9-174">Activation du groupe.</span><span class="sxs-lookup"><span data-stu-id="903f9-174">Group activation.</span></span> <span data-ttu-id="903f9-175">Le champ **GroupID** spécifie le groupe.</span><span class="sxs-lookup"><span data-stu-id="903f9-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="903f9-176"><dt>**Tâche \_ \_ \_ Compte de service d’ouverture de session**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="903f9-177">Indique qu’un compte système local, service local ou service réseau est utilisé comme contexte de sécurité pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="903f9-178"><dt>**Tâche \_ Jeton interactif d’ouverture de session \_ \_ \_ ou \_ mot de passe**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="903f9-179">Utilisez d’abord le jeton interactif.</span><span class="sxs-lookup"><span data-stu-id="903f9-179">First use the interactive token.</span></span> <span data-ttu-id="903f9-180">Si l’utilisateur n’est pas connecté (aucun jeton interactif n’est disponible), le mot de passe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="903f9-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="903f9-181">Le mot de passe doit être spécifié lors de l’inscription d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="903f9-182">Cet indicateur n’est pas recommandé pour les nouvelles tâches, car il est moins fiable que le \_ \_ mot de passe de connexion à la tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="903f9-183">*langage SDDL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="903f9-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-184">Descripteur de sécurité associé à la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="903f9-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="903f9-185">Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’une tâche afin d’autoriser ou de refuser l’accès à une tâche à certains utilisateurs et groupes.</span><span class="sxs-lookup"><span data-stu-id="903f9-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="903f9-186">Si l’accès à une tâche est refusé au compte système local, le service Planificateur de tâches peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="903f9-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="903f9-187">*ptask* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="903f9-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-188">Objet [**RegisteredTask**](registeredtask.md) qui représente la nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="903f9-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="903f9-189">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="903f9-189">Return value</span></span>

<span data-ttu-id="903f9-190">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="903f9-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="903f9-191">Notes</span><span class="sxs-lookup"><span data-stu-id="903f9-191">Remarks</span></span>

<span data-ttu-id="903f9-192">Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="903f9-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="903f9-193">Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété [**LogonType**](principal-logontype.md) du principal de la tâche, ou dans le paramètre *LogonType* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="903f9-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="903f9-194">Seul un membre du groupe administrateurs peut créer une tâche avec un déclencheur de démarrage.</span><span class="sxs-lookup"><span data-stu-id="903f9-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="903f9-195">Vous pouvez inscrire correctement une tâche avec un groupe spécifié dans le paramètre *userid* et 3 (**\_ \_ \_ jeton interactif d’ouverture de session de tâche**) spécifiés dans le paramètre *LogonType* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), mais la tâche ne s’exécutera pas.</span><span class="sxs-lookup"><span data-stu-id="903f9-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="903f9-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="903f9-196">Requirements</span></span>



| <span data-ttu-id="903f9-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="903f9-197">Requirement</span></span> | <span data-ttu-id="903f9-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="903f9-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="903f9-199">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="903f9-199">Minimum supported client</span></span><br/> | <span data-ttu-id="903f9-200">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="903f9-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="903f9-201">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="903f9-201">Minimum supported server</span></span><br/> | <span data-ttu-id="903f9-202">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="903f9-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="903f9-203">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="903f9-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="903f9-204"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="903f9-205">DLL</span><span class="sxs-lookup"><span data-stu-id="903f9-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="903f9-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="903f9-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="903f9-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="903f9-208">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="903f9-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="903f9-209">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="903f9-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="903f9-210">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="903f9-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

