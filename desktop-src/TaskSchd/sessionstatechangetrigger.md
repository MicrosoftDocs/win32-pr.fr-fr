---
title: Objet SessionStateChangeTrigger
description: Objet de script qui déclenche des tâches pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Objet SessionStateChangeTrigger Planificateur de tâches
- Planificateur de tâches d’objets SessionStateChangeTrigger, Description
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511545"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="46b1b-105">Objet SessionStateChangeTrigger</span><span class="sxs-lookup"><span data-stu-id="46b1b-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="46b1b-106">Objet de script qui déclenche des tâches pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail.</span><span class="sxs-lookup"><span data-stu-id="46b1b-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="46b1b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="46b1b-107">Members</span></span>

<span data-ttu-id="46b1b-108">L’objet **SessionStateChangeTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46b1b-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="46b1b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46b1b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46b1b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46b1b-110">Properties</span></span>

<span data-ttu-id="46b1b-111">L’objet **SessionStateChangeTrigger** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="46b1b-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="46b1b-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="46b1b-112">Property</span></span>                                                                | <span data-ttu-id="46b1b-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="46b1b-113">Access type</span></span>           | <span data-ttu-id="46b1b-114">Description</span><span class="sxs-lookup"><span data-stu-id="46b1b-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46b1b-115">**Retard**</span><span class="sxs-lookup"><span data-stu-id="46b1b-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="46b1b-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-116">Read/write</span></span><br/> | <span data-ttu-id="46b1b-117">Obtient ou définit une valeur qui indique la durée d’un délai avant le démarrage d’une tâche après la détection d’un changement d’état de session Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="46b1b-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="46b1b-118">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="46b1b-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="46b1b-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-119">Read/write</span></span><br/> | <span data-ttu-id="46b1b-120">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-121">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="46b1b-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="46b1b-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="46b1b-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="46b1b-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-123">Read/write</span></span><br/> | <span data-ttu-id="46b1b-124">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-125">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="46b1b-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="46b1b-126">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="46b1b-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="46b1b-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="46b1b-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="46b1b-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-128">Read/write</span></span><br/> | <span data-ttu-id="46b1b-129">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-130">Obtient ou définit la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="46b1b-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="46b1b-131">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="46b1b-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="46b1b-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-132">Read/write</span></span><br/> | <span data-ttu-id="46b1b-133">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-134">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="46b1b-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="46b1b-135">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="46b1b-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="46b1b-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-136">Read/write</span></span><br/> | <span data-ttu-id="46b1b-137">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-138">Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46b1b-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="46b1b-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="46b1b-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="46b1b-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-140">Read/write</span></span><br/> | <span data-ttu-id="46b1b-141">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-142">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="46b1b-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="46b1b-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="46b1b-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="46b1b-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-144">Read/write</span></span><br/> | <span data-ttu-id="46b1b-145">Obtient ou définit le type de Terminal Server modification de session qui déclenche un lancement de tâche.</span><span class="sxs-lookup"><span data-stu-id="46b1b-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="46b1b-146">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="46b1b-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="46b1b-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46b1b-147">Read-only</span></span><br/>  | <span data-ttu-id="46b1b-148">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="46b1b-149">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="46b1b-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="46b1b-150">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="46b1b-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="46b1b-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46b1b-151">Read/write</span></span><br/> | <span data-ttu-id="46b1b-152">Obtient ou définit l’utilisateur pour la session de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="46b1b-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="46b1b-153">Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="46b1b-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="46b1b-154">Notes</span><span class="sxs-lookup"><span data-stu-id="46b1b-154">Remarks</span></span>

<span data-ttu-id="46b1b-155">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, un déclencheur de changement d’état de session est spécifié à l’aide de l’élément [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="46b1b-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b1b-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46b1b-156">Requirements</span></span>



| <span data-ttu-id="46b1b-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46b1b-157">Requirement</span></span> | <span data-ttu-id="46b1b-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="46b1b-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46b1b-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46b1b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="46b1b-160">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46b1b-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46b1b-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46b1b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="46b1b-162">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46b1b-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46b1b-163">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="46b1b-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="46b1b-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46b1b-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46b1b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="46b1b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46b1b-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46b1b-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46b1b-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46b1b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b1b-168">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="46b1b-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="46b1b-169">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="46b1b-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





