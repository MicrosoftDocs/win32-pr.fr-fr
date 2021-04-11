---
description: Négociation de type de média EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Négociation de type de média EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321558"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="23397-103">Négociation de type de média EVR</span><span class="sxs-lookup"><span data-stu-id="23397-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="23397-104">Cette rubrique décrit comment le convertisseur de vidéo amélioré (EVR) valide les types de médias.</span><span class="sxs-lookup"><span data-stu-id="23397-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="23397-105">Pour le filtre DirectShow EVR, la négociation de type se produit lorsque les codes confidentiels du filtre sont connectés.</span><span class="sxs-lookup"><span data-stu-id="23397-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="23397-106">Pour le récepteur multimédia EVR, les types de média sont définis par le biais de l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sur les récepteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="23397-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="23397-107">En général, le chargeur de topologie négocie les types de média, bien que l’application puisse également définir les types de média directement.</span><span class="sxs-lookup"><span data-stu-id="23397-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="23397-108">EVR ne signale aucun type de média préféré.</span><span class="sxs-lookup"><span data-stu-id="23397-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="23397-109">Le client doit tester les types de média jusqu’à ce qu’il trouve un type acceptable.</span><span class="sxs-lookup"><span data-stu-id="23397-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="23397-110">Le type de média du flux de référence doit être défini pour que les types puissent être définis sur l’un des sous-flux.</span><span class="sxs-lookup"><span data-stu-id="23397-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="23397-111">Pour le flux de référence, le mixeur EVR obtient une liste de formats de cible d’accélération vidéo compatible DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="23397-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="23397-112">Le présentateur EVR utilise cette liste pour sélectionner le format de la chaîne de permutation Direct3D.</span><span class="sxs-lookup"><span data-stu-id="23397-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="23397-113">Si aucun format de cible de rendu compatible ne peut être trouvé, le EVR rejette le type de média.</span><span class="sxs-lookup"><span data-stu-id="23397-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="23397-114">Pour les sous-flux, le mélangeur EVR demande si l’appareil DXVA prend en charge ce format de sous-flux en association avec le format de la cible de rendu qui a été sélectionné pour le flux de référence.</span><span class="sxs-lookup"><span data-stu-id="23397-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="23397-115">Par conséquent, les formats de sous-flux disponibles peuvent changer en fonction du flux de référence.</span><span class="sxs-lookup"><span data-stu-id="23397-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="23397-116">Voici le processus plus en détail.</span><span class="sxs-lookup"><span data-stu-id="23397-116">Here is the process in more detail.</span></span> <span data-ttu-id="23397-117">Ces détails ne sont pas importants pour la plupart des applications, mais peuvent être utiles si vous écrivez un mélangeur ou un présentateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="23397-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="23397-118">Pour le flux de référence, la négociation se produit comme suit :</span><span class="sxs-lookup"><span data-stu-id="23397-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="23397-119">EVR appelle [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sur le mixer.</span><span class="sxs-lookup"><span data-stu-id="23397-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="23397-120">Le mélangeur convertit le type de média en une description DXVA 2,0, à l’aide de la structure [**\_ VideoDesc DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .</span><span class="sxs-lookup"><span data-stu-id="23397-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="23397-121">Le mélangeur appelle [**IDirectXVideoProcessorService :: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) pour obtenir la liste des GUID de processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="23397-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="23397-122">Pour chaque GUID de processeur vidéo, le mélangeur appelle [**IDirectXVideoProcessorService :: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) pour obtenir les formats de cible de rendu pris en charge.</span><span class="sxs-lookup"><span data-stu-id="23397-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="23397-123">EVR appelle [**IMFVideoPresenter ::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sur le présenteur avec le message MFVP \_ \_ INVALIDATEMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="23397-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="23397-124">Ce message force le présentateur à sélectionner un nouveau format.</span><span class="sxs-lookup"><span data-stu-id="23397-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="23397-125">Le présentateur appelle [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir la liste des formats de sortie disponibles à partir du mélangeur.</span><span class="sxs-lookup"><span data-stu-id="23397-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="23397-126">Le mélangeur génère cette liste à partir des formats obtenus à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="23397-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="23397-127">Le présentateur sélectionne un format et appelle [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sur le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="23397-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="23397-128">Pour les sous-flux, le processus est plus simple :</span><span class="sxs-lookup"><span data-stu-id="23397-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="23397-129">EVR appelle [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sur le mixer.</span><span class="sxs-lookup"><span data-stu-id="23397-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="23397-130">Le mélangeur appelle [**IDirectXVideoProcessorService :: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) pour obtenir la liste des formats de sous-flux disponibles.</span><span class="sxs-lookup"><span data-stu-id="23397-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="23397-131">Si le format proposé est contenu dans cette liste, le EVR accepte le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="23397-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23397-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23397-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23397-133">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="23397-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



