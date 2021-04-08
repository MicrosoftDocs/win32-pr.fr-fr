---
title: ActionCollection. Remove, méthode
description: Pour les scripts, supprime l’action spécifiée de la collection.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Supprimer la méthode Planificateur de tâches
- Remove, méthode Planificateur de tâches, objet ActionCollection
- Objet ActionCollection Planificateur de tâches, Remove, méthode
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742461"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="0d006-106">ActionCollection. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="0d006-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="0d006-107">Pour les scripts, supprime l’action spécifiée de la collection.</span><span class="sxs-lookup"><span data-stu-id="0d006-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d006-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d006-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="0d006-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d006-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d006-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d006-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d006-111">Index de l’action à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0d006-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d006-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d006-112">Return value</span></span>

<span data-ttu-id="0d006-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0d006-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d006-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0d006-114">Remarks</span></span>

<span data-ttu-id="0d006-115">Lorsque vous supprimez des éléments, Notez que l’index du premier élément de la collection est 1 et que l’index du dernier élément est la valeur de la propriété [**ActionCollection. Count**](actioncollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="0d006-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d006-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d006-116">Requirements</span></span>



| <span data-ttu-id="0d006-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d006-117">Requirement</span></span> | <span data-ttu-id="0d006-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d006-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d006-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d006-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d006-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d006-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0d006-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d006-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d006-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d006-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d006-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0d006-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d006-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d006-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d006-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d006-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d006-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d006-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d006-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d006-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d006-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0d006-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0d006-129">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="0d006-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





