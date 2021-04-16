---
title: Afficher un bitmap fourni par une application sur l’image composite
description: Affichage d’un bitmap Application-Supplied sur l’image composite
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520575"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="060e3-103">Afficher un bitmap fourni par une application sur l’image composite</span><span class="sxs-lookup"><span data-stu-id="060e3-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="060e3-104">Les applications peuvent utiliser le mode de mixage de VMR pour afficher des logos de canal à contrôle alpha, une interface utilisateur ou des publications, partiellement ou complètement dans le rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="060e3-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="060e3-105">Étant donné que la fusion est effectuée sur le matériel par le processeur graphique, l’impact est minime sur les performances de lecture du flux vidéo et il n’y a pas d’artefacts de scintillement ou de destruction détectables.</span><span class="sxs-lookup"><span data-stu-id="060e3-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="060e3-106">Les applications peuvent modifier l’image affichée aussi souvent qu’elles le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="060e3-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="060e3-107">Notez que les modifications sont reflétées uniquement à l’écran lorsque le graphique de filtre DirectShow est à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="060e3-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="060e3-108">VMR utilise son composant mixer pour superposer l’image bitmap sur l’image composite.</span><span class="sxs-lookup"><span data-stu-id="060e3-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="060e3-109">Avec VMR-7, l’application doit forcer VMR à charger son mélangeur, même s’il n’y a qu’un seul flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="060e3-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="060e3-110">Cela n’est pas nécessaire avec VMR-9 puisqu’il charge son mélangeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="060e3-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="060e3-111">Pour fusionner une image bitmap statique avec le flux vidéo, l’application crée le VMR et l’ajoute au graphique, puis appelle [**IVMRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="060e3-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="060e3-112">La valeur transmise à cette fonction identifie le nombre de broches d’entrée que VMR doit créer.</span><span class="sxs-lookup"><span data-stu-id="060e3-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="060e3-113">Les applications peuvent spécifier n’importe quelle valeur comprise entre 1 et MAX \_ \_ , les flux de mixage ; la valeur 1 est valide si l’application ne souhaite afficher qu’un seul flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="060e3-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="060e3-114">Même si VMR-7 a une seule broche d’entrée par défaut, cette méthode doit être appelée pour forcer le chargement de son composant mixer.</span><span class="sxs-lookup"><span data-stu-id="060e3-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="060e3-115">(Le VMR-9 charge son mélangeur et configure quatre codes PIN par défaut.)</span><span class="sxs-lookup"><span data-stu-id="060e3-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="060e3-116">Pour définir l’image bitmap, utilisez l’interface [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) sur l’interface VMR-7 ou [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) sur VMR-9.</span><span class="sxs-lookup"><span data-stu-id="060e3-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="060e3-117">La bitmap peut être spécifiée par un handle vers un contexte de périphérique GDI (hDC) ou par une interface de surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="060e3-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="060e3-118">Si l’application souhaite que l’image contienne des informations alpha incorporées (également appelées par pixel alpha), elle doit placer les données d’image dans une interface de surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="060e3-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="060e3-119">Cela est dû au fait qu’il n’est pas possible actuellement de placer des informations alpha par pixel avec un contexte de périphérique GDI.</span><span class="sxs-lookup"><span data-stu-id="060e3-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="060e3-120">La surface DirectDraw doit être RGB32 ou ARGB32 et doit être de préférence une surface de mémoire système.</span><span class="sxs-lookup"><span data-stu-id="060e3-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="060e3-121">Il n’est pas nécessaire que les dimensions de surface soient une puissance de 2.</span><span class="sxs-lookup"><span data-stu-id="060e3-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="060e3-122">VMR permet aux applications de spécifier l’emplacement et une valeur de transparence globale pour l’image.</span><span class="sxs-lookup"><span data-stu-id="060e3-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="060e3-123">Le code suivant montre comment passer des données d’image à VMR pour la fusion suivante :</span><span class="sxs-lookup"><span data-stu-id="060e3-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



<span data-ttu-id="060e3-124">Les concepts abordés dans cette rubrique sont illustrés dans l’exemple d’application [VMRPlayer](vmrplayer-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="060e3-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="060e3-125">**Création d’animations simples avec l’image bitmap**</span><span class="sxs-lookup"><span data-stu-id="060e3-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="060e3-126">Pour créer un logo simple animé simple, placez tous les « frames » bitmap dans une seule image, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="060e3-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![bande d’images VMR](images/vmr-image-strip.png)

<span data-ttu-id="060e3-128">Lorsque vous définissez initialement la bitmap à l’aide de [**IVMRMixerBitmap :: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), si la bitmap se trouve dans un HDC, définissez le champ **rSrc** de la structure **VMRALPHABITMAP** pour spécifier la taille de l’image bitmap entière au sein du HDC.</span><span class="sxs-lookup"><span data-stu-id="060e3-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="060e3-129">Les membres **supérieur** et **gauche** de la structure ont la valeur 0, et les membres de **droite** et **inférieurs** sont la largeur et la hauteur de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="060e3-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="060e3-130">Si la bitmap se trouve dans une surface DirectDraw, la taille de la surface est connue. il n’est donc pas nécessaire de spécifier rSrc dans cette méthode.</span><span class="sxs-lookup"><span data-stu-id="060e3-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="060e3-131">Quand vous appelez [**IVMRMixerBitmap :: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), utilisez le membre **rSrc** pour les bitmaps HDC et DirectDraw, pour spécifier le cadre ou le rectangle particulier dans l’image que vous souhaitez afficher, et définir l’indicateur **VMRBITMAP \_ SRCRECT** dans le membre **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="060e3-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="060e3-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="060e3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="060e3-133">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="060e3-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



