---
description: La surface par défaut Stride, pour un type de média vidéo non compressé. STRIDE est le nombre d’octets nécessaires pour passer d’une ligne de pixels à la suivante.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Attribut MF_MT_DEFAULT_STRIDE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201980"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="dd75d-104">\_ \_ Attribut Stride par défaut MF MT \_</span><span class="sxs-lookup"><span data-stu-id="dd75d-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="dd75d-105">La surface par défaut Stride, pour un type de média vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="dd75d-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="dd75d-106">STRIDE est le nombre d’octets nécessaires pour passer d’une ligne de pixels à la suivante.</span><span class="sxs-lookup"><span data-stu-id="dd75d-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="dd75d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="dd75d-107">Data type</span></span>

<span data-ttu-id="dd75d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dd75d-108">**UINT32**</span></span>

<span data-ttu-id="dd75d-109">Traiter en tant que valeur **Int32** .</span><span class="sxs-lookup"><span data-stu-id="dd75d-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd75d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dd75d-110">Remarks</span></span>

<span data-ttu-id="dd75d-111">La valeur de l’attribut est stockée sous la forme d’un **UInt32**, mais doit être castée en valeur entière signée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dd75d-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="dd75d-112">STRIDE peut être négatif.</span><span class="sxs-lookup"><span data-stu-id="dd75d-112">Stride can be negative.</span></span>

<span data-ttu-id="dd75d-113">STRIDE est positif pour les images de haut en bas et négatif pour les images de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="dd75d-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="dd75d-114">Cet attribut donne le Stride pour une représentation *contiguë* de l’image en mémoire ; autrement dit, une représentation sans octets de remplissage supplémentaires après chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="dd75d-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="dd75d-115">Si une mémoire tampon de média prend en charge l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , utilisez la méthode [**IMF2DBuffer :: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) pour obtenir le Stride réel de la surface, qui peut inclure des octets de remplissage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="dd75d-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="dd75d-116">Pour plus d’informations sur la Stride de surface, consultez [Stride d’image](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="dd75d-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="dd75d-117">Pour obtenir un exemple de calcul du Stride par défaut, consultez [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="dd75d-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="dd75d-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dd75d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd75d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd75d-119">Requirements</span></span>



| <span data-ttu-id="dd75d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd75d-120">Requirement</span></span> | <span data-ttu-id="dd75d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd75d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd75d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd75d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd75d-123">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd75d-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dd75d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd75d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd75d-125">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd75d-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dd75d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd75d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd75d-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd75d-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd75d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd75d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd75d-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd75d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dd75d-130">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dd75d-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dd75d-131">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dd75d-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dd75d-132">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dd75d-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dd75d-133">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="dd75d-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="dd75d-134">STRIDE d’image</span><span class="sxs-lookup"><span data-stu-id="dd75d-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




