---
title: IVMDVDDrive, propriété de la propriété image (VPCCOMInterfaces. h)
description: Récupère le chemin d’accès complet du jeu de fichiers image pour cet appareil.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Propriété de image Virtual PC
- Propriété de image Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, propriété image
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844205"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="a46a0-106">IVMDVDDrive :: image, propriété</span><span class="sxs-lookup"><span data-stu-id="a46a0-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="a46a0-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a46a0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a46a0-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a46a0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a46a0-109">Récupère le chemin d’accès complet du jeu de fichiers image pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="a46a0-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="a46a0-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a46a0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46a0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a46a0-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="a46a0-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a46a0-112">Property value</span></span>

<span data-ttu-id="a46a0-113">Chemin d’accès complet au fichier image.</span><span class="sxs-lookup"><span data-stu-id="a46a0-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a46a0-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a46a0-114">Error codes</span></span>



| <span data-ttu-id="a46a0-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a46a0-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="a46a0-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a46a0-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a46a0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="a46a0-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a46a0-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="a46a0-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="a46a0-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a46a0-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a46a0-121"><dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="a46a0-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a46a0-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="a46a0-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="a46a0-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="a46a0-124">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a46a0-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="a46a0-125"><dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="a46a0-126">L’emplacement du bus pour ce lecteur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a46a0-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="a46a0-127"><dt>Ordinateur virtuel \_ \_Type de média E \_ incorrect \_ </dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="a46a0-128">Le support capturé par ce lecteur de DVD n’est pas un fichier image ISO.</span><span class="sxs-lookup"><span data-stu-id="a46a0-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="a46a0-129"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="a46a0-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a46a0-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="a46a0-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a46a0-131">Requirements</span></span>



| <span data-ttu-id="a46a0-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a46a0-132">Requirement</span></span> | <span data-ttu-id="a46a0-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a46a0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a46a0-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a46a0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a46a0-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a46a0-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a46a0-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a46a0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a46a0-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a46a0-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a46a0-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a46a0-138">End of client support</span></span><br/>    | <span data-ttu-id="a46a0-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a46a0-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a46a0-140">Produit</span><span class="sxs-lookup"><span data-stu-id="a46a0-140">Product</span></span><br/>                  | <span data-ttu-id="a46a0-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a46a0-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a46a0-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="a46a0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a46a0-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a46a0-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a46a0-144">IID</span><span class="sxs-lookup"><span data-stu-id="a46a0-144">IID</span></span><br/>                      | <span data-ttu-id="a46a0-145">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="a46a0-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a46a0-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a46a0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46a0-147">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="a46a0-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

