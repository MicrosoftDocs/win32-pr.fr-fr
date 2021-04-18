---
title: Méthode IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Annule l’inscription d’une configuration de machine virtuelle sans supprimer le fichier de configuration.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Méthode UnregisterVirtualMachine Virtual PC
- Méthode UnregisterVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode UnregisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466826"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="a7f2c-106">IVMVirtualPC :: UnregisterVirtualMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="a7f2c-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="a7f2c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a7f2c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a7f2c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a7f2c-109">Annule l’inscription d’une configuration d’ordinateur virtuel sans supprimer le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f2c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7f2c-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="a7f2c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7f2c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f2c-112">*VirtualMachine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7f2c-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f2c-113">Pointeur vers un objet [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente la configuration de la machine virtuelle dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f2c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7f2c-114">Return value</span></span>

<span data-ttu-id="a7f2c-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a7f2c-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a7f2c-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="a7f2c-117">Description</span><span class="sxs-lookup"><span data-stu-id="a7f2c-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7f2c-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a7f2c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a7f2c-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a7f2c-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a7f2c-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a7f2c-121">Le paramètre *VirtualMachine* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="a7f2c-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="a7f2c-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="a7f2c-123">La machine virtuelle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="a7f2c-124"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a7f2c-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a7f2c-125">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a7f2c-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="a7f2c-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a7f2c-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a7f2c-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a7f2c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a7f2c-128">Remarks</span></span>

<span data-ttu-id="a7f2c-129">Seules les machines virtuelles arrêtées peuvent être désinscrites.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="a7f2c-130">Les données de l’état enregistré ou du lecteur d’annulations existantes pour cette configuration sont conservées lors de l’annulation de l’inscription d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f2c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7f2c-131">Requirements</span></span>



| <span data-ttu-id="a7f2c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7f2c-132">Requirement</span></span> | <span data-ttu-id="a7f2c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7f2c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f2c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f2c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f2c-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7f2c-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7f2c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f2c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f2c-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f2c-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a7f2c-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a7f2c-138">End of client support</span></span><br/>    | <span data-ttu-id="a7f2c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7f2c-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a7f2c-140">Produit</span><span class="sxs-lookup"><span data-stu-id="a7f2c-140">Product</span></span><br/>                  | <span data-ttu-id="a7f2c-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a7f2c-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a7f2c-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7f2c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f2c-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f2c-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a7f2c-144">IID</span><span class="sxs-lookup"><span data-stu-id="a7f2c-144">IID</span></span><br/>                      | <span data-ttu-id="a7f2c-145">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a7f2c-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a7f2c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7f2c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f2c-147">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a7f2c-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

