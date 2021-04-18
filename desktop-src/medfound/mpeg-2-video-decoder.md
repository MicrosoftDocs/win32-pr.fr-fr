---
description: Le décodeur vidéo MPEG-2 est une transformation de Media Foundation qui décode la vidéo MPEG-1 et MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Décodeur vidéo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527903"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="8fe1b-103">Décodeur vidéo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8fe1b-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="8fe1b-104">Le décodeur vidéo MPEG-2 est une [transformation de Media Foundation](media-foundation-transforms.md) qui décode la vidéo MPEG-1 et MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="8fe1b-105">Le décodeur prend en charge la vidéo de profil simple et MPEG-2 (H. 262, ISO/IEC 13818-2) et MPEG-1 Video (ISO/IEC 11172-2).</span><span class="sxs-lookup"><span data-stu-id="8fe1b-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="8fe1b-106">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="8fe1b-106">Input Types</span></span>

<span data-ttu-id="8fe1b-107">Le décodeur prend en charge les types de média d’entrée suivants.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="8fe1b-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="8fe1b-108">Attribute</span></span>                                                 | <span data-ttu-id="8fe1b-109">Description</span><span class="sxs-lookup"><span data-stu-id="8fe1b-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="8fe1b-110">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="8fe1b-111">**\_Vidéo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="8fe1b-112">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="8fe1b-113">**MFVideoFormat \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="8fe1b-114">**MFVideoFormat \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="8fe1b-115">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="8fe1b-115">Output Types</span></span>

<span data-ttu-id="8fe1b-116">Le décodeur prend en charge les types de sortie suivants.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="8fe1b-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="8fe1b-117">Attribute</span></span>                                                 | <span data-ttu-id="8fe1b-118">Description</span><span class="sxs-lookup"><span data-stu-id="8fe1b-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fe1b-119">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="8fe1b-120">**\_Vidéo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="8fe1b-121">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="8fe1b-122">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="8fe1b-123">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="8fe1b-124">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="8fe1b-125">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="8fe1b-126">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8fe1b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="8fe1b-127">Remarks</span></span>

<span data-ttu-id="8fe1b-128">Le décodeur vidéo MPEG-2 expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="8fe1b-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="8fe1b-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="8fe1b-130">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="8fe1b-131">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="8fe1b-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="8fe1b-133">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="8fe1b-134">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="8fe1b-135">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="8fe1b-136">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="8fe1b-137">L’entrée du décodeur doit être un flux élémentaire.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="8fe1b-138">La résolution maximale prise en charge est de 1920 × 1088 pixels.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="8fe1b-139">Le décodeur prend en charge l’accélération vidéo DirectX (DXVA) à l’aide de Microsoft Direct3D 9 ou Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="8fe1b-140">Modes de décodage spéciaux</span><span class="sxs-lookup"><span data-stu-id="8fe1b-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="8fe1b-141">**Mode de latence faible.**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-141">**Low latency mode.**</span></span> <span data-ttu-id="8fe1b-142">Ce mode est approprié pour des scénarios tels que les communications en temps réel.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="8fe1b-143">Cela réduit la latence de démarrage, de sorte que le décodeur produit le premier exemple de sortie plus tôt.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="8fe1b-144">Toutefois, le décodeur met en mémoire tampon moins d’échantillons dans ce mode, ce qui peut potentiellement entraîner des problèmes, car le décodeur ne décode pas autant de frames à l’avance.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="8fe1b-145">Pour activer le mode de faible latence, définissez l’attribut [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe1b-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="8fe1b-146">**Cherche.**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-146">**Seeking.**</span></span> <span data-ttu-id="8fe1b-147">Pour obtenir une recherche précise, appelez la méthode [**IMFTransform :: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) .</span><span class="sxs-lookup"><span data-stu-id="8fe1b-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="8fe1b-148">Lorsque cette méthode est appelée, le décodeur génère uniquement les trames qui se trouvent dans la plage d’horodatage spécifiée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="8fe1b-149">**Mode de génération de miniatures**.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="8fe1b-150">Ce mode est conçu pour la génération rapide d’images miniatures.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="8fe1b-151">Dans ce mode, le décodeur décode initialement uniquement les images I.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="8fe1b-152">Si aucun frame I n’est trouvé dans un certain nombre de frames, le décodeur commence à décoder les frames P et sort les trames non-I à un intervalle fixe (un par *N* images) jusqu’à ce qu’une image i soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="8fe1b-153">Pour activer le mode de génération de miniatures, définissez la propriété [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe1b-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="8fe1b-154">**Astuce.**</span><span class="sxs-lookup"><span data-stu-id="8fe1b-154">**Trick play.**</span></span> <span data-ttu-id="8fe1b-155">Le décodeur peut décoder à des vitesses plus rapides que le temps réel.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="8fe1b-156">À des vitesses de lecture plus élevées, le décodeur passe au décodage uniquement des trames.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="8fe1b-157">Pour la lecture inversée, seules les trames sont décodées.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="8fe1b-158">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="8fe1b-158">Codec Properties</span></span>

<span data-ttu-id="8fe1b-159">Le décodeur prend en charge les propriétés suivantes par le biais de la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="8fe1b-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="8fe1b-160">Propriété</span><span class="sxs-lookup"><span data-stu-id="8fe1b-160">Property</span></span>                                                                                                      | <span data-ttu-id="8fe1b-161">Description</span><span class="sxs-lookup"><span data-stu-id="8fe1b-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fe1b-162">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="8fe1b-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="8fe1b-163">Active ou désactive le mode de génération de miniatures.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="8fe1b-164">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="8fe1b-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="8fe1b-165">Active ou désactive le décodage à accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="8fe1b-166">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="8fe1b-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="8fe1b-167">Active ou désactive le mode faible latence.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="8fe1b-168">le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ ordre natif</span><span class="sxs-lookup"><span data-stu-id="8fe1b-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="8fe1b-169">Spécifie si le décodeur expose des types de sortie qui conviennent au transcodage avant d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="8fe1b-170">Parmi ces propriétés, vous pouvez également définir les éléments suivants à l’aide de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="8fe1b-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="8fe1b-171">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="8fe1b-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="8fe1b-172">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="8fe1b-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="8fe1b-173">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="8fe1b-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="8fe1b-174">Limites</span><span class="sxs-lookup"><span data-stu-id="8fe1b-174">Limitations</span></span>

-   <span data-ttu-id="8fe1b-175">Le décodeur n’est pas pris en charge sur les plateformes IA-64.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="8fe1b-176">Le décodeur ne prend pas en charge le déchiffrement CSS ou la lecture des DVD chiffrés.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe1b-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe1b-177">Requirements</span></span>



| <span data-ttu-id="8fe1b-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe1b-178">Requirement</span></span> | <span data-ttu-id="8fe1b-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe1b-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe1b-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe1b-180">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe1b-181">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe1b-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8fe1b-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe1b-182">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe1b-183">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe1b-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8fe1b-184">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe1b-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe1b-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe1b-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe1b-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe1b-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe1b-187">Objets codec</span><span class="sxs-lookup"><span data-stu-id="8fe1b-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
