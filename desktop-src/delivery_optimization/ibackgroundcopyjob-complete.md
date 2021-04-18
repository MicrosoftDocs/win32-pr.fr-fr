---
title: Méthode ibackgroundcopyjob méthode Complete (Deliveryoptimization. h)
description: Met fin au travail et enregistre les fichiers transférés sur le client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Méthode complète
- Méthode complète, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode complète
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103657"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="dbe59-106">Méthode ibackgroundcopyjob :: Complete, méthode</span><span class="sxs-lookup"><span data-stu-id="dbe59-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="dbe59-107">Met fin au travail et enregistre les fichiers transférés sur le client.</span><span class="sxs-lookup"><span data-stu-id="dbe59-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe59-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbe59-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="dbe59-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbe59-109">Parameters</span></span>

<span data-ttu-id="dbe59-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dbe59-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbe59-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbe59-111">Return value</span></span>

<span data-ttu-id="dbe59-112">Cette méthode retourne les valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbe59-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="dbe59-113">La méthode peut également retourner des erreurs liées au changement du nom des copies temporaires des fichiers transférés en leurs noms donnés.</span><span class="sxs-lookup"><span data-stu-id="dbe59-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="dbe59-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dbe59-114">Return code</span></span>                                                                                          | <span data-ttu-id="dbe59-115">Description</span><span class="sxs-lookup"><span data-stu-id="dbe59-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbe59-116"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="dbe59-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="dbe59-117">Tous les fichiers ont été transférés avec succès.</span><span class="sxs-lookup"><span data-stu-id="dbe59-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="dbe59-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe59-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="dbe59-119">Pour les téléchargements, l’état du travail ne peut pas être BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="dbe59-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="dbe59-120">Pour les téléchargements, l’état du travail doit être BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="dbe59-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbe59-121">Notes</span><span class="sxs-lookup"><span data-stu-id="dbe59-121">Remarks</span></span>

<span data-ttu-id="dbe59-122">Tous les fichiers ont été transférés avec succès si l’état du travail est **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="dbe59-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="dbe59-123">Pour vérifier l’état de la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="dbe59-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="dbe59-124">Vous pouvez également implémenter l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) pour recevoir une notification lorsque tous les fichiers ont été transférés au client.</span><span class="sxs-lookup"><span data-stu-id="dbe59-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="dbe59-125">Conserve uniquement les tâches qui sont inférieures à 30 jours.</span><span class="sxs-lookup"><span data-stu-id="dbe59-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="dbe59-126">Tous les travaux plus anciens seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="dbe59-126">All older jobs will be removed.</span></span> <span data-ttu-id="dbe59-127">Ne prend pas en charge le stratégie de groupe [paramètre jobinactivitytimeout](https://www.bing.com/search?q=JobInactivityTimeout) .</span><span class="sxs-lookup"><span data-stu-id="dbe59-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="dbe59-128">Pour les travaux de téléchargement, vous pouvez appeler la méthode **complète** à tout moment pendant le processus de transfert. Toutefois, seuls les fichiers qui ont été transférés vers le client avant l’appel de cette méthode sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="dbe59-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="dbe59-129">Par exemple, si vous appelez la méthode **Complete** pendant que effectue le traitement du troisième des cinq fichiers, seuls les deux premiers fichiers sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="dbe59-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="dbe59-130">Pour déterminer les fichiers qui ont été transférés, appelez la méthode [**IBackgroundCopyFile :: GetProgress**](ibackgroundcopyfile-getprogress-method.md) et comparez le membre **bytesTransferred** au membre **bytesTotal** de la structure [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="dbe59-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="dbe59-131">Pour les travaux de chargement, vous pouvez appeler la méthode **Complete** uniquement lorsque l’état du travail est **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="dbe59-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="dbe59-132">Le propriétaire du fichier est l’utilisateur qui a effectué l’appel.</span><span class="sxs-lookup"><span data-stu-id="dbe59-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="dbe59-133">Par exemple, si un administrateur termine la tâche de quelqu’un d’autre, l’administrateur n’est pas propriétaire du travail.</span><span class="sxs-lookup"><span data-stu-id="dbe59-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe59-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbe59-134">Requirements</span></span>



| <span data-ttu-id="dbe59-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbe59-135">Requirement</span></span> | <span data-ttu-id="dbe59-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe59-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe59-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe59-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe59-138">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe59-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dbe59-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe59-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe59-140">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe59-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dbe59-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbe59-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe59-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe59-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbe59-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="dbe59-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dbe59-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dbe59-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="dbe59-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dbe59-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbe59-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbe59-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="dbe59-147">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe59-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbe59-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbe59-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="dbe59-149">IID</span><span class="sxs-lookup"><span data-stu-id="dbe59-149">IID</span></span><br/>                      | <span data-ttu-id="dbe59-150">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="dbe59-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dbe59-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe59-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe59-152">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="dbe59-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="dbe59-153">**Méthode ibackgroundcopyjob :: Cancel**</span><span class="sxs-lookup"><span data-stu-id="dbe59-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="dbe59-154">**Méthode ibackgroundcopyjob :: GetState**</span><span class="sxs-lookup"><span data-stu-id="dbe59-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





