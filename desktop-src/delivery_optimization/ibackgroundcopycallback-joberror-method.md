---
title: Méthode IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: L’optimisation de la remise (DO) appelle votre implémentation de la méthode JobError lorsque l’état du travail passe à BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Méthode JobError
- Méthode JobError, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, méthode JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384516"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="4609d-106">IBackgroundCopyCallback :: JobError, méthode</span><span class="sxs-lookup"><span data-stu-id="4609d-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="4609d-107">L’optimisation de la remise (DO) appelle votre implémentation de la méthode [**JobError**](https://www.bing.com/search?q=**JobError**) lorsque l’état du travail passe à BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="4609d-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="4609d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4609d-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="4609d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4609d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4609d-110">*pJob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4609d-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4609d-111">Contient des informations relatives au travail, telles que le nombre d’octets et de fichiers transférés avant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4609d-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="4609d-112">Elle contient également les méthodes de reprise et d’annulation du travail.</span><span class="sxs-lookup"><span data-stu-id="4609d-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="4609d-113">Ne libérez pas *pJob*; Libère l’interface lorsque la méthode [**JOBERROR**](https://www.bing.com/search?q=**JobError**) est retournée.</span><span class="sxs-lookup"><span data-stu-id="4609d-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="4609d-114">*perror* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4609d-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4609d-115">Contient des informations sur l’erreur, telles que le fichier en cours de traitement au moment où l’erreur irrécupérable s’est produite et une description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4609d-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="4609d-116">Ne libérez pas *perror*; Libère l’interface lorsque la méthode [**JOBERROR**](https://www.bing.com/search?q=**JobError**) est retournée.</span><span class="sxs-lookup"><span data-stu-id="4609d-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4609d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4609d-117">Return value</span></span>

<span data-ttu-id="4609d-118">Cette méthode doit retourner **S_OK**; dans le cas contraire, continue à appeler cette méthode jusqu’à ce que **S_OK** soit retourné.</span><span class="sxs-lookup"><span data-stu-id="4609d-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="4609d-119">Pour des raisons de performances, vous devez limiter le nombre de fois où vous retournez une valeur autre que **S_OK** à plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="4609d-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="4609d-120">Au lieu de retourner un code d’erreur, envisagez de retourner toujours **S_OK** et de gérer l’erreur en interne.</span><span class="sxs-lookup"><span data-stu-id="4609d-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="4609d-121">L’intervalle auquel cette méthode est appelée est arbitraire.</span><span class="sxs-lookup"><span data-stu-id="4609d-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="4609d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4609d-122">Remarks</span></span>

<span data-ttu-id="4609d-123">Après avoir déterminé la cause de l’erreur, effectuez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="4609d-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="4609d-124">Pour annuler la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="4609d-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="4609d-125">Pour accepter la partie du travail qui a été transférée correctement avant que l’erreur ne s’est produite, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="4609d-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="4609d-126">Cette option ne s’applique pas aux travaux de chargement ; vous ne pouvez pas effectuer une partie d’une tâche de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4609d-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="4609d-127">Pour terminer le traitement du travail, corrigez le problème, puis appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="4609d-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="4609d-128">Les erreurs temporaires ne génèrent pas d’appels à la méthode [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="4609d-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="4609d-129">Retourne BG_ERROR_CONTEXT_REMOTE_FILE si la tâche atteint une erreur HTTP 403, BG_ERROR_CONTEXT_NONE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4609d-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4609d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4609d-130">Requirements</span></span>



| <span data-ttu-id="4609d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4609d-131">Requirement</span></span> | <span data-ttu-id="4609d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4609d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4609d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4609d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4609d-134">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4609d-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4609d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4609d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4609d-136">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4609d-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4609d-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="4609d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4609d-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4609d-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4609d-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="4609d-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4609d-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4609d-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4609d-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4609d-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="4609d-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4609d-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4609d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4609d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4609d-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4609d-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4609d-145">IID</span><span class="sxs-lookup"><span data-stu-id="4609d-145">IID</span></span><br/>                      | <span data-ttu-id="4609d-146">IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="4609d-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4609d-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4609d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4609d-148">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="4609d-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="4609d-149">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="4609d-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="4609d-150">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="4609d-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="4609d-151">**Méthode ibackgroundcopyjob :: Cancel**</span><span class="sxs-lookup"><span data-stu-id="4609d-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="4609d-152">**Méthode ibackgroundcopyjob :: Resume**</span><span class="sxs-lookup"><span data-stu-id="4609d-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





