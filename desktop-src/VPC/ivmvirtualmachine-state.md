---
title: Propriété d’État IVMVirtualMachine (VPCCOMInterfaces. h)
description: Récupère l’état actuel de l’ordinateur virtuel.
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- Propriété d’État Virtual PC
- Propriété d’État Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété State
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942614"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="351e1-106">IVMVirtualMachine :: State, propriété</span><span class="sxs-lookup"><span data-stu-id="351e1-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="351e1-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="351e1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="351e1-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="351e1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="351e1-109">Récupère l’état actuel de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="351e1-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="351e1-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="351e1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="351e1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="351e1-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="351e1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="351e1-112">Property value</span></span>

<span data-ttu-id="351e1-113">État actuel de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="351e1-113">The current state of the virtual machine.</span></span> <span data-ttu-id="351e1-114">Pour obtenir la liste des valeurs, consultez [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="351e1-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="351e1-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="351e1-115">Error codes</span></span>



| <span data-ttu-id="351e1-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="351e1-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="351e1-117">Signification</span><span class="sxs-lookup"><span data-stu-id="351e1-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="351e1-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="351e1-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="351e1-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="351e1-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="351e1-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="351e1-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="351e1-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="351e1-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="351e1-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="351e1-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="351e1-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="351e1-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="351e1-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="351e1-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="351e1-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="351e1-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="351e1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="351e1-126">Requirements</span></span>



| <span data-ttu-id="351e1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="351e1-127">Requirement</span></span> | <span data-ttu-id="351e1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="351e1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="351e1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="351e1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="351e1-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="351e1-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="351e1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="351e1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="351e1-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="351e1-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="351e1-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="351e1-133">End of client support</span></span><br/>    | <span data-ttu-id="351e1-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="351e1-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="351e1-135">Produit</span><span class="sxs-lookup"><span data-stu-id="351e1-135">Product</span></span><br/>                  | <span data-ttu-id="351e1-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="351e1-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="351e1-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="351e1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="351e1-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="351e1-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="351e1-139">IID</span><span class="sxs-lookup"><span data-stu-id="351e1-139">IID</span></span><br/>                      | <span data-ttu-id="351e1-140">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="351e1-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="351e1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="351e1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="351e1-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="351e1-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

