---
title: Méthode IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Attache une image ISO au lecteur de DVD au sein de la machine virtuelle.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Méthode AttachImage Virtual PC
- Méthode AttachImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385151"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="96671-106">IVMDVDDrive :: AttachImage, méthode</span><span class="sxs-lookup"><span data-stu-id="96671-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="96671-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96671-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96671-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96671-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96671-109">Attache une image ISO au lecteur de DVD au sein de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="96671-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="96671-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96671-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="96671-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96671-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96671-112">*ImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96671-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96671-113">Chemin d’accès complet à l’image ISO à attacher.</span><span class="sxs-lookup"><span data-stu-id="96671-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96671-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96671-114">Return value</span></span>

<span data-ttu-id="96671-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="96671-115">This method can return one of these values.</span></span>



| <span data-ttu-id="96671-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="96671-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="96671-117">Description</span><span class="sxs-lookup"><span data-stu-id="96671-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96671-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96671-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="96671-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="96671-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="96671-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="96671-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="96671-121">Le paramètre *ImagePath* est un répertoire.</span><span class="sxs-lookup"><span data-stu-id="96671-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="96671-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="96671-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="96671-123">Le paramètre *ImagePath* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="96671-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="96671-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="96671-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="96671-125">La machine virtuelle est introuvable.</span><span class="sxs-lookup"><span data-stu-id="96671-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="96671-126"><dt>**Ordinateur virtuel \_ \_Lecteur E \_ en cours d' \_ utilisation**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="96671-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="96671-127">Une image ISO ou un lecteur de DVD hôte est déjà attachée à ce lecteur.</span><span class="sxs-lookup"><span data-stu-id="96671-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="96671-128"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96671-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="96671-129">L’emplacement du bus pour ce lecteur n’est pas valide, ou le lecteur ne semble pas être un lecteur de DVD valide.</span><span class="sxs-lookup"><span data-stu-id="96671-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="96671-130"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="96671-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="96671-131">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="96671-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="96671-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96671-132">Requirements</span></span>



| <span data-ttu-id="96671-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96671-133">Requirement</span></span> | <span data-ttu-id="96671-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="96671-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96671-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96671-135">Minimum supported client</span></span><br/> | <span data-ttu-id="96671-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96671-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96671-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96671-137">Minimum supported server</span></span><br/> | <span data-ttu-id="96671-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="96671-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96671-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="96671-139">End of client support</span></span><br/>    | <span data-ttu-id="96671-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96671-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96671-141">Produit</span><span class="sxs-lookup"><span data-stu-id="96671-141">Product</span></span><br/>                  | <span data-ttu-id="96671-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96671-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96671-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="96671-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="96671-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96671-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96671-145">IID</span><span class="sxs-lookup"><span data-stu-id="96671-145">IID</span></span><br/>                      | <span data-ttu-id="96671-146">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="96671-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="96671-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96671-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96671-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="96671-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

