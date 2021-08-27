---
description: Filtre de convertisseur de mixage vidéo 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtre de convertisseur de mixage vidéo 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2077679599db45ab80e7be931a83f500c156405c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466586"
---
# <a name="video-mixing-renderer-filter-9"></a>Filtre de convertisseur de mixage vidéo 9

Dans DirectX 9, le filtre de mixage vidéo 9 (VMR-9) offre des fonctionnalités de rendu vidéo avancées sur toutes les plateformes prises en charge par DirectX. Il est entièrement intégré aux fonctionnalités 3D de DirectX 9. Par exemple, vous pouvez facilement ajouter de la vidéo aux jeux et à d’autres environnements 3D ou transformer des images vidéo à l’aide des nuanceurs de pixels Direct3D et d’autres effets.

Ce filtre ne prend pas en charge les ports vidéo.

Pour assurer la compatibilité descendante, VMR-9 n’est pas le convertisseur par défaut sur un système. Pour utiliser ce filtre, ajoutez-le explicitement au graphique de filtre et configurez-le avant de connecter les broches d’entrée. VMR-9 utilise son propre ensemble d’interfaces, de structures et d’énumérations, qui ne sont pas toujours identiques aux types de données correspondants utilisés avec VMR-7.

VMR-9 prend en charge jusqu’à 16 moniteurs.




| | | Filtrer les interfaces | VMR-9 prend en charge plusieurs modes de rendu distincts. Il prend en charge un autre ensemble d’interfaces en fonction du mode de rendu :<br /><ul><li>Tous les modes : <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Mode rendu non restitué : <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>Mode fenêtre : <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>Mode sans fenêtre : <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>Pour définir le mode de rendu, appelez <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9 :: SetRenderingMode</strong></a>. Pour plus d’informations, consultez <a href="vmr-modes-of-operation.md">modes de fonctionnement VMR</a>.<br /> | | Types de média de broche d’entrée | Les broches d’entrée se connectent avec n’importe quel type pris en charge par le matériel vidéo sous-jacent. | | Interfaces pin d’entrée | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | | Types de média de broche de sortie | Non applicable. | | Interfaces de broche de sortie | Non applicable. | | CLSID du filtre | CLSID_VideoMixingRenderer9 | | CLSID de page de propriétés | N/A | | Fichier exécutable | Quartz.dll | | <a href="merit.md">Mérite</a> | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Remarques

Une application peut fournir un objet aslocator-Presenter personnalisé qui expose les interfaces suivantes :

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (facultatif)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (facultatif)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (facultatif)

Pour plus d’informations sur les aslocateurs personnalisés, consultez [fourniture d’une Allocator-Presenter personnalisée pour VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Une application peut également fournir un compositeur de plug-in personnalisé qui expose l’interface suivante :

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Pour configurer VMR avec un compositeur personnalisé, appelez [**IVMRFilterConfig9 :: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




