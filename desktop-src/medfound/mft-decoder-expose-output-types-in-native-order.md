---
description: Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Attribut MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755277"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="7e840-103">Le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ attribut order natif</span><span class="sxs-lookup"><span data-stu-id="7e840-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="7e840-104">Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="7e840-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e840-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7e840-105">Data type</span></span>

<span data-ttu-id="7e840-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7e840-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e840-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7e840-107">Remarks</span></span>

<span data-ttu-id="7e840-108">Cet attribut est une indication pour le décodeur de réorganiser sa liste de types de sortie dans un ordre particulier, en fonction de l’utilisation prévue, de lecture ou de transcodage.</span><span class="sxs-lookup"><span data-stu-id="7e840-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="7e840-109">Pour la plupart des formats d’encodage (H. 264, MPEG-2, WMV), les décodeurs vidéo dans Microsoft Media Foundation prennent en charge plusieurs sorties YUV courantes, notamment NV12, YV12, YUY2, IYUV et I420.</span><span class="sxs-lookup"><span data-stu-id="7e840-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="7e840-110">Le décodeur offre une liste triée des types de sortie par le biais de sa méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .</span><span class="sxs-lookup"><span data-stu-id="7e840-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="7e840-111">Pour la lecture, NV12 est le format le plus efficace et le plus largement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7e840-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="7e840-112">Par conséquent, par défaut, les décodeurs offrent généralement NV12 comme premier type de sortie dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7e840-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="7e840-113">Cela réduit le temps nécessaire pour résoudre le type de média lors de la génération d’une topologie de lecture.</span><span class="sxs-lookup"><span data-stu-id="7e840-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="7e840-114">Toutefois, pour le transcodage, les IYUV ou les I420 sont plus efficaces pour le processeur et sont généralement préférés par des encodeurs.</span><span class="sxs-lookup"><span data-stu-id="7e840-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="7e840-115">Si un décodeur prend en charge cet attribut, l’attribut a le comportement suivant :</span><span class="sxs-lookup"><span data-stu-id="7e840-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="7e840-116">Si l’attribut a une valeur différente de zéro, IYUV et I420 apparaissent en premier dans la liste des types de médias de sortie.</span><span class="sxs-lookup"><span data-stu-id="7e840-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="7e840-117">Ce paramètre est plus efficace pour le transcodage.</span><span class="sxs-lookup"><span data-stu-id="7e840-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="7e840-118">Si l’attribut est égal à zéro, NV12 apparaît en premier dans la liste des types de médias de sortie.</span><span class="sxs-lookup"><span data-stu-id="7e840-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="7e840-119">Ce paramètre est plus efficace pour la lecture et est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7e840-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="7e840-120">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="7e840-120">To set this attribute:</span></span>

1.  <span data-ttu-id="7e840-121">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="7e840-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="7e840-122">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour ajouter l’attribut.</span><span class="sxs-lookup"><span data-stu-id="7e840-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e840-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e840-123">Requirements</span></span>



| <span data-ttu-id="7e840-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e840-124">Requirement</span></span> | <span data-ttu-id="7e840-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e840-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e840-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e840-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7e840-127">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e840-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7e840-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e840-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7e840-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e840-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7e840-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e840-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e840-131"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e840-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e840-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e840-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e840-133">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e840-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




