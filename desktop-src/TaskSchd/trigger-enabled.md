---
title: Déclencheur. Enabled, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Planificateur de tâches de la propriété Enabled
- Propriété Enabled Planificateur de tâches, objet Trigger
- Objet Trigger Planificateur de tâches, propriété Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941888"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="ebd58-106">Déclencheur. Enabled, propriété</span><span class="sxs-lookup"><span data-stu-id="ebd58-106">Trigger.Enabled property</span></span>

<span data-ttu-id="ebd58-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="ebd58-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd58-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebd58-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ebd58-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ebd58-109">Property value</span></span>

<span data-ttu-id="ebd58-110">True si le déclencheur est activé ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="ebd58-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="ebd58-111">La valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="ebd58-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd58-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ebd58-112">Remarks</span></span>

<span data-ttu-id="ebd58-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, la propriété Enabled est spécifiée à l’aide de l’élément [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="ebd58-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd58-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebd58-114">Requirements</span></span>



| <span data-ttu-id="ebd58-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebd58-115">Requirement</span></span> | <span data-ttu-id="ebd58-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebd58-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd58-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebd58-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd58-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebd58-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ebd58-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebd58-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd58-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebd58-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebd58-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ebd58-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebd58-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ebd58-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ebd58-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd58-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd58-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd58-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd58-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd58-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd58-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ebd58-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





