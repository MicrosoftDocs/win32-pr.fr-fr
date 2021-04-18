---
title: IVMHostInfo ParallelPort, propriété (VPCCOMInterfaces. h)
description: Récupère le port parallèle hôte qui peut être attaché à l’invité.
ms.assetid: 4c9486b8-ab66-4874-b467-a7a0ab7934f1
keywords:
- ParallelPort propriété Virtual PC
- ParallelPort, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété ParallelPort
topic_type:
- apiref
api_name:
- IVMHostInfo.ParallelPort
- IVMHostInfo.get_ParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0a2050ff505f5ed7a54cf3857ea28661d4d3d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508289"
---
# <a name="ivmhostinfoparallelport-property"></a><span data-ttu-id="210a0-106">IVMHostInfo ::P propriété arallelPort</span><span class="sxs-lookup"><span data-stu-id="210a0-106">IVMHostInfo::ParallelPort property</span></span>

<span data-ttu-id="210a0-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="210a0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="210a0-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="210a0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="210a0-109">Récupère le port parallèle hôte qui peut être attaché à l’invité.</span><span class="sxs-lookup"><span data-stu-id="210a0-109">Retrieves the host parallel port that can be attached to the guest.</span></span>

<span data-ttu-id="210a0-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="210a0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="210a0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="210a0-111">Syntax</span></span>


```C++
HRESULT get_ParallelPort(
  [out, retval] BSTR *vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="210a0-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="210a0-112">Property value</span></span>

<span data-ttu-id="210a0-113">Nom du port parallèle.</span><span class="sxs-lookup"><span data-stu-id="210a0-113">The name of the parallel port.</span></span>

## <a name="error-codes"></a><span data-ttu-id="210a0-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="210a0-114">Error codes</span></span>



| <span data-ttu-id="210a0-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="210a0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="210a0-116">Signification</span><span class="sxs-lookup"><span data-stu-id="210a0-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="210a0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="210a0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="210a0-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="210a0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="210a0-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="210a0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="210a0-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="210a0-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="210a0-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="210a0-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="210a0-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="210a0-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="210a0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="210a0-123">Requirements</span></span>



| <span data-ttu-id="210a0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="210a0-124">Requirement</span></span> | <span data-ttu-id="210a0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="210a0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="210a0-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="210a0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="210a0-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="210a0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="210a0-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="210a0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="210a0-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="210a0-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="210a0-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="210a0-130">End of client support</span></span><br/>    | <span data-ttu-id="210a0-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="210a0-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="210a0-132">Produit</span><span class="sxs-lookup"><span data-stu-id="210a0-132">Product</span></span><br/>                  | <span data-ttu-id="210a0-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="210a0-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="210a0-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="210a0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="210a0-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="210a0-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="210a0-136">IID</span><span class="sxs-lookup"><span data-stu-id="210a0-136">IID</span></span><br/>                      | <span data-ttu-id="210a0-137">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="210a0-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="210a0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="210a0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210a0-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="210a0-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

