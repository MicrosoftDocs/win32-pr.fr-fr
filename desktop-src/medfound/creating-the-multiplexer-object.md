---
description: Création de l’objet multiplexeur
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Création de l’objet multiplexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201169"
---
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="2ef0d-103">Création de l’objet multiplexeur</span><span class="sxs-lookup"><span data-stu-id="2ef0d-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="2ef0d-104">Le multiplexeur ASF est un objet de couche WMContainer qui fonctionne avec l' [objet de données ASF](asf-file-structure.md) et donne à une application la possibilité de générer des paquets de données ASF pour les flux de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="2ef0d-105">L’objet multiplexeur expose l’interface [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) .</span><span class="sxs-lookup"><span data-stu-id="2ef0d-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="2ef0d-106">Pour créer le multiplexeur, appelez [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="2ef0d-107">Cette fonction retourne un pointeur vers un objet vide.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="2ef0d-108">Si l’application écrit un nouveau fichier ASF, l’application doit initialiser le multiplexeur avec un objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="2ef0d-109">Pour ce faire, appelez [**IMFASFMultiplexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="2ef0d-110">L’objet ContentInfo spécifié représente l’objet d’en-tête ASF du nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="2ef0d-111">Pour plus d’informations sur la création et l’initialisation de l’objet ContentInfo pour un nouveau fichier, consultez [initialisation de l’objet ContentInfo d’un nouveau fichier ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="2ef0d-112">La méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analyse l’objet ContentInfo pour collecter des informations de configuration de flux, telles que le nombre de flux, la taille de paquet, le préroll.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="2ef0d-113">Éventuellement, le multiplexeur peut également avoir besoin de paramètres de compartiment avec fuite et les unités d’extension de charge utile.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="2ef0d-114">Ces informations sont nécessaires pour générer des paquets de données qui correspondent aux spécifications définies dans l’objet d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="2ef0d-115">La méthode **Initialize** configure le multiplexeur en fonction du type de média et des paramètres de configuration des flux.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="2ef0d-116">Par exemple, si un flux est configuré pour avoir des extensions de charge utile (voir [création et configuration de flux ASF](creating-and-configuring-asf-streams.md)), puis le multiplexeur est configuré pour ajouter ces valeurs aux paquets de données générés.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="2ef0d-117">La méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) obtient également un handle vers l’objet de données initial qui a été créé lors de la création de l’objet ContentInfo en écriture.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="2ef0d-118">Pendant la génération des paquets de données, le multiplexeur ajoute des paquets à l’objet de données et le met à jour de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="2ef0d-119">Une fois que le multiplexeur a généré tous les paquets de données, il met à jour l’objet ContentInfo fourni afin que certaines valeurs, telles que le nombre de paquets de données, soient mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="2ef0d-120">L’exemple de code suivant montre comment créer un multiplexeur et l’initialiser avec un objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



<span data-ttu-id="2ef0d-121">Pour voir cette fonction utilisée dans une application complète, consultez [Didacticiel : copie de flux de fichiers ASF d’un fichier vers un autre](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="2ef0d-122">Initialisation du multiplexeur et paramètres des compartiments de fuite</span><span class="sxs-lookup"><span data-stu-id="2ef0d-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="2ef0d-123">La méthode [**IMFASFMultiplexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configure le multiplexeur pour déterminer le flot de données de compartiments avec fuite.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="2ef0d-124">Pour configurer ces paramètres, assurez-vous que les valeurs de propriété suivantes sont définies sur l’objet ContentInfo spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="2ef0d-125">Pour plus d’informations sur la définition de ces propriétés, consultez [définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="2ef0d-126">[**MFPKEY \_ ASFMEDIASINK propriété \_ \_ vitesse de transmission**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) automatique : indique si le multiplexeur doit ajuster automatiquement la vitesse de transmission, pour maintenir le workflow dans le compartiment avec fuite.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="2ef0d-127">Ce paramètre peut être modifié par l’application en appelant [**IMFASFMultiplexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) et en passant l’indicateur de **\_ vitesse de \_ \_ transmission du multiplexeur MFASF** .</span><span class="sxs-lookup"><span data-stu-id="2ef0d-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="2ef0d-128">[**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) Property : l’heure d’envoi indique quand la charge utile dans le compartiment avec fuite est libérée.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="2ef0d-129">Les heures d’envoi doivent être supérieures ou égales à l’heure de la présentation, car la charge utile doit avoir le temps d’accéder à la destination avant l’heure de la présentation.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="2ef0d-130">Cette valeur de propriété est la première heure d’envoi.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-130">This property value is the first send time.</span></span> <span data-ttu-id="2ef0d-131">Le multiplexeur utilise cette valeur pour calculer les heures d’envoi suivantes afin de s’assurer que les données transitent régulièrement par le compartiment.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="2ef0d-132">Si l’indicateur de **\_ \_ \_ débit binaire MFASF du multiplexeur** est défini sur le multiplexeur, le multiplexeur ajuste la vitesse de transmission afin que la charge utile soit envoyée lorsque la fenêtre de la mémoire tampon est pleine.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="2ef0d-133">Si l’indicateur n’est pas défini, le multiplexeur ne parvient pas à générer des paquets de données en raison d’un dépassement de bande passante.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="2ef0d-134">Le multiplexeur obtient des informations de configuration de flux à partir du profil ASF associé à l’objet ContentInfo spécifié dans la méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) .</span><span class="sxs-lookup"><span data-stu-id="2ef0d-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="2ef0d-135">Les informations de configuration de flux incluent des paramètres de compartiments perdus.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="2ef0d-136">Cette valeur est requise par le multiplexeur pour générer des paquets de données.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="2ef0d-137">Pour spécifier les paramètres de compartiment à fuite, définissez les valeurs de l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) sur l’objet de configuration de flux qui représente le flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="2ef0d-138">Pour utiliser la valeur de la fenêtre de mémoire tampon, qui est utilisée par l’encodeur, appelez [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="2ef0d-139">La valeur réelle de la fenêtre de la mémoire tampon est connue uniquement après la définition du type de média de sortie de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="2ef0d-140">Pour plus d’informations sur la définition du type de média de sortie, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ef0d-141">Les valeurs de compartiment fuites utilisées par l’encodeur peuvent être différentes dans l’objet ContentInfo fourni par le profil ASF utilisé pour créer le multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="2ef0d-142">La méthode [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) met à jour l’objet ContentInfo afin que les valeurs correctes soient reflétées dans l’objet d’en-tête ASF final.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ef0d-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ef0d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ef0d-144">Multiplexeur ASF</span><span class="sxs-lookup"><span data-stu-id="2ef0d-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="2ef0d-145">Génération de nouveaux paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="2ef0d-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
