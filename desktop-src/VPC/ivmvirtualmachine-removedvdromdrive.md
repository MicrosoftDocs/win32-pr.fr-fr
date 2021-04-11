---
title: Méthode IVMVirtualMachine RemoveDVDROMDrive (VPCCOMInterfaces. h)
description: Supprime le lecteur de CD ou de DVD spécifié de la machine virtuelle.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- Méthode RemoveDVDROMDrive Virtual PC
- Méthode RemoveDVDROMDrive Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104098"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="c3d69-106">IVMVirtualMachine :: RemoveDVDROMDrive, méthode</span><span class="sxs-lookup"><span data-stu-id="c3d69-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="c3d69-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3d69-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c3d69-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c3d69-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c3d69-109">Supprime le lecteur de CD ou de DVD spécifié de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c3d69-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d69-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3d69-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="c3d69-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3d69-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d69-112">*dvdDrive* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3d69-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d69-113">Lecteur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c3d69-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d69-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3d69-114">Return value</span></span>

<span data-ttu-id="c3d69-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c3d69-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c3d69-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c3d69-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="c3d69-117">Description</span><span class="sxs-lookup"><span data-stu-id="c3d69-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3d69-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c3d69-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="c3d69-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c3d69-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="c3d69-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c3d69-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="c3d69-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c3d69-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c3d69-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="c3d69-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="c3d69-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="c3d69-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="c3d69-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="c3d69-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="c3d69-125">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="c3d69-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="c3d69-126"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c3d69-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="c3d69-127">Le lecteur spécifié n’est pas connecté à cet emplacement de bus.</span><span class="sxs-lookup"><span data-stu-id="c3d69-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="c3d69-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c3d69-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="c3d69-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c3d69-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="c3d69-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c3d69-130">Remarks</span></span>

<span data-ttu-id="c3d69-131">Vous pouvez uniquement supprimer un lecteur de CD ou de DVD existant d’un ordinateur virtuel arrêté.</span><span class="sxs-lookup"><span data-stu-id="c3d69-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d69-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3d69-132">Requirements</span></span>



| <span data-ttu-id="c3d69-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3d69-133">Requirement</span></span> | <span data-ttu-id="c3d69-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d69-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d69-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d69-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d69-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3d69-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3d69-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d69-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d69-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d69-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c3d69-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c3d69-139">End of client support</span></span><br/>    | <span data-ttu-id="c3d69-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3d69-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c3d69-141">Produit</span><span class="sxs-lookup"><span data-stu-id="c3d69-141">Product</span></span><br/>                  | <span data-ttu-id="c3d69-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c3d69-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c3d69-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3d69-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3d69-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d69-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c3d69-145">IID</span><span class="sxs-lookup"><span data-stu-id="c3d69-145">IID</span></span><br/>                      | <span data-ttu-id="c3d69-146">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c3d69-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c3d69-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d69-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d69-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c3d69-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

