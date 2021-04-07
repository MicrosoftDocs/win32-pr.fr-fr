---
description: Le filtre d’encodeur Microsoft MPEG-2 encode le contenu audio et vidéo MPEG-2 et multiplexe les flux pour générer un flux de données de programme MPEG-2 ou un flux de transport.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Encodeur Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745965"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="faa91-103">Encodeur Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="faa91-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="faa91-104">Le filtre d’encodeur Microsoft MPEG-2 encode le contenu audio et vidéo MPEG-2 et multiplexe les flux pour générer un flux de données de programme MPEG-2 ou un flux de transport.</span><span class="sxs-lookup"><span data-stu-id="faa91-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="faa91-105">Ce filtre n’est pas pris en charge sur les plateformes IA-64.</span><span class="sxs-lookup"><span data-stu-id="faa91-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="faa91-106">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="faa91-106">Filter Information</span></span>

<span data-ttu-id="faa91-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="faa91-107">Filter Interfaces</span></span>

[<span data-ttu-id="faa91-108">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="faa91-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="faa91-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="faa91-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="faa91-110">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="faa91-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="faa91-111">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="faa91-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="faa91-112">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="faa91-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="faa91-113">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="faa91-113">Input Pin Media Types</span></span>

<span data-ttu-id="faa91-114">Voir les notes</span><span class="sxs-lookup"><span data-stu-id="faa91-114">See Remarks</span></span>

<span data-ttu-id="faa91-115">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="faa91-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="faa91-116">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="faa91-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="faa91-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="faa91-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="faa91-118">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="faa91-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="faa91-119">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="faa91-119">Output Pin Media Types</span></span>

<span data-ttu-id="faa91-120">Voir les notes</span><span class="sxs-lookup"><span data-stu-id="faa91-120">See Remarks</span></span>

<span data-ttu-id="faa91-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="faa91-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="faa91-122">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="faa91-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="faa91-123">**IPin**</span><span class="sxs-lookup"><span data-stu-id="faa91-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="faa91-124">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="faa91-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="faa91-125">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="faa91-125">Filter CLSID</span></span>

<span data-ttu-id="faa91-126">**CLSID \_ CMPEG2EncoderDS** (déclaré dans wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="faa91-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="faa91-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="faa91-127">Executable</span></span>

<span data-ttu-id="faa91-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="faa91-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="faa91-129">Mérite</span><span class="sxs-lookup"><span data-stu-id="faa91-129">Merit</span></span>](merit.md)

<span data-ttu-id="faa91-130">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="faa91-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="faa91-131">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="faa91-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="faa91-132">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="faa91-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="faa91-133">Notes</span><span class="sxs-lookup"><span data-stu-id="faa91-133">Remarks</span></span>

<span data-ttu-id="faa91-134">Ce filtre combine la fonctionnalité d’encodage de deux autres filtres :</span><span class="sxs-lookup"><span data-stu-id="faa91-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="faa91-135">**Encodeur audio Microsoft MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="faa91-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="faa91-136">**Encodeur vidéo Microsoft MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="faa91-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="faa91-137">Sauf indication contraire, ce filtre prend en charge les mêmes fonctionnalités d’encodage que ces deux encodeurs.</span><span class="sxs-lookup"><span data-stu-id="faa91-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="faa91-138">Initialement, le filtre a une seule broche d’entrée, qui peut accepter les entrées audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="faa91-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="faa91-139">Lorsque ce code PIN est connecté, le filtre crée une deuxième broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="faa91-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="faa91-140">Si la première broche d’entrée reçoit du son, la deuxième broche d’entrée n’accepte que la vidéo, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="faa91-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="faa91-141">Chaque broche d’entrée prend en charge les mêmes types de supports que le filtre d’encodeur correspondant.</span><span class="sxs-lookup"><span data-stu-id="faa91-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="faa91-142">Si une seule broche d’entrée est connectée, le filtre prend en charge les mêmes types de sortie que l’encodeur audio ou vidéo correspondant.</span><span class="sxs-lookup"><span data-stu-id="faa91-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="faa91-143">Si les deux broches sont connectées, le filtre prend en charge les types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="faa91-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="faa91-144">Audio-Visual dans un flux de programme MPEG-2</span><span class="sxs-lookup"><span data-stu-id="faa91-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="faa91-145">Audio-visuel dans un flux de transport MPEG-2</span><span class="sxs-lookup"><span data-stu-id="faa91-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="faa91-146">Elles correspondent aux types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="faa91-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="faa91-147">**MediaType \_ Stream**, **\_ \_ programme MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="faa91-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="faa91-148">**MediaType \_ Flux**, **\_ \_ transport MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="faa91-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="faa91-149">Ce filtre ne peut pas multiplexer les flux qui ont été précédemment encodés.</span><span class="sxs-lookup"><span data-stu-id="faa91-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="faa91-150">Les flux d’entrée doivent être des données audio/vidéo non compressées, que le filtre encode avant le multiplexage.</span><span class="sxs-lookup"><span data-stu-id="faa91-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="faa91-151">Le flux multiplexé est limité à un programme, contenant jusqu’à un audio et un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="faa91-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="faa91-152">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="faa91-152">Codec Properties</span></span>

<span data-ttu-id="faa91-153">Le filtre prend en charge les propriétés combinées des filtres d’encodeur [**audio MPEG-2**](microsoft-mpeg-2-audio-encoder.md) et d' [**encodeur vidéo MPEG-2**](microsoft-mpeg-2-video-encoder.md) , à la différence suivante :</span><span class="sxs-lookup"><span data-stu-id="faa91-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="faa91-154">La propriété [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) définit la vitesse de transmission moyenne du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="faa91-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="faa91-155">La propriété [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) définit la vitesse de transmission moyenne du flux audio.</span><span class="sxs-lookup"><span data-stu-id="faa91-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa91-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faa91-156">Requirements</span></span>



| <span data-ttu-id="faa91-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faa91-157">Requirement</span></span> | <span data-ttu-id="faa91-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="faa91-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa91-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa91-159">Minimum supported client</span></span><br/> | <span data-ttu-id="faa91-160">Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faa91-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="faa91-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa91-161">Minimum supported server</span></span><br/> | <span data-ttu-id="faa91-162">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa91-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="faa91-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="faa91-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa91-164"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa91-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="faa91-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faa91-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa91-166">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="faa91-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
