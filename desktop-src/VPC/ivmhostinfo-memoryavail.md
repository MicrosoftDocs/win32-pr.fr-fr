---
title: IVMHostInfo MemoryAvail, propriété (VPCCOMInterfaces. h)
description: Récupère la quantité de mémoire physique disponible sur l’ordinateur hôte, en mégaoctets.
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- MemoryAvail propriété Virtual PC
- MemoryAvail, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété MemoryAvail
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df6be8bf62595720d01372ee891184952a0dd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513818"
---
# <a name="ivmhostinfomemoryavail-property"></a><span data-ttu-id="f7d2b-106">IVMHostInfo :: MemoryAvail, propriété</span><span class="sxs-lookup"><span data-stu-id="f7d2b-106">IVMHostInfo::MemoryAvail property</span></span>

<span data-ttu-id="f7d2b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f7d2b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f7d2b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f7d2b-109">Récupère la quantité de mémoire physique disponible sur l’ordinateur hôte, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-109">Retrieves the amount of available physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="f7d2b-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d2b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7d2b-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="f7d2b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7d2b-112">Property value</span></span>

<span data-ttu-id="f7d2b-113">Mémoire physique disponible, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-113">The available physical memory, in megabytes.</span></span> <span data-ttu-id="f7d2b-114">Cette valeur est une **variante** de type VT \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7d2b-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f7d2b-115">Error codes</span></span>



| <span data-ttu-id="f7d2b-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f7d2b-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f7d2b-117">Signification</span><span class="sxs-lookup"><span data-stu-id="f7d2b-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f7d2b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f7d2b-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f7d2b-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f7d2b-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f7d2b-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2b-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f7d2b-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f7d2b-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f7d2b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7d2b-124">Requirements</span></span>



| <span data-ttu-id="f7d2b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7d2b-125">Requirement</span></span> | <span data-ttu-id="f7d2b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7d2b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d2b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d2b-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7d2b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7d2b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d2b-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d2b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f7d2b-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f7d2b-131">End of client support</span></span><br/>    | <span data-ttu-id="f7d2b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7d2b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f7d2b-133">Produit</span><span class="sxs-lookup"><span data-stu-id="f7d2b-133">Product</span></span><br/>                  | <span data-ttu-id="f7d2b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f7d2b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f7d2b-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7d2b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d2b-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f7d2b-137">IID</span><span class="sxs-lookup"><span data-stu-id="f7d2b-137">IID</span></span><br/>                      | <span data-ttu-id="f7d2b-138">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="f7d2b-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f7d2b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7d2b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d2b-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="f7d2b-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

