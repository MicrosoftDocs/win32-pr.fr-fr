---
title: IVMAccountant CPUUtilization, propriété (VPCCOMInterfaces. h)
description: Récupère le pourcentage d’utilisation actuelle du processeur pour cet ordinateur virtuel.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- CPUUtilization propriété Virtual PC
- CPUUtilization, propriété Virtual PC, IVMAccountant, interface
- IVMAccountant interface Virtual PC, propriété CPUUtilization
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942787"
---
# <a name="ivmaccountantcpuutilization-property"></a><span data-ttu-id="a123d-106">IVMAccountant :: CPUUtilization, propriété</span><span class="sxs-lookup"><span data-stu-id="a123d-106">IVMAccountant::CPUUtilization property</span></span>

<span data-ttu-id="a123d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a123d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a123d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a123d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a123d-109">Récupère le pourcentage d’utilisation actuelle du processeur pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a123d-109">Retrieves the percentage of current CPU utilization for this virtual machine.</span></span>

<span data-ttu-id="a123d-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a123d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a123d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a123d-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="a123d-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a123d-112">Property value</span></span>

<span data-ttu-id="a123d-113">Pourcentage d’utilisation actuelle du processeur.</span><span class="sxs-lookup"><span data-stu-id="a123d-113">The percentage of current CPU utilization.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a123d-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a123d-114">Error codes</span></span>



| <span data-ttu-id="a123d-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a123d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a123d-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a123d-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a123d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a123d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a123d-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a123d-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="a123d-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a123d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a123d-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a123d-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="a123d-121"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a123d-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="a123d-122">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a123d-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="a123d-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a123d-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a123d-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a123d-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="a123d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a123d-125">Requirements</span></span>



| <span data-ttu-id="a123d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a123d-126">Requirement</span></span> | <span data-ttu-id="a123d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a123d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a123d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a123d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a123d-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a123d-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a123d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a123d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a123d-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a123d-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a123d-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a123d-132">End of client support</span></span><br/>    | <span data-ttu-id="a123d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a123d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a123d-134">Produit</span><span class="sxs-lookup"><span data-stu-id="a123d-134">Product</span></span><br/>                  | <span data-ttu-id="a123d-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a123d-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a123d-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a123d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a123d-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a123d-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a123d-138">IID</span><span class="sxs-lookup"><span data-stu-id="a123d-138">IID</span></span><br/>                      | <span data-ttu-id="a123d-139">IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="a123d-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="a123d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a123d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a123d-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="a123d-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

