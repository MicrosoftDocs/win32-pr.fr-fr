---
title: TriggerCollection. Item, propriété
description: Pour les scripts, obtient le déclencheur spécifié à partir de la collection.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet TriggerCollection
- Objet TriggerCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740773"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="aea2d-106">TriggerCollection. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="aea2d-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="aea2d-107">Pour les scripts, obtient le déclencheur spécifié à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="aea2d-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea2d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aea2d-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="aea2d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aea2d-109">Property value</span></span>

<span data-ttu-id="aea2d-110">Objet de [**déclencheur**](trigger.md) qui représente le déclencheur demandé.</span><span class="sxs-lookup"><span data-stu-id="aea2d-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea2d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="aea2d-111">Remarks</span></span>

<span data-ttu-id="aea2d-112">Les collections sont de base 1.</span><span class="sxs-lookup"><span data-stu-id="aea2d-112">Collections are 1-based.</span></span> <span data-ttu-id="aea2d-113">En d’autres termes, l’index du premier élément de la collection est 1.</span><span class="sxs-lookup"><span data-stu-id="aea2d-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea2d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aea2d-114">Requirements</span></span>



| <span data-ttu-id="aea2d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aea2d-115">Requirement</span></span> | <span data-ttu-id="aea2d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aea2d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aea2d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aea2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aea2d-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aea2d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aea2d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aea2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aea2d-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aea2d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aea2d-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="aea2d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="aea2d-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aea2d-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aea2d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aea2d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aea2d-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aea2d-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea2d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aea2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea2d-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aea2d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





