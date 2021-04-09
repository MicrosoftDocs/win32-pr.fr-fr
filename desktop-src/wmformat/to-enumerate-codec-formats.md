---
title: Pour énumérer les formats de codec
description: Pour énumérer les formats de codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- flux, énumération des formats de codec
- codecs, énumérations
- flux, formats de codec
- codecs, formats
- codecs, interface IWMCodecInfo
- IWMCodecInfo, formats de codec
- codecs, interface IWMCodecInfo3
- IWMCodecInfo3, formats de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030926"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="52edf-111">Pour énumérer les formats de codec</span><span class="sxs-lookup"><span data-stu-id="52edf-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="52edf-112">Un format de codec est un objet de configuration de flux rempli avec les données d’un codec.</span><span class="sxs-lookup"><span data-stu-id="52edf-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="52edf-113">Chaque format de codec contient une configuration de média prise en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="52edf-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="52edf-114">La plupart des codecs audio prennent en charge un nombre fini de formats, chacun d’entre eux étant énuméré par le codec et accessible à l’aide des méthodes de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span><span class="sxs-lookup"><span data-stu-id="52edf-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="52edf-115">En revanche, les codecs vidéo ne fournissent qu’un seul format.</span><span class="sxs-lookup"><span data-stu-id="52edf-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="52edf-116">Cela est dû au fait que les flux vidéo ont des variables, comme la taille du cadre, qui sont plus flexibles que les paramètres d’un flux audio.</span><span class="sxs-lookup"><span data-stu-id="52edf-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="52edf-117">Avec un flux vidéo, vous devez remplir certaines des valeurs de configuration de flux. les configurations de flux audio ne doivent être modifiées que pour assigner un nom, un nom de connexion et un numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="52edf-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="52edf-118">Pour plus d’informations, consultez [configuration commune à tous les flux](configuration-common-to-all-streams.md).</span><span class="sxs-lookup"><span data-stu-id="52edf-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="52edf-119">Les formats de codec énumérés dépendent des paramètres d’énumération de codec actuels, qui sont définis à l’aide de [**IWMCodecInfo3 :: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span><span class="sxs-lookup"><span data-stu-id="52edf-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="52edf-120">Seules deux propriétés de codec sont actuellement prises en charge : g \_ wszNumPasses, qui spécifie le nombre de passes d’encodage effectuées par le codec et g \_ wszVBREnabled, qui spécifie si le codec utilise l’encodage à vitesse de transmission variable.</span><span class="sxs-lookup"><span data-stu-id="52edf-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="52edf-121">Le nombre maximal de passes d’encodage pris en charge par l’un des codecs est de deux. il existe donc quatre configurations distinctes pour lesquelles vous pouvez récupérer des codecs, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="52edf-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|                  | <span data-ttu-id="52edf-122">Flux CBR (constant bit rate)</span><span class="sxs-lookup"><span data-stu-id="52edf-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="52edf-123">2-passer le flux CBR</span><span class="sxs-lookup"><span data-stu-id="52edf-123">2-pass CBR stream</span></span> | <span data-ttu-id="52edf-124">Débit binaire variable (VBR) basé sur la qualité</span><span class="sxs-lookup"><span data-stu-id="52edf-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="52edf-125">Flux VBR basé sur la fréquence de bits (contraint ou non contraint)</span><span class="sxs-lookup"><span data-stu-id="52edf-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="52edf-126">\_wszVBREnabled g</span><span class="sxs-lookup"><span data-stu-id="52edf-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="52edf-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="52edf-127">FALSE</span></span>                          | <span data-ttu-id="52edf-128">false</span><span class="sxs-lookup"><span data-stu-id="52edf-128">FALSE</span></span>             | <span data-ttu-id="52edf-129">VRAI</span><span class="sxs-lookup"><span data-stu-id="52edf-129">TRUE</span></span>                                         | <span data-ttu-id="52edf-130">TRUE</span><span class="sxs-lookup"><span data-stu-id="52edf-130">TRUE</span></span>                                                     |
| <span data-ttu-id="52edf-131">\_wszNumPasses g</span><span class="sxs-lookup"><span data-stu-id="52edf-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="52edf-132">1</span><span class="sxs-lookup"><span data-stu-id="52edf-132">1</span></span>                              | <span data-ttu-id="52edf-133">2</span><span class="sxs-lookup"><span data-stu-id="52edf-133">2</span></span>                 | <span data-ttu-id="52edf-134">1</span><span class="sxs-lookup"><span data-stu-id="52edf-134">1</span></span>                                            | <span data-ttu-id="52edf-135">2</span><span class="sxs-lookup"><span data-stu-id="52edf-135">2</span></span>                                                        |



 

<span data-ttu-id="52edf-136">Pour énumérer les formats pris en charge pour un codec, utilisez [**IWMCodecInfo :: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) pour rechercher le nombre de codecs pris en charge.</span><span class="sxs-lookup"><span data-stu-id="52edf-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="52edf-137">Appelez ensuite [**IWMCodecInfo :: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) pour chaque format.</span><span class="sxs-lookup"><span data-stu-id="52edf-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="52edf-138">Les index de format sont compris entre zéro et un nombre inférieur au nombre total de formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="52edf-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="52edf-139">Vous pouvez récupérer une description du format en appelant [**IWMCodecInfo2 :: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span><span class="sxs-lookup"><span data-stu-id="52edf-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="52edf-140">Lorsque vous utilisez **GetCodecFormatDesc**, vous n’avez pas besoin d’utiliser **GetCodecFormat**, car l’objet de configuration de flux est récupéré par les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="52edf-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="52edf-141">Les formats de codec vidéo n’incluent pas de description.</span><span class="sxs-lookup"><span data-stu-id="52edf-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="52edf-142">Chaque codec vidéo n’a qu’un seul format utilisé pour tous les flux de ce type.</span><span class="sxs-lookup"><span data-stu-id="52edf-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="52edf-143">Lorsque vous récupérez un format de codec, vous accédez à l’interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) d’un objet de configuration de flux contenant les paramètres de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="52edf-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52edf-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52edf-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52edf-145">**Obtention d’informations de configuration de flux à partir de codecs**</span><span class="sxs-lookup"><span data-stu-id="52edf-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




