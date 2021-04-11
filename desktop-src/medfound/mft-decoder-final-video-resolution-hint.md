---
description: Spécifie la résolution de sortie finale de l’image décodée, après le traitement vidéo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Attribut MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201874"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="071cd-103">\_ \_ Attribut d' \_ indicateur de résolution vidéo \_ final \_ du décodeur MFT</span><span class="sxs-lookup"><span data-stu-id="071cd-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="071cd-104">Spécifie la résolution de sortie finale de l’image décodée, après le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="071cd-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="071cd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="071cd-105">Data type</span></span>

<span data-ttu-id="071cd-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="071cd-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="071cd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="071cd-107">Remarks</span></span>

<span data-ttu-id="071cd-108">Cet attribut est pris en charge par certains décodeurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="071cd-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="071cd-109">Une application peut définir cet attribut pour indiquer la largeur et la hauteur de l’image après le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="071cd-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="071cd-110">Le décodeur peut utiliser ces informations pour optimiser le processus de décodage, en particulier si la taille de l’image finale est bien inférieure à la taille de l’image native.</span><span class="sxs-lookup"><span data-stu-id="071cd-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="071cd-111">Par exemple, le décodeur peut ignorer un filtre hors boucle.</span><span class="sxs-lookup"><span data-stu-id="071cd-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="071cd-112">Les 32 bits de poids fort contiennent la largeur et les 32 inférieurs contiennent la hauteur.</span><span class="sxs-lookup"><span data-stu-id="071cd-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="071cd-113">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="071cd-113">To set this attribute:</span></span>

1.  <span data-ttu-id="071cd-114">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="071cd-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="071cd-115">Appelez [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) pour ajouter l’attribut.</span><span class="sxs-lookup"><span data-stu-id="071cd-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="071cd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="071cd-116">Requirements</span></span>



| <span data-ttu-id="071cd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="071cd-117">Requirement</span></span> | <span data-ttu-id="071cd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="071cd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="071cd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="071cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="071cd-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="071cd-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="071cd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="071cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="071cd-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="071cd-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="071cd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="071cd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="071cd-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="071cd-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="071cd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="071cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071cd-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="071cd-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="071cd-127">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="071cd-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




