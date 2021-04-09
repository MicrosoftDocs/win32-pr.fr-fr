---
title: IEnumBackgroundCopyFiles Skip, méthode (Deliveryoptimization. h)
description: Ignore le nombre spécifié d’éléments suivant dans la séquence d’énumération. S’il y a moins d’éléments restants dans la séquence que le nombre demandé d’éléments à ignorer, il ignore le dernier élément de la séquence.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip (méthode)
- Skip, méthode, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, Skip (méthode)
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032504"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="33a4e-107">IEnumBackgroundCopyFiles :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="33a4e-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="33a4e-108">Ignore le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="33a4e-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="33a4e-109">S’il y a moins d’éléments restants dans la séquence que le nombre demandé d’éléments à ignorer, il ignore le dernier élément de la séquence.</span><span class="sxs-lookup"><span data-stu-id="33a4e-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a4e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33a4e-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="33a4e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33a4e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a4e-112">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33a4e-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a4e-113">Nombre d'éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="33a4e-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a4e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33a4e-114">Return value</span></span>

<span data-ttu-id="33a4e-115">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="33a4e-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="33a4e-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="33a4e-116">Return code</span></span>                                                                              | <span data-ttu-id="33a4e-117">Description</span><span class="sxs-lookup"><span data-stu-id="33a4e-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="33a4e-118"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="33a4e-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="33a4e-119">Le nombre d’éléments demandés a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="33a4e-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="33a4e-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="33a4e-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="33a4e-121">Valeur inférieure au nombre d’éléments demandés ignorée.</span><span class="sxs-lookup"><span data-stu-id="33a4e-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="33a4e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33a4e-122">Requirements</span></span>



| <span data-ttu-id="33a4e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33a4e-123">Requirement</span></span> | <span data-ttu-id="33a4e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="33a4e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a4e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33a4e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33a4e-126">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33a4e-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33a4e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33a4e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33a4e-128">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33a4e-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="33a4e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="33a4e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a4e-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a4e-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="33a4e-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="33a4e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33a4e-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33a4e-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="33a4e-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33a4e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="33a4e-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33a4e-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="33a4e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="33a4e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33a4e-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33a4e-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="33a4e-137">IID</span><span class="sxs-lookup"><span data-stu-id="33a4e-137">IID</span></span><br/>                      | <span data-ttu-id="33a4e-138">IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="33a4e-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="33a4e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33a4e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a4e-140">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="33a4e-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





