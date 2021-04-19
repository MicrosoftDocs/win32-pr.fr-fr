---
description: Cette rubrique est l’étape 2 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Étape 2 : déclarer CVideoRenderer et les classes dérivées'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544998"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="8a2d2-103">Étape 2 : déclarer CVideoRenderer et les classes dérivées</span><span class="sxs-lookup"><span data-stu-id="8a2d2-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="8a2d2-104">Cette rubrique est l’étape 2 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="8a2d2-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="8a2d2-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="8a2d2-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="8a2d2-106">DirectShow fournit plusieurs filtres différents qui restituent la vidéo :</span><span class="sxs-lookup"><span data-stu-id="8a2d2-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="8a2d2-107">[**Filtre de convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="8a2d2-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="8a2d2-108">[Filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="8a2d2-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="8a2d2-109">[Filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="8a2d2-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="8a2d2-110">Pour plus d’informations sur les différences entre ces filtres, consultez [choix du convertisseur vidéo approprié](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="8a2d2-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="8a2d2-111">Dans ce didacticiel, la classe abstraite suivante est utilisée pour encapsuler le filtre de convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



<span data-ttu-id="8a2d2-112">Remarques :</span><span class="sxs-lookup"><span data-stu-id="8a2d2-112">Notes:</span></span>

-   <span data-ttu-id="8a2d2-113">La `HasVideo` méthode retourne la **valeur true** si le convertisseur vidéo a été créé.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="8a2d2-114">La `AddToGraph` méthode ajoute le convertisseur vidéo au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="8a2d2-115">La `FinalizeGraph` méthode termine l’étape de création de graphiques.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="8a2d2-116">La `UpdateVideoWindow` méthode met à jour le rectangle de destination de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="8a2d2-117">La `Repaint` méthode redessine le frame vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="8a2d2-118">La `DisplayModeChanged` méthode gère les modifications du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="8a2d2-119">Chacune de ces méthodes est décrite en détail plus loin dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="8a2d2-120">Ensuite, déclarez une classe dérivée pour encapsuler chacun des trois convertisseurs vidéo : EVR, VMR-9 et VMR-7.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="8a2d2-121">CEVR, classe</span><span class="sxs-lookup"><span data-stu-id="8a2d2-121">CEVR Class</span></span>

<span data-ttu-id="8a2d2-122">La `CEVR` classe gère le EVR.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="8a2d2-123">Elle contient un pointeur vers les interfaces [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) et [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) de EVR.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a><span data-ttu-id="8a2d2-124">CVMR9, classe</span><span class="sxs-lookup"><span data-stu-id="8a2d2-124">CVMR9 Class</span></span>

<span data-ttu-id="8a2d2-125">La `CVMR9` classe gère VMR-9.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="8a2d2-126">Il contient un pointeur vers l’interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="8a2d2-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a><span data-ttu-id="8a2d2-127">CVMR7, classe</span><span class="sxs-lookup"><span data-stu-id="8a2d2-127">CVMR7 Class</span></span>

<span data-ttu-id="8a2d2-128">La `CVMR7` classe gère VMR-7.</span><span class="sxs-lookup"><span data-stu-id="8a2d2-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="8a2d2-129">Il contient un pointeur vers l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="8a2d2-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



<span data-ttu-id="8a2d2-130">[Étape 3 : générer le graphique de filtre](step-3--build-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="8a2d2-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a2d2-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a2d2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a2d2-132">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a2d2-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="8a2d2-133">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="8a2d2-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="8a2d2-134">Rendu vidéo</span><span class="sxs-lookup"><span data-stu-id="8a2d2-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
