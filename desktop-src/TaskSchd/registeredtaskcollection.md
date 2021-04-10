---
title: Objet RegisteredTaskCollection
description: Objet de script qui contient toutes les tâches inscrites.
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- Objet RegisteredTaskCollection Planificateur de tâches
- Planificateur de tâches d’objets RegisteredTaskCollection, Description
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032537"
---
# <a name="registeredtaskcollection-object"></a><span data-ttu-id="c0a93-105">Objet RegisteredTaskCollection</span><span class="sxs-lookup"><span data-stu-id="c0a93-105">RegisteredTaskCollection object</span></span>

<span data-ttu-id="c0a93-106">Objet de script qui contient toutes les tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="c0a93-106">Scripting object that contains all the tasks that are registered.</span></span>

## <a name="members"></a><span data-ttu-id="c0a93-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c0a93-107">Members</span></span>

<span data-ttu-id="c0a93-108">L’objet **RegisteredTaskCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0a93-108">The **RegisteredTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="c0a93-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a93-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0a93-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0a93-110">Properties</span></span>

<span data-ttu-id="c0a93-111">L’objet **RegisteredTaskCollection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0a93-111">The **RegisteredTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="c0a93-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="c0a93-112">Property</span></span>                                                   | <span data-ttu-id="c0a93-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c0a93-113">Access type</span></span>          | <span data-ttu-id="c0a93-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0a93-114">Description</span></span>                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="c0a93-115">**Saut**</span><span class="sxs-lookup"><span data-stu-id="c0a93-115">**Count**</span></span>](registeredtaskcollection-count.md)<br/> | <span data-ttu-id="c0a93-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0a93-116">Read-only</span></span><br/> | <span data-ttu-id="c0a93-117">Obtient le nombre de tâches inscrites dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c0a93-117">Gets the number of registered tasks in the collection.</span></span><br/>  |
| [<span data-ttu-id="c0a93-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c0a93-118">**Item**</span></span>](registeredtaskcollection-item.md)<br/>   | <span data-ttu-id="c0a93-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0a93-119">Read-only</span></span><br/> | <span data-ttu-id="c0a93-120">Obtient la tâche inscrite spécifiée à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="c0a93-120">Gets the specified registered task from the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="c0a93-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0a93-121">Examples</span></span>

<span data-ttu-id="c0a93-122">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [affichage des noms et des États des tâches (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="c0a93-122">For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a93-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0a93-123">Requirements</span></span>



| <span data-ttu-id="c0a93-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0a93-124">Requirement</span></span> | <span data-ttu-id="c0a93-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0a93-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a93-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0a93-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a93-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0a93-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0a93-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0a93-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a93-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0a93-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0a93-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c0a93-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0a93-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0a93-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0a93-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c0a93-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0a93-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0a93-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a93-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0a93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a93-135">**TaskFolder.GetTasks**</span><span class="sxs-lookup"><span data-stu-id="c0a93-135">**TaskFolder.GetTasks**</span></span>](taskfolder-gettasks.md)
</dt> </dl>

 

 





