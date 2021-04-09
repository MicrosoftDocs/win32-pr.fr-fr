---
description: Exemples vidéo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Exemples vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863925"
---
# <a name="video-samples"></a><span data-ttu-id="444df-103">Exemples vidéo</span><span class="sxs-lookup"><span data-stu-id="444df-103">Video Samples</span></span>

<span data-ttu-id="444df-104">L’exemple d’objet vidéo est une implémentation spécialisée de l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pour une utilisation avec le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="444df-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="444df-105">Pour créer une instance de cet objet, appelez la fonction [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) .</span><span class="sxs-lookup"><span data-stu-id="444df-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="444df-106">La fonction prend un pointeur vers une surface Direct3D et retourne un pointeur vers l’interface **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="444df-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="444df-107">Les types d’objets suivants doivent allouer des exemples à l’aide de cette fonction :</span><span class="sxs-lookup"><span data-stu-id="444df-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="444df-108">Présentateur EVR personnalisé.</span><span class="sxs-lookup"><span data-stu-id="444df-108">Custom EVR presenters.</span></span> <span data-ttu-id="444df-109">Un présentateur alloue des échantillons vidéo et les envoie à la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) de mixer.</span><span class="sxs-lookup"><span data-stu-id="444df-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="444df-110">Pour plus d’informations, consultez [Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="444df-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="444df-111">Décodeurs vidéo qui prennent en charge l’accélération vidéo.</span><span class="sxs-lookup"><span data-stu-id="444df-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="444df-112">Pour plus d’informations, consultez [prise en charge de DXVA 2,0 dans Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="444df-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="444df-113">L’exemple d’objet Video implémente les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="444df-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="444df-114">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="444df-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="444df-115">**IMFDesiredSample**</span><span class="sxs-lookup"><span data-stu-id="444df-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="444df-116">**IMFTrackedSample**</span><span class="sxs-lookup"><span data-stu-id="444df-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="444df-117">Si le paramètre *pUnkSurface* de [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) est non **null**, l’exemple de vidéo qui en résulte contient une seule mémoire tampon de média qui encapsule la surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="444df-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="444df-118">Cet objet de mémoire tampon a des fonctionnalités limitées :</span><span class="sxs-lookup"><span data-stu-id="444df-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="444df-119">La méthode [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) de la mémoire tampon retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="444df-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="444df-120">La mémoire tampon n’implémente pas l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="444df-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="444df-121">La seule façon d’accéder à la surface à partir de la mémoire tampon consiste à appeler [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)à l’aide de l’identificateur de service \_ service de mémoire tampon Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="444df-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="444df-122">Si le paramètre *pUnkSurface* est **null**, l’exemple de vidéo est créé avec des tampons de média nuls.</span><span class="sxs-lookup"><span data-stu-id="444df-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="444df-123">Pour ajouter un tampon à l’exemple, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="444df-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="444df-124">Créez une surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="444df-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="444df-125">Créez une mémoire tampon de surface en appelant [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span><span class="sxs-lookup"><span data-stu-id="444df-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="444df-126">Pour plus d’informations, consultez [DirectX surface buffer](directx-surface-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="444df-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="444df-127">Ajoutez la mémoire tampon à l’exemple en appelant [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="444df-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="444df-128">Utilisez cette approche si vous avez besoin que la mémoire de surface soit accessible par le biais de l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="444df-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="444df-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="444df-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="444df-130">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="444df-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="444df-131">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="444df-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
