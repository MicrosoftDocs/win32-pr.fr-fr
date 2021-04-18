---
description: Exemple MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Exemple MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519790"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="0e1c6-103">Exemple MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="0e1c6-103">MPEG1Source Sample</span></span>

<span data-ttu-id="0e1c6-104">Montre comment écrire une source de média personnalisée dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="0e1c6-105">L’exemple implémente une source de média qui analyse les flux de couche de systèmes MPEG-1 et génère des exemples qui contiennent des charges utiles MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="0e1c6-106">API illustrées</span><span class="sxs-lookup"><span data-stu-id="0e1c6-106">APIs Demonstrated</span></span>

<span data-ttu-id="0e1c6-107">Cet exemple illustre les interfaces de Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e1c6-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="0e1c6-108">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="0e1c6-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="0e1c6-109">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="0e1c6-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="0e1c6-110">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="0e1c6-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="0e1c6-111">Avant d’examiner cet exemple, vous souhaiterez peut-être examiner l' [exemple WavSource](wavsource-sample.md), qui fournit une implémentation plus simple d’une source de média.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="0e1c6-112">L’exemple MPEG1Source ajoute certaines fonctionnalités qui se trouvent dans la plupart des implémentations réelles d’une source de média :</span><span class="sxs-lookup"><span data-stu-id="0e1c6-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="0e1c6-113">Plusieurs flux de données</span><span class="sxs-lookup"><span data-stu-id="0e1c6-113">Multiple streams</span></span>
-   <span data-ttu-id="0e1c6-114">Méthodes asynchrones</span><span class="sxs-lookup"><span data-stu-id="0e1c6-114">Asynchronous methods</span></span>
-   <span data-ttu-id="0e1c6-115">E/s asynchrones</span><span class="sxs-lookup"><span data-stu-id="0e1c6-115">Asynchronous I/O</span></span>

<span data-ttu-id="0e1c6-116">Dans l’SDK Windows pour Windows Server 2008, cet exemple comprend également un exemple de décodeur vidéo MPEG-1 qui affiche le code de temps de chaque image vidéo.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="0e1c6-117">(Il ne décode pas en fait le flux binaire MPEG-1.)</span><span class="sxs-lookup"><span data-stu-id="0e1c6-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="0e1c6-118">À partir de la SDK Windows pour Windows 7, le décodeur a été déplacé vers un exemple distinct.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="0e1c6-119">Consultez [exemple de décodeur](decoder-sample.md).</span><span class="sxs-lookup"><span data-stu-id="0e1c6-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="0e1c6-120">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0e1c6-120">Usage</span></span>

<span data-ttu-id="0e1c6-121">L’exemple MPEG1Source génère une DLL qui est un serveur COM pour la source du média, le gestionnaire de flux d’octets de la source du média et la table MFT du décodeur.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="0e1c6-122">Avant d’utiliser la source du média, vous devez inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="0e1c6-123">Pour utiliser la source du média, vous pouvez exécuter l' [exemple BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e1c6-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="0e1c6-124">Le programme de résolution source chargera automatiquement la source du média si vous sélectionnez un fichier MPEG-1 pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="0e1c6-125">(Si une erreur se produit, assurez-vous que vous avez correctement inscrit la DLL MPEG1Source.)</span><span class="sxs-lookup"><span data-stu-id="0e1c6-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="0e1c6-126">Vous pouvez également utiliser l’outil TopoEdit pour générer une topologie de lecture qui contient la source du média.</span><span class="sxs-lookup"><span data-stu-id="0e1c6-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="0e1c6-127">Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="0e1c6-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e1c6-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e1c6-128">Requirements</span></span>



| <span data-ttu-id="0e1c6-129">Produit</span><span class="sxs-lookup"><span data-stu-id="0e1c6-129">Product</span></span>                                                        | <span data-ttu-id="0e1c6-130">Version</span><span class="sxs-lookup"><span data-stu-id="0e1c6-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0e1c6-131">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="0e1c6-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0e1c6-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e1c6-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0e1c6-133">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="0e1c6-133">Downloading the Sample</span></span>

<span data-ttu-id="0e1c6-134">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span><span class="sxs-lookup"><span data-stu-id="0e1c6-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e1c6-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e1c6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e1c6-136">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e1c6-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="0e1c6-137">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="0e1c6-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="0e1c6-138">Gestionnaires de schémas et gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="0e1c6-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="0e1c6-139">Didacticiel : écriture d’une source de média personnalisée</span><span class="sxs-lookup"><span data-stu-id="0e1c6-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="0e1c6-140">Exemple WavSource</span><span class="sxs-lookup"><span data-stu-id="0e1c6-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
