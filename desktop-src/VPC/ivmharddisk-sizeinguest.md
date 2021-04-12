---
title: IVMHardDisk SizeInGuest, propriété (VPCCOMInterfaces. h)
description: Récupère la taille du disque dur virtuel dans le système d’exploitation invité.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- SizeInGuest propriété Virtual PC
- SizeInGuest, propriété Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, propriété SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104917"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="babf8-106">IVMHardDisk :: SizeInGuest, propriété</span><span class="sxs-lookup"><span data-stu-id="babf8-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="babf8-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="babf8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="babf8-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="babf8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="babf8-109">Récupère la taille du disque dur virtuel dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="babf8-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="babf8-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="babf8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="babf8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="babf8-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="babf8-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="babf8-112">Property value</span></span>

<span data-ttu-id="babf8-113">Taille, en octets, de l’image de disque dur.</span><span class="sxs-lookup"><span data-stu-id="babf8-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="babf8-114">Cette valeur est une **variante** de type VT \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="babf8-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="babf8-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="babf8-115">Error codes</span></span>



| <span data-ttu-id="babf8-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="babf8-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="babf8-117">Signification</span><span class="sxs-lookup"><span data-stu-id="babf8-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="babf8-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="babf8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="babf8-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="babf8-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="babf8-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="babf8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="babf8-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="babf8-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="babf8-122">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="babf8-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="babf8-123">Le fichier de disque dur virtuel actuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="babf8-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="babf8-124"><dt>Ordinateur virtuel \_ \_Échec d' \_ \_ ouverture \_ d’une image HD E</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="babf8-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="babf8-125">Une erreur s’est produite lors de la tentative d’ouverture du fichier image de disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="babf8-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="babf8-126"><dt>Ordinateur virtuel \_ 0xA0040681 \_ d' \_ \_ accès à l’image HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="babf8-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="babf8-127">Une erreur s’est produite lors de la tentative d’accès au fichier image du disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="babf8-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="babf8-128"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="babf8-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="babf8-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="babf8-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="babf8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="babf8-130">Requirements</span></span>



| <span data-ttu-id="babf8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="babf8-131">Requirement</span></span> | <span data-ttu-id="babf8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="babf8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="babf8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="babf8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="babf8-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="babf8-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="babf8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="babf8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="babf8-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="babf8-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="babf8-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="babf8-137">End of client support</span></span><br/>    | <span data-ttu-id="babf8-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="babf8-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="babf8-139">Produit</span><span class="sxs-lookup"><span data-stu-id="babf8-139">Product</span></span><br/>                  | <span data-ttu-id="babf8-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="babf8-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="babf8-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="babf8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="babf8-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="babf8-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="babf8-143">IID</span><span class="sxs-lookup"><span data-stu-id="babf8-143">IID</span></span><br/>                      | <span data-ttu-id="babf8-144">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="babf8-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="babf8-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="babf8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="babf8-146">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="babf8-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

