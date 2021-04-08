---
title: IVMFloppyDrive, propriété de la propriété image (VPCCOMInterfaces. h)
description: Récupère le chemin d’accès complet du fichier image auquel le lecteur de disquette est attaché.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- Propriété de image Virtual PC
- Propriété de image Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, propriété image
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033072"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="51bb1-106">IVMFloppyDrive :: image, propriété</span><span class="sxs-lookup"><span data-stu-id="51bb1-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="51bb1-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="51bb1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="51bb1-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="51bb1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="51bb1-109">Récupère le chemin d’accès complet du fichier image auquel le lecteur de disquette est attaché.</span><span class="sxs-lookup"><span data-stu-id="51bb1-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="51bb1-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="51bb1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bb1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51bb1-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="51bb1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="51bb1-112">Property value</span></span>

<span data-ttu-id="51bb1-113">Chemin d’accès complet du fichier image.</span><span class="sxs-lookup"><span data-stu-id="51bb1-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="51bb1-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="51bb1-114">Error codes</span></span>



| <span data-ttu-id="51bb1-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="51bb1-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="51bb1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="51bb1-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51bb1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51bb1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="51bb1-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="51bb1-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="51bb1-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="51bb1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="51bb1-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="51bb1-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="51bb1-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="51bb1-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="51bb1-122">La configuration de cette machine virtuelle n’est pas valide ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="51bb1-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="51bb1-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="51bb1-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="51bb1-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="51bb1-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="51bb1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51bb1-125">Requirements</span></span>



| <span data-ttu-id="51bb1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51bb1-126">Requirement</span></span> | <span data-ttu-id="51bb1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="51bb1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bb1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51bb1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="51bb1-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51bb1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51bb1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51bb1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="51bb1-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="51bb1-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="51bb1-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="51bb1-132">End of client support</span></span><br/>    | <span data-ttu-id="51bb1-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51bb1-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="51bb1-134">Produit</span><span class="sxs-lookup"><span data-stu-id="51bb1-134">Product</span></span><br/>                  | <span data-ttu-id="51bb1-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="51bb1-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="51bb1-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="51bb1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="51bb1-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="51bb1-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="51bb1-138">IID</span><span class="sxs-lookup"><span data-stu-id="51bb1-138">IID</span></span><br/>                      | <span data-ttu-id="51bb1-139">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="51bb1-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="51bb1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51bb1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bb1-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="51bb1-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

