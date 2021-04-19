---
description: Un encodeur convertit le contenu audio ou vidéo non compressé en paquets compressés dans le format spécifié par l’application. Pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les codecs audio et vidéo Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Encodeurs Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524770"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="18166-104">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="18166-104">Windows Media Encoders</span></span>

<span data-ttu-id="18166-105">Un encodeur convertit le contenu audio ou vidéo non compressé en paquets compressés dans le format spécifié par l’application.</span><span class="sxs-lookup"><span data-stu-id="18166-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="18166-106">Pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les codecs audio et vidéo Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18166-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="18166-107">Un encodeur est identifié par le GUID qui représente la catégorie : audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="18166-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="18166-108">Le type de sortie de l’encodeur est représenté par le principal d’un type de média et le GUID de sous-type.</span><span class="sxs-lookup"><span data-stu-id="18166-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="18166-109">Codecs audio Windows Media</span><span class="sxs-lookup"><span data-stu-id="18166-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="18166-110">Catégorie : **\_ \_ \_ encodeur audio de catégorie MFT**</span><span class="sxs-lookup"><span data-stu-id="18166-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="18166-111">Type majeur : MFMediaType \_ audio</span><span class="sxs-lookup"><span data-stu-id="18166-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="18166-112">Sous-type : MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="18166-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="18166-113">Codecs Windows Media Video</span><span class="sxs-lookup"><span data-stu-id="18166-113">Windows Media video codecs</span></span>

    <span data-ttu-id="18166-114">Catégorie : **\_ \_ \_ encodeur vidéo de catégorie MFT**</span><span class="sxs-lookup"><span data-stu-id="18166-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="18166-115">Type majeur : \_ vidéo MFMediaType</span><span class="sxs-lookup"><span data-stu-id="18166-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="18166-116">SubType : MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="18166-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="18166-117">Ces encodeurs sont implémentés en tant que [Media Foundation Transform](media-foundation-transforms.md) (MFT) et Media Foundation permettent d’accéder à l’application par le biais de l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="18166-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="18166-118">Si vous utilisez des composants de couche de pipeline pour l’encodage ASF, la MFT d’encodeur est insérée dans le pipeline en tant que nœud de transformation, car il est chargé de transformer les données multimédias qui transitent par la source vers le récepteur.</span><span class="sxs-lookup"><span data-stu-id="18166-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="18166-119">Si la source est un type compressé, le pipeline ajoute les décodeurs requis pour convertir la source en un type non compressé.</span><span class="sxs-lookup"><span data-stu-id="18166-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="18166-120">Un encodeur a un flux d’entrée et un flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="18166-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="18166-121">L’encodeur reçoit des données d’entrée et produit des données encodées selon la configuration et le format définis par l’application avant la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="18166-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="18166-122">Le format du flux de sortie est décrit par un type de média.</span><span class="sxs-lookup"><span data-stu-id="18166-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="18166-123">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="18166-123">This section contains the following topics.</span></span>



| <span data-ttu-id="18166-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="18166-124">Topic</span></span>                                                                              | <span data-ttu-id="18166-125">Description</span><span class="sxs-lookup"><span data-stu-id="18166-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18166-126">Instanciation d’une table MFT d’encodeur</span><span class="sxs-lookup"><span data-stu-id="18166-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="18166-127">Explique comment créer l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="18166-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="18166-128">Propriétés d’encodage</span><span class="sxs-lookup"><span data-stu-id="18166-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="18166-129">Explique comment configurer l’encodeur en définissant les propriétés appropriées sur la MFT de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="18166-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="18166-130">Négociation de type de média sur l’encodeur</span><span class="sxs-lookup"><span data-stu-id="18166-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="18166-131">Explique comment définir les types de média d’entrée et de sortie sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="18166-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="18166-132">Configuration d’un encodeur WMV</span><span class="sxs-lookup"><span data-stu-id="18166-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="18166-133">Explique comment configurer un encodeur Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="18166-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="18166-134">Définition d’un type de sortie pour un encodeur WMA</span><span class="sxs-lookup"><span data-stu-id="18166-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="18166-135">Explique comment définir un type de sortie sur un encodeur Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="18166-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="18166-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18166-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18166-137">Composants ASF de couche de pipeline</span><span class="sxs-lookup"><span data-stu-id="18166-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



