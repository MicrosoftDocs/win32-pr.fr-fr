---
title: Méthode IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Récupère un travail spécifié à partir de la file d’attente de transfert. En règle générale, votre application conserve l’identificateur de tâche, ce qui vous permet de récupérer ultérieurement la tâche à partir de la file d’attente.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Méthode GetJob
- Méthode GetJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, méthode GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518080"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="80172-107">IBackgroundCopyManager :: GetJob, méthode</span><span class="sxs-lookup"><span data-stu-id="80172-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="80172-108">Récupère un travail spécifié à partir de la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="80172-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="80172-109">En règle générale, votre application conserve l’identificateur de tâche, ce qui vous permet de récupérer ultérieurement la tâche à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="80172-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="80172-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80172-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="80172-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80172-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80172-112">*JobID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80172-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80172-113">Identifie le travail à récupérer à partir de la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="80172-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="80172-114">La méthode [**createJob**](ibackgroundcopymanager-createjob.md) retourne l’identificateur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="80172-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="80172-115">*ppJob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80172-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80172-116">Pointeur d’interface [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) vers le travail spécifié par *JobID*.</span><span class="sxs-lookup"><span data-stu-id="80172-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="80172-117">Lorsque vous avez terminé, libérez *ppJob*.</span><span class="sxs-lookup"><span data-stu-id="80172-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80172-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80172-118">Return value</span></span>

<span data-ttu-id="80172-119">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="80172-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="80172-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="80172-120">Return code</span></span>                                                                                      | <span data-ttu-id="80172-121">Description</span><span class="sxs-lookup"><span data-stu-id="80172-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="80172-122"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="80172-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="80172-123">La tâche a été récupérée à partir de la file d’attente de transfert.</span><span class="sxs-lookup"><span data-stu-id="80172-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="80172-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="80172-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="80172-125">La tâche est introuvable dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="80172-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="80172-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="80172-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="80172-127">L’utilisateur n’a pas l’autorisation de récupérer le travail.</span><span class="sxs-lookup"><span data-stu-id="80172-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="80172-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80172-128">Requirements</span></span>



| <span data-ttu-id="80172-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80172-129">Requirement</span></span> | <span data-ttu-id="80172-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="80172-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80172-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80172-131">Minimum supported client</span></span><br/> | <span data-ttu-id="80172-132">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80172-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="80172-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80172-133">Minimum supported server</span></span><br/> | <span data-ttu-id="80172-134">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80172-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="80172-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="80172-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="80172-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="80172-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="80172-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="80172-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80172-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80172-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="80172-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80172-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="80172-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80172-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="80172-141">DLL</span><span class="sxs-lookup"><span data-stu-id="80172-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80172-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80172-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="80172-143">IID</span><span class="sxs-lookup"><span data-stu-id="80172-143">IID</span></span><br/>                      | <span data-ttu-id="80172-144">IID_IBackgroundCopyManager est défini en tant que 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="80172-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="80172-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80172-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80172-146">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="80172-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="80172-147">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="80172-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="80172-148">**Méthode ibackgroundcopyjob :: GetId**</span><span class="sxs-lookup"><span data-stu-id="80172-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="80172-149">**IBackgroundCopyManager :: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="80172-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





