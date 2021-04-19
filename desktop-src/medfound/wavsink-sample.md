---
description: Exemple WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Exemple WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524581"
---
# <a name="wavsink-sample"></a><span data-ttu-id="79b04-103">Exemple WavSink</span><span class="sxs-lookup"><span data-stu-id="79b04-103">WavSink Sample</span></span>

<span data-ttu-id="79b04-104">Montre comment implémenter un récepteur multimédia personnalisé dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="79b04-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="79b04-105">L’exemple implémente un récepteur d’archive qui écrit des données audio PCM non compressées dans un fichier. wav.</span><span class="sxs-lookup"><span data-stu-id="79b04-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="79b04-106">API illustrées</span><span class="sxs-lookup"><span data-stu-id="79b04-106">APIs Demonstrated</span></span>

<span data-ttu-id="79b04-107">Cet exemple illustre les interfaces de Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="79b04-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="79b04-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="79b04-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="79b04-109">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="79b04-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="79b04-110">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="79b04-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="79b04-111">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="79b04-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="79b04-112">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="79b04-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="79b04-113">Utilisation</span><span class="sxs-lookup"><span data-stu-id="79b04-113">Usage</span></span>

<span data-ttu-id="79b04-114">L’exemple WavSink contient deux projets Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="79b04-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="79b04-115">WavSink. vcproj génère une bibliothèque statique qui contient l’implémentation du récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="79b04-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="79b04-116">WriteWavFile. vcproj génère une application console qui utilise le récepteur multimédia pour produire un fichier. wav.</span><span class="sxs-lookup"><span data-stu-id="79b04-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="79b04-117">Cette application est liée à la bibliothèque créée par le projet WavSink.</span><span class="sxs-lookup"><span data-stu-id="79b04-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="79b04-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79b04-118">Requirements</span></span>



| <span data-ttu-id="79b04-119">Produit</span><span class="sxs-lookup"><span data-stu-id="79b04-119">Product</span></span>                                                        | <span data-ttu-id="79b04-120">Version</span><span class="sxs-lookup"><span data-stu-id="79b04-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="79b04-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="79b04-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="79b04-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79b04-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="79b04-123">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="79b04-123">Downloading the Sample</span></span>

<span data-ttu-id="79b04-124">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span><span class="sxs-lookup"><span data-stu-id="79b04-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79b04-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79b04-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79b04-126">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79b04-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="79b04-127">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="79b04-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



