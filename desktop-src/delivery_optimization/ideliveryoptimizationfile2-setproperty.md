---
title: 'IDeliveryOptimizationFile2 :: SetProperty, méthode'
description: 'Cette méthode retourne une seule propriété du fichier DO. | IDeliveryOptimizationFile2 :: SetProperty, méthode'
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, méthode SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535778"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="0f7a8-107">IDeliveryOptimizationFile2 :: SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="0f7a8-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="0f7a8-108">Cette méthode retourne une seule propriété du fichier DO.</span><span class="sxs-lookup"><span data-stu-id="0f7a8-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7a8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f7a8-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="0f7a8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f7a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7a8-111">*propid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f7a8-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7a8-112">ID de propriété requis à définir de type DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0f7a8-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="0f7a8-113">*propvalue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f7a8-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7a8-114">Valeur de la propriété à définir, de type VARIANT.</span><span class="sxs-lookup"><span data-stu-id="0f7a8-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7a8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f7a8-115">Return value</span></span>

<span data-ttu-id="0f7a8-116">Cette méthode retourne les valeurs HRESULT suivantes.</span><span class="sxs-lookup"><span data-stu-id="0f7a8-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="0f7a8-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0f7a8-117">Return code</span></span>                  | <span data-ttu-id="0f7a8-118">Description</span><span class="sxs-lookup"><span data-stu-id="0f7a8-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0f7a8-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="0f7a8-119">**S_OK**</span></span>                     | <span data-ttu-id="0f7a8-120">Succès</span><span class="sxs-lookup"><span data-stu-id="0f7a8-120">Success</span></span>                                                            |
| <span data-ttu-id="0f7a8-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="0f7a8-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="0f7a8-122">ID de propriété inconnu</span><span class="sxs-lookup"><span data-stu-id="0f7a8-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="0f7a8-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="0f7a8-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="0f7a8-124">Le travail n’est pas actuellement dans un État qui autorise un paramètre de propriété</span><span class="sxs-lookup"><span data-stu-id="0f7a8-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="0f7a8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f7a8-125">Requirements</span></span>

| <span data-ttu-id="0f7a8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f7a8-126">Requirement</span></span> | <span data-ttu-id="0f7a8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f7a8-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f7a8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f7a8-128">Minimum supported client</span></span>  | <span data-ttu-id="0f7a8-129">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f7a8-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="0f7a8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f7a8-130">Minimum supported server</span></span>  | <span data-ttu-id="0f7a8-131">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f7a8-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="0f7a8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f7a8-132">Header</span></span>                    | <span data-ttu-id="0f7a8-133">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="0f7a8-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="0f7a8-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="0f7a8-134">IDL</span></span>                       | <span data-ttu-id="0f7a8-135">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="0f7a8-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="0f7a8-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0f7a8-136">Library</span></span>                   | <span data-ttu-id="0f7a8-137">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="0f7a8-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="0f7a8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0f7a8-138">DLL</span></span>                       | <span data-ttu-id="0f7a8-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="0f7a8-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="0f7a8-140">IID</span><span class="sxs-lookup"><span data-stu-id="0f7a8-140">IID</span></span>                       | <span data-ttu-id="0f7a8-141">IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="0f7a8-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="0f7a8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f7a8-142">See also</span></span>

[<span data-ttu-id="0f7a8-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="0f7a8-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
