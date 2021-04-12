---
title: ActionCollection. Item, propriété
description: Pour les scripts, obtient une action spécifiée à partir de la collection.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet ActionCollection
- Objet ActionCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385012"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="4e124-106">ActionCollection. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="4e124-106">ActionCollection.Item property</span></span>

<span data-ttu-id="4e124-107">Pour les scripts, obtient une action spécifiée à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="4e124-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e124-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e124-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="4e124-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e124-109">Property value</span></span>

<span data-ttu-id="4e124-110">Objet d' [**action**](action.md) qui représente l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="4e124-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e124-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4e124-111">Remarks</span></span>

<span data-ttu-id="4e124-112">Les collections sont de base 1.</span><span class="sxs-lookup"><span data-stu-id="4e124-112">Collections are 1-based.</span></span> <span data-ttu-id="4e124-113">En d’autres termes, l’index du premier élément de la collection est 1.</span><span class="sxs-lookup"><span data-stu-id="4e124-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e124-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e124-114">Requirements</span></span>



| <span data-ttu-id="4e124-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e124-115">Requirement</span></span> | <span data-ttu-id="4e124-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e124-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e124-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e124-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4e124-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e124-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4e124-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e124-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4e124-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e124-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e124-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4e124-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e124-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4e124-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4e124-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4e124-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e124-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e124-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e124-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e124-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e124-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4e124-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4e124-127">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="4e124-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





