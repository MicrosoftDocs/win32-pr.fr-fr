---
title: Interface IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implémentez l’interface IBackgroundCopyCallback pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est erroné. Les clients utilisent cette interface au lieu d’interroger l’état du travail.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540774"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="c4561-106">Interface IBackgroundCopyCallback</span><span class="sxs-lookup"><span data-stu-id="c4561-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="c4561-107">Implémentez l’interface **IBackgroundCopyCallback** pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est erroné.</span><span class="sxs-lookup"><span data-stu-id="c4561-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="c4561-108">Les clients utilisent cette interface au lieu d’interroger l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="c4561-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="c4561-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c4561-109">Members</span></span>

<span data-ttu-id="c4561-110">L’interface **IBackgroundCopyCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c4561-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4561-111">**IBackgroundCopyCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4561-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c4561-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4561-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4561-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4561-113">Methods</span></span>

<span data-ttu-id="c4561-114">L’interface **IBackgroundCopyCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c4561-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="c4561-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="c4561-115">Method</span></span>                                                                    | <span data-ttu-id="c4561-116">Description</span><span class="sxs-lookup"><span data-stu-id="c4561-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="c4561-117">**JobError**</span><span class="sxs-lookup"><span data-stu-id="c4561-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="c4561-118">Appelée lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="c4561-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="c4561-119">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="c4561-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="c4561-120">Appelé lorsqu’un travail est modifié.</span><span class="sxs-lookup"><span data-stu-id="c4561-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="c4561-121">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="c4561-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="c4561-122">Appelé lorsque tous les fichiers du travail ont été transférés avec succès.</span><span class="sxs-lookup"><span data-stu-id="c4561-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4561-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c4561-123">Remarks</span></span>

<span data-ttu-id="c4561-124">Pour recevoir des notifications, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) pour spécifier le pointeur d’interface vers votre implémentation **IBackgroundCopyCallback** .</span><span class="sxs-lookup"><span data-stu-id="c4561-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="c4561-125">Pour spécifier les notifications que vous souhaitez recevoir, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .</span><span class="sxs-lookup"><span data-stu-id="c4561-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="c4561-126">Appelez vos rappels tant que le pointeur d’interface est valide.</span><span class="sxs-lookup"><span data-stu-id="c4561-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="c4561-127">L’interface de notification n’est plus valide lorsque votre application se termine ; Ne conserve pas l’interface Notify.</span><span class="sxs-lookup"><span data-stu-id="c4561-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="c4561-128">Par conséquent, le processus d’initialisation de votre application doit appeler la méthode [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) sur les tâches existantes pour lesquelles vous souhaitez recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="c4561-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4561-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4561-129">Requirements</span></span>



| <span data-ttu-id="c4561-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4561-130">Requirement</span></span> | <span data-ttu-id="c4561-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4561-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4561-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4561-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c4561-133">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4561-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4561-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4561-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c4561-135">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4561-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c4561-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4561-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4561-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4561-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4561-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="c4561-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4561-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4561-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4561-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4561-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4561-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4561-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c4561-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c4561-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4561-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4561-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c4561-144">IID</span><span class="sxs-lookup"><span data-stu-id="c4561-144">IID</span></span><br/>                      | <span data-ttu-id="c4561-145">IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="c4561-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c4561-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4561-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4561-147">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="c4561-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c4561-148">**Méthode ibackgroundcopyjob :: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="c4561-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="c4561-149">**Méthode ibackgroundcopyjob :: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="c4561-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

