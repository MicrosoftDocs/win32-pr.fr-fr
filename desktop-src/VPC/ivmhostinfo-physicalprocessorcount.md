---
title: IVMHostInfo PhysicalProcessorCount, propriété (VPCCOMInterfaces. h)
description: Récupère le nombre de processeurs physiques sur l’ordinateur hôte.
ms.assetid: b8f805a6-2962-4a48-94e9-bd76220974f0
keywords:
- PhysicalProcessorCount propriété Virtual PC
- PhysicalProcessorCount, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété PhysicalProcessorCount
topic_type:
- apiref
api_name:
- IVMHostInfo.PhysicalProcessorCount
- IVMHostInfo.get_PhysicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b161795a8430b6006d1f6a8aa87e91225430016c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102812"
---
# <a name="ivmhostinfophysicalprocessorcount-property"></a><span data-ttu-id="78596-106">IVMHostInfo ::P propriété hysicalProcessorCount</span><span class="sxs-lookup"><span data-stu-id="78596-106">IVMHostInfo::PhysicalProcessorCount property</span></span>

<span data-ttu-id="78596-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78596-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="78596-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="78596-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="78596-109">Récupère le nombre de processeurs physiques sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="78596-109">Retrieves the number of physical processors in the host machine.</span></span>

<span data-ttu-id="78596-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="78596-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78596-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78596-111">Syntax</span></span>


```C++
HRESULT get_PhysicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a><span data-ttu-id="78596-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="78596-112">Property value</span></span>

<span data-ttu-id="78596-113">Nombre de processeurs physiques.</span><span class="sxs-lookup"><span data-stu-id="78596-113">The number of physical processors.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78596-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="78596-114">Error codes</span></span>



| <span data-ttu-id="78596-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="78596-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="78596-116">Signification</span><span class="sxs-lookup"><span data-stu-id="78596-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="78596-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78596-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="78596-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="78596-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="78596-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="78596-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="78596-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="78596-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="78596-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="78596-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="78596-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="78596-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="78596-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78596-123">Requirements</span></span>



| <span data-ttu-id="78596-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78596-124">Requirement</span></span> | <span data-ttu-id="78596-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="78596-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78596-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78596-126">Minimum supported client</span></span><br/> | <span data-ttu-id="78596-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78596-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78596-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78596-128">Minimum supported server</span></span><br/> | <span data-ttu-id="78596-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="78596-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="78596-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="78596-130">End of client support</span></span><br/>    | <span data-ttu-id="78596-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="78596-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="78596-132">Produit</span><span class="sxs-lookup"><span data-stu-id="78596-132">Product</span></span><br/>                  | <span data-ttu-id="78596-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="78596-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="78596-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="78596-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="78596-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="78596-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="78596-136">IID</span><span class="sxs-lookup"><span data-stu-id="78596-136">IID</span></span><br/>                      | <span data-ttu-id="78596-137">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="78596-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="78596-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78596-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78596-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="78596-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

