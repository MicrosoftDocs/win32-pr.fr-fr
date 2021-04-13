---
title: 'IDeliveryOptimizationFile2 :: GetProperty, méthode'
description: 'Cette méthode retourne une seule propriété du fichier DO. | IDeliveryOptimizationFile2 :: GetProperty, méthode'
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, méthode GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322466"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="ef8ba-107">IDeliveryOptimizationFile2 :: GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="ef8ba-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="ef8ba-108">Cette méthode retourne une seule propriété du fichier DO.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef8ba-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="ef8ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef8ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8ba-111">*propid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef8ba-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8ba-112">ID de propriété requis pour la récupération de type DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="ef8ba-113">*propvalue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef8ba-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8ba-114">Valeur de propriété stockée dans un VARIANT.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8ba-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef8ba-115">Return value</span></span>

<span data-ttu-id="ef8ba-116">Cette méthode retourne les valeurs HRESULT suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="ef8ba-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef8ba-117">Return code</span></span>                  | <span data-ttu-id="ef8ba-118">Description</span><span class="sxs-lookup"><span data-stu-id="ef8ba-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="ef8ba-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="ef8ba-119">**S_OK**</span></span>                     | <span data-ttu-id="ef8ba-120">Succès</span><span class="sxs-lookup"><span data-stu-id="ef8ba-120">Success</span></span>                                             |
| <span data-ttu-id="ef8ba-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="ef8ba-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="ef8ba-122">ID de propriété inconnu.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="ef8ba-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="ef8ba-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="ef8ba-124">La propriété est en écriture seule et ne peut pas être lue.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="ef8ba-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="ef8ba-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="ef8ba-126">Aucune propriété n’a été définie par le biais de la méthode SetProperty.</span><span class="sxs-lookup"><span data-stu-id="ef8ba-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="ef8ba-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="ef8ba-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="ef8ba-128">Échec d’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="ef8ba-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="ef8ba-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef8ba-129">Requirements</span></span>

| <span data-ttu-id="ef8ba-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef8ba-130">Requirement</span></span> | <span data-ttu-id="ef8ba-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8ba-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef8ba-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef8ba-132">Minimum supported client</span></span>  | <span data-ttu-id="ef8ba-133">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef8ba-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="ef8ba-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef8ba-134">Minimum supported server</span></span>  | <span data-ttu-id="ef8ba-135">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef8ba-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="ef8ba-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef8ba-136">Header</span></span>                    | <span data-ttu-id="ef8ba-137">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="ef8ba-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="ef8ba-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="ef8ba-138">IDL</span></span>                       | <span data-ttu-id="ef8ba-139">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="ef8ba-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="ef8ba-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef8ba-140">Library</span></span>                   | <span data-ttu-id="ef8ba-141">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="ef8ba-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="ef8ba-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ef8ba-142">DLL</span></span>                       | <span data-ttu-id="ef8ba-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="ef8ba-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="ef8ba-144">IID</span><span class="sxs-lookup"><span data-stu-id="ef8ba-144">IID</span></span>                       | <span data-ttu-id="ef8ba-145">IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="ef8ba-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="ef8ba-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef8ba-146">See also</span></span>

[<span data-ttu-id="ef8ba-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="ef8ba-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
