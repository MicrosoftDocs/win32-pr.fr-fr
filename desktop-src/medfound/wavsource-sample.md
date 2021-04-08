---
description: Exemple WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Exemple WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863922"
---
# <a name="wavsource-sample"></a><span data-ttu-id="9e7ce-103">Exemple WavSource</span><span class="sxs-lookup"><span data-stu-id="9e7ce-103">WavSource Sample</span></span>

<span data-ttu-id="9e7ce-104">Montre comment créer une source de média personnalisée dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="9e7ce-105">L’exemple implémente une source multimédia qui analyse les fichiers audio. wav.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="9e7ce-106">Cet exemple est un exemple relativement simple d’une source de média :</span><span class="sxs-lookup"><span data-stu-id="9e7ce-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="9e7ce-107">Il n’existe qu’un seul flux, il n’y a donc aucun code pour implémenter la sélection de flux.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="9e7ce-108">La source du média n’implémente pas le contrôle de la fréquence (autrement dit, la lecture rapide ou inversée).</span><span class="sxs-lookup"><span data-stu-id="9e7ce-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="9e7ce-109">Toutes les méthodes de source et de flux sont implémentées en tant que méthodes synchrones.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="9e7ce-110">Étant donné que la partie données d’un fichier. wav est un bloc unique de données audio PCM non compressées, la source du média n’a pas besoin de lire les en-têtes de paquets ou d’analyser le flux pendant la lecture, à l’exception de la lecture de l’en-tête [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) initial.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="9e7ce-111">Pour obtenir un exemple plus avancé d’une source de média, consultez l' [exemple MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9e7ce-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="9e7ce-112">API illustrées</span><span class="sxs-lookup"><span data-stu-id="9e7ce-112">APIs Demonstrated</span></span>

<span data-ttu-id="9e7ce-113">Cet exemple illustre les interfaces de Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e7ce-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="9e7ce-114">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="9e7ce-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="9e7ce-115">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="9e7ce-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="9e7ce-116">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="9e7ce-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="9e7ce-117">Utilisation</span><span class="sxs-lookup"><span data-stu-id="9e7ce-117">Usage</span></span>

<span data-ttu-id="9e7ce-118">L’exemple WavSource génère une DLL qui est un serveur COM pour la source du média et le gestionnaire de flux d’octets de la source du média.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="9e7ce-119">Avant d’utiliser la source du média, vous devez inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="9e7ce-120">Pour utiliser la source du média, vous pouvez exécuter le [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9e7ce-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="9e7ce-121">Le programme de résolution source chargera automatiquement la source du média si vous sélectionnez un fichier. wav pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="9e7ce-122">(Si une erreur se produit, assurez-vous que vous avez correctement inscrit la DLL WavSource.)</span><span class="sxs-lookup"><span data-stu-id="9e7ce-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="9e7ce-123">Vous pouvez également utiliser l’outil TopoEdit pour générer une topologie de lecture qui contient la source du média.</span><span class="sxs-lookup"><span data-stu-id="9e7ce-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="9e7ce-124">Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="9e7ce-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7ce-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e7ce-125">Requirements</span></span>



| <span data-ttu-id="9e7ce-126">Produit</span><span class="sxs-lookup"><span data-stu-id="9e7ce-126">Product</span></span>                                                        | <span data-ttu-id="9e7ce-127">Version</span><span class="sxs-lookup"><span data-stu-id="9e7ce-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="9e7ce-128">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="9e7ce-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="9e7ce-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e7ce-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9e7ce-130">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="9e7ce-130">Downloading the Sample</span></span>

<span data-ttu-id="9e7ce-131">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span><span class="sxs-lookup"><span data-stu-id="9e7ce-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e7ce-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e7ce-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e7ce-133">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e7ce-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="9e7ce-134">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="9e7ce-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="9e7ce-135">Exemple MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="9e7ce-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="9e7ce-136">Gestionnaires de schémas et gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="9e7ce-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="9e7ce-137">Écriture d’une source de média personnalisée</span><span class="sxs-lookup"><span data-stu-id="9e7ce-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
