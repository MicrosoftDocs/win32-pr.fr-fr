---
title: Méthode ibackgroundcopyjob GetType, méthode (Deliveryoptimization. h)
description: Récupère le type de transfert effectué, tel qu’un téléchargement de fichier ou un chargement.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType (méthode)
- GetType, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032505"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="9ff7e-106">Méthode ibackgroundcopyjob :: GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="9ff7e-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="9ff7e-107">Récupère le type de transfert effectué, tel qu’un téléchargement de fichier ou un chargement.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff7e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ff7e-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="9ff7e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ff7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff7e-110">*pJobType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9ff7e-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff7e-111">Type de transfert effectué.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-111">Type of transfer being performed.</span></span> <span data-ttu-id="9ff7e-112">Pour obtenir la liste des types de transfert, consultez l’énumération [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff7e-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff7e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ff7e-113">Return value</span></span>

<span data-ttu-id="9ff7e-114">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9ff7e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9ff7e-115">Return code</span></span>                                                                              | <span data-ttu-id="9ff7e-116">Description</span><span class="sxs-lookup"><span data-stu-id="9ff7e-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="9ff7e-117"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7e-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="9ff7e-118">Le type de transfert a été correctement récupéré.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ff7e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9ff7e-119">Remarks</span></span>

<span data-ttu-id="9ff7e-120">Spécifiez le type de transfert lors de la création du travail.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff7e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ff7e-121">Requirements</span></span>



| <span data-ttu-id="9ff7e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ff7e-122">Requirement</span></span> | <span data-ttu-id="9ff7e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ff7e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff7e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ff7e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff7e-125">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ff7e-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9ff7e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ff7e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff7e-127">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ff7e-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9ff7e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ff7e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff7e-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7e-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ff7e-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="9ff7e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ff7e-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7e-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9ff7e-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ff7e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ff7e-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7e-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9ff7e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff7e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff7e-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff7e-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9ff7e-136">IID</span><span class="sxs-lookup"><span data-stu-id="9ff7e-136">IID</span></span><br/>                      | <span data-ttu-id="9ff7e-137">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="9ff7e-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9ff7e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ff7e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff7e-139">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="9ff7e-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9ff7e-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="9ff7e-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="9ff7e-141">**IBackgroundCopyManager :: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="9ff7e-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





