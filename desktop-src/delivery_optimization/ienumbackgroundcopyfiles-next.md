---
title: Méthode IEnumBackgroundCopyFiles Next (Deliveryoptimization. h)
description: Récupère un nombre spécifié d’éléments dans la séquence d’énumération. Si le nombre d’éléments restants dans la séquence est inférieur au nombre demandé, il récupère les éléments restants.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Next, méthode
- Next, méthode, IEnumBackgroundCopyFiles, interface
- Interface IEnumBackgroundCopyFiles, méthode Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942605"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="b4a0b-107">IEnumBackgroundCopyFiles :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="b4a0b-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="b4a0b-108">Récupère un nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="b4a0b-109">Si le nombre d’éléments restants dans la séquence est inférieur au nombre demandé, il récupère les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a0b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4a0b-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b4a0b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4a0b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a0b-112">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4a0b-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a0b-113">Nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="b4a0b-114">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4a0b-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a0b-115">Tableau d’objets [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a0b-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="b4a0b-116">Lorsque vous avez terminé, vous devez libérer chaque objet dans *rgelt* .</span><span class="sxs-lookup"><span data-stu-id="b4a0b-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="b4a0b-117">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4a0b-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a0b-118">Nombre d’éléments retournés dans *rgelt*.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="b4a0b-119">Vous pouvez affecter à *pceltFetched* la **valeur null** si *celt* est un.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="b4a0b-120">Sinon, initialisez la valeur de *pceltFetched* à 0 avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a0b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4a0b-121">Return value</span></span>

<span data-ttu-id="b4a0b-122">Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b4a0b-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4a0b-123">Return code</span></span>                                                                              | <span data-ttu-id="b4a0b-124">Description</span><span class="sxs-lookup"><span data-stu-id="b4a0b-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4a0b-125"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b4a0b-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b4a0b-126">Le nombre d’éléments demandés a été retourné.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="b4a0b-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a0b-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="b4a0b-128">Retourne une valeur inférieure au nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="b4a0b-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="b4a0b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4a0b-129">Requirements</span></span>



| <span data-ttu-id="b4a0b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4a0b-130">Requirement</span></span> | <span data-ttu-id="b4a0b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4a0b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a0b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4a0b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a0b-133">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4a0b-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b4a0b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4a0b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a0b-135">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4a0b-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b4a0b-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4a0b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4a0b-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a0b-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4a0b-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="b4a0b-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4a0b-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4a0b-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4a0b-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4a0b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4a0b-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4a0b-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b4a0b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b4a0b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4a0b-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4a0b-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b4a0b-144">IID</span><span class="sxs-lookup"><span data-stu-id="b4a0b-144">IID</span></span><br/>                      | <span data-ttu-id="b4a0b-145">IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="b4a0b-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="b4a0b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4a0b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a0b-147">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="b4a0b-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





