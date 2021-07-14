---
description: Signale les métadonnées et la mémoire tampon de masque pour un masque de segmentation d’arrière-plan qui fait la distinction entre l’arrière-plan et le premier plan d’une image vidéo.
title: Attribut MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK (Mfapi. h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691842"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="26319-103">\_Attribut de \_ \_ masque d' \_ arrière-plan du frame de MÉTADONNÉEs de capture MF \_</span><span class="sxs-lookup"><span data-stu-id="26319-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="26319-104">Signale les métadonnées et la mémoire tampon de masque pour un masque de segmentation d’arrière-plan qui fait la distinction entre l’arrière-plan et le premier plan d’une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="26319-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="26319-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="26319-105">Data type</span></span>

<span data-ttu-id="26319-106">**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="26319-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="26319-107">Notes</span><span class="sxs-lookup"><span data-stu-id="26319-107">Remarks</span></span>

<span data-ttu-id="26319-108">Les données fournies par cet attribut sont une structure [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) qui contient des informations sur les dimensions du masque d’arrière-plan, ainsi que la couverture du frame à partir duquel il est déduit, qui est le frame qui est sorti par le flux.</span><span class="sxs-lookup"><span data-stu-id="26319-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="26319-109">Il comporte également une mémoire tampon contiguë représentant le masque à exploiter par l’application consommatrice pour définir les pixels qui sont considérés comme faisant partie du premier plan ou de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="26319-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="26319-110">La mise à l’échelle et la corrélation de la coordonnée d’image du masque concernant le frame sont gérées par l’application consommatrice.</span><span class="sxs-lookup"><span data-stu-id="26319-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="26319-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26319-111">Requirements</span></span>



| <span data-ttu-id="26319-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26319-112">Requirement</span></span> | <span data-ttu-id="26319-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="26319-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26319-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26319-114">Minimum supported client</span></span><br/> | <span data-ttu-id="26319-115">Windows 22000t de build</span><span class="sxs-lookup"><span data-stu-id="26319-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="26319-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26319-116">Minimum supported server</span></span><br/> | <span data-ttu-id="26319-117">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="26319-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="26319-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="26319-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="26319-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26319-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26319-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26319-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26319-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26319-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26319-122">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="26319-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="26319-123">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="26319-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="26319-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="26319-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="26319-125">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="26319-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




