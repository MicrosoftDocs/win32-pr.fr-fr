---
description: Filtre de convertisseur de mixage vidéo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtre de convertisseur de mixage vidéo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527813"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="00fab-103">Filtre de convertisseur de mixage vidéo 7</span><span class="sxs-lookup"><span data-stu-id="00fab-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="00fab-104">Cette rubrique s’applique à Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="00fab-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="00fab-105">Dans Windows XP et versions ultérieures, le convertisseur de mixage vidéo 7 (VMR-7) est le convertisseur vidéo par défaut.</span><span class="sxs-lookup"><span data-stu-id="00fab-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="00fab-106">Elle est appelée VMR-7 car en interne, elle utilise DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="00fab-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="00fab-107">Dans DirectX 9, un filtre similaire mais distinct, le VMR-9, est disponible pour la redistribution sur les systèmes non-XP.</span><span class="sxs-lookup"><span data-stu-id="00fab-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="00fab-108">VMR-9 utilise Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="00fab-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="00fab-109">VMR est disponible sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="00fab-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="00fab-110">Elle n’est pas disponible via le package redistribuable DirectX ou sur les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="00fab-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="00fab-111">Pour la plupart des scénarios, les applications doivent utiliser le [convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md).</span><span class="sxs-lookup"><span data-stu-id="00fab-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="00fab-112">Les fonctionnalités de VMR sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00fab-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="00fab-113">Vraie fusion alpha d’un maximum de 16 flux d’entrée</span><span class="sxs-lookup"><span data-stu-id="00fab-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="00fab-114">Accès à l’image composite avant son rendu</span><span class="sxs-lookup"><span data-stu-id="00fab-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="00fab-115">Modèle de plug-in qui permet à des tiers d’implémenter des effets vidéo personnalisés.</span><span class="sxs-lookup"><span data-stu-id="00fab-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="00fab-116">Prise en charge d’un maximum de 15 analyses.</span><span class="sxs-lookup"><span data-stu-id="00fab-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="00fab-117">Lors de la génération du graphique sur Windows XP et versions ultérieures, le gestionnaire de graphique de filtre n’utilise pas les filtres de convertisseur de vidéo ou de mixage de superposition antérieurs, à moins que l’application ne les crée explicitement et les ajoute au graphique.</span><span class="sxs-lookup"><span data-stu-id="00fab-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="00fab-118">Pour plus d’informations, consultez [utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="00fab-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00fab-119">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="00fab-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="00fab-120">Tous les modes :</span><span class="sxs-lookup"><span data-stu-id="00fab-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="00fab-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="00fab-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="00fab-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="00fab-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="00fab-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="00fab-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="00fab-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="00fab-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="00fab-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="00fab-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="00fab-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="00fab-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="00fab-133">Mode fenêtre :</span><span class="sxs-lookup"><span data-stu-id="00fab-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="00fab-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="00fab-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="00fab-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="00fab-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="00fab-138">Mode sans fenêtre :</span><span class="sxs-lookup"><span data-stu-id="00fab-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="00fab-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="00fab-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="00fab-141">Mode de rendu :</span><span class="sxs-lookup"><span data-stu-id="00fab-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="00fab-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="00fab-143">Mode de mixage :</span><span class="sxs-lookup"><span data-stu-id="00fab-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="00fab-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="00fab-145">Pour plus d’informations sur les différents modes VMR-7, consultez <a href="vmr-modes-of-operation.md">modes de fonctionnement VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="00fab-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00fab-146">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="00fab-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="00fab-147">Type majeur : MEDIATYPE_VideoSubtype : dépend du matériel graphique.</span><span class="sxs-lookup"><span data-stu-id="00fab-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="00fab-148">Doit être une vidéo non compressée.</span><span class="sxs-lookup"><span data-stu-id="00fab-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00fab-149">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="00fab-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="00fab-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="00fab-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="00fab-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (consultez la section Notes)</span><span class="sxs-lookup"><span data-stu-id="00fab-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="00fab-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="00fab-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="00fab-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="00fab-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="00fab-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00fab-157">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="00fab-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="00fab-158">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="00fab-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00fab-159">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="00fab-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="00fab-160">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="00fab-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00fab-161">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="00fab-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="00fab-162">Deux CLSID sont associés à ce filtre :</span><span class="sxs-lookup"><span data-stu-id="00fab-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="00fab-163">CLSID_VideoMixingRenderer : crée VMR-7.</span><span class="sxs-lookup"><span data-stu-id="00fab-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="00fab-164">Si les ressources système sont insuffisantes pour créer VMR-7, l’appel à <strong>CoCreateInstance</strong> échoue.</span><span class="sxs-lookup"><span data-stu-id="00fab-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="00fab-165">CLSID_VideoRendererDefault : crée VMR-7 si les ressources système sont disponibles, ou crée l’ancien filtre de <a href="video-renderer-filter.md">convertisseur vidéo</a> .</span><span class="sxs-lookup"><span data-stu-id="00fab-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="00fab-166">Utilisez CLSID_VideoMixingRenderer si vous avez besoin des fonctionnalités spécifiques de VMR-7.</span><span class="sxs-lookup"><span data-stu-id="00fab-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="00fab-167">Dans le cas contraire, utilisez CLSID_VideoRendererDefault, qui est presque certain de ne pas échouer, car il revient à l’ancien filtre de convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="00fab-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00fab-168">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="00fab-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="00fab-169">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="00fab-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00fab-170">Exécutable</span><span class="sxs-lookup"><span data-stu-id="00fab-170">Executable</span></span></td>
<td><span data-ttu-id="00fab-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="00fab-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00fab-172"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="00fab-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="00fab-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="00fab-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00fab-174"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="00fab-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="00fab-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="00fab-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="00fab-176">Notes</span><span class="sxs-lookup"><span data-stu-id="00fab-176">Remarks</span></span>

