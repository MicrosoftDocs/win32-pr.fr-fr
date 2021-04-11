---
title: Objet LogonTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Planificateur de tâches de déclencheur de connexion, objet
- Objet LogonTrigger Planificateur de tâches
- Planificateur de tâches d’objets LogonTrigger, Description
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942426"
---
# <a name="logontrigger-object"></a><span data-ttu-id="69be7-106">Objet LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="69be7-106">LogonTrigger object</span></span>

<span data-ttu-id="69be7-107">Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="69be7-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="69be7-108">Au démarrage du service Planificateur de tâches, tous les utilisateurs connectés sont énumérés et toutes les tâches inscrites avec des déclencheurs de connexion qui correspondent à l’utilisateur connecté sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="69be7-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="69be7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="69be7-109">Members</span></span>

<span data-ttu-id="69be7-110">L’objet **LogonTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="69be7-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="69be7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69be7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69be7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69be7-112">Properties</span></span>

<span data-ttu-id="69be7-113">L’objet **LogonTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="69be7-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="69be7-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="69be7-114">Property</span></span>                                                            | <span data-ttu-id="69be7-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="69be7-115">Access type</span></span>           | <span data-ttu-id="69be7-116">Description</span><span class="sxs-lookup"><span data-stu-id="69be7-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69be7-117">**Retard**</span><span class="sxs-lookup"><span data-stu-id="69be7-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="69be7-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-118">Read/write</span></span><br/> | <span data-ttu-id="69be7-119">Obtient ou définit une valeur qui indique la durée entre le moment où l’utilisateur ouvre une session et le moment où le travail est démarré.</span><span class="sxs-lookup"><span data-stu-id="69be7-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="69be7-120">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="69be7-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="69be7-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-121">Read/write</span></span><br/> | <span data-ttu-id="69be7-122">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-123">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="69be7-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="69be7-124">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="69be7-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="69be7-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-125">Read/write</span></span><br/> | <span data-ttu-id="69be7-126">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-127">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="69be7-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="69be7-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="69be7-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="69be7-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="69be7-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="69be7-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-130">Read/write</span></span><br/> | <span data-ttu-id="69be7-131">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-132">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="69be7-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="69be7-133">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="69be7-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="69be7-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-134">Read/write</span></span><br/> | <span data-ttu-id="69be7-135">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-136">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="69be7-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="69be7-137">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="69be7-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="69be7-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-138">Read/write</span></span><br/> | <span data-ttu-id="69be7-139">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-140">Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="69be7-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="69be7-141">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="69be7-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="69be7-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-142">Read/write</span></span><br/> | <span data-ttu-id="69be7-143">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-144">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="69be7-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="69be7-145">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="69be7-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="69be7-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69be7-146">Read-only</span></span><br/>  | <span data-ttu-id="69be7-147">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="69be7-148">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="69be7-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="69be7-149">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="69be7-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="69be7-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69be7-150">Read/write</span></span><br/> | <span data-ttu-id="69be7-151">Obtient ou définit l'identificateur de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69be7-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="69be7-152">Notes</span><span class="sxs-lookup"><span data-stu-id="69be7-152">Remarks</span></span>

<span data-ttu-id="69be7-153">Si vous souhaitez qu’une tâche soit déclenchée lorsqu’un membre d’un groupe se connecte à l’ordinateur plutôt qu’à un utilisateur spécifique, n’affectez pas de valeur à la propriété [**LogonTrigger. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="69be7-154">Au lieu de cela, créez un déclencheur LOGON avec une propriété **LogonTrigger. UserID** vide et attribuez une valeur au principal pour la tâche à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="69be7-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="69be7-155">Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur LOGON est spécifié à l’aide de l’élément [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="69be7-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="69be7-156">Exemples</span><span class="sxs-lookup"><span data-stu-id="69be7-156">Examples</span></span>

<span data-ttu-id="69be7-157">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur de connexion (script)](logon-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="69be7-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69be7-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69be7-158">Requirements</span></span>



| <span data-ttu-id="69be7-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69be7-159">Requirement</span></span> | <span data-ttu-id="69be7-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="69be7-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69be7-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69be7-161">Minimum supported client</span></span><br/> | <span data-ttu-id="69be7-162">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69be7-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="69be7-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69be7-163">Minimum supported server</span></span><br/> | <span data-ttu-id="69be7-164">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69be7-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69be7-165">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="69be7-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="69be7-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="69be7-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="69be7-167">DLL</span><span class="sxs-lookup"><span data-stu-id="69be7-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69be7-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69be7-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69be7-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69be7-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69be7-170">**Stead**</span><span class="sxs-lookup"><span data-stu-id="69be7-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





