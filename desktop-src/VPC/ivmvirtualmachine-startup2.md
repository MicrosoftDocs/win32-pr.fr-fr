---
title: Méthode IVMVirtualMachine Startup2 (VPCCOMInterfaces. h)
description: Démarre l’ordinateur virtuel à partir de l’état non initialisé ou enregistré, avec des options avancées.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Méthode Startup2 Virtual PC
- Méthode Startup2 Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Startup2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384740"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="e1fa4-106">IVMVirtualMachine :: Startup2, méthode</span><span class="sxs-lookup"><span data-stu-id="e1fa4-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="e1fa4-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e1fa4-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e1fa4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e1fa4-109">Démarre la machine virtuelle à partir de l’état non initialisé ou enregistré, avec les options avancées.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="e1fa4-110">Cette méthode fournit un mécanisme permettant de démarrer une machine virtuelle avec un disque de différenciation même si l’horodateur du disque parent a été modifié.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1fa4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1fa4-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="e1fa4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1fa4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1fa4-113">*startupOption* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1fa4-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa4-114">Option de démarrage avancé.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-114">The advanced startup option.</span></span> <span data-ttu-id="e1fa4-115">Les valeurs possibles proviennent de l’énumération [**VMStartupOption**](vmstartupoption.md) .</span><span class="sxs-lookup"><span data-stu-id="e1fa4-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa4-116">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e1fa4-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa4-117">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1fa4-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1fa4-118">Return value</span></span>

<span data-ttu-id="e1fa4-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-119">This method can return one of these values.</span></span>



| <span data-ttu-id="e1fa4-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e1fa4-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="e1fa4-121">Description</span><span class="sxs-lookup"><span data-stu-id="e1fa4-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1fa4-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="e1fa4-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="e1fa4-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="e1fa4-125">Le paramètre *startupOption* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="e1fa4-126"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="e1fa4-127">Le paramètre *startupTask* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="e1fa4-128">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="e1fa4-129">L’appelant doit disposer des autorisations d’accès en exécution pour démarrer cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="e1fa4-130"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="e1fa4-131">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="e1fa4-132"><dt>**Ordinateur virtuel \_ 0xA0040203 \_ \_ de \_ ressources insuffisantes**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="e1fa4-133">Les ressources de l’ordinateur hôte sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="e1fa4-134"><dt>**Ordinateur virtuel \_ E \_ trop \_ de \_ machines virtuelles**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="e1fa4-135">Le nombre de machines virtuelles actives est trop important.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e1fa4-136"><dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="e1fa4-137">La machine virtuelle est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="e1fa4-138"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="e1fa4-139">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="e1fa4-140">Notes</span><span class="sxs-lookup"><span data-stu-id="e1fa4-140">Remarks</span></span>

<span data-ttu-id="e1fa4-141">Les valeurs suivantes peuvent être retournées par le biais de la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="e1fa4-142">Code d' [**erreur**](ivmtask-error.md) /valeur</span><span class="sxs-lookup"><span data-stu-id="e1fa4-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="e1fa4-143">Description</span><span class="sxs-lookup"><span data-stu-id="e1fa4-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="e1fa4-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="e1fa4-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="e1fa4-145">Le matériel ne prend pas en charge la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="e1fa4-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="e1fa4-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="e1fa4-147">La virtualisation matérielle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="e1fa4-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="e1fa4-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="e1fa4-149">Virtual PC 2007 et Windows Virtual PC sont tous deux installés.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="e1fa4-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="e1fa4-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="e1fa4-151">D’autres logiciels de virtualisation sont installés.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="e1fa4-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="e1fa4-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="e1fa4-153">Les ressources de l’ordinateur hôte sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="e1fa4-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="e1fa4-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1fa4-154">Requirements</span></span>



| <span data-ttu-id="e1fa4-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1fa4-155">Requirement</span></span> | <span data-ttu-id="e1fa4-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1fa4-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fa4-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1fa4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="e1fa4-158">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1fa4-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1fa4-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1fa4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="e1fa4-160">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1fa4-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e1fa4-161">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e1fa4-161">End of client support</span></span><br/>    | <span data-ttu-id="e1fa4-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1fa4-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e1fa4-163">Produit</span><span class="sxs-lookup"><span data-stu-id="e1fa4-163">Product</span></span><br/>                  | <span data-ttu-id="e1fa4-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e1fa4-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e1fa4-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1fa4-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1fa4-166"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1fa4-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e1fa4-167">IID</span><span class="sxs-lookup"><span data-stu-id="e1fa4-167">IID</span></span><br/>                      | <span data-ttu-id="e1fa4-168">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e1fa4-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e1fa4-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fa4-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fa4-170">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e1fa4-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

