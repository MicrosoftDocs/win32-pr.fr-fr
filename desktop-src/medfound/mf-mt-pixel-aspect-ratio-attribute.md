---
description: Proportions de pixels pour un type de média vidéo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Attribut MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526601"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="683d9-103">\_Attribut des \_ \_ \_ proportions de pixels MF MT</span><span class="sxs-lookup"><span data-stu-id="683d9-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="683d9-104">Proportions de pixels pour un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="683d9-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="683d9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="683d9-105">Data type</span></span>

<span data-ttu-id="683d9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="683d9-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="683d9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="683d9-107">Remarks</span></span>

<span data-ttu-id="683d9-108">Les 32 bits supérieurs contiennent le numérateur des proportions de pixels et les 32 bits inférieurs contiennent le dénominateur.</span><span class="sxs-lookup"><span data-stu-id="683d9-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="683d9-109">Le numérateur est le composant horizontal des proportions ; le dénominateur est le composant vertical.</span><span class="sxs-lookup"><span data-stu-id="683d9-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="683d9-110">Pour définir cet attribut, utilisez la fonction [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="683d9-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="683d9-111">Pour récupérer cet attribut, utilisez la fonction [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="683d9-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="683d9-112">Les proportions de pixels décrivent la forme des pixels de l’image vidéo affichée.</span><span class="sxs-lookup"><span data-stu-id="683d9-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="683d9-113">Définissez cet attribut si l’image a des pixels non carrés.</span><span class="sxs-lookup"><span data-stu-id="683d9-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="683d9-114">Pour afficher correctement sur un appareil d’affichage avec des pixels carrés, l’image doit être mise à l’échelle par l’inverse des proportions de pixels de l’image.</span><span class="sxs-lookup"><span data-stu-id="683d9-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="683d9-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="683d9-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="683d9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="683d9-116">Requirements</span></span>



| <span data-ttu-id="683d9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="683d9-117">Requirement</span></span> | <span data-ttu-id="683d9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="683d9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="683d9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="683d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="683d9-120">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="683d9-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="683d9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="683d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="683d9-122">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="683d9-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="683d9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="683d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="683d9-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="683d9-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683d9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="683d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683d9-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="683d9-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="683d9-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="683d9-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="683d9-128">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="683d9-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="683d9-129">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="683d9-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




