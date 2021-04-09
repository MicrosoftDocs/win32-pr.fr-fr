---
title: Méthode IBackgroundCopyManager CreateJob (Deliveryoptimization.h)
description: Crée un travail.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Méthode CreateJob
- Méthode CreateJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, méthode CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "104042889"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="4361a-106">IBackgroundCopyManager :: CreateJob, méthode</span><span class="sxs-lookup"><span data-stu-id="4361a-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="4361a-107">Crée un travail.</span><span class="sxs-lookup"><span data-stu-id="4361a-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4361a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4361a-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="4361a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4361a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4361a-110">*pDisplayName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4361a-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4361a-111">Chaîne terminée par le caractère null qui contient un nom complet pour le travail.</span><span class="sxs-lookup"><span data-stu-id="4361a-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="4361a-112">En règle générale, le nom complet est utilisé pour identifier la tâche dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4361a-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="4361a-113">Notez que plusieurs travaux peuvent avoir le même nom complet.</span><span class="sxs-lookup"><span data-stu-id="4361a-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="4361a-114">Ne doit pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4361a-114">Must not be **NULL**.</span></span> <span data-ttu-id="4361a-115">Le nom est limité à 256 caractères, à l’exclusion de la marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="4361a-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="4361a-116">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4361a-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4361a-117">Type de tâche de transfert, par exemple BG_JOB_TYPE_DOWNLOAD.</span><span class="sxs-lookup"><span data-stu-id="4361a-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="4361a-118">Pour obtenir la liste des types de transfert, consultez l’énumération [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4361a-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="4361a-119">*pJobID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4361a-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4361a-120">Identifie de façon unique votre travail dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4361a-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="4361a-121">Utilisez cet identificateur lorsque vous appelez la méthode [**IBackgroundCopyManager :: GetJob**](ibackgroundcopymanager-getjob.md) pour obtenir un travail à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4361a-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="4361a-122">*ppJob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4361a-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4361a-123">Pointeur d’interface [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) que vous utilisez pour modifier les propriétés du travail et spécifier les fichiers à transférer.</span><span class="sxs-lookup"><span data-stu-id="4361a-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="4361a-124">Pour activer le travail dans la file d’attente, appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="4361a-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="4361a-125">Libérez *ppJob* quand vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="4361a-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4361a-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4361a-126">Return value</span></span>

<span data-ttu-id="4361a-127">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="4361a-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="4361a-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4361a-128">Return code</span></span>                                                                              | <span data-ttu-id="4361a-129">Description</span><span class="sxs-lookup"><span data-stu-id="4361a-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4361a-130"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4361a-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="4361a-131">La nouvelle tâche a été générée.</span><span class="sxs-lookup"><span data-stu-id="4361a-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4361a-132">Notes</span><span class="sxs-lookup"><span data-stu-id="4361a-132">Remarks</span></span>

<span data-ttu-id="4361a-133">Seul l’utilisateur qui crée le travail ou un utilisateur disposant de privilèges d’administrateur peut [Ajouter des fichiers au travail](https://www.bing.com/search?q=add+files+to+the+job) et [modifier les propriétés du travail](https://www.bing.com/search?q=change+the+job's+properties).</span><span class="sxs-lookup"><span data-stu-id="4361a-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="4361a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4361a-134">Requirements</span></span>



| <span data-ttu-id="4361a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4361a-135">Requirement</span></span> | <span data-ttu-id="4361a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4361a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4361a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4361a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4361a-138">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4361a-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4361a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4361a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4361a-140">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4361a-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4361a-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="4361a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4361a-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4361a-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4361a-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="4361a-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4361a-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4361a-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4361a-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4361a-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="4361a-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4361a-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4361a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4361a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4361a-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4361a-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4361a-149">IID</span><span class="sxs-lookup"><span data-stu-id="4361a-149">IID</span></span><br/>                      | <span data-ttu-id="4361a-150">IID_IBackgroundCopyManager est défini en tant que 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="4361a-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4361a-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4361a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4361a-152">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="4361a-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="4361a-153">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="4361a-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="4361a-154">**Méthode ibackgroundcopyjob :: Resume**</span><span class="sxs-lookup"><span data-stu-id="4361a-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>
