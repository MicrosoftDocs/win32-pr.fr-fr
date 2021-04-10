---
description: Encodage à vitesse binaire constante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Encodage à vitesse binaire constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950900"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="73ad7-103">Encodage à vitesse binaire constante</span><span class="sxs-lookup"><span data-stu-id="73ad7-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="73ad7-104">Dans l’encodage CBR (constant bit rate), l’encodeur connaît la vitesse de transmission des échantillons de média de sortie et la fenêtre de mémoire tampon (paramètres de compartiment avec fuite) avant le début de la session de codage.</span><span class="sxs-lookup"><span data-stu-id="73ad7-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="73ad7-105">L’encodeur utilise le même nombre de bits pour encoder chaque seconde de l’échantillon tout au long de la durée du fichier pour atteindre la vitesse de transmission cible d’un flux.</span><span class="sxs-lookup"><span data-stu-id="73ad7-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="73ad7-106">Cela limite la variation de la taille des exemples de flux.</span><span class="sxs-lookup"><span data-stu-id="73ad7-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="73ad7-107">En outre, pendant la session d’encodage, la vitesse de transmission n’est pas exactement à la valeur spécifiée, mais reste proche de la vitesse de transmission cible.</span><span class="sxs-lookup"><span data-stu-id="73ad7-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="73ad7-108">L'encodage en mode CBR est utile quand vous voulez connaître le débit binaire ou la durée approximative d'un fichier sans analyser le fichier complet.</span><span class="sxs-lookup"><span data-stu-id="73ad7-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="73ad7-109">Ceci est requis dans les scénarios de diffusion en continu dans lesquels le contenu multimédia doit être diffusé à un débit binaire prévisible et avec une utilisation cohérente de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="73ad7-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="73ad7-110">L’inconvénient de l’encodage CBR est que la qualité du contenu encodé n’est pas constante.</span><span class="sxs-lookup"><span data-stu-id="73ad7-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="73ad7-111">Étant donné que le contenu est plus difficile à compresser, les parties d’un flux CBR auront une qualité inférieure à celle des autres.</span><span class="sxs-lookup"><span data-stu-id="73ad7-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="73ad7-112">Par exemple, un film classique présente des scènes relativement statiques et des scènes qui sont pleines d’actions.</span><span class="sxs-lookup"><span data-stu-id="73ad7-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="73ad7-113">Si vous encodez un film à l’aide de CBR, les scènes qui sont statiques et, par conséquent, faciles à coder efficacement, présentent une qualité supérieure à celle des scènes d’action, ce qui aurait nécessité des tailles d’échantillonnage supérieures pour maintenir la même qualité.</span><span class="sxs-lookup"><span data-stu-id="73ad7-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="73ad7-114">En général, les variations de la qualité d’un fichier CBR sont plus prononcées à des vitesses de transmission inférieures.</span><span class="sxs-lookup"><span data-stu-id="73ad7-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="73ad7-115">À des vitesses de transmission supérieures, la qualité d’un fichier encodé CBR continuera à varier, mais les problèmes de qualité seront moins perceptibles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="73ad7-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="73ad7-116">Lorsque vous utilisez l’encodage CBR, vous devez définir la bande passante aussi élevée que possible.</span><span class="sxs-lookup"><span data-stu-id="73ad7-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="73ad7-117">Paramètres de configuration CBR</span><span class="sxs-lookup"><span data-stu-id="73ad7-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="73ad7-118">Paramètres de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="73ad7-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="73ad7-119">Paramètres de configuration CBR</span><span class="sxs-lookup"><span data-stu-id="73ad7-119">CBR Configuration Settings</span></span>

