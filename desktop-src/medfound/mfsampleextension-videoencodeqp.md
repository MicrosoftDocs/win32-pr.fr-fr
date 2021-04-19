---
description: Spécifie le paramètre de quantification (QP) utilisé pour encoder un échantillon vidéo.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Attribut MFSampleExtension_VideoEncodeQP (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524144"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="18d94-103">\_Attribut MFSampleExtension VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="18d94-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="18d94-104">Spécifie le paramètre de quantification (QP) utilisé pour encoder un échantillon vidéo.</span><span class="sxs-lookup"><span data-stu-id="18d94-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="18d94-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="18d94-105">Data type</span></span>

<span data-ttu-id="18d94-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="18d94-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="18d94-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="18d94-107">Get/set</span></span>

<span data-ttu-id="18d94-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="18d94-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="18d94-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="18d94-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="18d94-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="18d94-110">Applies to</span></span>

[<span data-ttu-id="18d94-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="18d94-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="18d94-112">Notes</span><span class="sxs-lookup"><span data-stu-id="18d94-112">Remarks</span></span>

<span data-ttu-id="18d94-113">L' [**encodeur vidéo H. 264**](h-264-video-encoder.md) définit cet attribut sur les exemples de sortie qu’il génère.</span><span class="sxs-lookup"><span data-stu-id="18d94-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d94-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18d94-114">Requirements</span></span>



| <span data-ttu-id="18d94-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18d94-115">Requirement</span></span> | <span data-ttu-id="18d94-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d94-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18d94-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d94-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18d94-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="18d94-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="18d94-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d94-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18d94-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d94-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="18d94-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="18d94-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d94-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d94-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d94-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d94-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d94-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18d94-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18d94-125">**Encodeur vidéo H. 264**</span><span class="sxs-lookup"><span data-stu-id="18d94-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="18d94-126">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="18d94-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="18d94-127">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="18d94-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




