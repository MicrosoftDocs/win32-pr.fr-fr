---
title: Objet TriggerCollection (Windows. UI. Xaml. h)
description: Objet de script utilisé pour ajouter, supprimer et récupérer les déclencheurs d’une tâche.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- déclencheurs Planificateur de tâches, objet de collection de déclencheurs
- Objet TriggerCollection Planificateur de tâches
- Planificateur de tâches d’objets TriggerCollection, Description
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103273"
---
# <a name="triggercollection-object"></a><span data-ttu-id="fb08d-106">Objet TriggerCollection</span><span class="sxs-lookup"><span data-stu-id="fb08d-106">TriggerCollection object</span></span>

<span data-ttu-id="fb08d-107">Objet de script utilisé pour ajouter, supprimer et récupérer les déclencheurs d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="fb08d-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="fb08d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fb08d-108">Members</span></span>

<span data-ttu-id="fb08d-109">L’objet **TriggerCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb08d-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="fb08d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb08d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="fb08d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb08d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fb08d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb08d-112">Methods</span></span>

<span data-ttu-id="fb08d-113">L’objet **TriggerCollection** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fb08d-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="fb08d-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="fb08d-114">Method</span></span>                                     | <span data-ttu-id="fb08d-115">Description</span><span class="sxs-lookup"><span data-stu-id="fb08d-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb08d-116">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="fb08d-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="fb08d-117">Efface tous les déclencheurs de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb08d-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="fb08d-118">**Créés**</span><span class="sxs-lookup"><span data-stu-id="fb08d-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="fb08d-119">Crée un déclencheur pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="fb08d-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="fb08d-120">**Installez**</span><span class="sxs-lookup"><span data-stu-id="fb08d-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="fb08d-121">Supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fb08d-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fb08d-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb08d-122">Properties</span></span>

<span data-ttu-id="fb08d-123">L’objet **TriggerCollection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fb08d-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="fb08d-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="fb08d-124">Property</span></span>                                            | <span data-ttu-id="fb08d-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="fb08d-125">Access type</span></span>          | <span data-ttu-id="fb08d-126">Description</span><span class="sxs-lookup"><span data-stu-id="fb08d-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="fb08d-127">**Saut**</span><span class="sxs-lookup"><span data-stu-id="fb08d-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="fb08d-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb08d-128">Read-only</span></span><br/> | <span data-ttu-id="fb08d-129">Obtient le nombre de déclencheurs dans la collection.</span><span class="sxs-lookup"><span data-stu-id="fb08d-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="fb08d-130">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fb08d-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="fb08d-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb08d-131">Read-only</span></span><br/> | <span data-ttu-id="fb08d-132">Obtient le déclencheur spécifié à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb08d-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb08d-133">Notes</span><span class="sxs-lookup"><span data-stu-id="fb08d-133">Remarks</span></span>

<span data-ttu-id="fb08d-134">Lors de la lecture ou de l’écriture de données XML pour une tâche, les déclencheurs de la tâche sont spécifiés dans l’élément [**triggers**](taskschedulerschema-triggers-tasktype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fb08d-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="fb08d-135">Pour plus d’informations sur chaque type de déclencheur, consultez [types de déclencheurs](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="fb08d-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fb08d-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="fb08d-136">Examples</span></span>

<span data-ttu-id="fb08d-137">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="fb08d-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb08d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb08d-138">Requirements</span></span>



| <span data-ttu-id="fb08d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb08d-139">Requirement</span></span> | <span data-ttu-id="fb08d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb08d-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb08d-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb08d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fb08d-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb08d-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fb08d-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb08d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fb08d-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb08d-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fb08d-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb08d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb08d-146"><dt>Windows. UI. Xaml. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb08d-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="fb08d-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fb08d-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb08d-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb08d-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="fb08d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="fb08d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb08d-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb08d-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="fb08d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb08d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb08d-152">**Stead**</span><span class="sxs-lookup"><span data-stu-id="fb08d-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





