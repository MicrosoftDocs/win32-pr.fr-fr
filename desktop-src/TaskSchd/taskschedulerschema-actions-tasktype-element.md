---
title: Élément actions (taskType)
description: Contient les actions effectuées par la tâche.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Élément actions (taskType) Planificateur de tâches
- actions Planificateur de tâches, XML
- Actions, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384224"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="52201-106">Élément actions (taskType)</span><span class="sxs-lookup"><span data-stu-id="52201-106">Actions (taskType) Element</span></span>

<span data-ttu-id="52201-107">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="52201-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="52201-108">L’élément **actions** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="52201-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="52201-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="52201-109">Parent element</span></span>



| <span data-ttu-id="52201-110">Élément</span><span class="sxs-lookup"><span data-stu-id="52201-110">Element</span></span>                                          | <span data-ttu-id="52201-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="52201-111">Derived from</span></span>                                                 | <span data-ttu-id="52201-112">Description</span><span class="sxs-lookup"><span data-stu-id="52201-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="52201-113">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="52201-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="52201-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="52201-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="52201-115">Décrit la tâche effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="52201-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="52201-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52201-116">Child elements</span></span>



| <span data-ttu-id="52201-117">Élément</span><span class="sxs-lookup"><span data-stu-id="52201-117">Element</span></span>                                                                    | <span data-ttu-id="52201-118">Type</span><span class="sxs-lookup"><span data-stu-id="52201-118">Type</span></span>                                                                       | <span data-ttu-id="52201-119">Description</span><span class="sxs-lookup"><span data-stu-id="52201-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="52201-120">**Comgérer**</span><span class="sxs-lookup"><span data-stu-id="52201-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="52201-121">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="52201-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="52201-122">Spécifie une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="52201-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="52201-123">**Exécutable**</span><span class="sxs-lookup"><span data-stu-id="52201-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="52201-124">**execType**</span><span class="sxs-lookup"><span data-stu-id="52201-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="52201-125">Spécifie une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="52201-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="52201-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="52201-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="52201-127">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="52201-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="52201-128">Spécifie une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="52201-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="52201-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="52201-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="52201-130">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="52201-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="52201-131">Spécifie une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="52201-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="52201-132">Attributs</span><span class="sxs-lookup"><span data-stu-id="52201-132">Attributes</span></span>



| <span data-ttu-id="52201-133">Nom</span><span class="sxs-lookup"><span data-stu-id="52201-133">Name</span></span>    | <span data-ttu-id="52201-134">Type</span><span class="sxs-lookup"><span data-stu-id="52201-134">Type</span></span> | <span data-ttu-id="52201-135">Description</span><span class="sxs-lookup"><span data-stu-id="52201-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52201-136">Context</span><span class="sxs-lookup"><span data-stu-id="52201-136">Context</span></span> |      | <span data-ttu-id="52201-137">Identificateur principal de l’utilisateur qui est le contexte de sécurité pour les actions de la tâche.</span><span class="sxs-lookup"><span data-stu-id="52201-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="52201-138">Notes</span><span class="sxs-lookup"><span data-stu-id="52201-138">Remarks</span></span>

<span data-ttu-id="52201-139">Les éléments enfants répertoriés précédemment (32 maximum) sont définis par le groupe [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="52201-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="52201-140">Ces éléments peuvent être ajoutés dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="52201-140">These elements can be added in any order.</span></span>

<span data-ttu-id="52201-141">Pour le développement C++, les actions d’une tâche sont définies dans l’interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .</span><span class="sxs-lookup"><span data-stu-id="52201-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="52201-142">Pour le développement de scripts, les actions d’une tâche sont définies dans l’objet [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="52201-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="52201-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="52201-143">Examples</span></span>

<span data-ttu-id="52201-144">Pour plus d’informations et pour obtenir un exemple complet de code XML pour une tâche qui contient une seule action d’exécution, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="52201-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52201-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52201-145">Requirements</span></span>



| <span data-ttu-id="52201-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52201-146">Requirement</span></span> | <span data-ttu-id="52201-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="52201-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52201-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52201-148">Minimum supported client</span></span><br/> | <span data-ttu-id="52201-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52201-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52201-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52201-150">Minimum supported server</span></span><br/> | <span data-ttu-id="52201-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52201-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52201-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52201-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52201-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="52201-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="52201-154">**actionGroup**</span><span class="sxs-lookup"><span data-stu-id="52201-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="52201-155">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="52201-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="52201-156">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="52201-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





