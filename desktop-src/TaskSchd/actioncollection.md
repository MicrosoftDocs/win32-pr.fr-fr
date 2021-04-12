---
title: Objet ActionCollection
description: Objet de script qui contient les actions effectuées par la tâche.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- actions Planificateur de tâches, objet collection
- Objet ActionCollection Planificateur de tâches
- Planificateur de tâches d’objets ActionCollection, Description
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519145"
---
# <a name="actioncollection-object"></a><span data-ttu-id="4a639-106">Objet ActionCollection</span><span class="sxs-lookup"><span data-stu-id="4a639-106">ActionCollection object</span></span>

<span data-ttu-id="4a639-107">Objet de script qui contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="4a639-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="4a639-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4a639-108">Members</span></span>

<span data-ttu-id="4a639-109">L’objet **ActionCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4a639-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="4a639-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a639-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4a639-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4a639-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4a639-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a639-112">Methods</span></span>

<span data-ttu-id="4a639-113">L’objet **ActionCollection** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4a639-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="4a639-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="4a639-114">Method</span></span>                                    | <span data-ttu-id="4a639-115">Description</span><span class="sxs-lookup"><span data-stu-id="4a639-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="4a639-116">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="4a639-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="4a639-117">Efface toutes les actions de la collection.</span><span class="sxs-lookup"><span data-stu-id="4a639-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="4a639-118">**Créés**</span><span class="sxs-lookup"><span data-stu-id="4a639-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="4a639-119">Crée et ajoute une nouvelle action à la collection.</span><span class="sxs-lookup"><span data-stu-id="4a639-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="4a639-120">**Installez**</span><span class="sxs-lookup"><span data-stu-id="4a639-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="4a639-121">Supprime une action spécifiée de la collection.</span><span class="sxs-lookup"><span data-stu-id="4a639-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="4a639-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4a639-122">Properties</span></span>

<span data-ttu-id="4a639-123">L’objet **ActionCollection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4a639-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="4a639-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="4a639-124">Property</span></span>                                               | <span data-ttu-id="4a639-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="4a639-125">Access type</span></span>           | <span data-ttu-id="4a639-126">Description</span><span class="sxs-lookup"><span data-stu-id="4a639-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="4a639-127">**Context**</span><span class="sxs-lookup"><span data-stu-id="4a639-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="4a639-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4a639-128">Read/write</span></span><br/> | <span data-ttu-id="4a639-129">Obtient ou définit l’identificateur du principal pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="4a639-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="4a639-130">**Saut**</span><span class="sxs-lookup"><span data-stu-id="4a639-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="4a639-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4a639-131">Read-only</span></span><br/>  | <span data-ttu-id="4a639-132">Obtient le nombre d’actions dans la collection.</span><span class="sxs-lookup"><span data-stu-id="4a639-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="4a639-133">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4a639-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="4a639-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4a639-134">Read-only</span></span><br/>  | <span data-ttu-id="4a639-135">Obtient une action spécifiée de la collection.</span><span class="sxs-lookup"><span data-stu-id="4a639-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="4a639-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="4a639-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="4a639-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4a639-137">Read/write</span></span><br/> | <span data-ttu-id="4a639-138">Obtient ou définit une version au format XML de la collection.</span><span class="sxs-lookup"><span data-stu-id="4a639-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="4a639-139">Notes</span><span class="sxs-lookup"><span data-stu-id="4a639-139">Remarks</span></span>

<span data-ttu-id="4a639-140">Lors de la lecture ou de l’écriture de données XML, les actions d’une tâche sont spécifiées dans l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4a639-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="4a639-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="4a639-141">Examples</span></span>

<span data-ttu-id="4a639-142">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md), [exemple de déclenchement d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), exemple de [déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (](registration-trigger-example--scripting-.md)script), exemple de [déclencheur hebdomadaire (](weekly-trigger-example--scripting-.md)script), exemple de [déclencheur LOGON (script)](logon-trigger-example--scripting-.md)ou [exemple de déclencheur de démarrage](boot-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="4a639-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a639-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a639-143">Requirements</span></span>



| <span data-ttu-id="4a639-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a639-144">Requirement</span></span> | <span data-ttu-id="4a639-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a639-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a639-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a639-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4a639-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a639-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4a639-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a639-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4a639-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a639-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a639-150">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4a639-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a639-151"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a639-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a639-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4a639-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a639-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a639-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





