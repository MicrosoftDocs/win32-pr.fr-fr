---
title: 'IDeliveryOptimizationJob2 :: SetProperty, méthode'
description: Cette méthode n’est pas utilisée.
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, méthode SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384776"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="7e592-106">IDeliveryOptimizationJob2 :: SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="7e592-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="7e592-107">Cette méthode n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7e592-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e592-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e592-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="7e592-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e592-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e592-110">*propid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e592-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e592-111">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7e592-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7e592-112">*propvalue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e592-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e592-113">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7e592-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e592-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e592-114">Return value</span></span>

<span data-ttu-id="7e592-115">Si propId est **DOJobPropertyId_ExtendedErrorInfo**, la valeur retournée est **DO_E_READ_ONLY_PROPERTY**; sinon, la fonction retourne **DO_E_UNKNOWN_PROPERTY_ID**.</span><span class="sxs-lookup"><span data-stu-id="7e592-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e592-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e592-116">Requirements</span></span>

| <span data-ttu-id="7e592-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e592-117">Requirement</span></span> | <span data-ttu-id="7e592-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e592-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7e592-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e592-119">Minimum supported client</span></span>  | <span data-ttu-id="7e592-120">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e592-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="7e592-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e592-121">Minimum supported server</span></span>  | <span data-ttu-id="7e592-122">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e592-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="7e592-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e592-123">Header</span></span>                    | <span data-ttu-id="7e592-124">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="7e592-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="7e592-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="7e592-125">IDL</span></span>                       | <span data-ttu-id="7e592-126">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="7e592-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="7e592-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e592-127">Library</span></span>                   | <span data-ttu-id="7e592-128">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="7e592-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="7e592-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7e592-129">DLL</span></span>                       | <span data-ttu-id="7e592-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="7e592-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="7e592-131">IID</span><span class="sxs-lookup"><span data-stu-id="7e592-131">IID</span></span>                       | <span data-ttu-id="7e592-132">IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="7e592-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="7e592-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e592-133">See also</span></span>

[<span data-ttu-id="7e592-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="7e592-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
