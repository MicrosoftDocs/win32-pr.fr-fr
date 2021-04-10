---
title: Méthode de démarrage IVMVirtualMachine (VPCCOMInterfaces. h)
description: Démarre l’ordinateur virtuel à partir de l’état non initialisé ou enregistré.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Méthode de démarrage Virtual PC
- Méthode de démarrage Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Startup
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942615"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="c21b1-106">IVMVirtualMachine :: Startup, méthode</span><span class="sxs-lookup"><span data-stu-id="c21b1-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="c21b1-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c21b1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c21b1-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c21b1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c21b1-109">Démarre l’ordinateur virtuel à partir de l’état non initialisé ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="c21b1-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21b1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c21b1-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="c21b1-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c21b1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21b1-112">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c21b1-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c21b1-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c21b1-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21b1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c21b1-114">Return value</span></span>

<span data-ttu-id="c21b1-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c21b1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c21b1-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c21b1-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="c21b1-117">Description</span><span class="sxs-lookup"><span data-stu-id="c21b1-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c21b1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="c21b1-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c21b1-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="c21b1-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="c21b1-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c21b1-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="c21b1-122">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="c21b1-123">L’appelant doit disposer des autorisations d’accès en exécution pour démarrer cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c21b1-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="c21b1-124"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="c21b1-125">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="c21b1-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="c21b1-126"><dt>**Ordinateur virtuel \_ 0xA0040203 \_ \_ de \_ ressources insuffisantes**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="c21b1-127">Les ressources de l’ordinateur hôte sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="c21b1-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="c21b1-128"><dt>**Ordinateur virtuel \_ E \_ trop \_ de \_ machines virtuelles**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="c21b1-129">Le nombre d’ordinateurs virtuels actifs est trop important.</span><span class="sxs-lookup"><span data-stu-id="c21b1-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c21b1-130"><dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="c21b1-131">L’ordinateur virtuel est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c21b1-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c21b1-132"><dt>**Ordinateur virtuel \_ 0xA00400687 \_ \_ modifié parent E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="c21b1-133">Impossible de démarrer l’ordinateur virtuel, car le disque dur virtuel parent a été modifié.</span><span class="sxs-lookup"><span data-stu-id="c21b1-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="c21b1-134"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="c21b1-135">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c21b1-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="c21b1-136">Notes</span><span class="sxs-lookup"><span data-stu-id="c21b1-136">Remarks</span></span>

<span data-ttu-id="c21b1-137">Si la machine virtuelle est enregistrée, elle est restaurée à partir de l’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="c21b1-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="c21b1-138">Les valeurs suivantes peuvent être retournées par le biais de la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné.</span><span class="sxs-lookup"><span data-stu-id="c21b1-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="c21b1-139">Code d' [**erreur**](ivmtask-error.md) /valeur</span><span class="sxs-lookup"><span data-stu-id="c21b1-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="c21b1-140">Description</span><span class="sxs-lookup"><span data-stu-id="c21b1-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c21b1-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="c21b1-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="c21b1-142">Le matériel ne prend pas en charge la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="c21b1-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="c21b1-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="c21b1-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="c21b1-144">La virtualisation matérielle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c21b1-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="c21b1-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="c21b1-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="c21b1-146">Virtual PC 2007 et Windows Virtual PC sont tous deux installés.</span><span class="sxs-lookup"><span data-stu-id="c21b1-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="c21b1-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="c21b1-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="c21b1-148">D’autres logiciels de virtualisation sont installés.</span><span class="sxs-lookup"><span data-stu-id="c21b1-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="c21b1-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="c21b1-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="c21b1-150">Les ressources de l’ordinateur hôte sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="c21b1-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="c21b1-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c21b1-151">Requirements</span></span>



| <span data-ttu-id="c21b1-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c21b1-152">Requirement</span></span> | <span data-ttu-id="c21b1-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="c21b1-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21b1-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21b1-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c21b1-155">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c21b1-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c21b1-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21b1-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c21b1-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21b1-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c21b1-158">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c21b1-158">End of client support</span></span><br/>    | <span data-ttu-id="c21b1-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c21b1-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c21b1-160">Produit</span><span class="sxs-lookup"><span data-stu-id="c21b1-160">Product</span></span><br/>                  | <span data-ttu-id="c21b1-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c21b1-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c21b1-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="c21b1-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21b1-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c21b1-164">IID</span><span class="sxs-lookup"><span data-stu-id="c21b1-164">IID</span></span><br/>                      | <span data-ttu-id="c21b1-165">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c21b1-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c21b1-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c21b1-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21b1-167">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c21b1-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

