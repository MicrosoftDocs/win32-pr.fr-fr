---
title: Méthode méthode ibackgroundcopyjob SetNotifyInterface (Deliveryoptimization. h)
description: Identifie votre implémentation de l’interface IBackgroundCopyCallback. Utilisez l’interface IBackgroundCopyCallback pour recevoir la notification des événements liés aux travaux.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Méthode SetNotifyInterface
- Méthode SetNotifyInterface, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317225"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="364fc-107">Méthode ibackgroundcopyjob :: SetNotifyInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="364fc-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="364fc-108">Identifie votre implémentation de l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="364fc-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="364fc-109">Utilisez l’interface **IBackgroundCopyCallback** pour recevoir la notification des événements liés aux travaux.</span><span class="sxs-lookup"><span data-stu-id="364fc-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="364fc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="364fc-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="364fc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="364fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="364fc-112">*pNotifyInterface*</span><span class="sxs-lookup"><span data-stu-id="364fc-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="364fc-113">Pointeur d’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="364fc-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="364fc-114">Pour supprimer le pointeur d’interface de rappel actuel, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="364fc-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="364fc-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="364fc-115">Return value</span></span>

<span data-ttu-id="364fc-116">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="364fc-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="364fc-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="364fc-117">Return code</span></span>                                                                              | <span data-ttu-id="364fc-118">Description</span><span class="sxs-lookup"><span data-stu-id="364fc-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="364fc-119"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="364fc-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="364fc-120">Le pointeur d’interface de notification a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="364fc-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="364fc-121">Notes</span><span class="sxs-lookup"><span data-stu-id="364fc-121">Remarks</span></span>

<span data-ttu-id="364fc-122">Appelez cette méthode uniquement si vous implémentez l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="364fc-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="364fc-123">Utilisez la méthode **SetNotifyInterface** conjointement avec la méthode [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) pour spécifier le type de notification que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="364fc-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="364fc-124">L’interface de notification n’est plus valide quand votre application se termine ; Ne conserve pas l’interface Notify.</span><span class="sxs-lookup"><span data-stu-id="364fc-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="364fc-125">Par conséquent, le processus d’initialisation de votre application doit appeler la méthode **SetNotifyInterface** sur les tâches existantes pour lesquelles vous souhaitez recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="364fc-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="364fc-126">Si vous avez besoin de capturer l’État et les informations de progression qui se sont produites depuis la dernière exécution de votre application, interrogez les informations d’État et de progression pendant l’initialisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="364fc-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="364fc-127">Seul le propriétaire/créateur du travail ou un administrateur peut s’inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="364fc-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="364fc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="364fc-128">Requirements</span></span>



| <span data-ttu-id="364fc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="364fc-129">Requirement</span></span> | <span data-ttu-id="364fc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="364fc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="364fc-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="364fc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="364fc-132">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="364fc-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="364fc-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="364fc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="364fc-134">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="364fc-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="364fc-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="364fc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="364fc-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="364fc-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="364fc-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="364fc-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="364fc-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="364fc-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="364fc-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="364fc-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="364fc-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="364fc-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="364fc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="364fc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="364fc-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="364fc-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="364fc-143">IID</span><span class="sxs-lookup"><span data-stu-id="364fc-143">IID</span></span><br/>                      | <span data-ttu-id="364fc-144">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="364fc-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="364fc-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="364fc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="364fc-146">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="364fc-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="364fc-147">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="364fc-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="364fc-148">**Méthode ibackgroundcopyjob :: GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="364fc-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="364fc-149">**Méthode ibackgroundcopyjob :: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="364fc-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





