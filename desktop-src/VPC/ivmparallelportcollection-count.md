---
title: Propriété Count IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Nombre de ports parallèles dans cette collection.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMParallelPortCollection, interface
- IVMParallelPortCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942220"
---
# <a name="ivmparallelportcollectioncount-property"></a><span data-ttu-id="3d4cb-106">IVMParallelPortCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="3d4cb-106">IVMParallelPortCollection::Count property</span></span>

<span data-ttu-id="3d4cb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d4cb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3d4cb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3d4cb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3d4cb-109">Récupère le nombre de ports parallèles de cette collection.</span><span class="sxs-lookup"><span data-stu-id="3d4cb-109">Retrieves the number of parallel ports in this collection.</span></span>

<span data-ttu-id="3d4cb-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3d4cb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4cb-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d4cb-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="3d4cb-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d4cb-112">Property value</span></span>

<span data-ttu-id="3d4cb-113">Nombre de ports parallèles.</span><span class="sxs-lookup"><span data-stu-id="3d4cb-113">The number of parallel ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d4cb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3d4cb-114">Error codes</span></span>



| <span data-ttu-id="3d4cb-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="3d4cb-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="3d4cb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="3d4cb-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="3d4cb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d4cb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="3d4cb-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3d4cb-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="3d4cb-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3d4cb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="3d4cb-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3d4cb-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="3d4cb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d4cb-121">Requirements</span></span>



| <span data-ttu-id="3d4cb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d4cb-122">Requirement</span></span> | <span data-ttu-id="3d4cb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d4cb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4cb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d4cb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d4cb-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d4cb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d4cb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d4cb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d4cb-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d4cb-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3d4cb-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3d4cb-128">End of client support</span></span><br/>    | <span data-ttu-id="3d4cb-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d4cb-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3d4cb-130">Produit</span><span class="sxs-lookup"><span data-stu-id="3d4cb-130">Product</span></span><br/>                  | <span data-ttu-id="3d4cb-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3d4cb-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3d4cb-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d4cb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d4cb-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4cb-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3d4cb-134">IID</span><span class="sxs-lookup"><span data-stu-id="3d4cb-134">IID</span></span><br/>                      | <span data-ttu-id="3d4cb-135">IID \_ IVMParallelPortCollection est défini en tant que 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="3d4cb-135">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3d4cb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d4cb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4cb-137">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="3d4cb-137">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

