---
description: Encodage de la vitesse de transmission variable sans contrainte
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Encodage de la vitesse de transmission variable sans contrainte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524986"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="2437e-103">Encodage de la vitesse de transmission variable sans contrainte</span><span class="sxs-lookup"><span data-stu-id="2437e-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="2437e-104">Dans le mode d’encodage VBR (variable bit rate) sans contrainte, le contenu est encodé à la qualité la plus élevée possible tout en conservant une vitesse de transmission spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2437e-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="2437e-105">L’encodage VBR sans contrainte utilise deux passes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="2437e-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="2437e-106">Lorsque vous utilisez l’encodage VBR non restreint, vous spécifiez une vitesse de transmission pour le flux, comme vous le feriez avec un [encodage à débit binaire constant](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="2437e-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="2437e-107">Toutefois, l’encodeur utilise cette valeur uniquement comme la vitesse de transmission moyenne pour le flux et l’encodage afin que la qualité soit aussi élevée que possible tout en conservant la moyenne.</span><span class="sxs-lookup"><span data-stu-id="2437e-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="2437e-108">Les échantillons individuels produits par l’encodeur varient en fonction de la taille sans limite de mémoire tampon explicite.</span><span class="sxs-lookup"><span data-stu-id="2437e-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="2437e-109">Toutefois, la vitesse de transmission moyenne pendant la session d’encodage et la durée du flux ne doivent pas être supérieures à la valeur que vous avez spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2437e-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="2437e-110">La vitesse de transmission réelle à n’importe quel point dans le flux encodé peut varier considérablement de la valeur moyenne.</span><span class="sxs-lookup"><span data-stu-id="2437e-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="2437e-111">Vous ne définissez pas de fenêtre de mémoire tampon pour l’encodage VBR sans contrainte.</span><span class="sxs-lookup"><span data-stu-id="2437e-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="2437e-112">Au lieu de cela, l’encodeur calcule la taille de la fenêtre de mémoire tampon requise en fonction des spécifications des exemples encodés.</span><span class="sxs-lookup"><span data-stu-id="2437e-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="2437e-113">Cela signifie qu’il n’existe aucune limite à la taille des échantillons individuels dans le flux, tant que la vitesse de transmission moyenne est inférieure ou égale à la valeur que vous avez définie.</span><span class="sxs-lookup"><span data-stu-id="2437e-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="2437e-114">L’avantage d’un encodage VBR non restreint est que le flux compressé a la qualité la plus élevée possible tout en restant dans une bande passante moyenne prévisible.</span><span class="sxs-lookup"><span data-stu-id="2437e-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="2437e-115">Utilisez cette valeur lorsque vous devez spécifier une bande passante, mais que des fluctuations autour de la bande passante spécifiée sont acceptables. par exemple, pour les fichiers locaux ou uniquement pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2437e-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="2437e-116">L’inconvénient de ce mode de codage est que l’encodeur peut définir la fenêtre de mémoire tampon sur la valeur requise après l’encodage, ce qui vous permet de contrôler la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2437e-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="2437e-117">Dans la plupart des cas, si vous ne vous inquiétez pas de la taille de la mémoire tampon ou de la cohérence de l’utilisation de la bande passante, vous devez utiliser l' [encodage de la vitesse de transmission variable basée sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="2437e-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="2437e-118">Configuration de l’encodeur pour le VBR non restreint</span><span class="sxs-lookup"><span data-stu-id="2437e-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="2437e-119">La configuration de l’encodeur est définie via des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="2437e-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="2437e-120">Ces propriétés sont définies dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="2437e-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="2437e-121">Les propriétés de configuration doivent être définies sur l’encodeur avant de négocier le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="2437e-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="2437e-122">Pour plus d’informations sur la façon de définir des propriétés sur l’encodeur, consultez [configuration de l’encodeur](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2437e-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="2437e-123">En fonction des valeurs de propriété spécifiées, vous pouvez énumérer les types de sortie VBR pris en charge et sélectionner celui qui est requis sur l’encodeur [Media Foundation transformer](media-foundation-transforms.md) (MFT) en fonction de la vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="2437e-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="2437e-124">La liste suivante répertorie les propriétés que vous devez définir pour ce type d’encodage :</span><span class="sxs-lookup"><span data-stu-id="2437e-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="2437e-125">Spécifiez le mode d’encodage VBR en affectant \_ à la propriété MFPKEY VBRENABLED la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="2437e-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="2437e-126">Affectez la valeur \_ 2 à MFPKEY PASSESUSED, car le mode VBR sans contrainte utilise deux passes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="2437e-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="2437e-127">Lors de l’énumération du type de média de sortie, vérifiez l’attribut [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde des octets audio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (pour les flux audio) ou l’attribut vitesse de [**\_ \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) (pour les flux vidéo) des types de supports de sortie disponibles.</span><span class="sxs-lookup"><span data-stu-id="2437e-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="2437e-128">Choisissez un type de média de sortie dont le débit moyen est le plus proche de la vitesse de transmission moyenne souhaitée que vous souhaitez que l’encodeur conserve dans le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="2437e-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="2437e-129">Pour plus d’informations sur la sélection du type de média de sortie, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2437e-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="2437e-130">Pour faire en sorte que la valeur de la fenêtre de mémoire tampon soit définie par l’encodeur, appelez **IWMCodecLeakyBucket :: GetBufferSizeBits**, défini dans wmcodecifaces. h et wmcodecdspuuid. lib, après la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="2437e-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="2437e-131">Pour ajouter une prise en charge VBR sans contrainte pour les flux, vous devez définir cette valeur dans l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valeurs de compartiment de fuite moyenne) sur l’objet de configuration de flux lors de la configuration du profil ASF.</span><span class="sxs-lookup"><span data-stu-id="2437e-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="2437e-132">La commande suivante modifie la méthode SetEncodingType de l’exemple de classe CEncoder pour configurer le mode VBR sans contrainte.</span><span class="sxs-lookup"><span data-stu-id="2437e-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="2437e-133">Pour plus d’informations sur cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="2437e-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="2437e-134">Pour plus d’informations sur les macros d’assistance utilisées dans cet exemple, consultez Utilisation des exemples de code Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2437e-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="2437e-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2437e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2437e-136">Types d’encodage ASF</span><span class="sxs-lookup"><span data-stu-id="2437e-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="2437e-137">Modèle de mémoire tampon de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="2437e-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="2437e-138">Comment créer une topologie pour Two-Pass l’encodage Windows Media</span><span class="sxs-lookup"><span data-stu-id="2437e-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



