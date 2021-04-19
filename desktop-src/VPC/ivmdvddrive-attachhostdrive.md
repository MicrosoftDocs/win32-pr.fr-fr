---
title: Méthode IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Attache un lecteur hôte au lecteur de DVD de l’ordinateur virtuel.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Méthode AttachHostDrive Virtual PC
- Méthode AttachHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511391"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="628ae-106">IVMDVDDrive :: AttachHostDrive, méthode</span><span class="sxs-lookup"><span data-stu-id="628ae-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="628ae-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="628ae-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="628ae-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="628ae-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="628ae-109">Attache un lecteur hôte au lecteur de DVD de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="628ae-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="628ae-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="628ae-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="628ae-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="628ae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="628ae-112">lettre de *lecteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="628ae-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628ae-113">Lettre du lecteur hôte à attacher.</span><span class="sxs-lookup"><span data-stu-id="628ae-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="628ae-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="628ae-114">Return value</span></span>

<span data-ttu-id="628ae-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="628ae-115">This method can return one of these values.</span></span>



| <span data-ttu-id="628ae-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="628ae-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="628ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="628ae-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="628ae-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="628ae-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="628ae-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="628ae-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="628ae-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="628ae-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="628ae-121">Aucune lettre de lecteur n’a été spécifiée, ou la lettre de lecteur spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="628ae-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="628ae-122"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="628ae-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="628ae-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="628ae-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="628ae-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="628ae-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="628ae-125">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="628ae-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="628ae-126"><dt>**Ordinateur virtuel \_ \_Lecteur E \_ en cours d' \_ utilisation**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="628ae-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="628ae-127">Un lecteur DVD hôte ou une image ISO est déjà attaché à ce lecteur au sein de la machine virtuelle, ou le lecteur hôte spécifié est déjà utilisé dans un autre ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="628ae-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="628ae-128"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="628ae-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="628ae-129">L’emplacement du bus pour ce lecteur n’est pas valide, ou le lecteur ne semble pas être un lecteur de DVD valide.</span><span class="sxs-lookup"><span data-stu-id="628ae-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="628ae-130"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="628ae-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="628ae-131">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="628ae-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="628ae-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="628ae-132">Requirements</span></span>



| <span data-ttu-id="628ae-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="628ae-133">Requirement</span></span> | <span data-ttu-id="628ae-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="628ae-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="628ae-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="628ae-135">Minimum supported client</span></span><br/> | <span data-ttu-id="628ae-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="628ae-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="628ae-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="628ae-137">Minimum supported server</span></span><br/> | <span data-ttu-id="628ae-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="628ae-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="628ae-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="628ae-139">End of client support</span></span><br/>    | <span data-ttu-id="628ae-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="628ae-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="628ae-141">Produit</span><span class="sxs-lookup"><span data-stu-id="628ae-141">Product</span></span><br/>                  | <span data-ttu-id="628ae-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="628ae-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="628ae-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="628ae-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="628ae-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="628ae-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="628ae-145">IID</span><span class="sxs-lookup"><span data-stu-id="628ae-145">IID</span></span><br/>                      | <span data-ttu-id="628ae-146">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="628ae-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="628ae-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="628ae-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628ae-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="628ae-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

