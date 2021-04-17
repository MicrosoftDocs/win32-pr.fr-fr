---
description: Le décodeur vidéo Media Foundation H. 265 est une transformation Media Foundation qui prend en charge le décodage du contenu H. 265/HEVC dans l’annexe B et qui peut être utilisée pour la lecture de fichiers MP4 et M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Décodeur vidéo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527699"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="71262-103">Décodeur vidéo H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="71262-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="71262-104">Le décodeur vidéo Media Foundation H. 265 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge le décodage du contenu h. 265/HEVC dans l’annexe B et qui peut être utilisée pour la lecture de fichiers MP4 et M2TS.</span><span class="sxs-lookup"><span data-stu-id="71262-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="71262-105">Le décodeur vidéo H. 265 expose les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="71262-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="71262-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (pris en charge dans Windows 8)</span><span class="sxs-lookup"><span data-stu-id="71262-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="71262-107">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="71262-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="71262-108">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="71262-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="71262-109">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="71262-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="71262-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="71262-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="71262-111">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="71262-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="71262-112">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="71262-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="71262-113">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="71262-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="71262-114">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="71262-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="71262-115">Pour créer une instance du décodeur, appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="71262-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="71262-116">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="71262-116">Input Types</span></span>

<span data-ttu-id="71262-117">Le type d’entrée doit contenir au moins les deux attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="71262-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="71262-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="71262-118">Attribute</span></span>                                                 | <span data-ttu-id="71262-119">Description</span><span class="sxs-lookup"><span data-stu-id="71262-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71262-120">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="71262-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="71262-121">**\_Vidéo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="71262-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="71262-122">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="71262-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="71262-123">[MFVideoFormat \_ HEVC](video-subtype-guids.md) ou MFVideoFormat \_ HEVC \_ es</span><span class="sxs-lookup"><span data-stu-id="71262-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="71262-124">Le premier sous-type de média, MFVideoFormat \_ HEVC, indique que les exemples de supports transportent le flux de sortie H. 265 avec les codes de démarrage et que le flux a des SPS/PPS entrelacés.</span><span class="sxs-lookup"><span data-stu-id="71262-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="71262-125">Il suppose une trame par échantillon.</span><span class="sxs-lookup"><span data-stu-id="71262-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="71262-126">Le sous-type de média MFVideoFormat \_ HEVC \_ es permet d’indiquer que les exemples de supports transportent des flux binaires élémentaires H. 265, où chaque exemple peut contenir une image partielle, plusieurs images, certaines images et une image partielle.</span><span class="sxs-lookup"><span data-stu-id="71262-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="71262-127">Les types de média d’entrée ne peuvent pas changer dynamiquement entre deux types.</span><span class="sxs-lookup"><span data-stu-id="71262-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="71262-128">Le décodeur peut détecter les modifications de format de sortie en cours en fonction de la syntaxe de flux élémentaire (proportions, dimension, indicateurs entrelacés, informations de colorimétrie) et déclencher les modifications de type de média de sortie correspondantes.</span><span class="sxs-lookup"><span data-stu-id="71262-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="71262-129">Pour le type de média d’entrée, le décodeur s’attend à ce que la source définisse le profil approprié.</span><span class="sxs-lookup"><span data-stu-id="71262-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="71262-130">Par exemple, si le contenu va être 10, le type de média d’entrée doit spécifier le profil en tant que Main10.</span><span class="sxs-lookup"><span data-stu-id="71262-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="71262-131">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="71262-131">Output Types</span></span>

<span data-ttu-id="71262-132">Le décodeur prend en charge les sous-types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="71262-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="71262-133">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="71262-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="71262-134">**MFVideoFormat \_ P010**</span><span class="sxs-lookup"><span data-stu-id="71262-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="71262-135">Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="71262-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="71262-136">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="71262-136">Transform Attributes</span></span>

