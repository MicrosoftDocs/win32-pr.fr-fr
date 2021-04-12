---
title: Méthode méthode ibackgroundcopyjob GetError (Deliveryoptimization. h)
description: Récupère l’interface d’erreur après qu’une erreur s’est produite.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Méthode GetError
- Méthode GetError, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384659"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="346d9-106">Méthode ibackgroundcopyjob :: GetError, méthode</span><span class="sxs-lookup"><span data-stu-id="346d9-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="346d9-107">Récupère l’interface d’erreur après qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="346d9-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="346d9-108">L’optimisation de la remise (DO) génère un objet d’erreur lorsque l’état du travail est BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="346d9-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="346d9-109">Le service ne crée pas d’objet d’erreur lorsqu’un appel à une méthode d’interface **IBackgroundCopyXXXX** échoue.</span><span class="sxs-lookup"><span data-stu-id="346d9-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="346d9-110">L’objet d’erreur est disponible jusqu’à ce que commence à transférer les données (l’état du travail passe à BG_JOB_STATE_TRANSFERRING) pour le travail ou jusqu’à ce que votre application se ferme.</span><span class="sxs-lookup"><span data-stu-id="346d9-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="346d9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="346d9-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="346d9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="346d9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346d9-113">*ppError* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="346d9-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="346d9-114">Interface d’erreur qui fournit le code d’erreur, une description de l’erreur et le contexte dans lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="346d9-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="346d9-115">Ce paramètre identifie également le fichier transféré au moment où l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="346d9-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="346d9-116">Libérez *ppError* quand vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="346d9-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346d9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="346d9-117">Return value</span></span>

<span data-ttu-id="346d9-118">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="346d9-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="346d9-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="346d9-119">Return code</span></span>                                                                                                           | <span data-ttu-id="346d9-120">Description</span><span class="sxs-lookup"><span data-stu-id="346d9-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="346d9-121"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="346d9-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="346d9-122">L’objet d’erreur a été généré.</span><span class="sxs-lookup"><span data-stu-id="346d9-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="346d9-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="346d9-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="346d9-124">L’interface d’erreur n’est disponible qu’après qu’une erreur s’est produite (BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR) et avant que ne commence à transférer les données (BG_JOB_STATE_TRANSFERRING).</span><span class="sxs-lookup"><span data-stu-id="346d9-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="346d9-125">Notes</span><span class="sxs-lookup"><span data-stu-id="346d9-125">Remarks</span></span>

<span data-ttu-id="346d9-126">Le travail est placé dans un état d’erreur en cas d’erreurs irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="346d9-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="346d9-127">Utilisez l’une des options suivantes pour déterminer si le travail est en erreur :</span><span class="sxs-lookup"><span data-stu-id="346d9-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="346d9-128">Pour interroger l’état de la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="346d9-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="346d9-129">Le travail est erroné si l’État est BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="346d9-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="346d9-130">Pour recevoir une notification lorsqu’une erreur se produit, implémentez l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (plus précisément, la méthode [**JobError**](https://www.bing.com/search?q=**JobError**) ).</span><span class="sxs-lookup"><span data-stu-id="346d9-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="346d9-131">Ensuite, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) pour inscrire le rappel et la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) pour définir l’indicateur de BG_NOTIFY_JOB_ERROR.</span><span class="sxs-lookup"><span data-stu-id="346d9-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="346d9-132">L’interface [**IBackgroundCopyError**](ibackgroundcopyerror.md) contient des informations que vous utilisez pour déterminer la cause de l’erreur et si le processus de transfert peut se poursuivre.</span><span class="sxs-lookup"><span data-stu-id="346d9-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="346d9-133">Après avoir déterminé la cause de l’erreur, effectuez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="346d9-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="346d9-134">Pour annuler la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="346d9-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="346d9-135">Pour enregistrer les fichiers qui ont été transférés avec succès avant que l’erreur ne se produise, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="346d9-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="346d9-136">Pour terminer le traitement du travail, corrigez le problème, puis appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="346d9-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="346d9-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="346d9-137">Requirements</span></span>



| <span data-ttu-id="346d9-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="346d9-138">Requirement</span></span> | <span data-ttu-id="346d9-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="346d9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346d9-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="346d9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="346d9-141">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="346d9-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="346d9-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="346d9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="346d9-143">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="346d9-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="346d9-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="346d9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="346d9-145"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="346d9-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="346d9-146">MIDL</span><span class="sxs-lookup"><span data-stu-id="346d9-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="346d9-147"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="346d9-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="346d9-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="346d9-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="346d9-149"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="346d9-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="346d9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="346d9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="346d9-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="346d9-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="346d9-152">IID</span><span class="sxs-lookup"><span data-stu-id="346d9-152">IID</span></span><br/>                      | <span data-ttu-id="346d9-153">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="346d9-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="346d9-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="346d9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346d9-155">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="346d9-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="346d9-156">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="346d9-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="346d9-157">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="346d9-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="346d9-158">**Méthode ibackgroundcopyjob :: GetState**</span><span class="sxs-lookup"><span data-stu-id="346d9-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