<span data-ttu-id="73ad7-120">Vous devez configurer un encodeur en spécifiant le type d’encodage et les différents paramètres spécifiques au flux avant la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="73ad7-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="73ad7-121">**Pour configurer l’encodeur pour l’encodage CBR**</span><span class="sxs-lookup"><span data-stu-id="73ad7-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="73ad7-122">Spécifiez le mode d’encodage CBR.</span><span class="sxs-lookup"><span data-stu-id="73ad7-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="73ad7-123">Par défaut, l’encodeur est configuré pour utiliser l’encodage CBR.</span><span class="sxs-lookup"><span data-stu-id="73ad7-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="73ad7-124">La configuration de l’encodeur est définie via des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="73ad7-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="73ad7-125">Ces propriétés sont définies dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="73ad7-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="73ad7-126">Vous pouvez spécifier explicitement ce mode en affectant à la propriété [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la \_ valeur variant false.</span><span class="sxs-lookup"><span data-stu-id="73ad7-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="73ad7-127">Pour plus d’informations sur la façon de définir des propriétés sur des encodeurs, consultez [configuration de l'](configuring-the-encoder.md)encodeur.</span><span class="sxs-lookup"><span data-stu-id="73ad7-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="73ad7-128">Choisissez la vitesse de transmission du codage.</span><span class="sxs-lookup"><span data-stu-id="73ad7-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="73ad7-129">Pour l’encodage CBR, vous devez connaître la vitesse de transmission à laquelle vous souhaitez encoder le flux avant le début de la session de codage.</span><span class="sxs-lookup"><span data-stu-id="73ad7-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="73ad7-130">Vous devez définir la vitesse de transmission pendant que vous configurez l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="73ad7-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="73ad7-131">Pour ce faire, pendant que vous effectuez la négociation de type de média, vérifiez l’attribut [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) du type de données audio MF MT (pour les flux audio) ou la vitesse moyenne (pour les flux vidéo) des types de médias de sortie disponibles, puis choisissez un type de média de sortie dont le débit moyen est le plus proche de la vitesse de transmission cible. [**\_ \_ \_**](mf-mt-avg-bitrate-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="73ad7-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="73ad7-132">Pour plus d’informations, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="73ad7-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="73ad7-133">L’exemple de code suivant montre l’implémentation de SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="73ad7-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="73ad7-134">Cette fonction définit les propriétés d’encodage de niveau flux pour CBR et VBR.</span><span class="sxs-lookup"><span data-stu-id="73ad7-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="73ad7-135">Paramètres de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="73ad7-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="73ad7-136">Pour l’encodage CBR, la moyenne et les valeurs maximales de compartiment avec fuites pour le flux sont identiques.</span><span class="sxs-lookup"><span data-stu-id="73ad7-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="73ad7-137">Pour plus d’informations sur ces paramètres, consultez [le modèle de tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="73ad7-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="73ad7-138">Pour encoder des flux audio CBR, vous devez définir les valeurs des compartiments de fuites après avoir négocié le type de média de sortie sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="73ad7-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="73ad7-139">L’encodeur calcule la fenêtre de mémoire tampon en interne en fonction de la vitesse de transmission moyenne définie sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="73ad7-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="73ad7-140">Pour définir des valeurs de compartiment fuites, créez un tableau de DWORDs. vous pouvez définir les valeurs suivantes dans la propriété [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigée \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) dans la Banque de propriétés du récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="73ad7-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="73ad7-141">Pour plus d’informations, consultez [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="73ad7-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="73ad7-142">Vitesse de transmission moyenne : obtient la vitesse de transmission moyenne à partir du type de média de sortie sélectionné lors de la négociation de type de média.</span><span class="sxs-lookup"><span data-stu-id="73ad7-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="73ad7-143">Utilisez l' [**attribut \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de l’entrée de données audio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="73ad7-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="73ad7-144">Fenêtre de mémoire tampon : interrogez l’encodeur pour l’interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) , puis appelez [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).</span><span class="sxs-lookup"><span data-stu-id="73ad7-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="73ad7-145">Taille de la mémoire tampon initiale : définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="73ad7-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73ad7-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73ad7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73ad7-147">Types d’encodage ASF</span><span class="sxs-lookup"><span data-stu-id="73ad7-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="73ad7-148">Didacticiel : 1-passer l’encodage Windows Media</span><span class="sxs-lookup"><span data-stu-id="73ad7-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="73ad7-149">Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR</span><span class="sxs-lookup"><span data-stu-id="73ad7-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
