---
description: Modes de Run-Time MPEG-2 demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modes de Run-Time MPEG-2 demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109646"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="34ac3-103">Modes de Run-Time MPEG-2 demux</span><span class="sxs-lookup"><span data-stu-id="34ac3-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="34ac3-104">Le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) (« demux ») peut fonctionner en mode push ou en mode par extraction.</span><span class="sxs-lookup"><span data-stu-id="34ac3-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="34ac3-105">En mode push, les données proviennent d’une source active, telle qu’une diffusion réseau.</span><span class="sxs-lookup"><span data-stu-id="34ac3-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="34ac3-106">En mode par extraction, les données proviennent d’un fichier local.</span><span class="sxs-lookup"><span data-stu-id="34ac3-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="34ac3-107">Le mode par extraction est disponible dans Windows XP et versions ultérieures, uniquement pour les flux de programme.</span><span class="sxs-lookup"><span data-stu-id="34ac3-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="34ac3-108">Sur les plateformes de niveau supérieur, utilisez le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="34ac3-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="34ac3-109">Le mode push est disponible sur toutes les plateformes, pour les flux de programme et les flux de transport.</span><span class="sxs-lookup"><span data-stu-id="34ac3-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="34ac3-110">Le demux prend donc en charge trois modes possibles : les flux de programme en mode par extraction, les flux de programme en mode push et les flux de transport en mode push.</span><span class="sxs-lookup"><span data-stu-id="34ac3-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="34ac3-111">Le demux détermine le mode à utiliser au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="34ac3-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="34ac3-112">Le mode est déterminé lorsque la broche d’entrée se connecte, ou lorsque la première broche de sortie est configurée, selon ce qui se produit en premier :</span><span class="sxs-lookup"><span data-stu-id="34ac3-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="34ac3-113">Lorsque la broche d’entrée se connecte : sur Windows XP et versions ultérieures, le demux interroge le filtre en amont pour l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; Si le filtre en amont expose cette interface, demux se configure lui-même pour les flux de programme en mode par extraction.</span><span class="sxs-lookup"><span data-stu-id="34ac3-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="34ac3-114">Dans le cas contraire, le demux utilise le mode push et le type de média détermine le type de flux (flux de programme ou flux de transport).</span><span class="sxs-lookup"><span data-stu-id="34ac3-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="34ac3-115">Pour obtenir la liste des types d’entrée, consultez [**types de média MPEG-2 DEMULTIPLEXEUR**](mpeg-2-demultiplexer-media-types.md) .</span><span class="sxs-lookup"><span data-stu-id="34ac3-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="34ac3-116">Quand la première broche de sortie est configurée : Si vous créez une broche de sortie et que vous la interrogez pour [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), le demux se configure pour les flux de transport en mode push.</span><span class="sxs-lookup"><span data-stu-id="34ac3-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="34ac3-117">Si vous interrogez le code PIN pour [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), le demux se configure lui-même pour les flux de programme, également en mode push.</span><span class="sxs-lookup"><span data-stu-id="34ac3-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="34ac3-118">Toutes les requêtes suivantes pour l’autre interface échouent, car le demux ne peut pas fonctionner en deux modes à la fois.</span><span class="sxs-lookup"><span data-stu-id="34ac3-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="34ac3-119">Une fois que le demux a été configuré pour un mode particulier, il reste dans ce mode.</span><span class="sxs-lookup"><span data-stu-id="34ac3-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="34ac3-120">Pour utiliser un mode différent, vous devez créer une nouvelle instance de demux.</span><span class="sxs-lookup"><span data-stu-id="34ac3-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34ac3-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34ac3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34ac3-122">Utilisation du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="34ac3-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



