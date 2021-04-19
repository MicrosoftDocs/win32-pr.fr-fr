---
title: Méthode IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Supprime une configuration d’ordinateur virtuel.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Méthode DeleteVirtualMachine Virtual PC
- Méthode DeleteVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515075"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="23ad0-106">IVMVirtualPC ::D méthode eleteVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="23ad0-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="23ad0-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="23ad0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="23ad0-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="23ad0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="23ad0-109">Supprime une configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="23ad0-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="23ad0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23ad0-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="23ad0-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23ad0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ad0-112">*VirtualMachine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23ad0-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ad0-113">Pointeur vers un objet [**IVMVirtualMachine**](ivmvirtualmachine.md) représentant la configuration de l’ordinateur virtuel à supprimer.</span><span class="sxs-lookup"><span data-stu-id="23ad0-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23ad0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23ad0-114">Return value</span></span>

<span data-ttu-id="23ad0-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="23ad0-115">This method can return one of these values.</span></span>



| <span data-ttu-id="23ad0-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="23ad0-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="23ad0-117">Description</span><span class="sxs-lookup"><span data-stu-id="23ad0-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23ad0-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="23ad0-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="23ad0-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="23ad0-120"><dt>**S \_ FALSe**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="23ad0-121">La configuration spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="23ad0-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="23ad0-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="23ad0-123">Le paramètre *VirtualMachine* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="23ad0-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="23ad0-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="23ad0-125">La machine virtuelle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="23ad0-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="23ad0-126"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="23ad0-127">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="23ad0-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="23ad0-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="23ad0-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="23ad0-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="23ad0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="23ad0-130">Remarks</span></span>

<span data-ttu-id="23ad0-131">Seules les machines virtuelles arrêtées peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="23ad0-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="23ad0-132">Notez que les données d’état enregistré ou de lecteur d’annulation existantes pour cette configuration seront supprimées en plus du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="23ad0-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ad0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23ad0-133">Requirements</span></span>



| <span data-ttu-id="23ad0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23ad0-134">Requirement</span></span> | <span data-ttu-id="23ad0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="23ad0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23ad0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23ad0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="23ad0-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23ad0-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23ad0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23ad0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="23ad0-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="23ad0-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="23ad0-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="23ad0-140">End of client support</span></span><br/>    | <span data-ttu-id="23ad0-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23ad0-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="23ad0-142">Produit</span><span class="sxs-lookup"><span data-stu-id="23ad0-142">Product</span></span><br/>                  | <span data-ttu-id="23ad0-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="23ad0-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="23ad0-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="23ad0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="23ad0-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ad0-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="23ad0-146">IID</span><span class="sxs-lookup"><span data-stu-id="23ad0-146">IID</span></span><br/>                      | <span data-ttu-id="23ad0-147">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="23ad0-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="23ad0-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23ad0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ad0-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="23ad0-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