<span data-ttu-id="00fab-177">La broche d’entrée expose l’interface **IOverlay** uniquement lorsque le filtre VMR-7 est en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00fab-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="00fab-178">La seule méthode **IOverlay** implémentée par le code PIN est **GetWindowHandle**, ce qui permet à une application d’obtenir un handle vers la fenêtre vidéo du filtre.</span><span class="sxs-lookup"><span data-stu-id="00fab-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="00fab-179">Toutes les autres méthodes **IOverlay** retournent E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="00fab-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="00fab-180">En mode sans fenêtre, le filtre ne crée pas de fenêtre vidéo, donc le code pin n’expose pas l’interface.</span><span class="sxs-lookup"><span data-stu-id="00fab-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="00fab-181">Une application peut fournir un objet aslocator-Presenter personnalisé qui expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="00fab-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="00fab-182">**IVMRImagePresenter**</span><span class="sxs-lookup"><span data-stu-id="00fab-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="00fab-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="00fab-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="00fab-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="00fab-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="00fab-185">**IVMRSurfaceAllocator**</span><span class="sxs-lookup"><span data-stu-id="00fab-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="00fab-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="00fab-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="00fab-187">Pour plus d’informations sur les aslocateurs personnalisés, consultez [fourniture d’une Allocator-Presenter personnalisée pour VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span><span class="sxs-lookup"><span data-stu-id="00fab-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="00fab-188">Une application peut également fournir un compositeur de plug-in personnalisé qui expose l’interface suivante :</span><span class="sxs-lookup"><span data-stu-id="00fab-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="00fab-189">**IVMRImageCompositor**</span><span class="sxs-lookup"><span data-stu-id="00fab-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="00fab-190">Pour configurer VMR avec un compositeur personnalisé, appelez [**IVMRFilterConfig :: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="00fab-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00fab-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="00fab-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00fab-192">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="00fab-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




