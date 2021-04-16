---
description: Cette rubrique est une vue d’ensemble des API d’encodage de fichier fournies dans Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Vue d’ensemble de l’encodage dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558640"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="1ca89-103">Vue d’ensemble de l’encodage dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ca89-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="1ca89-104">Cette rubrique est une vue d’ensemble des API d’encodage de fichier fournies dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1ca89-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="1ca89-105">Terminologie</span><span class="sxs-lookup"><span data-stu-id="1ca89-105">Terminology</span></span>

<span data-ttu-id="1ca89-106">L' *encodage* est un terme général qui couvre plusieurs processus distincts :</span><span class="sxs-lookup"><span data-stu-id="1ca89-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="1ca89-107">Encodage d’un flux audio ou vidéo dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="1ca89-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="1ca89-108">Par exemple, l’encodage d’un flux vidéo en vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="1ca89-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="1ca89-109">Multiplexage (« muxing ») un ou plusieurs flux en un seul flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="1ca89-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="1ca89-110">En règle générale, les flux entrants sont encodés en premier.</span><span class="sxs-lookup"><span data-stu-id="1ca89-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="1ca89-111">Cette étape peut impliquer la transmission de paquets de flux encodés.</span><span class="sxs-lookup"><span data-stu-id="1ca89-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="1ca89-112">Écriture d’un flux d’octets multiplexés dans un fichier, tel qu’un fichier MP4 ou ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="1ca89-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1ca89-113">Le flux Multiplexed peut également être envoyé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="1ca89-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="1ca89-114">Le diagramme suivant illustre ces trois processus :</span><span class="sxs-lookup"><span data-stu-id="1ca89-114">The following diagram shows these three processes:</span></span>

![Diagramme montrant les processus d’encodage et de multiplexage](images/encoding03.png)

<span data-ttu-id="1ca89-116">Les variantes de ce processus incluent le transcodage et la remuxing :</span><span class="sxs-lookup"><span data-stu-id="1ca89-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="1ca89-117">Le *transcodage* consiste à décoder un fichier existant, à ré-encoder les flux et à Remultiplexer les flux encodés.</span><span class="sxs-lookup"><span data-stu-id="1ca89-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="1ca89-118">Le transcodage peut être effectué pour convertir un fichier d’un type d’encodage à un autre. par exemple, pour convertir la vidéo H. 264 en Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="1ca89-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="1ca89-119">Elle peut également être effectuée pour modifier la vitesse de transmission encodée. taille de l’image vidéo ; la fréquence d’images ; ou d’autres paramètres de format.</span><span class="sxs-lookup"><span data-stu-id="1ca89-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="1ca89-120">Le *Remultiplexage* ou *remuxing* désigne le démultiplexage d’un fichier et le Remultiplexage des flux, sans étape de décodage/codage.</span><span class="sxs-lookup"><span data-stu-id="1ca89-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="1ca89-121">Cela peut être fait pour modifier la façon dont les paquets audio/vidéo sont multiplexés, pour supprimer un flux ou pour combiner des flux de deux fichiers sources différents.</span><span class="sxs-lookup"><span data-stu-id="1ca89-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="1ca89-122">La conversion est un cas particulier de transcodage, où le débit *binaire est modifié* sans modifier le type de compression.</span><span class="sxs-lookup"><span data-stu-id="1ca89-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="1ca89-123">Par exemple, vous pouvez convertir un fichier à taux binaire élevé en un débit inférieur.</span><span class="sxs-lookup"><span data-stu-id="1ca89-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="1ca89-124">Un scénario classique dans lequel la transclassification peut être utilisée consiste à synchroniser le contenu multimédia d’un PC à un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="1ca89-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="1ca89-125">Si le périphérique portable ne prend pas en charge une vitesse de transmission élevée, il est possible que le fichier soit au prorata avant d’être copié sur le périphérique portable.</span><span class="sxs-lookup"><span data-stu-id="1ca89-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="1ca89-126">Le diagramme de blocs suivant illustre le processus de transcodage.</span><span class="sxs-lookup"><span data-stu-id="1ca89-126">The following block diagram shows the transcoding process.</span></span>

![Diagramme montrant le processus de transcodage](images/encoding05.png)

<span data-ttu-id="1ca89-128">Le diagramme de blocs suivant illustre le processus remuxing.</span><span class="sxs-lookup"><span data-stu-id="1ca89-128">The following block diagram shows the remuxing process.</span></span>

