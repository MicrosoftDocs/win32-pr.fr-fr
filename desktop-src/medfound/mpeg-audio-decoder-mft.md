---
description: Le décodeur audio Microsoft MPEG est une transformation de Media Foundation synchrone (MFT) qui permet de décoder des formats de flux élémentaires MPEG Audio à l’aide du pipeline Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Décodeur audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951483"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="9a9d4-103">Décodeur audio MPEG</span><span class="sxs-lookup"><span data-stu-id="9a9d4-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="9a9d4-104">Le décodeur audio Microsoft MPEG est une [transformation de Media Foundation](media-foundation-transforms.md) synchrone (MFT) qui permet de décoder des formats de flux élémentaires MPEG Audio à l’aide du pipeline Media Foundation (MF).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="9a9d4-105">Le décodeur prend en charge les formats de flux élémentaires MPEG suivants.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="9a9d4-106">MPEG-1 audio Layers I et II (ISO/IEC 11172-3).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="9a9d4-107">2.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-107">2.</span></span> <span data-ttu-id="9a9d4-108">MPEG-2 à compatibilité descendante, couches I et II (ISO</span><span class="sxs-lookup"><span data-stu-id="9a9d4-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="9a9d4-109">MPEG-2 à compatibilité descendante, couches I et II (ISO/IEC 13818-3), mono et stéréo uniquement</span><span class="sxs-lookup"><span data-stu-id="9a9d4-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="9a9d4-110">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="9a9d4-110">Class Identifier</span></span>

<span data-ttu-id="9a9d4-111">L’identificateur de classe (CLSID) du décodeur audio MPEG est **CLSID \_ MSMPEGAudDecMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="9a9d4-112">Types de médias d’entrée</span><span class="sxs-lookup"><span data-stu-id="9a9d4-112">Input Media Types</span></span>

<span data-ttu-id="9a9d4-113">Le décodeur audio MPEG prend en charge les attributs de type de média d’entrée suivants.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="9a9d4-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="9a9d4-114">Attribute</span></span>                                                                               | <span data-ttu-id="9a9d4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a9d4-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a9d4-116">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="9a9d4-117">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="9a9d4-118">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="9a9d4-119">**\_MPEG MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="9a9d4-120">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="9a9d4-121">Facultatif Habituellement 1 pour mono ou 2 pour stéréo, il peut y avoir jusqu’à 6 canaux.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="9a9d4-122">**\_masque de \_ \_ canal audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="9a9d4-123">Facultatif En général, 0x4 pour mono ou 0x3 pour stéréo, mais peut également être l’un des masques de canal associés à 6 canaux (3/2/1, 3/2, 3/1, 2/2, 2/1).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="9a9d4-124">Si elle est présente, le masque de canal doit être cohérent avec le nombre d’entrée spécifié de canaux.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="9a9d4-125">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="9a9d4-126">Facultatif L’un des éléments suivants : 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="9a9d4-127">S’il est spécifié, le taux d’échantillonnage d’entrée doit être l’un des taux d’échantillonnage MPEG valides.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="9a9d4-128">Types de médias de sortie</span><span class="sxs-lookup"><span data-stu-id="9a9d4-128">Output Media Types</span></span>

<span data-ttu-id="9a9d4-129">Le décodeur audio MPEG prend en charge jusqu’à quatre sous-types de médias de sortie, dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="9a9d4-130">Stéréo, virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="9a9d4-131">Stéréo, PCM 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="9a9d4-132">Mono, à virgule flottante (uniquement si l’entrée est mono ou double mono).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="9a9d4-133">Mono, PCM 16 bits (uniquement si l’entrée est mono ou double mono).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="9a9d4-134">Le décodeur prend toujours en charge la sortie stéréo et il est énuméré comme premier type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="9a9d4-135">Le décodeur prend en charge les attributs de type de média de sortie suivants.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="9a9d4-136">Attribut</span><span class="sxs-lookup"><span data-stu-id="9a9d4-136">Attribute</span></span>                                                                           | <span data-ttu-id="9a9d4-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a9d4-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="9a9d4-138">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="9a9d4-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="9a9d4-139">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="9a9d4-140">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="9a9d4-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="9a9d4-141">**MFAudioFormat \_ PCM** ou **MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="9a9d4-142">\_bits de \_ sortie audio MF \_ \_ par \_ échantillon</span><span class="sxs-lookup"><span data-stu-id="9a9d4-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="9a9d4-143">16 ou 32</span><span class="sxs-lookup"><span data-stu-id="9a9d4-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="9a9d4-144">\_canaux de \_ \_ numéros audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="9a9d4-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="9a9d4-145">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="9a9d4-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="9a9d4-146">\_masque de \_ \_ canal audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="9a9d4-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="9a9d4-147">0x4 pour mono ou 0x3 pour stéréo</span><span class="sxs-lookup"><span data-stu-id="9a9d4-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="9a9d4-148">\_ \_ échantillons audio MF \_ MT \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="9a9d4-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="9a9d4-149">L’un des éléments suivants : 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="9a9d4-150">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="9a9d4-150">Transform Attributes</span></span>

<span data-ttu-id="9a9d4-151">Le décodeur audio MPEG implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="9a9d4-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="9a9d4-152">Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="9a9d4-153">Attribut</span><span class="sxs-lookup"><span data-stu-id="9a9d4-153">Attribute</span></span>                                                                               | <span data-ttu-id="9a9d4-154">Description</span><span class="sxs-lookup"><span data-stu-id="9a9d4-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a9d4-155">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="9a9d4-156">Spécifie si le contenu audio à 2 canaux en cours de décodage est double mono ou non.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="9a9d4-157">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-157">Read-only.</span></span> <span data-ttu-id="9a9d4-158">Défini par la table MFT.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-158">Set by the MFT.</span></span> <span data-ttu-id="9a9d4-159">Pour plus d’informations, consultez [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="9a9d4-160">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="9a9d4-161">Spécifie comment le décodeur reproduit un double audio mono.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="9a9d4-162">La valeur par défaut **est \_ eAVDecAudioDualMonoReproMode \_ mono gauche**.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="9a9d4-163">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-163">Read/Write.</span></span> <span data-ttu-id="9a9d4-164">Les applications peuvent définir cette propriété pour modifier le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="9a9d4-165">Pour plus d’informations, consultez [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="9a9d4-166">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="9a9d4-167">Spécifie la vitesse de transmission de flux compressée.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="9a9d4-168">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-168">Read-only.</span></span> <span data-ttu-id="9a9d4-169">Défini par la table MFT.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="9a9d4-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a9d4-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9d4-171">Objets codec</span><span class="sxs-lookup"><span data-stu-id="9a9d4-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
