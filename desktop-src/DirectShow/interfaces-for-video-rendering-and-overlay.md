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
# <a name="interfaces-for-video-rendering-and-overlay"></a>Interfaces pour le rendu et la superposition vidéo

Ces interfaces prennent en charge le contrôle d’application sur le rendu vidéo. Notez que certaines de ces interfaces sont maintenant dépréciées, car le filtre de convertisseur de mixage vidéo offre un meilleur contrôle de rendu et de superposition.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Interface</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></td>
<td>Permet d’accéder aux informations et aux paramètres de sous-titrage.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></td>
<td>Appliquez des effets de superposition à la surface vidéo. (Déconseillée).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></td>
<td>Contrôler la façon dont DirectShow met à l’échelle une image vidéo si la fenêtre vidéo est plus petite que la taille native de la vidéo. (Déconseillée).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></td>
<td>Définissez les propriétés de la vidéo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></td>
<td>Affichez la vidéo en mode plein écran exclusif Microsoft DirectDraw. (Déconseillée).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></td>
<td>Interface de rappel pour recevoir une notification concernant les modifications apportées à la position, à la taille et à la visibilité de la superposition. (Déconseillée).</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></td>
<td>Désactive les fonctionnalités DirectDraw spécifiées. (Déconseillée).</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></td>
<td>Accédez à une surface DirectDraw allouée par le filtre de <a href="overlay-mixer-filter.md">mixage de superposition</a> . (Déconseillé.)</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></td>
<td>Implémenté sur le mélangeur de superposition. Permet aux clients sans fenêtre tels que les contrôles de® ActiveX d’acquérir et de définir les propriétés du rectangle vidéo et de conseiller le filtre des événements.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></td>
<td>Implémenté par les clients sans fenêtre et appelé par le mélangeur de superposition pour envoyer des notifications d’événements affectant le rectangle d’affichage de la vidéo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></td>
<td>Définissez les contrôles de couleur vidéo sur le filtre de mixage de superposition lors du mélange de plusieurs flux vidéo. (Déconseillée).</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></td>
<td>Interroger un convertisseur vidéo pour obtenir des informations sur les performances.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></td>
<td>Définissez les propriétés de la fenêtre vidéo.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul></td>
<td>Interfaces du convertisseur de mixage vidéo 9.</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li>
</ul></td>
<td>Interfaces du convertisseur de mixage vidéo 7.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