![Diagramme montrant le processus remuxing](images/encoding06.png)

<span data-ttu-id="1ca89-130">Cette documentation utilise parfois le terme *encodage* pour inclure le transcodage et les remuxing.</span><span class="sxs-lookup"><span data-stu-id="1ca89-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="1ca89-131">Lorsqu’il est important de faire la distinction entre ces deux éléments, la documentation indique la différence.</span><span class="sxs-lookup"><span data-stu-id="1ca89-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="1ca89-132">Voir aussi : [Media Foundation : concepts essentiels](media-foundation-programming--essential-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="1ca89-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="1ca89-133">Architecture d’encodage Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ca89-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="1ca89-134">Au niveau de la couche la plus basse de l’architecture Media Foundation, les types de composant suivants sont utilisés pour l’encodage :</span><span class="sxs-lookup"><span data-stu-id="1ca89-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="1ca89-135">Pour le transcodage, les [sources de média](media-sources.md) sont utilisées pour démultiplexer le fichier source.</span><span class="sxs-lookup"><span data-stu-id="1ca89-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="1ca89-136">Pour le processus d’encodage, les [transformations Media Foundation](media-foundation-transforms.md) sont utilisées pour décoder et encoder les flux.</span><span class="sxs-lookup"><span data-stu-id="1ca89-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="1ca89-137">Pour le processus de multiplexage, les [récepteurs de médias](media-sinks.md) sont utilisés pour multiplexer les flux et écrire le flux multiplexé dans un fichier ou un réseau.</span><span class="sxs-lookup"><span data-stu-id="1ca89-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="1ca89-138">Le diagramme suivant montre le déroulement des données entre ces composants dans un scénario de transcodage :</span><span class="sxs-lookup"><span data-stu-id="1ca89-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![Diagramme montrant les composants utilisés dans le transcodage](images/encoding04.png)

<span data-ttu-id="1ca89-140">La plupart des applications n’utilisent pas directement ces composants.</span><span class="sxs-lookup"><span data-stu-id="1ca89-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="1ca89-141">Au lieu de cela, une application utilise des API de niveau supérieur qui gèrent ces composants de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="1ca89-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="1ca89-142">Media Foundation fournit deux API de niveau supérieur pour l’encodage :</span><span class="sxs-lookup"><span data-stu-id="1ca89-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="1ca89-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Session multimédia](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="1ca89-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="1ca89-144">La session multimédia fournit un pipeline de bout en bout qui déplace les données de la source du média, via les codecs, et enfin vers le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="1ca89-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="1ca89-145">L’application contrôle la session multimédia et reçoit des événements d’état de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="1ca89-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="1ca89-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Lecteur source](source-reader.md) et [enregistreur récepteur](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="1ca89-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="1ca89-147">Le lecteur source encapsule la source du média et éventuellement les décodeurs.</span><span class="sxs-lookup"><span data-stu-id="1ca89-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="1ca89-148">Il fournit à l’application des exemples encodés ou décodés.</span><span class="sxs-lookup"><span data-stu-id="1ca89-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="1ca89-149">Le writer du récepteur encapsule le récepteur multimédia et éventuellement les encodeurs.</span><span class="sxs-lookup"><span data-stu-id="1ca89-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="1ca89-150">L’application transmet des exemples au writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="1ca89-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="1ca89-151">Le diagramme suivant illustre la session de média :</span><span class="sxs-lookup"><span data-stu-id="1ca89-151">The following diagram shows the Media Session:</span></span>

![Diagramme montrant comment la session multimédia effectue le transcodage](images/encoding01.png)

<span data-ttu-id="1ca89-153">L' [API de transcodage](transcode-api.md) (zone ombrée bleue) est un ensemble d’API introduites dans Windows 7, ce qui facilite la configuration de la session multimédia pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="1ca89-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="1ca89-154">Le diagramme suivant montre le lecteur source et le writer du récepteur :</span><span class="sxs-lookup"><span data-stu-id="1ca89-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![Diagramme montrant le transcodage avec le lecteur source et le writer du récepteur](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="1ca89-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ca89-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ca89-157">Codage et création de fichier</span><span class="sxs-lookup"><span data-stu-id="1ca89-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="1ca89-158">Programmation Media Foundation : concepts essentiels</span><span class="sxs-lookup"><span data-stu-id="1ca89-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



