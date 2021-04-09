---
title: IBackgroundCopyJob5 GetProperty, méthode (Deliveryoptimization. h)
description: Méthode générique pour obtenir les propriétés du travail d’optimisation de la remise (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, méthode GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942217"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="be0ac-106">IBackgroundCopyJob5 :: GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="be0ac-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="be0ac-107">Méthode générique pour obtenir les propriétés du travail d’optimisation de la remise (DO).</span><span class="sxs-lookup"><span data-stu-id="be0ac-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be0ac-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="be0ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be0ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0ac-110">*PropertyId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be0ac-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0ac-111">ID de la propriété obtenue spécifiée comme [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valeur enum.</span><span class="sxs-lookup"><span data-stu-id="be0ac-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="be0ac-112">*pPropertyValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be0ac-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be0ac-113">Valeur de la propriété retournée en tant qu’BITS_JOB_PROPERTY_VALUE Union.</span><span class="sxs-lookup"><span data-stu-id="be0ac-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0ac-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be0ac-114">Return value</span></span>

<span data-ttu-id="be0ac-115">La méthode retourne les valeurs de retour suivantes.</span><span class="sxs-lookup"><span data-stu-id="be0ac-115">The method returns the following return values.</span></span>



| <span data-ttu-id="be0ac-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="be0ac-116">Return code</span></span>                                                                          | <span data-ttu-id="be0ac-117">Description</span><span class="sxs-lookup"><span data-stu-id="be0ac-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="be0ac-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be0ac-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="be0ac-119">Succès</span><span class="sxs-lookup"><span data-stu-id="be0ac-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be0ac-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be0ac-120">Requirements</span></span>



| <span data-ttu-id="be0ac-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be0ac-121">Requirement</span></span> | <span data-ttu-id="be0ac-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="be0ac-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be0ac-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be0ac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be0ac-124">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be0ac-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="be0ac-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be0ac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be0ac-126">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be0ac-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be0ac-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="be0ac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be0ac-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="be0ac-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="be0ac-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="be0ac-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be0ac-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be0ac-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="be0ac-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be0ac-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="be0ac-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be0ac-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="be0ac-133">DLL</span><span class="sxs-lookup"><span data-stu-id="be0ac-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be0ac-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be0ac-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="be0ac-135">IID</span><span class="sxs-lookup"><span data-stu-id="be0ac-135">IID</span></span><br/>                      | <span data-ttu-id="be0ac-136">IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="be0ac-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="be0ac-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be0ac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0ac-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="be0ac-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="be0ac-139">**IBackgroundCopyJob5 :: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="be0ac-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





