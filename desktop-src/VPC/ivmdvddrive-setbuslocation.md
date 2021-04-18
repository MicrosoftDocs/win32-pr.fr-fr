---
title: Méthode IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Attache le lecteur de DVD à l’emplacement de bus spécifié sur l’ordinateur virtuel.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Méthode SetBusLocation Virtual PC
- Méthode SetBusLocation Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512395"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="f6c58-106">IVMDVDDrive :: SetBusLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="f6c58-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="f6c58-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f6c58-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f6c58-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f6c58-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f6c58-109">Attache le lecteur de DVD à l’emplacement de bus spécifié sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f6c58-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c58-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6c58-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="f6c58-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6c58-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c58-112">*busNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6c58-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c58-113">Numéro de bus auquel ce lecteur doit être attaché.</span><span class="sxs-lookup"><span data-stu-id="f6c58-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="f6c58-114">Par exemple, sur un bus IDE, ce nombre indique s’il faut utiliser le numéro de bus principal ou secondaire.</span><span class="sxs-lookup"><span data-stu-id="f6c58-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="f6c58-115">*deviceNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6c58-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c58-116">Numéro de l’appareil auquel ce lecteur doit être attaché.</span><span class="sxs-lookup"><span data-stu-id="f6c58-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="f6c58-117">Par exemple, sur un bus IDE, ce nombre indique s’il faut utiliser l’emplacement de l’appareil principal ou secondaire.</span><span class="sxs-lookup"><span data-stu-id="f6c58-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c58-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6c58-118">Return value</span></span>

<span data-ttu-id="f6c58-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f6c58-119">This method can return one of these values.</span></span>



| <span data-ttu-id="f6c58-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f6c58-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="f6c58-121">Description</span><span class="sxs-lookup"><span data-stu-id="f6c58-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6c58-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="f6c58-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f6c58-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="f6c58-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="f6c58-125">L’emplacement de bus spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f6c58-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="f6c58-126"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="f6c58-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f6c58-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="f6c58-128"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="f6c58-129">Impossible de définir l’emplacement du bus pendant que l’ordinateur virtuel est en cours d’exécution ou dans un état enregistré.</span><span class="sxs-lookup"><span data-stu-id="f6c58-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f6c58-130"><dt>**machine \_ virtuelle \_ E \_ bus \_ en cours d' \_ utilisation**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="f6c58-131">Un autre périphérique est déjà attaché à l’emplacement de bus spécifié.</span><span class="sxs-lookup"><span data-stu-id="f6c58-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f6c58-132"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="f6c58-133">Impossible d’initialiser le lecteur actif.</span><span class="sxs-lookup"><span data-stu-id="f6c58-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="f6c58-134"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="f6c58-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="f6c58-135">Les modifications n’ont pas pu être écrites dans le fichier de préférences, car l’ordinateur virtuel pour ce lecteur n’a pas pu être déterminé.</span><span class="sxs-lookup"><span data-stu-id="f6c58-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="f6c58-136"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="f6c58-137">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f6c58-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="f6c58-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6c58-138">Requirements</span></span>



| <span data-ttu-id="f6c58-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6c58-139">Requirement</span></span> | <span data-ttu-id="f6c58-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6c58-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c58-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6c58-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c58-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6c58-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6c58-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6c58-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c58-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6c58-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f6c58-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f6c58-145">End of client support</span></span><br/>    | <span data-ttu-id="f6c58-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6c58-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f6c58-147">Produit</span><span class="sxs-lookup"><span data-stu-id="f6c58-147">Product</span></span><br/>                  | <span data-ttu-id="f6c58-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f6c58-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f6c58-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6c58-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c58-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c58-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f6c58-151">IID</span><span class="sxs-lookup"><span data-stu-id="f6c58-151">IID</span></span><br/>                      | <span data-ttu-id="f6c58-152">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="f6c58-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f6c58-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6c58-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c58-154">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f6c58-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

