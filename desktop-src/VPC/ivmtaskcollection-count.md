---
title: Propriété Count IVMTaskCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de tâches de cette collection.
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMTaskCollection, interface
- IVMTaskCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843949"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="88fac-106">IVMTaskCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="88fac-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="88fac-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88fac-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88fac-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88fac-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88fac-109">Récupère le nombre de tâches de cette collection.</span><span class="sxs-lookup"><span data-stu-id="88fac-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="88fac-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="88fac-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88fac-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88fac-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="88fac-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="88fac-112">Property value</span></span>

<span data-ttu-id="88fac-113">Nombre de tâches.</span><span class="sxs-lookup"><span data-stu-id="88fac-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88fac-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="88fac-114">Error codes</span></span>



| <span data-ttu-id="88fac-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="88fac-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="88fac-116">Signification</span><span class="sxs-lookup"><span data-stu-id="88fac-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="88fac-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88fac-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="88fac-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="88fac-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="88fac-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="88fac-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="88fac-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="88fac-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="88fac-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="88fac-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="88fac-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="88fac-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="88fac-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88fac-123">Requirements</span></span>



| <span data-ttu-id="88fac-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88fac-124">Requirement</span></span> | <span data-ttu-id="88fac-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="88fac-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88fac-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88fac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88fac-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88fac-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88fac-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88fac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88fac-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="88fac-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88fac-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="88fac-130">End of client support</span></span><br/>    | <span data-ttu-id="88fac-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88fac-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88fac-132">Produit</span><span class="sxs-lookup"><span data-stu-id="88fac-132">Product</span></span><br/>                  | <span data-ttu-id="88fac-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88fac-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88fac-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="88fac-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="88fac-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="88fac-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="88fac-136">IID</span><span class="sxs-lookup"><span data-stu-id="88fac-136">IID</span></span><br/>                      | <span data-ttu-id="88fac-137">IID \_ IVMTaskCollection est défini en tant que 5c4387c8-0e8b-4B97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="88fac-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="88fac-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88fac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fac-139">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="88fac-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

