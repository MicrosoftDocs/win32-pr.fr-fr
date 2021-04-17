---
title: Méthode méthode ibackgroundcopyjob GetTimes (Deliveryoptimization. h)
description: Récupère les horodatages liés aux travaux, tels que l’heure à laquelle le travail a été créé ou modifié pour la dernière fois.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Méthode GetTimes
- Méthode GetTimes, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetTimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465518"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="ef0da-106">Méthode ibackgroundcopyjob :: GetTimes, méthode</span><span class="sxs-lookup"><span data-stu-id="ef0da-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="ef0da-107">Récupère les horodatages liés aux travaux, tels que l’heure à laquelle le travail a été créé ou modifié pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="ef0da-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0da-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef0da-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="ef0da-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef0da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef0da-110">*pTimes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef0da-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0da-111">Contient des horodatages liés aux travaux.</span><span class="sxs-lookup"><span data-stu-id="ef0da-111">Contains job-related time stamps.</span></span> <span data-ttu-id="ef0da-112">Pour connaître les horodatages disponibles, consultez la structure [**BG_JOB_TIMES**](bg-job-times.md) .</span><span class="sxs-lookup"><span data-stu-id="ef0da-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef0da-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef0da-113">Return value</span></span>

<span data-ttu-id="ef0da-114">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="ef0da-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="ef0da-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef0da-115">Return code</span></span>                                                                              | <span data-ttu-id="ef0da-116">Description</span><span class="sxs-lookup"><span data-stu-id="ef0da-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="ef0da-117"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ef0da-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="ef0da-118">Les horodatages ont été correctement récupérés.</span><span class="sxs-lookup"><span data-stu-id="ef0da-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef0da-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef0da-119">Requirements</span></span>



| <span data-ttu-id="ef0da-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef0da-120">Requirement</span></span> | <span data-ttu-id="ef0da-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef0da-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0da-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef0da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0da-123">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef0da-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef0da-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef0da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0da-125">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef0da-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef0da-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef0da-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef0da-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef0da-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef0da-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="ef0da-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef0da-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef0da-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef0da-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef0da-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef0da-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef0da-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ef0da-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0da-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0da-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0da-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ef0da-134">IID</span><span class="sxs-lookup"><span data-stu-id="ef0da-134">IID</span></span><br/>                      | <span data-ttu-id="ef0da-135">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="ef0da-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ef0da-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef0da-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0da-137">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="ef0da-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ef0da-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="ef0da-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





