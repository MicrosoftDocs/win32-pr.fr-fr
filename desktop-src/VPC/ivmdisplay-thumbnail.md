---
title: IVMDisplay, propriété de la miniature (VPCCOMInterfaces. h)
description: Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel. | IVMDisplay, propriété de la miniature (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propriété de miniature Virtual PC
- Propriété de miniature Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, propriété thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953533"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="80f44-107">IVMDisplay :: Thumbnail, propriété</span><span class="sxs-lookup"><span data-stu-id="80f44-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="80f44-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="80f44-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="80f44-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="80f44-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="80f44-110">Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="80f44-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="80f44-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="80f44-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80f44-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80f44-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="80f44-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="80f44-113">Property value</span></span>

<span data-ttu-id="80f44-114">Variante de type VT de \_ tableau \| VT \_ contenant des entrées de type VT \_ UI4, une pour chaque pixel de la miniature.</span><span class="sxs-lookup"><span data-stu-id="80f44-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80f44-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="80f44-115">Error codes</span></span>



| <span data-ttu-id="80f44-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="80f44-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="80f44-117">Signification</span><span class="sxs-lookup"><span data-stu-id="80f44-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="80f44-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80f44-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="80f44-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="80f44-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="80f44-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="80f44-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="80f44-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="80f44-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="80f44-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="80f44-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="80f44-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="80f44-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="80f44-124">Notes</span><span class="sxs-lookup"><span data-stu-id="80f44-124">Remarks</span></span>

<span data-ttu-id="80f44-125">Cette interface retourne la miniature moins efficacement que la méthode [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , mais elle est utilisable à partir des clients de script.</span><span class="sxs-lookup"><span data-stu-id="80f44-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="80f44-126">La miniature est toujours de 64 pixels de large de 48 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="80f44-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="80f44-127">Chaque pixel est 32 bits.</span><span class="sxs-lookup"><span data-stu-id="80f44-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="80f44-128">Les 64 premiers éléments du tableau sont la première ligne de pixels de la miniature, les 64 suivants étant la deuxième ligne, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="80f44-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f44-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80f44-129">Requirements</span></span>



| <span data-ttu-id="80f44-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80f44-130">Requirement</span></span> | <span data-ttu-id="80f44-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="80f44-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f44-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80f44-132">Minimum supported client</span></span><br/> | <span data-ttu-id="80f44-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80f44-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80f44-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80f44-134">Minimum supported server</span></span><br/> | <span data-ttu-id="80f44-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80f44-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="80f44-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="80f44-136">End of client support</span></span><br/>    | <span data-ttu-id="80f44-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80f44-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="80f44-138">Produit</span><span class="sxs-lookup"><span data-stu-id="80f44-138">Product</span></span><br/>                  | <span data-ttu-id="80f44-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80f44-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="80f44-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="80f44-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="80f44-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="80f44-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="80f44-142">IID</span><span class="sxs-lookup"><span data-stu-id="80f44-142">IID</span></span><br/>                      | <span data-ttu-id="80f44-143">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="80f44-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="80f44-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80f44-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80f44-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="80f44-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

