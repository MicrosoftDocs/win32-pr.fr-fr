---
description: À l’aide de MFTrace, vous pouvez filtrer les résultats de la trace en spécifiant une liste de mots clés.
ms.assetid: e7c382cb-94ac-4f90-a3dd-32f94c538396
title: Mots clés MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d18a91aede8692209b9d5b7a2759c460e44043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114383"
---
# <a name="mftrace-keywords"></a><span data-ttu-id="72632-103">Mots clés MFTrace</span><span class="sxs-lookup"><span data-stu-id="72632-103">MFTrace Keywords</span></span>

<span data-ttu-id="72632-104">À l’aide de [MFTrace](mftrace.md), vous pouvez filtrer les résultats de la trace en spécifiant une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="72632-104">Using [MFTrace](mftrace.md), you can filter the trace results by specifying a list of keywords.</span></span> <span data-ttu-id="72632-105">Sur la ligne de commande, utilisez l’argument de ligne **de commande-k** .</span><span class="sxs-lookup"><span data-stu-id="72632-105">At the command line, use the **-k** command-line argument.</span></span> <span data-ttu-id="72632-106">Vous pouvez également spécifier l’élément de [**mot clé**](keyword.md) dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="72632-106">Alternatively, specify the [**keyword**](keyword.md) element in the configuration file.</span></span> <span data-ttu-id="72632-107">Pour plus d’informations, consultez [utilisation de MFTrace](using-mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="72632-107">For more information, see [Using MFTrace](using-mftrace.md).</span></span>

<span data-ttu-id="72632-108">MFTrace prend en charge les mots clés suivants.</span><span class="sxs-lookup"><span data-stu-id="72632-108">MFTrace supports the following keywords.</span></span> <span data-ttu-id="72632-109">La plupart font référence à des interfaces ou des exportations de bibliothèque particulières.</span><span class="sxs-lookup"><span data-stu-id="72632-109">Most refer to particular interfaces or library exports.</span></span>

-   <span data-ttu-id="72632-110">« Toutes »</span><span class="sxs-lookup"><span data-stu-id="72632-110">"All"</span></span>
-   <span data-ttu-id="72632-111">Valeurs</span><span class="sxs-lookup"><span data-stu-id="72632-111">"Default"</span></span>
-   <span data-ttu-id="72632-112">Détours</span><span class="sxs-lookup"><span data-stu-id="72632-112">"Detours"</span></span>
-   <span data-ttu-id="72632-113">"IFilterGraph"</span><span class="sxs-lookup"><span data-stu-id="72632-113">"IFilterGraph"</span></span>
-   <span data-ttu-id="72632-114">"IGraphBuilder"</span><span class="sxs-lookup"><span data-stu-id="72632-114">"IGraphBuilder"</span></span>
-   <span data-ttu-id="72632-115">Appel</span><span class="sxs-lookup"><span data-stu-id="72632-115">"IMediaControl"</span></span>
-   <span data-ttu-id="72632-116">"IMediaObject"</span><span class="sxs-lookup"><span data-stu-id="72632-116">"IMediaObject"</span></span>
-   <span data-ttu-id="72632-117">"IMemInputPin"</span><span class="sxs-lookup"><span data-stu-id="72632-117">"IMemInputPin"</span></span>
-   <span data-ttu-id="72632-118">"IMFActivate"</span><span class="sxs-lookup"><span data-stu-id="72632-118">"IMFActivate"</span></span>
-   <span data-ttu-id="72632-119">"IMFAttributes"</span><span class="sxs-lookup"><span data-stu-id="72632-119">"IMFAttributes"</span></span>
-   <span data-ttu-id="72632-120">"IMFByteStream"</span><span class="sxs-lookup"><span data-stu-id="72632-120">"IMFByteStream"</span></span>
-   <span data-ttu-id="72632-121">"IMFByteStreamHandler"</span><span class="sxs-lookup"><span data-stu-id="72632-121">"IMFByteStreamHandler"</span></span>
-   <span data-ttu-id="72632-122">"IMFClock"</span><span class="sxs-lookup"><span data-stu-id="72632-122">"IMFClock"</span></span>
-   <span data-ttu-id="72632-123">"IMFMediaEventGenerator"</span><span class="sxs-lookup"><span data-stu-id="72632-123">"IMFMediaEventGenerator"</span></span>
-   <span data-ttu-id="72632-124">"IMFMediaSession"</span><span class="sxs-lookup"><span data-stu-id="72632-124">"IMFMediaSession"</span></span>
-   <span data-ttu-id="72632-125">"IMFMediaSink"</span><span class="sxs-lookup"><span data-stu-id="72632-125">"IMFMediaSink"</span></span>
-   <span data-ttu-id="72632-126">"IMFMediaSource"</span><span class="sxs-lookup"><span data-stu-id="72632-126">"IMFMediaSource"</span></span>
-   <span data-ttu-id="72632-127">"IMFMediaStream"</span><span class="sxs-lookup"><span data-stu-id="72632-127">"IMFMediaStream"</span></span>
-   <span data-ttu-id="72632-128">"IMFPMediaItem"</span><span class="sxs-lookup"><span data-stu-id="72632-128">"IMFPMediaItem"</span></span>
-   <span data-ttu-id="72632-129">"IMFPMediaPlayer"</span><span class="sxs-lookup"><span data-stu-id="72632-129">"IMFPMediaPlayer"</span></span>
-   <span data-ttu-id="72632-130">"IMFPMediaPlayerCallback"</span><span class="sxs-lookup"><span data-stu-id="72632-130">"IMFPMediaPlayerCallback"</span></span>
-   <span data-ttu-id="72632-131">"IMFPresentationClock"</span><span class="sxs-lookup"><span data-stu-id="72632-131">"IMFPresentationClock"</span></span>
-   <span data-ttu-id="72632-132">"IMFQualityAdvise"</span><span class="sxs-lookup"><span data-stu-id="72632-132">"IMFQualityAdvise"</span></span>
-   <span data-ttu-id="72632-133">"IMFQualityAdvise2"</span><span class="sxs-lookup"><span data-stu-id="72632-133">"IMFQualityAdvise2"</span></span>
-   <span data-ttu-id="72632-134">"IMFQualityManager"</span><span class="sxs-lookup"><span data-stu-id="72632-134">"IMFQualityManager"</span></span>
-   <span data-ttu-id="72632-135">"IMFReadWriteClassFactory"</span><span class="sxs-lookup"><span data-stu-id="72632-135">"IMFReadWriteClassFactory"</span></span>
-   <span data-ttu-id="72632-136">"IMFSample"</span><span class="sxs-lookup"><span data-stu-id="72632-136">"IMFSample"</span></span>
-   <span data-ttu-id="72632-137">"IMFSchemeHandler"</span><span class="sxs-lookup"><span data-stu-id="72632-137">"IMFSchemeHandler"</span></span>
-   <span data-ttu-id="72632-138">"IMFSinkWriter"</span><span class="sxs-lookup"><span data-stu-id="72632-138">"IMFSinkWriter"</span></span>
-   <span data-ttu-id="72632-139">IMFSourceReader</span><span class="sxs-lookup"><span data-stu-id="72632-139">"IMFSourceReader"</span></span>
-   <span data-ttu-id="72632-140">"IMFSourceReaderCallback"</span><span class="sxs-lookup"><span data-stu-id="72632-140">"IMFSourceReaderCallback"</span></span>
-   <span data-ttu-id="72632-141">"IMFSourceResolver"</span><span class="sxs-lookup"><span data-stu-id="72632-141">"IMFSourceResolver"</span></span>
-   <span data-ttu-id="72632-142">"IMFStreamSink"</span><span class="sxs-lookup"><span data-stu-id="72632-142">"IMFStreamSink"</span></span>
-   <span data-ttu-id="72632-143">"IMFTopoLoader"</span><span class="sxs-lookup"><span data-stu-id="72632-143">"IMFTopoLoader"</span></span>
-   <span data-ttu-id="72632-144">"IMFTopology"</span><span class="sxs-lookup"><span data-stu-id="72632-144">"IMFTopology"</span></span>
-   <span data-ttu-id="72632-145">"IMFTopologyNode"</span><span class="sxs-lookup"><span data-stu-id="72632-145">"IMFTopologyNode"</span></span>
-   <span data-ttu-id="72632-146">"IMFTransform"</span><span class="sxs-lookup"><span data-stu-id="72632-146">"IMFTransform"</span></span>
-   <span data-ttu-id="72632-147">"IWMReader"</span><span class="sxs-lookup"><span data-stu-id="72632-147">"IWMReader"</span></span>
-   <span data-ttu-id="72632-148">"Kernel32Export"</span><span class="sxs-lookup"><span data-stu-id="72632-148">"Kernel32Export"</span></span>
-   <span data-ttu-id="72632-149">"MFExport"</span><span class="sxs-lookup"><span data-stu-id="72632-149">"MFExport"</span></span>
-   <span data-ttu-id="72632-150">"MFPlatExport"</span><span class="sxs-lookup"><span data-stu-id="72632-150">"MFPlatExport"</span></span>
-   <span data-ttu-id="72632-151">"MFPlayExport"</span><span class="sxs-lookup"><span data-stu-id="72632-151">"MFPlayExport"</span></span>
-   <span data-ttu-id="72632-152">"MFPublic"</span><span class="sxs-lookup"><span data-stu-id="72632-152">"MFPublic"</span></span>
-   <span data-ttu-id="72632-153">"MFReadWriteExport"</span><span class="sxs-lookup"><span data-stu-id="72632-153">"MFReadWriteExport"</span></span>
-   <span data-ttu-id="72632-154">"Ole32Export"</span><span class="sxs-lookup"><span data-stu-id="72632-154">"Ole32Export"</span></span>
-   <span data-ttu-id="72632-155">"wmvCoreExport"</span><span class="sxs-lookup"><span data-stu-id="72632-155">"wmvCoreExport"</span></span>

## <a name="related-topics"></a><span data-ttu-id="72632-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72632-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72632-157">MFTrace</span><span class="sxs-lookup"><span data-stu-id="72632-157">MFTrace</span></span>](mftrace.md)
</dt> <dt>

[<span data-ttu-id="72632-158">Utilisation de MFTrace</span><span class="sxs-lookup"><span data-stu-id="72632-158">Using MFTrace</span></span>](using-mftrace.md)
</dt> </dl>

 

 



