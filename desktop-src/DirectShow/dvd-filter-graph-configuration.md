---
description: Configuration du graphique de filtre DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuration du graphique de filtre DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522404"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="e897a-103">Configuration du graphique de filtre DVD</span><span class="sxs-lookup"><span data-stu-id="e897a-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="e897a-104">Cette section décrit les différentes configurations de graphique de filtre pour la lecture de DVD dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e897a-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="e897a-105">Ces diagrammes sont fournis principalement à des fins de référence.</span><span class="sxs-lookup"><span data-stu-id="e897a-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="e897a-106">Le navigateur DVD génère le graphique. ainsi, en général, il n’est pas nécessaire de comprendre les détails de la configuration du graphique.</span><span class="sxs-lookup"><span data-stu-id="e897a-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="e897a-107">Pour plus d’informations, consultez [génération du graphique de filtre DVD](building-the-dvd-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e897a-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="e897a-108">L’illustration suivante montre un graphique de filtre DVD avec un décodeur logiciel.</span><span class="sxs-lookup"><span data-stu-id="e897a-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![graphique de filtre DVD pour Windows XP](images/dvd-graph-xp.png)

<span data-ttu-id="e897a-110">Lorsqu’un décodeur matériel est présent, il est généralement connecté directement à la carte vidéo par un port vidéo.</span><span class="sxs-lookup"><span data-stu-id="e897a-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="e897a-111">Cela permet d’envoyer les bits vidéo décodés directement à la mémoire tampon de trame sur la carte graphique sans passer à la mémoire de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="e897a-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="e897a-112">Pour gérer cette connexion directe sur les versions antérieures de Windows, DirectShow prend en charge les extensions de port vidéo DirectDraw (VPE) via une interface sur le [filtre de mixage de superposition](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e897a-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="e897a-113">Le mélangeur de superposition est maintenant déconseillé.</span><span class="sxs-lookup"><span data-stu-id="e897a-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="e897a-114">Dans Windows XP et versions ultérieures, un décodeur matériel peut se connecter au filtre du [Gestionnaire de port vidéo](video-port-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="e897a-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![graphique DVD pour Windows XP avec un décodeur matériel](images/dvd-hwgraph-xp.png)

<span data-ttu-id="e897a-116">Dans tous ces graphiques, le navigateur DVD est le filtre source ; il effectue plusieurs tâches :</span><span class="sxs-lookup"><span data-stu-id="e897a-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="e897a-117">Lit les données de navigation et de vidéo à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="e897a-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="e897a-118">Démultiplexe les données vidéo, audio et de sous-image en flux distincts.</span><span class="sxs-lookup"><span data-stu-id="e897a-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="e897a-119">Pompe les flux dans le graphique pour un traitement ultérieur et un rendu éventuel.</span><span class="sxs-lookup"><span data-stu-id="e897a-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="e897a-120">Informe votre application d’événements liés aux DVD.</span><span class="sxs-lookup"><span data-stu-id="e897a-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="e897a-121">Sur le flux audio, le navigateur DVD se connecte en aval à un décodeur audio, qui se connecte au [filtre de convertisseur DirectSound](directsound-renderer-filter.md), le convertisseur audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="e897a-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="e897a-122">Dans les flux vidéo et sous-image, les filtres en aval sont le décodeur vidéo tiers et le convertisseur de mixage vidéo (ou le [mélangeur de superposition](overlay-mixer-filter.md)et le [convertisseur vidéo](video-renderer-filter.md) sur les applications de niveau inférieur).</span><span class="sxs-lookup"><span data-stu-id="e897a-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="e897a-123">Si votre application doit gérer les données de sous-titres de la ligne 21, vous devez ajouter le filtre de la ligne de code de la ligne 21 DirectShow au graphique.</span><span class="sxs-lookup"><span data-stu-id="e897a-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="e897a-124">Cela implique un appel de méthode unique ; le filtre sera automatiquement connecté.</span><span class="sxs-lookup"><span data-stu-id="e897a-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="e897a-125">Votre application communique avec et contrôle le navigateur DVD par le biais des interfaces personnalisées exposées par le navigateur DVD : [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), les méthodes « Set », et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), les méthodes « d’extraction ».</span><span class="sxs-lookup"><span data-stu-id="e897a-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="e897a-126">Il doit également communiquer avec le gestionnaire de graphique de filtre (par le biais de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) pour arrêter, démarrer et contrôler le graphique.</span><span class="sxs-lookup"><span data-stu-id="e897a-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="e897a-127">Vous devrez peut-être également contrôler d’autres filtres individuels, tels que le filtre de mixage de superposition pour basculer entre les affichages plein écran et fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e897a-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="e897a-128">Pour plus d’informations, consultez [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span><span class="sxs-lookup"><span data-stu-id="e897a-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="e897a-129">La configuration exacte du graphique varie selon le type de décodeur MPEG-2 que vous avez installé, si vous devez gérer les données de sous-titrage de ligne 21 et d’autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="e897a-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e897a-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e897a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e897a-131">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="e897a-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



