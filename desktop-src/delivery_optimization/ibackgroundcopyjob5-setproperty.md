---
title: IBackgroundCopyJob5 SetProperty, méthode (Deliveryoptimization. h)
description: Méthode générique pour définir les propriétés d’une tâche d’optimisation de la remise.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, méthode SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742860"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="9fd8d-106">IBackgroundCopyJob5 :: SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="9fd8d-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="9fd8d-107">Méthode générique pour définir les propriétés d’une tâche d’optimisation de la remise.</span><span class="sxs-lookup"><span data-stu-id="9fd8d-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd8d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fd8d-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="9fd8d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fd8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd8d-110">*PropertyId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9fd8d-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fd8d-111">ID de la propriété définie spécifiée comme [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valeur d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9fd8d-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="9fd8d-112">*PropertyValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9fd8d-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fd8d-113">Valeur de la propriété qui est définie.</span><span class="sxs-lookup"><span data-stu-id="9fd8d-113">The value of the property that is being set.</span></span> <span data-ttu-id="9fd8d-114">Pour stocker une valeur dont le type est approprié à la propriété, cette valeur est spécifiée via le [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Union qui est composé de tous les types de propriété connus.</span><span class="sxs-lookup"><span data-stu-id="9fd8d-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd8d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fd8d-115">Return value</span></span>

<span data-ttu-id="9fd8d-116">La méthode retourne les valeurs de retour suivantes.</span><span class="sxs-lookup"><span data-stu-id="9fd8d-116">The method returns the following return values.</span></span>



| <span data-ttu-id="9fd8d-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9fd8d-117">Return code</span></span>                                                                          | <span data-ttu-id="9fd8d-118">Description</span><span class="sxs-lookup"><span data-stu-id="9fd8d-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="9fd8d-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9fd8d-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="9fd8d-120">Succès</span><span class="sxs-lookup"><span data-stu-id="9fd8d-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9fd8d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fd8d-121">Requirements</span></span>



| <span data-ttu-id="9fd8d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fd8d-122">Requirement</span></span> | <span data-ttu-id="9fd8d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fd8d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd8d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd8d-125">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fd8d-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9fd8d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd8d-127">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fd8d-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9fd8d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fd8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd8d-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd8d-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fd8d-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="9fd8d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9fd8d-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9fd8d-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9fd8d-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9fd8d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fd8d-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fd8d-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9fd8d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9fd8d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fd8d-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fd8d-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9fd8d-136">IID</span><span class="sxs-lookup"><span data-stu-id="9fd8d-136">IID</span></span><br/>                      | <span data-ttu-id="9fd8d-137">IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="9fd8d-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="9fd8d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fd8d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd8d-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="9fd8d-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="9fd8d-140">**IBackgroundCopyJob5 :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="9fd8d-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





