---
description: Filtre de convertisseur de mixage vidéo 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtre de convertisseur de mixage vidéo 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757672"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="59aa1-103">Filtre de convertisseur de mixage vidéo 9</span><span class="sxs-lookup"><span data-stu-id="59aa1-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="59aa1-104">Dans DirectX 9, le filtre de mixage vidéo 9 (VMR-9) offre des fonctionnalités de rendu vidéo avancées sur toutes les plateformes prises en charge par DirectX.</span><span class="sxs-lookup"><span data-stu-id="59aa1-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="59aa1-105">Il est entièrement intégré aux fonctionnalités 3D de DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="59aa1-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="59aa1-106">Par exemple, vous pouvez facilement ajouter de la vidéo aux jeux et à d’autres environnements 3D ou transformer des images vidéo à l’aide des nuanceurs de pixels Direct3D et d’autres effets.</span><span class="sxs-lookup"><span data-stu-id="59aa1-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="59aa1-107">Ce filtre ne prend pas en charge les ports vidéo.</span><span class="sxs-lookup"><span data-stu-id="59aa1-107">This filter does not support video ports.</span></span>

<span data-ttu-id="59aa1-108">Pour assurer la compatibilité descendante, VMR-9 n’est pas le convertisseur par défaut sur un système.</span><span class="sxs-lookup"><span data-stu-id="59aa1-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="59aa1-109">Pour utiliser ce filtre, ajoutez-le explicitement au graphique de filtre et configurez-le avant de connecter les broches d’entrée.</span><span class="sxs-lookup"><span data-stu-id="59aa1-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="59aa1-110">VMR-9 utilise son propre ensemble d’interfaces, de structures et d’énumérations, qui ne sont pas toujours identiques aux types de données correspondants utilisés avec VMR-7.</span><span class="sxs-lookup"><span data-stu-id="59aa1-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="59aa1-111">VMR-9 prend en charge jusqu’à 16 moniteurs.</span><span class="sxs-lookup"><span data-stu-id="59aa1-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59aa1-112">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="59aa1-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="59aa1-113">VMR-9 prend en charge plusieurs modes de rendu distincts.</span><span class="sxs-lookup"><span data-stu-id="59aa1-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="59aa1-114">Il prend en charge un autre ensemble d’interfaces en fonction du mode de rendu :</span><span class="sxs-lookup"><span data-stu-id="59aa1-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="59aa1-115">Tous les modes : <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="59aa1-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="59aa1-116">Mode rendu non restitué : <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="59aa1-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="59aa1-117">Mode fenêtre : <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="59aa1-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="59aa1-118">Mode sans fenêtre : <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="59aa1-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="59aa1-119">Pour définir le mode de rendu, appelez <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9 :: SetRenderingMode</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="59aa1-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="59aa1-120">Pour plus d’informations, consultez <a href="vmr-modes-of-operation.md">modes de fonctionnement VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="59aa1-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59aa1-121">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="59aa1-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="59aa1-122">Les broches d’entrée se connectent avec n’importe quel type pris en charge par le matériel vidéo sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="59aa1-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59aa1-123">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="59aa1-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="59aa1-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="59aa1-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59aa1-125">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="59aa1-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="59aa1-126">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="59aa1-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59aa1-127">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="59aa1-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="59aa1-128">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="59aa1-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59aa1-129">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="59aa1-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="59aa1-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="59aa1-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59aa1-131">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="59aa1-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="59aa1-132">N/A</span><span class="sxs-lookup"><span data-stu-id="59aa1-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59aa1-133">Exécutable</span><span class="sxs-lookup"><span data-stu-id="59aa1-133">Executable</span></span></td>
<td><span data-ttu-id="59aa1-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="59aa1-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59aa1-135"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="59aa1-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="59aa1-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="59aa1-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59aa1-137"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="59aa1-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="59aa1-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="59aa1-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="59aa1-139">Notes</span><span class="sxs-lookup"><span data-stu-id="59aa1-139">Remarks</span></span>

<span data-ttu-id="59aa1-140">Une application peut fournir un objet aslocator-Presenter personnalisé qui expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="59aa1-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="59aa1-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="59aa1-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="59aa1-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="59aa1-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="59aa1-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="59aa1-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="59aa1-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="59aa1-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="59aa1-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="59aa1-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="59aa1-146">Pour plus d’informations sur les aslocateurs personnalisés, consultez [fourniture d’une Allocator-Presenter personnalisée pour VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span><span class="sxs-lookup"><span data-stu-id="59aa1-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="59aa1-147">Une application peut également fournir un compositeur de plug-in personnalisé qui expose l’interface suivante :</span><span class="sxs-lookup"><span data-stu-id="59aa1-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="59aa1-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="59aa1-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="59aa1-149">Pour configurer VMR avec un compositeur personnalisé, appelez [**IVMRFilterConfig9 :: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="59aa1-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59aa1-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59aa1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59aa1-151">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="59aa1-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="59aa1-152">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="59aa1-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




