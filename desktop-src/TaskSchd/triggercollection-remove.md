---
title: TriggerCollection. Remove, méthode
description: Pour les scripts, supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- déclenche Planificateur de tâches, suppression
- Supprimer la méthode Planificateur de tâches
- Remove, méthode Planificateur de tâches, objet TriggerCollection
- Objet TriggerCollection Planificateur de tâches, Remove, méthode
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317221"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="4e843-107">TriggerCollection. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="4e843-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="4e843-108">Pour les scripts, supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="4e843-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e843-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e843-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="4e843-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e843-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e843-111">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e843-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e843-112">Index du déclencheur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4e843-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e843-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e843-113">Return value</span></span>

<span data-ttu-id="4e843-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4e843-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e843-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4e843-115">Remarks</span></span>

<span data-ttu-id="4e843-116">Lorsque vous supprimez des éléments, Notez que l’index du premier élément de la collection est 1 et que l’index du dernier élément est la valeur de la propriété [**TriggerCollection. Count**](triggercollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="4e843-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e843-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e843-117">Requirements</span></span>



| <span data-ttu-id="4e843-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e843-118">Requirement</span></span> | <span data-ttu-id="4e843-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e843-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e843-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e843-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e843-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e843-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4e843-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e843-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e843-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e843-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e843-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4e843-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e843-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4e843-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4e843-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4e843-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e843-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e843-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e843-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e843-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e843-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4e843-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





