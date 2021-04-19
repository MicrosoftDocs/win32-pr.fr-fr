---
title: Propriété mémoire IVMVirtualMachine (VPCCOMInterfaces. h)
description: Quantité de mémoire physique de l’ordinateur virtuel, en mégaoctets.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propriété mémoire Virtual PC
- Propriété mémoire Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété mémoire
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518055"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="127d6-106">IVMVirtualMachine :: Memory, propriété</span><span class="sxs-lookup"><span data-stu-id="127d6-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="127d6-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="127d6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="127d6-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="127d6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="127d6-109">Récupère et définit la quantité de mémoire physique de l’ordinateur virtuel, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="127d6-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="127d6-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="127d6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="127d6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="127d6-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="127d6-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="127d6-112">Property value</span></span>

<span data-ttu-id="127d6-113">Spécifie la quantité de mémoire physique, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="127d6-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="127d6-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="127d6-114">Error codes</span></span>



| <span data-ttu-id="127d6-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="127d6-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="127d6-116">Signification</span><span class="sxs-lookup"><span data-stu-id="127d6-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="127d6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="127d6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="127d6-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="127d6-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="127d6-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="127d6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="127d6-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="127d6-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="127d6-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="127d6-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="127d6-122">Le paramètre n’est pas valide ou est hors limites.</span><span class="sxs-lookup"><span data-stu-id="127d6-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="127d6-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="127d6-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="127d6-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="127d6-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="127d6-125"><dt>Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="127d6-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="127d6-126">La préférence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="127d6-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="127d6-127"><dt>Ordinateur virtuel \_ E/r 0xA0040302 \_ \_ \_ active VM</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="127d6-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="127d6-128">L’ordinateur virtuel est en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="127d6-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="127d6-129"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="127d6-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="127d6-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="127d6-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="127d6-131">Notes</span><span class="sxs-lookup"><span data-stu-id="127d6-131">Remarks</span></span>

<span data-ttu-id="127d6-132">La quantité de mémoire physique d’un ordinateur virtuel doit être d’au moins 4 Mo.</span><span class="sxs-lookup"><span data-stu-id="127d6-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="127d6-133">La limite supérieure de la mémoire dépend de la configuration de l’hôte, mais elle peut être d’au plus 3 712 Mo.</span><span class="sxs-lookup"><span data-stu-id="127d6-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="127d6-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="127d6-134">Requirements</span></span>



| <span data-ttu-id="127d6-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="127d6-135">Requirement</span></span> | <span data-ttu-id="127d6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="127d6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="127d6-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="127d6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="127d6-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="127d6-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="127d6-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="127d6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="127d6-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="127d6-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="127d6-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="127d6-141">End of client support</span></span><br/>    | <span data-ttu-id="127d6-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="127d6-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="127d6-143">Produit</span><span class="sxs-lookup"><span data-stu-id="127d6-143">Product</span></span><br/>                  | <span data-ttu-id="127d6-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="127d6-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="127d6-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="127d6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="127d6-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="127d6-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="127d6-147">IID</span><span class="sxs-lookup"><span data-stu-id="127d6-147">IID</span></span><br/>                      | <span data-ttu-id="127d6-148">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="127d6-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="127d6-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="127d6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127d6-150">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="127d6-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

