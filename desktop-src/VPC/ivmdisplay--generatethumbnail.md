---
title: IVMDisplay _GenerateThumbnail, méthode (VPCCOMInterfaces. h)
description: Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel. | IVMDisplay _GenerateThumbnail, méthode (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- Méthode _GenerateThumbnail Virtual PC
- _GenerateThumbnail méthode Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, méthode _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539834"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="ef16e-107">IVMDisplay :: \_ GenerateThumbnail, méthode</span><span class="sxs-lookup"><span data-stu-id="ef16e-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="ef16e-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ef16e-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ef16e-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ef16e-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ef16e-110">Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ef16e-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef16e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef16e-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="ef16e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef16e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef16e-113">*thumbnailimage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef16e-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef16e-114">Tableau de pixels représentant une image miniature de l’écran de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ef16e-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef16e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef16e-115">Return value</span></span>

<span data-ttu-id="ef16e-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="ef16e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ef16e-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ef16e-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ef16e-118">Description</span><span class="sxs-lookup"><span data-stu-id="ef16e-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ef16e-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef16e-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ef16e-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ef16e-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ef16e-121"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ef16e-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ef16e-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ef16e-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ef16e-123"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ef16e-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ef16e-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ef16e-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef16e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ef16e-125">Remarks</span></span>

<span data-ttu-id="ef16e-126">Cette interface retourne plus efficacement la miniature que la propriété [**thumbnail**](ivmdisplay-thumbnail.md) , mais elle n’est pas utilisable à partir de scripts de clients.</span><span class="sxs-lookup"><span data-stu-id="ef16e-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="ef16e-127">La miniature est toujours de 64 pixels de large de 48 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="ef16e-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="ef16e-128">Chaque pixel est 32 bits, où les 8 bits de poids fort représentent la valeur bleue du pixel, les 8 bits suivants représentent la valeur verte du pixel, et les 8 bits suivants représentent la valeur rouge du pixel.</span><span class="sxs-lookup"><span data-stu-id="ef16e-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="ef16e-129">Les 64 premiers éléments du tableau sont la première ligne de la miniature, les 64 suivants sont la deuxième ligne, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ef16e-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="ef16e-130">Cette méthode retourne un tableau statique de pixels, qui est plus efficace que le retour d’un **SAFEARRAY** de valeurs **Variant** , mais n’est pas compatible avec les clients de script.</span><span class="sxs-lookup"><span data-stu-id="ef16e-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef16e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef16e-131">Requirements</span></span>



| <span data-ttu-id="ef16e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef16e-132">Requirement</span></span> | <span data-ttu-id="ef16e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef16e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef16e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef16e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ef16e-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef16e-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef16e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef16e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ef16e-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef16e-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ef16e-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ef16e-138">End of client support</span></span><br/>    | <span data-ttu-id="ef16e-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef16e-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ef16e-140">Produit</span><span class="sxs-lookup"><span data-stu-id="ef16e-140">Product</span></span><br/>                  | <span data-ttu-id="ef16e-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ef16e-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ef16e-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef16e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef16e-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef16e-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ef16e-144">IID</span><span class="sxs-lookup"><span data-stu-id="ef16e-144">IID</span></span><br/>                      | <span data-ttu-id="ef16e-145">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="ef16e-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ef16e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef16e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef16e-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="ef16e-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

