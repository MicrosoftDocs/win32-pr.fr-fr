---
title: Propriété Trigger.Id
description: Pour les scripts, obtient ou définit l’identificateur pour le déclencheur.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Propriété ID Planificateur de tâches
- Propriété ID Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet Trigger, propriété ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508429"
---
# <a name="triggerid-property"></a><span data-ttu-id="8f964-106">Propriété Trigger.Id</span><span class="sxs-lookup"><span data-stu-id="8f964-106">Trigger.Id property</span></span>

<span data-ttu-id="8f964-107">Pour les scripts, obtient ou définit l’identificateur pour le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="8f964-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f964-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f964-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="8f964-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8f964-109">Property value</span></span>

<span data-ttu-id="8f964-110">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="8f964-110">The identifier for the trigger.</span></span> <span data-ttu-id="8f964-111">Cet identificateur est utilisé par le Planificateur de tâches à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="8f964-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f964-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8f964-112">Remarks</span></span>

<span data-ttu-id="8f964-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur du déclencheur est spécifié dans l’attribut ID des éléments Trigger individuels (par exemple, l’attribut ID de l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="8f964-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f964-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f964-114">Requirements</span></span>



| <span data-ttu-id="8f964-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f964-115">Requirement</span></span> | <span data-ttu-id="8f964-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f964-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f964-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f964-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f964-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f964-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8f964-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f964-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f964-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f964-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8f964-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8f964-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f964-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8f964-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8f964-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8f964-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f964-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f964-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f964-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f964-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f964-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8f964-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





