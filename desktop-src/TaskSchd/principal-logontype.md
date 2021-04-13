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
# <a name="principallogontype-property"></a><span data-ttu-id="03f37-106">Propriété principal. LogonType</span><span class="sxs-lookup"><span data-stu-id="03f37-106">Principal.LogonType property</span></span>

<span data-ttu-id="03f37-107">Pour les scripts, obtient ou définit la méthode de connexion à la sécurité requise pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="03f37-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f37-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03f37-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="03f37-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="03f37-109">Property value</span></span>

<span data-ttu-id="03f37-110">Définissez l’une des constantes d’énumération de [**\_ type d’ouverture de session des tâches**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) suivantes.</span><span class="sxs-lookup"><span data-stu-id="03f37-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="03f37-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f37-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="03f37-112">Signification</span><span class="sxs-lookup"><span data-stu-id="03f37-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="03f37-113"><dt>**Tâche \_ Ouverture de session \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="03f37-114">La méthode d’ouverture de session n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="03f37-114">The logon method is not specified.</span></span> <span data-ttu-id="03f37-115">Utilisé pour les informations d’identification non-NT.</span><span class="sxs-lookup"><span data-stu-id="03f37-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="03f37-116"><dt>**Tâche \_ \_Mot de passe de connexion**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="03f37-117">Utilisez un mot de passe pour la journalisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03f37-117">Use a password for logging on the user.</span></span> <span data-ttu-id="03f37-118">Le mot de passe doit être fourni au moment de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="03f37-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="03f37-119"><dt>**Tâche \_ CONNEXION \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="03f37-120">Utilisez un jeton interactif existant pour exécuter une tâche.</span><span class="sxs-lookup"><span data-stu-id="03f37-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="03f37-121">L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user).</span><span class="sxs-lookup"><span data-stu-id="03f37-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="03f37-122">Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a aucun accès au réseau ou aux fichiers chiffrés.</span><span class="sxs-lookup"><span data-stu-id="03f37-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="03f37-123"><dt>**Tâche \_ Ouverture de session \_ interactive \_ Token**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="03f37-124">L’utilisateur doit déjà avoir ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="03f37-124">User must already be logged on.</span></span> <span data-ttu-id="03f37-125">La tâche est exécutée uniquement dans une session interactive existante.</span><span class="sxs-lookup"><span data-stu-id="03f37-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="03f37-126"><dt>**Tâche \_ \_Groupe d’ouverture de session**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="03f37-127">Activation du groupe.</span><span class="sxs-lookup"><span data-stu-id="03f37-127">Group activation.</span></span> <span data-ttu-id="03f37-128">Le champ userId spécifie le groupe.</span><span class="sxs-lookup"><span data-stu-id="03f37-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="03f37-129"><dt>**Tâche \_ \_ \_ Compte de service d’ouverture de session**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="03f37-130">Indique qu’un compte système local, service local ou service réseau est utilisé comme contexte de sécurité pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="03f37-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="03f37-131"><dt>**Tâche \_ Jeton interactif d’ouverture de session \_ \_ \_ ou \_ mot de passe**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="03f37-132">Utilisez d’abord le jeton interactif.</span><span class="sxs-lookup"><span data-stu-id="03f37-132">First use the interactive token.</span></span> <span data-ttu-id="03f37-133">Si l’utilisateur n’est pas connecté (aucun jeton interactif n’est disponible), le mot de passe est utilisé.</span><span class="sxs-lookup"><span data-stu-id="03f37-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="03f37-134">Le mot de passe doit être spécifié lors de l’inscription d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="03f37-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="03f37-135">Cet indicateur n’est pas recommandé pour les nouvelles tâches, car il est moins fiable que le \_ \_ mot de passe de connexion à la tâche.</span><span class="sxs-lookup"><span data-stu-id="03f37-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03f37-136">Notes</span><span class="sxs-lookup"><span data-stu-id="03f37-136">Remarks</span></span>

<span data-ttu-id="03f37-137">Cette propriété est valide uniquement lorsqu’un identificateur d’utilisateur est spécifié par la propriété [**userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="03f37-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="03f37-138">Lors de la lecture ou de l’écriture de données XML pour une tâche, le type de connexion est spécifié dans l' [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) élément du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="03f37-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="03f37-139">Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="03f37-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="03f37-140">Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété **LogonType** du principal de la tâche, ou dans le paramètre *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="03f37-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03f37-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03f37-141">Requirements</span></span>



| <span data-ttu-id="03f37-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03f37-142">Requirement</span></span> | <span data-ttu-id="03f37-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f37-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f37-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f37-144">Minimum supported client</span></span><br/> | <span data-ttu-id="03f37-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03f37-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="03f37-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f37-146">Minimum supported server</span></span><br/> | <span data-ttu-id="03f37-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03f37-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03f37-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="03f37-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="03f37-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="03f37-150">DLL</span><span class="sxs-lookup"><span data-stu-id="03f37-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f37-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f37-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f37-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03f37-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f37-153">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="03f37-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="03f37-154">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="03f37-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





