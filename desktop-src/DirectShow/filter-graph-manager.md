---
description: Gestionnaire de graphique de filtre
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gestionnaire de graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845790"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="4a0d6-103">Gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="4a0d6-103">Filter Graph Manager</span></span>

<span data-ttu-id="4a0d6-104">Le gestionnaire de graphique de filtre génère et contrôle les graphiques de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="4a0d6-105">Cet objet est le composant central de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="4a0d6-106">Les applications l’utilisent pour générer et contrôler les graphiques de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="4a0d6-107">Le gestionnaire de graphes de filtre gère également la synchronisation, la notification d’événements et d’autres aspects du graphique de filtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="4a0d6-108">Créez cet objet en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="4a0d6-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a0d6-109">CLSID</span></span>

<span data-ttu-id="4a0d6-110">Il existe deux CLSID pour créer le gestionnaire de graphes de filtre :</span><span class="sxs-lookup"><span data-stu-id="4a0d6-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="4a0d6-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a0d6-111">CLSID</span></span>                      | <span data-ttu-id="4a0d6-112">Description</span><span class="sxs-lookup"><span data-stu-id="4a0d6-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="4a0d6-113">CLSID \_ FilterGraph</span><span class="sxs-lookup"><span data-stu-id="4a0d6-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="4a0d6-114">Crée le gestionnaire de graphes de filtre sur un thread de travail partagé.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="4a0d6-115">CLSID \_ FilterGraphNoThread</span><span class="sxs-lookup"><span data-stu-id="4a0d6-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="4a0d6-116">Crée le gestionnaire de graphes de filtre sur le thread d’application.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="4a0d6-117">En règle générale, les applications doivent utiliser le CLSID \_ FilterGraph.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="4a0d6-118">Les deux CLSID créent le même objet, mais ils utilisent différents modèles de thread :</span><span class="sxs-lookup"><span data-stu-id="4a0d6-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="4a0d6-119">\_Le CLSID FilterGraph crée le gestionnaire de graphes de filtre sur un thread de travail, qui est partagé par toutes les \_ instances du CLSID FilterGraph au sein du même processus.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="4a0d6-120">Le thread distribue les messages envoyés par les filtres et contrôle la durée de vie des fenêtres créées par des filtres.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="4a0d6-121">CLSID \_ FilterGraphNoThread crée le gestionnaire de graphes de filtre sur le thread de l’application.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="4a0d6-122">Si vous utilisez ce CLSID, le thread qui appelle **CoCreateInstance** doit avoir une boucle de message qui distribue les messages ; dans le cas contraire, des interblocages peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="4a0d6-123">De plus, avant que le thread d’application ne s’arrête, il doit libérer le gestionnaire de graphique de filtre et tous les objets de graphique (tels que les filtres, les broches, les horloges de référence, etc.).</span><span class="sxs-lookup"><span data-stu-id="4a0d6-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="4a0d6-124">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4a0d6-124">Interfaces</span></span>

<span data-ttu-id="4a0d6-125">Le gestionnaire de graphique de filtre expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a0d6-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="4a0d6-126">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="4a0d6-127">**IAMStats**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="4a0d6-128">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="4a0d6-129">**IBasicVideo**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="4a0d6-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="4a0d6-131">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="4a0d6-132">**IFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="4a0d6-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="4a0d6-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="4a0d6-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="4a0d6-136">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="4a0d6-137">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="4a0d6-138">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="4a0d6-139">**Appel**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="4a0d6-140">**IMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="4a0d6-141">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="4a0d6-142">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="4a0d6-143">**IMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="4a0d6-144">**IMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="4a0d6-145">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="4a0d6-146">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="4a0d6-147">**IRegisterServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="4a0d6-148">**IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="4a0d6-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="4a0d6-150">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="4a0d6-151">**IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="4a0d6-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="4a0d6-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a0d6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a0d6-153">Objets DirectShow</span><span class="sxs-lookup"><span data-stu-id="4a0d6-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



