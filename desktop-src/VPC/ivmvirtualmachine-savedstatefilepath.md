---
title: IVMVirtualMachine SavedStateFilePath, propriété (VPCCOMInterfaces. h)
description: Récupère le chemin d’accès complet au fichier d’état enregistré.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- SavedStateFilePath propriété Virtual PC
- SavedStateFilePath, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété SavedStateFilePath
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105340"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="3e12e-106">IVMVirtualMachine :: SavedStateFilePath, propriété</span><span class="sxs-lookup"><span data-stu-id="3e12e-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="3e12e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e12e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e12e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e12e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e12e-109">Récupère le chemin d’accès complet au fichier d’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="3e12e-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="3e12e-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e12e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e12e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e12e-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="3e12e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3e12e-112">Property value</span></span>

<span data-ttu-id="3e12e-113">Chemin d’accès complet au fichier d’état enregistré de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3e12e-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e12e-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3e12e-114">Error codes</span></span>



| <span data-ttu-id="3e12e-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="3e12e-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="3e12e-116">Signification</span><span class="sxs-lookup"><span data-stu-id="3e12e-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e12e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e12e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="3e12e-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3e12e-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="3e12e-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3e12e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="3e12e-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3e12e-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="3e12e-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3e12e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="3e12e-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="3e12e-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="3e12e-123"><dt>Ordinateur virtuel \_ E \_ VM \_ sans \_ \_ état enregistré</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="3e12e-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="3e12e-124">Aucun fichier d’état enregistré n’est associé à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3e12e-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="3e12e-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3e12e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="3e12e-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3e12e-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="3e12e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e12e-127">Requirements</span></span>



| <span data-ttu-id="3e12e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e12e-128">Requirement</span></span> | <span data-ttu-id="3e12e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e12e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e12e-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e12e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3e12e-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e12e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e12e-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e12e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3e12e-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e12e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e12e-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3e12e-134">End of client support</span></span><br/>    | <span data-ttu-id="3e12e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e12e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e12e-136">Produit</span><span class="sxs-lookup"><span data-stu-id="3e12e-136">Product</span></span><br/>                  | <span data-ttu-id="3e12e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e12e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e12e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e12e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e12e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e12e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e12e-140">IID</span><span class="sxs-lookup"><span data-stu-id="3e12e-140">IID</span></span><br/>                      | <span data-ttu-id="3e12e-141">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3e12e-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3e12e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e12e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e12e-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3e12e-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

