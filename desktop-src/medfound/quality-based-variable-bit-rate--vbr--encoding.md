---
description: Encodage à vitesse de transmission variable Quality-Based
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Encodage à vitesse de transmission variable Quality-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524944"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="4e056-103">Encodage à vitesse de transmission variable Quality-Based</span><span class="sxs-lookup"><span data-stu-id="4e056-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="4e056-104">Contrairement à l' [encodage à débit binaire constant](constant-bit-rate-encoding.md) (CBR), où l’encodeur s’efforce de maintenir une vitesse de transmission particulière du média encodé, en mode VBR (variable bit rate), l’encodeur s’efforce d’obtenir la meilleure qualité possible du média encodé.</span><span class="sxs-lookup"><span data-stu-id="4e056-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="4e056-105">La principale différence entre CBR et VBR est la taille de la fenêtre de mémoire tampon utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e056-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="4e056-106">Les flux encodés VBR ont généralement des fenêtres de tampon volumineuses par rapport aux flux encodés CBR.</span><span class="sxs-lookup"><span data-stu-id="4e056-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="4e056-107">La qualité du contenu encodé est déterminée par la quantité de données perdues lorsque le contenu est compressé.</span><span class="sxs-lookup"><span data-stu-id="4e056-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="4e056-108">De nombreux facteurs affectent la perte de données dans le processus de compression ; mais en général, plus les données d’origine sont complexes et plus le taux de compression est élevé, plus le processus de compression est détaillé.</span><span class="sxs-lookup"><span data-stu-id="4e056-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="4e056-109">En mode VBR basé sur la qualité, vous ne définissez pas une vitesse de transmission ou une fenêtre de mémoire tampon que l’encodeur doit suivre.</span><span class="sxs-lookup"><span data-stu-id="4e056-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="4e056-110">Au lieu de cela, vous spécifiez un niveau de qualité pour un flux multimédia numérique au lieu d’une vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="4e056-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="4e056-111">L’encodeur compresse le contenu afin que tous les échantillons soient de qualité comparable. Cela garantit la cohérence de la qualité tout au long de la durée de la lecture, indépendamment des exigences de mémoire tampon du flux résultant.</span><span class="sxs-lookup"><span data-stu-id="4e056-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="4e056-112">L’encodage VBR basé sur la qualité tend à créer de grands flux compressés.</span><span class="sxs-lookup"><span data-stu-id="4e056-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="4e056-113">En général, ce type d’encodage est bien adapté à la lecture locale ou aux connexions réseau à bande passante élevée (ou téléchargement et lecture).</span><span class="sxs-lookup"><span data-stu-id="4e056-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="4e056-114">Par exemple, vous pouvez écrire une application pour copier des chansons de fichiers CD vers ASF sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4e056-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="4e056-115">L’utilisation de l’encodage VBR basé sur la qualité garantit que toutes les chansons copiées sont de la même qualité.</span><span class="sxs-lookup"><span data-stu-id="4e056-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="4e056-116">Dans ce cas, la qualité cohérente offre une meilleure expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e056-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="4e056-117">L’inconvénient du codage VBR basé sur la qualité est qu’il n’existe aucun moyen de connaître les exigences de taille ou de bande passante des médias encodés avant la session d’encodage, car l’encodeur utilise une seule passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="4e056-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="4e056-118">Cela peut rendre les fichiers au format VBR basés sur la qualité inappropriés pour les cas où la mémoire ou la bande passante sont restreintes, par exemple pour la lecture de contenu sur des lecteurs multimédias portables ou la diffusion en continu sur un réseau à faible bande passante.</span><span class="sxs-lookup"><span data-stu-id="4e056-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="4e056-119">Configuration de l’encodeur pour l’encodage Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="4e056-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="4e056-120">La configuration de l’encodeur est définie via des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="4e056-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="4e056-121">Ces propriétés sont définies dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="4e056-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="4e056-122">Les propriétés de configuration doivent être définies sur l’encodeur avant de négocier le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="4e056-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="4e056-123">Pour plus d’informations sur la façon de définir des propriétés sur l’encodeur, consultez [configuration de l’encodeur](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4e056-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="4e056-124">La liste suivante répertorie les propriétés que vous devez définir pour ce type d’encodage :</span><span class="sxs-lookup"><span data-stu-id="4e056-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="4e056-125">Spécifiez le mode d’encodage VBR en affectant à la propriété **MFPKEY \_ VBRENABLED** la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="4e056-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="4e056-126">Affectez la valeur 1 à **MFPKEY \_ PASSESUSED** , car ce mode VBR utilise une seule passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="4e056-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="4e056-127">Définissez le niveau de qualité souhaité (de 0 à 100) en définissant la propriété **MFPKEY \_ souhaitée \_ VBRQUALITY** .</span><span class="sxs-lookup"><span data-stu-id="4e056-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="4e056-128">La fonction VBR basée sur la qualité n’encode pas le contenu dans des paramètres de mémoire tampon prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="4e056-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="4e056-129">Ce niveau de qualité sera conservé pour l’ensemble du flux, indépendamment des exigences de vitesse de transmission qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="4e056-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="4e056-130">Pour les flux vidéo, définissez la vitesse de transmission moyenne sur une valeur différente de zéro dans l’attribut de [**\_ vitesse de \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) sur le type de média de sortie de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="4e056-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="4e056-131">La vitesse de transmission exacte est mise à jour une fois la session de codage terminée.</span><span class="sxs-lookup"><span data-stu-id="4e056-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="4e056-132">L’exemple de code suivant montre l’implémentation de SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="4e056-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="4e056-133">Cette fonction définit les propriétés d’encodage de niveau flux pour CBR et VBR.</span><span class="sxs-lookup"><span data-stu-id="4e056-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4e056-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e056-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e056-135">Types d’encodage ASF</span><span class="sxs-lookup"><span data-stu-id="4e056-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



