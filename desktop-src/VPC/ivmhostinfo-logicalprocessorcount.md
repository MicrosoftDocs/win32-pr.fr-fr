---
title: IVMHostInfo LogicalProcessorCount, propriété (VPCCOMInterfaces. h)
description: Récupère le nombre de processeurs logiques de l’ordinateur hôte.
ms.assetid: bf978a80-9a21-426a-ac18-109f20d38cbb
keywords:
- LogicalProcessorCount propriété Virtual PC
- LogicalProcessorCount, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété LogicalProcessorCount
topic_type:
- apiref
api_name:
- IVMHostInfo.LogicalProcessorCount
- IVMHostInfo.get_LogicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7668bb4332a41b1cae809c6c2f29a8eac99bade
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511922"
---
# <a name="ivmhostinfologicalprocessorcount-property"></a><span data-ttu-id="0568c-106">IVMHostInfo :: LogicalProcessorCount, propriété</span><span class="sxs-lookup"><span data-stu-id="0568c-106">IVMHostInfo::LogicalProcessorCount property</span></span>

<span data-ttu-id="0568c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0568c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0568c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0568c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0568c-109">Récupère le nombre de processeurs logiques de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="0568c-109">Retrieves the number of logical processors in the host machine.</span></span>

<span data-ttu-id="0568c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0568c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0568c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0568c-111">Syntax</span></span>


```C++
HRESULT get_LogicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a><span data-ttu-id="0568c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0568c-112">Property value</span></span>

<span data-ttu-id="0568c-113">Nombre de processeurs logiques.</span><span class="sxs-lookup"><span data-stu-id="0568c-113">The number of logical processors.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0568c-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0568c-114">Error codes</span></span>



| <span data-ttu-id="0568c-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="0568c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0568c-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0568c-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0568c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0568c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0568c-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0568c-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0568c-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0568c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0568c-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0568c-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0568c-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0568c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0568c-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0568c-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0568c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0568c-123">Requirements</span></span>



| <span data-ttu-id="0568c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0568c-124">Requirement</span></span> | <span data-ttu-id="0568c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0568c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0568c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0568c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0568c-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0568c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0568c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0568c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0568c-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0568c-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0568c-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0568c-130">End of client support</span></span><br/>    | <span data-ttu-id="0568c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0568c-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0568c-132">Produit</span><span class="sxs-lookup"><span data-stu-id="0568c-132">Product</span></span><br/>                  | <span data-ttu-id="0568c-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0568c-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0568c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0568c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0568c-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0568c-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0568c-136">IID</span><span class="sxs-lookup"><span data-stu-id="0568c-136">IID</span></span><br/>                      | <span data-ttu-id="0568c-137">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="0568c-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0568c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0568c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0568c-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="0568c-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

