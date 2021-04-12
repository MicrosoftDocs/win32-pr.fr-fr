---
title: Objet ComHandlerAction
description: Objet de script qui représente une action qui déclenche un gestionnaire.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Action du gestionnaire COM Planificateur de tâches, objet
- Objet ComHandlerAction Planificateur de tâches
- Planificateur de tâches d’objets ComHandlerAction, Description
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464194"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="aa30d-106">Objet ComHandlerAction</span><span class="sxs-lookup"><span data-stu-id="aa30d-106">ComHandlerAction object</span></span>

<span data-ttu-id="aa30d-107">Objet de script qui représente une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="aa30d-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="aa30d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="aa30d-108">Members</span></span>

<span data-ttu-id="aa30d-109">L’objet **ComHandlerAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aa30d-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="aa30d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa30d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa30d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa30d-111">Properties</span></span>

<span data-ttu-id="aa30d-112">L’objet **ComHandlerAction** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa30d-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="aa30d-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="aa30d-113">Property</span></span>                                               | <span data-ttu-id="aa30d-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="aa30d-114">Access type</span></span>           | <span data-ttu-id="aa30d-115">Description</span><span class="sxs-lookup"><span data-stu-id="aa30d-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa30d-116">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="aa30d-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="aa30d-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa30d-117">Read/write</span></span><br/> | <span data-ttu-id="aa30d-118">Obtient ou définit l’identificateur de la classe de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="aa30d-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="aa30d-119">**Données**</span><span class="sxs-lookup"><span data-stu-id="aa30d-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="aa30d-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa30d-120">Read/write</span></span><br/> | <span data-ttu-id="aa30d-121">Obtient ou définit les données supplémentaires associées au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="aa30d-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="aa30d-122">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="aa30d-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="aa30d-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa30d-123">Read/write</span></span><br/> | <span data-ttu-id="aa30d-124">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="aa30d-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="aa30d-125">Obtient ou définit l’identificateur de l’action.</span><span class="sxs-lookup"><span data-stu-id="aa30d-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="aa30d-126">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="aa30d-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="aa30d-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aa30d-127">Read-only</span></span><br/>  | <span data-ttu-id="aa30d-128">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="aa30d-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="aa30d-129">Obtient le type d'action.</span><span class="sxs-lookup"><span data-stu-id="aa30d-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="aa30d-130">Notes</span><span class="sxs-lookup"><span data-stu-id="aa30d-130">Remarks</span></span>

<span data-ttu-id="aa30d-131">Les gestionnaires COM doivent implémenter l’interface [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) pour que le planificateur de tâches démarre et arrête le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="aa30d-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="aa30d-132">En retour, le gestionnaire COM utilise les méthodes de l’objet [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) pour communiquer l’état au planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="aa30d-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="aa30d-133">Lors de la lecture ou [**de l’écriture**](taskschedulerschema-comhandler-actiongroup-element.md) de données XML, une action de gestionnaire com est spécifiée dans l’élément comhandler du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="aa30d-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa30d-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa30d-134">Requirements</span></span>



| <span data-ttu-id="aa30d-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa30d-135">Requirement</span></span> | <span data-ttu-id="aa30d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa30d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa30d-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa30d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="aa30d-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa30d-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa30d-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa30d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="aa30d-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa30d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa30d-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="aa30d-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa30d-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa30d-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa30d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="aa30d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa30d-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa30d-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa30d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa30d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa30d-146">**TaskHandlerStatus**</span><span class="sxs-lookup"><span data-stu-id="aa30d-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="aa30d-147">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aa30d-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="aa30d-148">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aa30d-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





