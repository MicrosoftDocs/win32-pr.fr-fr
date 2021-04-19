---
description: Contient le IMFMediaType qui décrit le type de format d’image contenu dans l' \_ attribut de Photominiature MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Attribut MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539792"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="ded27-103">\_Attribut MFSampleExtension PhotoThumbnailMediaType</span><span class="sxs-lookup"><span data-stu-id="ded27-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="ded27-104">Contient le [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) qui décrit le type de format d’image contenu dans l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="ded27-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="ded27-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ded27-105">Data type</span></span>

<span data-ttu-id="ded27-106">**IUnknown** stocké en tant que **IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ded27-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="ded27-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ded27-107">Remarks</span></span>

<span data-ttu-id="ded27-108">Si l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) est présent sur l’échantillon de photo, le \_ PhotoThumbnailMediaType MFSampleExtension est obligatoire et doit contenir au minimum le [type de clé \_ \_ principale \_ MF MT](mf-mt-major-type-attribute.md), le sous- [ \_ \_ type MF MT](mf-mt-subtype-attribute.md) et la [ \_ \_ \_ taille d’image MF MT](mf-mt-frame-size-attribute.md) qui décrivent la miniature.</span><span class="sxs-lookup"><span data-stu-id="ded27-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded27-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ded27-109">Requirements</span></span>



| <span data-ttu-id="ded27-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ded27-110">Requirement</span></span> | <span data-ttu-id="ded27-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ded27-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ded27-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded27-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ded27-113">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ded27-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ded27-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded27-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ded27-115">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ded27-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ded27-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ded27-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded27-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded27-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded27-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ded27-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded27-119">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ded27-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ded27-120">Miniature de MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="ded27-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




