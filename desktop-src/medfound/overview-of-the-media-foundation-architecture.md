---
description: Cette rubrique décrit la conception générale de Microsoft Media Foundation. Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez Media Foundation Guide de programmation.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Vue d’ensemble de l’architecture Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104565336"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="3807c-104">Vue d’ensemble de l’architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3807c-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="3807c-105">Cette rubrique décrit la conception générale de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3807c-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="3807c-106">Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez [Media Foundation Guide de programmation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="3807c-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="3807c-107">Le diagramme suivant présente une vue d’ensemble de l’architecture Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3807c-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![Diagramme montrant une vue d’ensemble de l’architecture de Media Foundation.](images/mfarch01.png)

<span data-ttu-id="3807c-109">Media Foundation fournit deux modèles de programmation distincts.</span><span class="sxs-lookup"><span data-stu-id="3807c-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="3807c-110">Le premier modèle, affiché sur le côté gauche du diagramme, utilise un pipeline de bout en bout pour les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="3807c-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="3807c-111">L’application initialise le pipeline, par exemple en fournissant l’URL d’un fichier à lire, puis appelle les méthodes pour contrôler la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="3807c-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="3807c-112">Dans le deuxième modèle, indiqué sur le côté droit du diagramme, l’application extrait les données d’une source ou les transmet à une destination (ou les deux).</span><span class="sxs-lookup"><span data-stu-id="3807c-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="3807c-113">Ce modèle est particulièrement utile si vous avez besoin de traiter les données, car l’application a un accès direct au flux de données.</span><span class="sxs-lookup"><span data-stu-id="3807c-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="3807c-114">Primitives et plateforme</span><span class="sxs-lookup"><span data-stu-id="3807c-114">Primitives and Platform</span></span>

<span data-ttu-id="3807c-115">À partir du bas du diagramme, les *primitives* sont des objets d’assistance utilisés dans l’API Media Foundation :</span><span class="sxs-lookup"><span data-stu-id="3807c-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="3807c-116">Les [attributs](attributes-and-properties.md) sont un moyen générique de stocker des informations à l’intérieur d’un objet, sous la forme d’une liste de paires clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="3807c-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="3807c-117">Les [types de médias](media-types.md) décrivent le format d’un flux de données multimédia.</span><span class="sxs-lookup"><span data-stu-id="3807c-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="3807c-118">Les [mémoires tampons de média](media-buffers.md) contiennent des blocs de données multimédias, tels que des images vidéo et des échantillons audio, et sont utilisés pour transporter des données entre des objets.</span><span class="sxs-lookup"><span data-stu-id="3807c-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="3807c-119">Les [exemples de supports](media-samples.md) sont des conteneurs pour les mémoires tampons de média.</span><span class="sxs-lookup"><span data-stu-id="3807c-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="3807c-120">Elles contiennent également des métadonnées sur les mémoires tampons, telles que les horodatages.</span><span class="sxs-lookup"><span data-stu-id="3807c-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="3807c-121">Les [API de plateforme Media Foundation](media-foundation-platform-apis.md) fournissent certaines fonctionnalités de base utilisées par le pipeline Media Foundation, telles que les rappels asynchrones et les files d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="3807c-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="3807c-122">Certaines applications peuvent avoir besoin d’appeler ces API directement. en outre, vous en aurez besoin si vous implémentez une source, une transformation ou un récepteur personnalisé pour Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3807c-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="3807c-123">Pipeline de média</span><span class="sxs-lookup"><span data-stu-id="3807c-123">Media Pipeline</span></span>

<span data-ttu-id="3807c-124">Le pipeline de média contient trois types d’objets qui génèrent ou traitent des données multimédias :</span><span class="sxs-lookup"><span data-stu-id="3807c-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="3807c-125">Les [sources multimédias](media-sources.md) introduisent des données dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="3807c-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="3807c-126">Une source de média peut obtenir des données à partir d’un fichier local, tel qu’un fichier vidéo ; à partir d’un flux réseau ; ou à partir d’un périphérique de capture matérielle.</span><span class="sxs-lookup"><span data-stu-id="3807c-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="3807c-127">[Media Foundation transforme](media-foundation-transforms.md) les données de processus (MFTS) à partir d’un flux.</span><span class="sxs-lookup"><span data-stu-id="3807c-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="3807c-128">Les encodeurs et les décodeurs sont implémentés en tant que MFTs.</span><span class="sxs-lookup"><span data-stu-id="3807c-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="3807c-129">Les [récepteurs de médias](media-sinks.md) consomment les données ; par exemple, en affichant une vidéo sur l’écran, en lisant l’audio ou en écrivant les données dans un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="3807c-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="3807c-130">Des tiers peuvent implémenter leurs propres sources personnalisées, récepteurs et MFTs. par exemple, pour prendre en charge de nouveaux formats de fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="3807c-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="3807c-131">La [session multimédia](media-session.md) contrôle le flux de données via le pipeline et gère les tâches telles que le contrôle de qualité, la synchronisation audio/vidéo et la réponse aux modifications de format.</span><span class="sxs-lookup"><span data-stu-id="3807c-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="3807c-132">Lecteur source et enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="3807c-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="3807c-133">Le [lecteur source](source-reader.md) et le [writer du récepteur](sink-writer.md) offrent un autre moyen d’utiliser les composants de base du Media Foundation (sources de média, transformations et récepteurs multimédias).</span><span class="sxs-lookup"><span data-stu-id="3807c-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="3807c-134">Le lecteur source héberge une source multimédia et zéro ou plusieurs décodeurs, tandis que le writer du récepteur héberge un récepteur multimédia et zéro ou plusieurs encodeurs.</span><span class="sxs-lookup"><span data-stu-id="3807c-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="3807c-135">Vous pouvez utiliser le lecteur source pour obtenir des données compressées ou non compressées à partir d’une source multimédia, et utiliser le writer de récepteur pour encoder les données et les envoyer à un récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="3807c-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="3807c-136">Le lecteur source et le writer du récepteur sont disponibles dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3807c-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="3807c-137">Ce modèle de programmation offre à l’application davantage de contrôle sur le workflow des données et donne également à l’application un accès direct aux données à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="3807c-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3807c-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3807c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3807c-139">Media Foundation : notions essentielles</span><span class="sxs-lookup"><span data-stu-id="3807c-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="3807c-140">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3807c-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



