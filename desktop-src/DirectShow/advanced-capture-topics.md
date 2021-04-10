---
description: Rubriques avancées sur la capture
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Rubriques avancées sur la capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109546"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="8f9c6-103">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="8f9c6-103">Advanced Capture Topics</span></span>

<span data-ttu-id="8f9c6-104">Cette section décrit certains aspects avancés de la capture vidéo dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8f9c6-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="8f9c6-105">La plupart des problèmes décrits dans cette section sont gérés automatiquement par l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="8f9c6-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="8f9c6-106">Toutefois, les informations fournies ici peuvent être utiles si vous devez dépanner une application de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8f9c6-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="8f9c6-107">Vous devez également lire cette section si votre application génère un graphique de capture personnalisé d’un certain type et que ICaptureGraphBuilder2 ne répond pas à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8f9c6-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="8f9c6-108">Enfin, cette section contient des informations sur l’utilisation du filtre de mixage vidéo (VMR) dans une application de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8f9c6-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="8f9c6-109">Il est possible de créer un graphique de capture vidéo entièrement à l’aide des méthodes [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8f9c6-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="8f9c6-110">Vous pouvez également combiner les deux interfaces, à l’aide de ICaptureGraphBuilder2 pour certaines tâches et IGraphBuilder pour d’autres.</span><span class="sxs-lookup"><span data-stu-id="8f9c6-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="8f9c6-111">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f9c6-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="8f9c6-112">Gestion des événements de redessin dans la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8f9c6-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="8f9c6-113">Utilisation des catégories de code confidentiel</span><span class="sxs-lookup"><span data-stu-id="8f9c6-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="8f9c6-114">Utilisation du filtre tee Smart</span><span class="sxs-lookup"><span data-stu-id="8f9c6-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="8f9c6-115">Utilisation du mélangeur de superposition dans la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8f9c6-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="8f9c6-116">Broches de port vidéo</span><span class="sxs-lookup"><span data-stu-id="8f9c6-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="8f9c6-117">Type de format VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="8f9c6-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="8f9c6-118">Création de filtres de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="8f9c6-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="8f9c6-119">Filtres de pilote de classe WDM</span><span class="sxs-lookup"><span data-stu-id="8f9c6-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="8f9c6-120">Utilisation de la capture WDDM dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f9c6-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="8f9c6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f9c6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9c6-122">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8f9c6-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



