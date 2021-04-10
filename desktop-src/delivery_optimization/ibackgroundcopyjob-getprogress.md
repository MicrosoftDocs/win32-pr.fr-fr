---
title: Méthode méthode ibackgroundcopyjob GetProgress (Deliveryoptimization. h)
description: Récupère des informations de progression relatives au travail, telles que le nombre d’octets et de fichiers transférés.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Méthode GetProgress
- Méthode GetProgress, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103954"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="b6967-106">Méthode ibackgroundcopyjob :: GetProgress, méthode</span><span class="sxs-lookup"><span data-stu-id="b6967-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="b6967-107">Récupère des informations de progression relatives au travail, telles que le nombre d’octets et de fichiers transférés.</span><span class="sxs-lookup"><span data-stu-id="b6967-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6967-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6967-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="b6967-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6967-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6967-110">*pProgress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6967-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6967-111">Contient des données que vous pouvez utiliser pour calculer le pourcentage d’achèvement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="b6967-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6967-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6967-112">Return value</span></span>

<span data-ttu-id="b6967-113">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="b6967-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b6967-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b6967-114">Return code</span></span>                                                                              | <span data-ttu-id="b6967-115">Description</span><span class="sxs-lookup"><span data-stu-id="b6967-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="b6967-116"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b6967-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b6967-117">Les informations de progression ont été récupérées avec succès.</span><span class="sxs-lookup"><span data-stu-id="b6967-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b6967-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6967-118">Requirements</span></span>



| <span data-ttu-id="b6967-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6967-119">Requirement</span></span> | <span data-ttu-id="b6967-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6967-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6967-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6967-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6967-122">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6967-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b6967-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6967-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6967-124">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6967-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b6967-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6967-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6967-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6967-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6967-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="b6967-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6967-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6967-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b6967-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6967-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6967-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6967-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b6967-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b6967-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6967-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6967-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b6967-133">IID</span><span class="sxs-lookup"><span data-stu-id="b6967-133">IID</span></span><br/>                      | <span data-ttu-id="b6967-134">IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="b6967-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b6967-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6967-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6967-136">**Méthode ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="b6967-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





