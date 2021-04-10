---
title: Interface IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Utilisez cette interface pour interroger ou définir plusieurs comportements facultatifs d’un travail.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105325"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="d1e00-105">Interface IBackgroundCopyJob5</span><span class="sxs-lookup"><span data-stu-id="d1e00-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="d1e00-106">Utilisez cette interface pour interroger ou définir plusieurs comportements facultatifs d’un travail.</span><span class="sxs-lookup"><span data-stu-id="d1e00-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="d1e00-107">Pour accéder à cette interface, appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** en utilisant `__uuidof(IBackgroundCopyJob5)` comme identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="d1e00-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="d1e00-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d1e00-108">Members</span></span>

<span data-ttu-id="d1e00-109">L’interface **IBackgroundCopyJob5** hérite de [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md).</span><span class="sxs-lookup"><span data-stu-id="d1e00-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="d1e00-110">**IBackgroundCopyJob5** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1e00-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="d1e00-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1e00-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d1e00-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1e00-112">Methods</span></span>

<span data-ttu-id="d1e00-113">L’interface **IBackgroundCopyJob5** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d1e00-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="d1e00-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="d1e00-114">Method</span></span>                                                 | <span data-ttu-id="d1e00-115">Description</span><span class="sxs-lookup"><span data-stu-id="d1e00-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="d1e00-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="d1e00-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="d1e00-117">Méthode générique pour l’obtention des propriétés de tâche DO.</span><span class="sxs-lookup"><span data-stu-id="d1e00-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="d1e00-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="d1e00-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="d1e00-119">Méthode générique pour définir les propriétés d’un travail.</span><span class="sxs-lookup"><span data-stu-id="d1e00-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1e00-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1e00-120">Requirements</span></span>



| <span data-ttu-id="d1e00-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1e00-121">Requirement</span></span> | <span data-ttu-id="d1e00-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1e00-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e00-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e00-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e00-124">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1e00-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d1e00-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e00-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e00-126">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1e00-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d1e00-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1e00-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e00-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e00-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1e00-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="d1e00-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1e00-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1e00-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d1e00-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1e00-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1e00-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1e00-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d1e00-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e00-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e00-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1e00-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d1e00-135">IID</span><span class="sxs-lookup"><span data-stu-id="d1e00-135">IID</span></span><br/>                      | <span data-ttu-id="d1e00-136">IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="d1e00-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d1e00-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1e00-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e00-138">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="d1e00-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