<span data-ttu-id="71262-137">Le décodeur H. 265 implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="71262-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="71262-138">Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="71262-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="71262-139">Attribut</span><span class="sxs-lookup"><span data-stu-id="71262-139">Attribute</span></span>                                                                                       | <span data-ttu-id="71262-140">Description</span><span class="sxs-lookup"><span data-stu-id="71262-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71262-141">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="71262-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="71262-142">Active ou désactive le mode de décodage à latence faible.</span><span class="sxs-lookup"><span data-stu-id="71262-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="71262-143">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="71262-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="71262-144">Définit le nombre de threads de travail utilisés par le décodeur.</span><span class="sxs-lookup"><span data-stu-id="71262-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="71262-145">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="71262-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="71262-146">Active ou désactive le mode de génération de miniatures.</span><span class="sxs-lookup"><span data-stu-id="71262-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="71262-147">\_longueur de Nalu MF \_ \_ définie</span><span class="sxs-lookup"><span data-stu-id="71262-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="71262-148">Indique que les informations de longueur NALU sont envoyées en tant qu’objet BLOB avec chaque exemple H. 265 compressé.</span><span class="sxs-lookup"><span data-stu-id="71262-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="71262-149">\_ \_ informations sur la longueur Nalu MF \_</span><span class="sxs-lookup"><span data-stu-id="71262-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="71262-150">Indique les longueurs de NALUs dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="71262-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="71262-151">Il s’agit d’un objet BLOB MF qui est défini sur les exemples d’entrée compressés sur le décodeur H. 265.</span><span class="sxs-lookup"><span data-stu-id="71262-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="71262-152">\_ \_ nombre minimal d' \_ échantillons de sortie MF \_ sa \_</span><span class="sxs-lookup"><span data-stu-id="71262-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="71262-153">Spécifie le nombre maximal d’échantillons de sortie.</span><span class="sxs-lookup"><span data-stu-id="71262-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="71262-154">Le décodeur H. 265 prend en charge l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="71262-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="71262-155">Cette interface fournit une API alternativate pour définir les propriétés de codec suivantes.</span><span class="sxs-lookup"><span data-stu-id="71262-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="71262-156">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="71262-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="71262-157">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="71262-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="71262-158">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="71262-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="71262-159">Contraintes de format</span><span class="sxs-lookup"><span data-stu-id="71262-159">Format Constraints</span></span>

<span data-ttu-id="71262-160">Le décodeur prend en charge les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="71262-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="71262-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71262-161">Requirement</span></span> | <span data-ttu-id="71262-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="71262-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71262-163">Profils/niveaux</span><span class="sxs-lookup"><span data-stu-id="71262-163">Profiles/Levels</span></span>    | <span data-ttu-id="71262-164">Profils main, main Still image et Main10</span><span class="sxs-lookup"><span data-stu-id="71262-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="71262-165">Formats de chrominance</span><span class="sxs-lookup"><span data-stu-id="71262-165">Chroma Formats</span></span>     | <span data-ttu-id="71262-166">4:2:0 Chroma</span><span class="sxs-lookup"><span data-stu-id="71262-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="71262-167">Résolution minimale</span><span class="sxs-lookup"><span data-stu-id="71262-167">Minimum Resolution</span></span> | <span data-ttu-id="71262-168">48 × 48 pixels</span><span class="sxs-lookup"><span data-stu-id="71262-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="71262-169">Résolution maximale</span><span class="sxs-lookup"><span data-stu-id="71262-169">Maximum Resolution</span></span> | <span data-ttu-id="71262-170">4096 × 2304 pixels</span><span class="sxs-lookup"><span data-stu-id="71262-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="71262-171">La résolution maximale garantie pour l’accélération DXVA est de 1920 × 1088 pixels ; à des résolutions supérieures, le décodage s’effectue avec DXVA, s’il est pris en charge par le matériel sous-jacent ; sinon, le décodage est effectué avec le logiciel.</span><span class="sxs-lookup"><span data-stu-id="71262-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="71262-172">DXVA</span><span class="sxs-lookup"><span data-stu-id="71262-172">DXVA</span></span>               | <span data-ttu-id="71262-173">Le décodeur prend en charge DX11 et DX12 DXVA, mais pas DXVA version 2 ou DXVA version 1.</span><span class="sxs-lookup"><span data-stu-id="71262-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="71262-174">Les données d’entrée doivent être conformes à l’annexe B de l’ITU-T H. 265 \| ISO/IEC 23008-2.</span><span class="sxs-lookup"><span data-stu-id="71262-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="71262-175">Les données doivent inclure les codes de début.</span><span class="sxs-lookup"><span data-stu-id="71262-175">The data must include the start codes.</span></span> <span data-ttu-id="71262-176">Le décodeur ignore les octets jusqu’à ce qu’il trouve un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) valides dans le flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="71262-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="71262-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71262-177">Requirements</span></span>



| <span data-ttu-id="71262-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71262-178">Requirement</span></span> | <span data-ttu-id="71262-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="71262-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71262-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71262-180">Minimum supported client</span></span><br/> | <span data-ttu-id="71262-181">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71262-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="71262-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71262-182">Minimum supported server</span></span><br/> | <span data-ttu-id="71262-183">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="71262-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="71262-184">DLL</span><span class="sxs-lookup"><span data-stu-id="71262-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71262-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71262-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71262-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71262-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71262-187">Objets codec</span><span class="sxs-lookup"><span data-stu-id="71262-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
