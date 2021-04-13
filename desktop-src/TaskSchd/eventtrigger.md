---
title: EventTrigger, objet (Windows. UI. Xaml. h)
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un événement système se produit.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Planificateur de tâches de déclencheur d’événement, objet
- Objet EventTrigger Planificateur de tâches
- Planificateur de tâches d’objets EventTrigger, Description
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509126"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="31d9a-106">EventTrigger (objet)</span><span class="sxs-lookup"><span data-stu-id="31d9a-106">EventTrigger object</span></span>

<span data-ttu-id="31d9a-107">Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="31d9a-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="31d9a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="31d9a-108">Members</span></span>

<span data-ttu-id="31d9a-109">L’objet **EventTrigger** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="31d9a-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="31d9a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31d9a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31d9a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31d9a-111">Properties</span></span>

<span data-ttu-id="31d9a-112">L’objet **EventTrigger** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="31d9a-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="31d9a-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="31d9a-113">Property</span></span>                                                            | <span data-ttu-id="31d9a-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="31d9a-114">Access type</span></span>           | <span data-ttu-id="31d9a-115">Description</span><span class="sxs-lookup"><span data-stu-id="31d9a-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31d9a-116">**Retard**</span><span class="sxs-lookup"><span data-stu-id="31d9a-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="31d9a-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-117">Read/write</span></span><br/> | <span data-ttu-id="31d9a-118">Obtient ou définit une valeur qui indique la durée écoulée entre le moment où l’événement se produit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="31d9a-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="31d9a-119">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="31d9a-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="31d9a-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-120">Read/write</span></span><br/> | <span data-ttu-id="31d9a-121">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-122">Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="31d9a-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="31d9a-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="31d9a-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="31d9a-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-124">Read/write</span></span><br/> | <span data-ttu-id="31d9a-125">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-126">Obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="31d9a-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="31d9a-127">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="31d9a-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="31d9a-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="31d9a-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="31d9a-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-129">Read/write</span></span><br/> | <span data-ttu-id="31d9a-130">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-131">Obtient ou définit la durée maximale pendant laquelle la tâche lancée par ce déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="31d9a-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="31d9a-132">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="31d9a-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="31d9a-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-133">Read/write</span></span><br/> | <span data-ttu-id="31d9a-134">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-135">Obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="31d9a-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="31d9a-136">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="31d9a-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="31d9a-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-137">Read/write</span></span><br/> | <span data-ttu-id="31d9a-138">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-139">Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="31d9a-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="31d9a-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="31d9a-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="31d9a-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-141">Read/write</span></span><br/> | <span data-ttu-id="31d9a-142">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-143">Obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="31d9a-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="31d9a-144">**Abonnement**</span><span class="sxs-lookup"><span data-stu-id="31d9a-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="31d9a-145">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-145">Read/write</span></span><br/> | <span data-ttu-id="31d9a-146">Obtient ou définit la chaîne de requête XPath qui identifie l’événement qui déclenche le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="31d9a-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="31d9a-147">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="31d9a-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="31d9a-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31d9a-148">Read-only</span></span><br/>  | <span data-ttu-id="31d9a-149">Héritée de l’objet [**déclencheur**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="31d9a-150">Obtient le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="31d9a-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="31d9a-151">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="31d9a-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="31d9a-152">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31d9a-152">Read/write</span></span><br/> | <span data-ttu-id="31d9a-153">Obtient ou définit une collection de requêtes XPath nommées.</span><span class="sxs-lookup"><span data-stu-id="31d9a-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="31d9a-154">Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans la propriété [**subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="31d9a-155">Le nom de la requête peut être utilisé en tant que variable dans le message d’une action [**ShowMessageAction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="31d9a-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31d9a-156">Notes</span><span class="sxs-lookup"><span data-stu-id="31d9a-156">Remarks</span></span>

<span data-ttu-id="31d9a-157">Vous pouvez créer au maximum 500 tâches avec des abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="31d9a-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="31d9a-158">Un abonnement aux événements qui interroge un grand nombre d’événements peut être utilisé pour déclencher une tâche qui utilise la même action en réponse aux événements journalisés.</span><span class="sxs-lookup"><span data-stu-id="31d9a-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="31d9a-159">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, un déclencheur d’événement est spécifié à l’aide de l’élément [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="31d9a-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="31d9a-160">Exemples</span><span class="sxs-lookup"><span data-stu-id="31d9a-160">Examples</span></span>

<span data-ttu-id="31d9a-161">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur d’événements (script)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31d9a-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="31d9a-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31d9a-162">Requirements</span></span>



| <span data-ttu-id="31d9a-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31d9a-163">Requirement</span></span> | <span data-ttu-id="31d9a-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="31d9a-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d9a-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31d9a-165">Minimum supported client</span></span><br/> | <span data-ttu-id="31d9a-166">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31d9a-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="31d9a-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31d9a-167">Minimum supported server</span></span><br/> | <span data-ttu-id="31d9a-168">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31d9a-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31d9a-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="31d9a-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d9a-170"><dt>Windows. UI. Xaml. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d9a-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="31d9a-171">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="31d9a-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="31d9a-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31d9a-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="31d9a-173">DLL</span><span class="sxs-lookup"><span data-stu-id="31d9a-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d9a-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d9a-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="31d9a-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31d9a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d9a-176">**Stead**</span><span class="sxs-lookup"><span data-stu-id="31d9a-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="31d9a-177">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="31d9a-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="31d9a-178">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="31d9a-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

