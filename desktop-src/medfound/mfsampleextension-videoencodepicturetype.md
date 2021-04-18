---
description: Spécifie le type d’image qui est sortie par un encodeur vidéo.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Attribut MFSampleExtension_VideoEncodePictureType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519585"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="08b28-103">\_Attribut MFSampleExtension VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="08b28-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="08b28-104">Spécifie le type d’image qui est sortie par un encodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="08b28-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="08b28-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="08b28-105">Data type</span></span>

<span data-ttu-id="08b28-106">**eAVEncH264PictureType \_ B** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08b28-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="08b28-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="08b28-107">Get/set</span></span>

<span data-ttu-id="08b28-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="08b28-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="08b28-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="08b28-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="08b28-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="08b28-110">Applies to</span></span>

[<span data-ttu-id="08b28-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="08b28-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="08b28-112">Notes</span><span class="sxs-lookup"><span data-stu-id="08b28-112">Remarks</span></span>

<span data-ttu-id="08b28-113">L' [**encodeur vidéo H. 264**](h-264-video-encoder.md) définit cet attribut sur les exemples de sortie qu’il génère.</span><span class="sxs-lookup"><span data-stu-id="08b28-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="08b28-114">La valeur de l’attribut est un membre de l’énumération [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .</span><span class="sxs-lookup"><span data-stu-id="08b28-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b28-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08b28-115">Requirements</span></span>



| <span data-ttu-id="08b28-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08b28-116">Requirement</span></span> | <span data-ttu-id="08b28-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="08b28-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08b28-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08b28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08b28-119">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="08b28-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="08b28-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08b28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08b28-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="08b28-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="08b28-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="08b28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08b28-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="08b28-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b28-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08b28-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b28-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08b28-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08b28-126">**Encodeur vidéo H. 264**</span><span class="sxs-lookup"><span data-stu-id="08b28-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="08b28-127">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="08b28-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="08b28-128">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="08b28-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




