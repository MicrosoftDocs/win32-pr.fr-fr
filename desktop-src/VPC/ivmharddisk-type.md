---
title: Propriété de type IVMHardDisk (VPCCOMInterfaces. h)
description: Type du disque dur virtuel.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Propriété de type Virtual PC
- Propriété de type Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, type, propriété
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032818"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="744b6-106">IVMHardDisk :: type, propriété</span><span class="sxs-lookup"><span data-stu-id="744b6-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="744b6-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="744b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="744b6-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="744b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="744b6-109">Récupère le type du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="744b6-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="744b6-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="744b6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="744b6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="744b6-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="744b6-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="744b6-112">Property value</span></span>

<span data-ttu-id="744b6-113">Type de l’image de disque dur actuelle.</span><span class="sxs-lookup"><span data-stu-id="744b6-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="744b6-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="744b6-114">Error codes</span></span>



| <span data-ttu-id="744b6-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="744b6-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="744b6-116">Signification</span><span class="sxs-lookup"><span data-stu-id="744b6-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="744b6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="744b6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="744b6-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="744b6-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="744b6-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="744b6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="744b6-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="744b6-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="744b6-121">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="744b6-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="744b6-122">Le fichier image de disque dur actuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="744b6-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="744b6-123"><dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="744b6-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="744b6-124">Le type de l’image actuelle du disque dur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="744b6-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="744b6-125"><dt>Ordinateur virtuel \_ \_Échec d' \_ \_ ouverture \_ d’une image HD E</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="744b6-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="744b6-126">Une erreur s’est produite lors de la tentative d’ouverture du fichier image de disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="744b6-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="744b6-127"><dt>Ordinateur virtuel \_ 0xA0040681 \_ d' \_ \_ accès à l’image HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="744b6-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="744b6-128">Une erreur s’est produite lors de la tentative d’accès au fichier image du disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="744b6-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="744b6-129"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="744b6-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="744b6-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="744b6-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="744b6-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="744b6-131">Requirements</span></span>



| <span data-ttu-id="744b6-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="744b6-132">Requirement</span></span> | <span data-ttu-id="744b6-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="744b6-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="744b6-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="744b6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="744b6-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="744b6-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="744b6-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="744b6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="744b6-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="744b6-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="744b6-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="744b6-138">End of client support</span></span><br/>    | <span data-ttu-id="744b6-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="744b6-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="744b6-140">Produit</span><span class="sxs-lookup"><span data-stu-id="744b6-140">Product</span></span><br/>                  | <span data-ttu-id="744b6-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="744b6-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="744b6-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="744b6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="744b6-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="744b6-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="744b6-144">IID</span><span class="sxs-lookup"><span data-stu-id="744b6-144">IID</span></span><br/>                      | <span data-ttu-id="744b6-145">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="744b6-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="744b6-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="744b6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744b6-147">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="744b6-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

