---
description: Interfaces pour le rendu et la superposition vidéo
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Interfaces pour le rendu et la superposition vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747101"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a><span data-ttu-id="2316b-103">Interfaces pour le rendu et la superposition vidéo</span><span class="sxs-lookup"><span data-stu-id="2316b-103">Interfaces for Video Rendering and Overlay</span></span>

<span data-ttu-id="2316b-104">Ces interfaces prennent en charge le contrôle d’application sur le rendu vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-104">These interfaces support application control over video rendering.</span></span> <span data-ttu-id="2316b-105">Notez que certaines de ces interfaces sont maintenant dépréciées, car le filtre de convertisseur de mixage vidéo offre un meilleur contrôle de rendu et de superposition.</span><span class="sxs-lookup"><span data-stu-id="2316b-105">Note that some of these interfaces are now deprecated, because the Video Mixing Renderer filter provides superior rendering and overlay control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2316b-106">Interface</span><span class="sxs-lookup"><span data-stu-id="2316b-106">Interface</span></span></th>
<th><span data-ttu-id="2316b-107">Description</span><span class="sxs-lookup"><span data-stu-id="2316b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2316b-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span></span></td>
<td><span data-ttu-id="2316b-109">Permet d’accéder aux informations et aux paramètres de sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="2316b-109">Provides access to closed-captioned information and settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2316b-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span></span></td>
<td><span data-ttu-id="2316b-111">Appliquez des effets de superposition à la surface vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-111">Apply overlay effects to the video surface.</span></span> <span data-ttu-id="2316b-112">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="2316b-112">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2316b-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span></span></td>
<td><span data-ttu-id="2316b-114">Contrôler la façon dont DirectShow met à l’échelle une image vidéo si la fenêtre vidéo est plus petite que la taille native de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-114">Control how DirectShow scales a video image if the video window is smaller than the native size of the video.</span></span> <span data-ttu-id="2316b-115">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="2316b-115">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2316b-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></td>
<td><span data-ttu-id="2316b-117">Définissez les propriétés de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-117">Set video properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2316b-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span></span></td>
<td><span data-ttu-id="2316b-119">Affichez la vidéo en mode plein écran exclusif Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2316b-119">Render video in Microsoft DirectDraw exclusive full-screen mode.</span></span> <span data-ttu-id="2316b-120">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="2316b-120">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2316b-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span></span></td>
<td><span data-ttu-id="2316b-122">Interface de rappel pour recevoir une notification concernant les modifications apportées à la position, à la taille et à la visibilité de la superposition.</span><span class="sxs-lookup"><span data-stu-id="2316b-122">Callback interface to receive notification about changes to the overlay position, size, and visibility.</span></span> <span data-ttu-id="2316b-123">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="2316b-123">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2316b-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span></span></td>
<td><span data-ttu-id="2316b-125">Désactive les fonctionnalités DirectDraw spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2316b-125">Disable specified DirectDraw capabilities.</span></span> <span data-ttu-id="2316b-126">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="2316b-126">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2316b-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span></span></td>
<td><span data-ttu-id="2316b-128">Accédez à une surface DirectDraw allouée par le filtre de <a href="overlay-mixer-filter.md">mixage de superposition</a> . (Déconseillé.)</span><span class="sxs-lookup"><span data-stu-id="2316b-128">Access a DirectDraw surface allocated by the <a href="overlay-mixer-filter.md">Overlay Mixer</a> filter.(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2316b-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span></span></td>
<td><span data-ttu-id="2316b-130">Implémenté sur le mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="2316b-130">Implemented on the Overlay Mixer.</span></span> <span data-ttu-id="2316b-131">Permet aux clients sans fenêtre tels que les contrôles de® ActiveX d’acquérir et de définir les propriétés du rectangle vidéo et de conseiller le filtre des événements.</span><span class="sxs-lookup"><span data-stu-id="2316b-131">Enables windowless clients such as ActiveX® controls to get and set properties of the video rectangle and advise the filter of events.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2316b-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span></span></td>
<td><span data-ttu-id="2316b-133">Implémenté par les clients sans fenêtre et appelé par le mélangeur de superposition pour envoyer des notifications d’événements affectant le rectangle d’affichage de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-133">Implemented by windowless clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2316b-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span></span></td>
<td><span data-ttu-id="2316b-135">Définissez les contrôles de couleur vidéo sur le filtre de mixage de superposition lors du mélange de plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-135">Set video color controls on the Overlay Mixer filter when mixing multiple video streams.</span></span> <span data-ttu-id="2316b-136">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="2316b-136">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2316b-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></td>
<td><span data-ttu-id="2316b-138">Interroger un convertisseur vidéo pour obtenir des informations sur les performances.</span><span class="sxs-lookup"><span data-stu-id="2316b-138">Query a video renderer for performance information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2316b-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></td>
<td><span data-ttu-id="2316b-140">Définissez les propriétés de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="2316b-140">Set video window properties.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="2316b-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="2316b-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="2316b-155">Interfaces du convertisseur de mixage vidéo 9.</span><span class="sxs-lookup"><span data-stu-id="2316b-155">Video Mixing Renderer 9 interfaces.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2316b-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="2316b-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="2316b-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="2316b-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span></span></li>
<li><span data-ttu-id="2316b-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span></span></li>
<li><span data-ttu-id="2316b-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span></span></li>
<li><span data-ttu-id="2316b-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
<li><span data-ttu-id="2316b-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
<li><span data-ttu-id="2316b-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span></span></li>
<li><span data-ttu-id="2316b-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
<li><span data-ttu-id="2316b-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2316b-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="2316b-167">Interfaces du convertisseur de mixage vidéo 7.</span><span class="sxs-lookup"><span data-stu-id="2316b-167">Video Mixing Renderer 7 interfaces.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2316b-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2316b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2316b-169">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="2316b-169">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



