---
description: Contient la miniature de photo d’un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Attribut MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114999"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="6f528-103">MFSampleExtension- \_ miniature, attribut</span><span class="sxs-lookup"><span data-stu-id="6f528-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="6f528-104">Contient la miniature de photo d’un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="6f528-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="6f528-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6f528-105">Data type</span></span>

<span data-ttu-id="6f528-106">**IUnknown** stocké en tant que **IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f528-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="6f528-107">La miniature est configurée à l’aide de **KSPROPERTYSETID \_ ExtendedCameraControl**.</span><span class="sxs-lookup"><span data-stu-id="6f528-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f528-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6f528-108">Remarks</span></span>

<span data-ttu-id="6f528-109">Cet attribut est défini sur le [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fourni par MFT0 et est l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associé à la miniature de photo.</span><span class="sxs-lookup"><span data-stu-id="6f528-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="6f528-110">Le format de la miniature de photo peut être JPEG (image de type majeure), NV12 ou ARGB32.</span><span class="sxs-lookup"><span data-stu-id="6f528-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="6f528-111">Le [ \_ PhotoThumbnailMediaType MFSampleExtension](mfsampleextension-photothumbnailmediatype.md) est requis pour les miniatures pour décrire le type de média.</span><span class="sxs-lookup"><span data-stu-id="6f528-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f528-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f528-112">Requirements</span></span>



| <span data-ttu-id="6f528-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f528-113">Requirement</span></span> | <span data-ttu-id="6f528-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f528-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f528-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f528-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6f528-116">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6f528-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="6f528-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f528-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6f528-118">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6f528-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6f528-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f528-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f528-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f528-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f528-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f528-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f528-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f528-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f528-123">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="6f528-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
