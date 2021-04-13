---
title: Objet d’action
description: Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets d’action.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Objet d’action Planificateur de tâches
- Planificateur de tâches d’objet d’action, Description
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508882"
---
# <a name="action-object"></a><span data-ttu-id="20fcd-105">Objet d’action</span><span class="sxs-lookup"><span data-stu-id="20fcd-105">Action object</span></span>

<span data-ttu-id="20fcd-106">Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets d’action.</span><span class="sxs-lookup"><span data-stu-id="20fcd-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="20fcd-107">Un objet d’action est créé par la méthode [**ActionCollection. Create**](actioncollection-create.md) .</span><span class="sxs-lookup"><span data-stu-id="20fcd-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="20fcd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="20fcd-108">Members</span></span>

<span data-ttu-id="20fcd-109">L’objet d' **action** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="20fcd-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="20fcd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20fcd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20fcd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20fcd-111">Properties</span></span>

<span data-ttu-id="20fcd-112">L’objet d' **action** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="20fcd-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="20fcd-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="20fcd-113">Property</span></span>                               | <span data-ttu-id="20fcd-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="20fcd-114">Access type</span></span>           | <span data-ttu-id="20fcd-115">Description</span><span class="sxs-lookup"><span data-stu-id="20fcd-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="20fcd-116">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="20fcd-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="20fcd-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="20fcd-117">Read/write</span></span><br/> | <span data-ttu-id="20fcd-118">Obtient ou définit l’identificateur de l’action.</span><span class="sxs-lookup"><span data-stu-id="20fcd-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="20fcd-119">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="20fcd-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="20fcd-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20fcd-120">Read-only</span></span><br/>  | <span data-ttu-id="20fcd-121">Obtient le type d'action.</span><span class="sxs-lookup"><span data-stu-id="20fcd-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="20fcd-122">Notes</span><span class="sxs-lookup"><span data-stu-id="20fcd-122">Remarks</span></span>

<span data-ttu-id="20fcd-123">Pour plus d’informations sur la façon dont les actions et les tâches fonctionnent ensemble, consultez [actions des tâches](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="20fcd-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="20fcd-124">Le tableau suivant contient les objets de script qui représentent les actions qui peuvent être effectuées :</span><span class="sxs-lookup"><span data-stu-id="20fcd-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="20fcd-125">API</span><span class="sxs-lookup"><span data-stu-id="20fcd-125">API</span></span>                                            | <span data-ttu-id="20fcd-126">Description</span><span class="sxs-lookup"><span data-stu-id="20fcd-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="20fcd-127">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="20fcd-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="20fcd-128">Représente une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="20fcd-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="20fcd-129">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="20fcd-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="20fcd-130">Représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="20fcd-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="20fcd-131">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="20fcd-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="20fcd-132">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="20fcd-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="20fcd-133">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="20fcd-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="20fcd-134">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="20fcd-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="20fcd-135">Lors de la lecture ou de l’écriture de données XML, les actions d’une tâche sont spécifiées dans l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="20fcd-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="20fcd-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="20fcd-136">Examples</span></span>

<span data-ttu-id="20fcd-137">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md) , [exemple de déclenchement d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), exemple de [déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (](registration-trigger-example--scripting-.md)script), exemple de [déclencheur hebdomadaire (](weekly-trigger-example--scripting-.md)script), exemple de [déclencheur LOGON (script)](logon-trigger-example--scripting-.md)ou [exemple de déclencheur de démarrage](boot-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="20fcd-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20fcd-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20fcd-138">Requirements</span></span>



| <span data-ttu-id="20fcd-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20fcd-139">Requirement</span></span> | <span data-ttu-id="20fcd-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="20fcd-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20fcd-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20fcd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="20fcd-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20fcd-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="20fcd-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20fcd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="20fcd-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20fcd-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20fcd-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="20fcd-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="20fcd-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20fcd-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20fcd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="20fcd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20fcd-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20fcd-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fcd-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20fcd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fcd-150">Planificateur de tâches des objets de script</span><span class="sxs-lookup"><span data-stu-id="20fcd-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="20fcd-151">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="20fcd-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





