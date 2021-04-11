---
title: RunningTaskCollection. Item, propriété
description: Pour les scripts, obtient la tâche spécifiée à partir de la collection.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet RunningTaskCollection
- Objet RunningTaskCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104650"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="b5153-106">RunningTaskCollection. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="b5153-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="b5153-107">Pour les scripts, obtient la tâche spécifiée à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="b5153-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5153-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5153-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="b5153-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b5153-109">Property value</span></span>

<span data-ttu-id="b5153-110">Objet [**RunningTask**](runningtask.md) qui contient le contexte demandé.</span><span class="sxs-lookup"><span data-stu-id="b5153-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5153-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b5153-111">Remarks</span></span>

<span data-ttu-id="b5153-112">Les collections sont de base 1.</span><span class="sxs-lookup"><span data-stu-id="b5153-112">Collections are 1-based.</span></span> <span data-ttu-id="b5153-113">En d’autres termes, l’index du premier élément de la collection est 1.</span><span class="sxs-lookup"><span data-stu-id="b5153-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5153-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5153-114">Requirements</span></span>



| <span data-ttu-id="b5153-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5153-115">Requirement</span></span> | <span data-ttu-id="b5153-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5153-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5153-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5153-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5153-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5153-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5153-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5153-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5153-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5153-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5153-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b5153-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5153-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5153-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5153-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b5153-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5153-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5153-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5153-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5153-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5153-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b5153-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





