---
title: Interface IBackgroundCopyManager (Deliveryoptimization. h)
description: Crée des tâches de transfert, extrait un objet énumérateur qui contient les travaux dans la file d’attente et extrait des tâches individuelles de la file d’attente.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942250"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="ad39f-105">Interface IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="ad39f-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="ad39f-106">Crée des tâches de transfert, extrait un objet énumérateur qui contient les travaux dans la file d’attente et extrait des tâches individuelles de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ad39f-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="ad39f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ad39f-107">Members</span></span>

<span data-ttu-id="ad39f-108">L’interface **IBackgroundCopyManager** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ad39f-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ad39f-109">**IBackgroundCopyManager** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ad39f-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="ad39f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ad39f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad39f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ad39f-111">Methods</span></span>

<span data-ttu-id="ad39f-112">L’interface **IBackgroundCopyManager** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ad39f-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="ad39f-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="ad39f-113">Method</span></span>                                                | <span data-ttu-id="ad39f-114">Description</span><span class="sxs-lookup"><span data-stu-id="ad39f-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="ad39f-115">**CreateJob**</span><span class="sxs-lookup"><span data-stu-id="ad39f-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="ad39f-116">Crée une tâche de transfert.</span><span class="sxs-lookup"><span data-stu-id="ad39f-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="ad39f-117">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="ad39f-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="ad39f-118">Récupère un travail spécifié de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ad39f-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad39f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad39f-119">Requirements</span></span>



| <span data-ttu-id="ad39f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad39f-120">Requirement</span></span> | <span data-ttu-id="ad39f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad39f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad39f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad39f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad39f-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad39f-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ad39f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad39f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad39f-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad39f-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ad39f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad39f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad39f-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad39f-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad39f-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="ad39f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ad39f-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad39f-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ad39f-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad39f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad39f-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad39f-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ad39f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ad39f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad39f-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad39f-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ad39f-134">IID</span><span class="sxs-lookup"><span data-stu-id="ad39f-134">IID</span></span><br/>                      | <span data-ttu-id="ad39f-135">IID_IBackgroundCopyManager est défini en tant que 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="ad39f-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ad39f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad39f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad39f-137">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="ad39f-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

