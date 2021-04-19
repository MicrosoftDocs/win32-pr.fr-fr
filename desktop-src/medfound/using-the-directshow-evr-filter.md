---
description: Utilisation du filtre DirectShow EVR
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Utilisation du filtre DirectShow EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534185"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="51e65-103">Utilisation du filtre DirectShow EVR</span><span class="sxs-lookup"><span data-stu-id="51e65-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="51e65-104">Pour créer le filtre EVR (Enhanced Video Renderer), appelez **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="51e65-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="51e65-105">Le CLSID est CLSID \_ EnhancedVideoRenderer, défini dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="51e65-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="51e65-106">Vous n’avez pas besoin d’appeler [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ou [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour utiliser le filtre EVR.</span><span class="sxs-lookup"><span data-stu-id="51e65-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="51e65-107">Pour plus d’informations sur l’utilisation du filtre EVR dans une application DirectShow, consultez [lecture audio/vidéo dans DirectShow](../directshow/audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="51e65-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="51e65-108">Le filtre EVR commence par une broche d’entrée, qui correspond au flux de référence.</span><span class="sxs-lookup"><span data-stu-id="51e65-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="51e65-109">Pour ajouter des codes confidentiels pour les sous-flux, interrogez le filtre de l’interface [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) et appelez [**IEVRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="51e65-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="51e65-110">Appelez cette méthode avant de connecter des broches d’entrée.</span><span class="sxs-lookup"><span data-stu-id="51e65-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="51e65-111">La broche 0 est toujours le flux de référence.</span><span class="sxs-lookup"><span data-stu-id="51e65-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="51e65-112">Connectez ce code confidentiel avant tout autre pin, car le format du flux de référence peut limiter les formats de sous-flux disponibles.</span><span class="sxs-lookup"><span data-stu-id="51e65-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="51e65-113">Avant de démarrer le graphique, définissez la fenêtre de découpage vidéo et le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="51e65-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="51e65-114">Pour plus d’informations, consultez [utilisation des contrôles d’affichage vidéo](using-the-video-display-controls.md).</span><span class="sxs-lookup"><span data-stu-id="51e65-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="51e65-115">Contrairement au convertisseur de mixage vidéo (VMR), le EVR n’a pas de modes opérationnels (fenêtre, sans fenêtre, etc.).</span><span class="sxs-lookup"><span data-stu-id="51e65-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="51e65-116">En particulier :</span><span class="sxs-lookup"><span data-stu-id="51e65-116">In particular:</span></span>

-   <span data-ttu-id="51e65-117">EVR ne prend pas en charge le mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="51e65-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="51e65-118">L’application doit fournir la fenêtre de découpage.</span><span class="sxs-lookup"><span data-stu-id="51e65-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="51e65-119">Le EVR n’a pas de mode sans rendu.</span><span class="sxs-lookup"><span data-stu-id="51e65-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="51e65-120">Pour remplacer le présentateur par défaut, appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="51e65-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="51e65-121">Le EVR n’a pas de mode de mélange.</span><span class="sxs-lookup"><span data-stu-id="51e65-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="51e65-122">Le EVR crée toujours le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="51e65-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="51e65-123">Si vous avez un flux d’entrée, il n’est pas nécessaire d’appeler [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) pour forcer le EVR à utiliser le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="51e65-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="51e65-124">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="51e65-124">Filter Interfaces</span></span>

<span data-ttu-id="51e65-125">Le filtre EVR expose les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="51e65-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="51e65-126">Certaines de ces interfaces sont documentées dans le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="51e65-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="51e65-127">Utilisez **QueryInterface** pour récupérer les pointeurs vers ces interfaces :</span><span class="sxs-lookup"><span data-stu-id="51e65-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="51e65-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="51e65-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="51e65-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="51e65-131">**IEVRFilterConfig**</span><span class="sxs-lookup"><span data-stu-id="51e65-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="51e65-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="51e65-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="51e65-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="51e65-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="51e65-135">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="51e65-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="51e65-136">**IMFVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="51e65-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="51e65-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="51e65-137">**IPersistStream**</span></span>
-   <span data-ttu-id="51e65-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="51e65-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="51e65-140">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="51e65-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="51e65-141">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="51e65-141">Input Pin Interfaces</span></span>

<span data-ttu-id="51e65-142">Les broches d’entrée sur le filtre EVR exposent les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="51e65-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="51e65-143">Utilisez **QueryInterface** pour récupérer les pointeurs vers ces interfaces :</span><span class="sxs-lookup"><span data-stu-id="51e65-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="51e65-144">**IEVRVideoStreamControl**</span><span class="sxs-lookup"><span data-stu-id="51e65-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="51e65-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="51e65-146">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="51e65-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="51e65-147">[**IPIN**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="51e65-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="51e65-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="51e65-149">En outre, vous pouvez utiliser l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) pour récupérer l’interface suivante :</span><span class="sxs-lookup"><span data-stu-id="51e65-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="51e65-150">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="51e65-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="51e65-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51e65-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e65-152">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="51e65-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="51e65-153">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="51e65-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
