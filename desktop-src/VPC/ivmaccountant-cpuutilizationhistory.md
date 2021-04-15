---
title: IVMAccountant CPUUtilizationHistory, propriété (VPCCOMInterfaces. h)
description: Récupère l’utilisation récente du processeur de cet ordinateur virtuel (sous la forme d’un tableau de valeurs de pourcentage).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- CPUUtilizationHistory propriété Virtual PC
- CPUUtilizationHistory, propriété Virtual PC, IVMAccountant, interface
- IVMAccountant interface Virtual PC, propriété CPUUtilizationHistory
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466843"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="cdda1-106">IVMAccountant :: CPUUtilizationHistory, propriété</span><span class="sxs-lookup"><span data-stu-id="cdda1-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="cdda1-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdda1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cdda1-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cdda1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cdda1-109">Récupère l’utilisation récente du processeur de cet ordinateur virtuel (sous la forme d’un tableau de valeurs de pourcentage).</span><span class="sxs-lookup"><span data-stu-id="cdda1-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="cdda1-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cdda1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdda1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdda1-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="cdda1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cdda1-112">Property value</span></span>

<span data-ttu-id="cdda1-113">Utilisation récente de l’UC de cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="cdda1-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="cdda1-114">Ces données sont retournées sous la forme d’un tableau d’éléments 60 qui représentent le pourcentage d’utilisation du processeur à chaque seconde au cours de la minute passée.</span><span class="sxs-lookup"><span data-stu-id="cdda1-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="cdda1-115">Le type Variant est \_ \| VT Array VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="cdda1-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cdda1-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cdda1-116">Error codes</span></span>



| <span data-ttu-id="cdda1-117">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="cdda1-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cdda1-118">Signification</span><span class="sxs-lookup"><span data-stu-id="cdda1-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdda1-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cdda1-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cdda1-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="cdda1-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="cdda1-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cdda1-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cdda1-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cdda1-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="cdda1-123"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cdda1-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="cdda1-124">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cdda1-124">The virtual machine is not running.</span></span> <span data-ttu-id="cdda1-125">Tous les éléments de tableau 60 ont la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="cdda1-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="cdda1-126"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cdda1-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cdda1-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cdda1-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="cdda1-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdda1-128">Requirements</span></span>



| <span data-ttu-id="cdda1-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdda1-129">Requirement</span></span> | <span data-ttu-id="cdda1-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdda1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdda1-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdda1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cdda1-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdda1-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdda1-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdda1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cdda1-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdda1-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cdda1-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cdda1-135">End of client support</span></span><br/>    | <span data-ttu-id="cdda1-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cdda1-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cdda1-137">Produit</span><span class="sxs-lookup"><span data-stu-id="cdda1-137">Product</span></span><br/>                  | <span data-ttu-id="cdda1-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cdda1-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cdda1-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdda1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdda1-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdda1-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cdda1-141">IID</span><span class="sxs-lookup"><span data-stu-id="cdda1-141">IID</span></span><br/>                      | <span data-ttu-id="cdda1-142">IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="cdda1-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="cdda1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdda1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdda1-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="cdda1-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

