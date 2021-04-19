---
description: Utilisation de la capture WDDM dans DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Utilisation de la capture WDDM dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528208"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="989f9-103">Utilisation de la capture WDDM dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="989f9-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="989f9-104">Cette rubrique s’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="989f9-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="989f9-105">Certaines cartes vidéo possèdent une fonctionnalité de capture vidéo intégrée.</span><span class="sxs-lookup"><span data-stu-id="989f9-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="989f9-106">Sur ces cartes, les images capturées sont placées dans la mémoire vidéo (VRAM).</span><span class="sxs-lookup"><span data-stu-id="989f9-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="989f9-107">Avant Windows Vista, il n’existait pas de mécanisme standard pour le traitement des frames pendant qu’ils étaient restés dans VRAM.</span><span class="sxs-lookup"><span data-stu-id="989f9-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="989f9-108">Au lieu de cela, les données devaient être copiées dans la mémoire système, traitées, puis recopiées dans VRAM pour s’afficher.</span><span class="sxs-lookup"><span data-stu-id="989f9-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="989f9-109">Dans Windows Vista, DirectShow prend désormais en charge un mécanisme de conservation des images vidéo dans la mémoire VRAM dans tout le pipeline de traitement, de la capture à l’affichage.</span><span class="sxs-lookup"><span data-stu-id="989f9-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="989f9-110">Le filtre KsProxy détermine si le pilote prend en charge la capture de la surface VRAM en interrogeant le pilote pour la \_ propriété de surface de capture par défaut KSPROPERTY \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="989f9-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="989f9-111">(Cette propriété est documentée dans la documentation du kit de pilotes Windows.) Si le pilote prend en charge la capture de la surface VRAM, KsProxy alloue un type spécial d’exemple de média qui contient un pointeur vers une surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="989f9-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="989f9-112">Ensuite, KsProxy détermine si le filtre en aval prend en charge l’accélération vidéo DirectX (DXVA) 2,0, comme suit :</span><span class="sxs-lookup"><span data-stu-id="989f9-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="989f9-113">KsProxy interroge la broche d’entrée en aval pour l’interface **IMFGetService** .</span><span class="sxs-lookup"><span data-stu-id="989f9-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="989f9-114">Si le code PIN expose **IMFGetService**, ksproxy appelle **IMFGetService :: GetService** pour l’interface **IDirect3DDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="989f9-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="989f9-115">Le service identier est un \_ service d’accélération vidéo de m \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="989f9-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="989f9-116">Ces deux interfaces sont documentées dans la documentation du kit de développement logiciel (SDK) Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="989f9-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="989f9-117">Si le filtre en aval ne prend pas en charge DXVA 2,0, KsProxy alloue une mémoire tampon système supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="989f9-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="989f9-118">Elle utilise cette mémoire tampon pour copier les images vidéo de la mémoire VRAM vers la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="989f9-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="989f9-119">La méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) de l’exemple de média retourne un pointeur vers cette mémoire tampon système.</span><span class="sxs-lookup"><span data-stu-id="989f9-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="989f9-120">Toutefois, si le filtre en aval ne prend pas en charge DXVA 2,0, KsProxy n’alloue pas de mémoire tampon système.</span><span class="sxs-lookup"><span data-stu-id="989f9-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="989f9-121">Dans ce cas, la méthode **GetPointer** retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="989f9-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="989f9-122">Au lieu de cela, le filtre en aval est supposé accéder directement à la surface Direct3D de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="989f9-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="989f9-123">Il existe deux façons pour le filtre en aval d’obtenir un pointeur vers la surface, les deux équivalentes :</span><span class="sxs-lookup"><span data-stu-id="989f9-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="989f9-124">Interrogez l’exemple pour l’interface **IMFGetService** et appelez **GetService** pour l’interface **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="989f9-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="989f9-125">L’identificateur de service est un \_ service de mémoire tampon Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="989f9-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="989f9-126">Interrogez l’exemple pour l’interface [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) et appelez [**IMediaSample2Config :: GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span><span class="sxs-lookup"><span data-stu-id="989f9-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="989f9-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="989f9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989f9-128">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="989f9-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



