---
description: 'Dans la vitesse de transmission variable (VBR), le contenu est encodé à une vitesse de transmission et à des valeurs maximales spécifiées : une vitesse de transmission maximale et une fenêtre de mémoire tampon de pointe.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Encodage à vitesse de transmission variable Peak-Constrained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520428"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="6abec-103">Encodage à vitesse de transmission variable Peak-Constrained</span><span class="sxs-lookup"><span data-stu-id="6abec-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="6abec-104">Dans la vitesse de transmission variable (VBR), le contenu est encodé à une vitesse de transmission et à des *valeurs maximales* spécifiées : une vitesse de transmission maximale et une fenêtre de mémoire tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="6abec-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="6abec-105">Ces valeurs de pic sont également appelées les *valeurs de plage de pics de fuites*.</span><span class="sxs-lookup"><span data-stu-id="6abec-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="6abec-106">Le fichier est encodé pour se conformer à une mémoire tampon décrite par les valeurs de pic, de sorte que la vitesse de transmission moyenne globale du flux est égale ou inférieure à la valeur de vitesse de transmission moyenne que vous avez spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6abec-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="6abec-107">En règle générale, le taux binaire de pointe est assez élevé.</span><span class="sxs-lookup"><span data-stu-id="6abec-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="6abec-108">L’encodeur garantit que la valeur de la vitesse de transmission moyenne spécifiée est conservée pendant la durée du flux (vitesse de transmission moyenne >= (taille totale du flux en bits/durée en secondes)).</span><span class="sxs-lookup"><span data-stu-id="6abec-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="6abec-109">Prenons l’exemple suivant : vous configurez un flux avec une vitesse de transmission moyenne de 16 000 bits par seconde, un taux de bits de pic de 48 000 bits par seconde et une fenêtre de mémoire tampon de pointe de 3 000 (3 secondes).</span><span class="sxs-lookup"><span data-stu-id="6abec-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="6abec-110">La taille de la mémoire tampon utilisée pour le flux est de 144 000 bits (48 000 bits par seconde \* 3 secondes), comme déterminé par les valeurs de pic.</span><span class="sxs-lookup"><span data-stu-id="6abec-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="6abec-111">L’encodeur compresse les données pour se conformer à cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6abec-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="6abec-112">En outre, la vitesse de transmission moyenne du flux doit être inférieure ou égale à 16 000.</span><span class="sxs-lookup"><span data-stu-id="6abec-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="6abec-113">Si l’encodeur doit créer des échantillons de grande taille pour gérer un segment de contenu complexe, il peut tirer parti de la grande taille de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6abec-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="6abec-114">Toutefois, d’autres parties du flux doivent être encodées à une vitesse de transmission inférieure pour ramener la moyenne au niveau spécifié.</span><span class="sxs-lookup"><span data-stu-id="6abec-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="6abec-115">L’encodage VBR maximal limité est utile pour les périphériques de lecture avec une capacité de mémoire tampon finie et des contraintes de débit de données.</span><span class="sxs-lookup"><span data-stu-id="6abec-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="6abec-116">Un exemple courant est l’encodage utilisé pour les DVD quand le décodage est effectué par une puce dans un appareil, où des limitations matérielles doivent être prises en compte.</span><span class="sxs-lookup"><span data-stu-id="6abec-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="6abec-117">Configuration de l’encodeur pour Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="6abec-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="6abec-118">Le VBR limité au maximum est comme un VBR non [restreint](unconstrained-variable-bit-rate--vbr--encoding.md) en ce qu’il est limité à un débit binaire moyen sur la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="6abec-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="6abec-119">En outre, le VBR maximal restreint est conforme à une mémoire tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="6abec-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="6abec-120">Cette mémoire tampon est décrite à l’aide d’une vitesse de pointe et d’une fenêtre de tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="6abec-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="6abec-121">Ce mode utilise deux passes d’encodage et donne à l’encodeur la flexibilité nécessaire pour coder les exemples individuels tout en adhérant aux limitations de pointe.</span><span class="sxs-lookup"><span data-stu-id="6abec-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="6abec-122">La configuration de l’encodeur est définie via des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="6abec-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="6abec-123">Ces propriétés sont définies dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="6abec-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="6abec-124">Les propriétés de configuration doivent être définies sur l’encodeur avant de négocier le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="6abec-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="6abec-125">Pour plus d’informations sur la façon de définir des propriétés sur l’encodeur, consultez [configuration de l’encodeur](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6abec-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="6abec-126">En fonction des valeurs de propriété spécifiées, vous pouvez énumérer les types de sortie VBR pris en charge et sélectionner celui qui est requis sur l’encodeur [Media Foundation transformer](media-foundation-transforms.md) (MFT) en fonction de la vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="6abec-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="6abec-127">Vous devez définir les Propertiesfor suivants pour ce type d’encodage :</span><span class="sxs-lookup"><span data-stu-id="6abec-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="6abec-128">Spécifiez le mode d’encodage VBR en affectant \_ à la propriété MFPKEY VBRENABLED la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="6abec-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="6abec-129">Affectez la valeur \_ 2 à MFPKEY PASSESUSED, car le mode VBR avec un pic restreint utilise deux passes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6abec-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="6abec-130">Définissez MFPKEY \_ Rmax pour spécifier la vitesse de transmission maximale et définissez MFPKEY \_ BMAX pour spécifier la fenêtre de mémoire tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="6abec-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="6abec-131">Lors de l’énumération du type de média de sortie, vérifiez l’attribut [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) (pour les flux audio) et le débit moyen des signaux audio (pour les flux vidéo) de sortie, puis choisissez un type de média de sortie dont le débit moyen est le plus proche de la vitesse de transmission moyenne souhaitée que l’encodeur doit conserver dans le contenu encodé. [**\_ \_ \_**](mf-mt-avg-bitrate-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="6abec-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="6abec-132">Pour plus d’informations sur la sélection du type de média de sortie, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6abec-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="6abec-133">Il est recommandé de définir le taux de bits de pointe sur au moins deux fois la vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="6abec-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="6abec-134">Le fait de définir le taux de pic sur une valeur inférieure peut entraîner l’encodeur à encoder le contenu sous la forme d’un CBR à deux passes au lieu du VBR avec un pic restreint.</span><span class="sxs-lookup"><span data-stu-id="6abec-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="6abec-135">Pour récupérer la valeur de la fenêtre de mémoire tampon définie par l’encodeur, appelez **IWMCodecLeakyBucket :: GetBufferSizeBits**, défini dans wmcodecifaces. h, wmcodecdspuuid. lib, après la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6abec-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="6abec-136">Pour ajouter une prise en charge VBR sans contrainte pour les flux, vous devez définir cette valeur dans l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valeurs de compartiment avec fuite de pic) sur l’objet de configuration de flux lors de la configuration du profil ASF.</span><span class="sxs-lookup"><span data-stu-id="6abec-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="6abec-137">L’exemple de code suivant modifie la méthode SetEncodingType de l’exemple de classe CEncoder pour configurer le mode VBR avec des pics de charge.</span><span class="sxs-lookup"><span data-stu-id="6abec-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="6abec-138">Pour plus d’informations sur cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="6abec-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="6abec-139">Pour plus d’informations sur les macros d’assistance utilisées dans cet exemple, consultez Utilisation des exemples de code Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6abec-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="6abec-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6abec-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6abec-141">Types d’encodage ASF</span><span class="sxs-lookup"><span data-stu-id="6abec-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="6abec-142">Modèle de mémoire tampon de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="6abec-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="6abec-143">Comment créer une topologie pour Two-Pass l’encodage Windows Media</span><span class="sxs-lookup"><span data-stu-id="6abec-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



