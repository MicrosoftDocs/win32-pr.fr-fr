---
description: Filtre de convertisseur de mixage vidéo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtre de convertisseur de mixage vidéo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988af74dc2e4abac06215f283a496bb719384891
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989162"
---
# <a name="video-mixing-renderer-filter-7"></a>Filtre de convertisseur de mixage vidéo 7

cette rubrique s’applique à Windows XP ou version ultérieure.

dans Windows XP et versions ultérieures, le convertisseur de mixage vidéo 7 (VMR-7) est le convertisseur vidéo par défaut. Elle est appelée VMR-7 car en interne, elle utilise DirectDraw 7. Dans DirectX 9, un filtre similaire mais distinct, le VMR-9, est disponible pour la redistribution sur les systèmes non-XP. VMR-9 utilise Direct3D 9.

> [!Note]  
> VMR est disponible sur Windows XP et versions ultérieures. Elle n’est pas disponible via le package redistribuable DirectX, ni dans les versions précédentes de Windows. Pour la plupart des scénarios, les applications doivent utiliser le [convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md).

 

Les fonctionnalités de VMR sont les suivantes :

-   Vraie fusion alpha d’un maximum de 16 flux d’entrée
-   Accès à l’image composite avant son rendu
-   Modèle de plug-in qui permet à des tiers d’implémenter des effets vidéo personnalisés.
-   Prise en charge d’un maximum de 15 analyses.

au cours de la création de graphiques sur Windows XP et versions ultérieures, le gestionnaire de Graph de filtre n’utilise pas les filtres de Mixer de rendu vidéo ou de superposition les plus anciens, sauf si l’application les crée explicitement et s’ajoute au graphique.

Pour plus d’informations, consultez [utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md).




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | Tous les modes :<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li></ul>Mode fenêtre :<br /><ul><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Mode sans fenêtre :<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Mode de rendu :<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li></ul>mode de Mixer :<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li></ul>Pour plus d’informations sur les différents modes VMR-7, consultez <a href="vmr-modes-of-operation.md">modes de fonctionnement VMR</a>.<br /> | 
| Types de média de broche d’entrée | Type majeur : MEDIATYPE_VideoSubtype : dépend du matériel graphique. Doit être une vidéo non compressée.<br /> | 
| Interfaces pin d’entrée | <ul><li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (consultez la section Notes)</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li></ul> | 
| Types de média de broche de sortie | Non applicable. | 
| Interfaces de broche de sortie | Non applicable. | 
| CLSID du filtre | Deux CLSID sont associés à ce filtre :<ul><li>CLSID_VideoMixingRenderer : crée VMR-7. Si les ressources système sont insuffisantes pour créer VMR-7, l’appel à <strong>CoCreateInstance</strong> échoue.</li><li>CLSID_VideoRendererDefault : crée VMR-7 si les ressources système sont disponibles, ou crée l’ancien filtre de <a href="video-renderer-filter.md">convertisseur vidéo</a> .</li></ul>Utilisez CLSID_VideoMixingRenderer si vous avez besoin des fonctionnalités spécifiques de VMR-7. Dans le cas contraire, utilisez CLSID_VideoRendererDefault, qui est presque certain de ne pas échouer, car il revient à l’ancien filtre de convertisseur vidéo.<br /> | 
| CLSID de page de propriétés | Non applicable. | 
| Exécutable | Quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Remarques

La broche d’entrée expose l’interface **IOverlay** uniquement lorsque le filtre VMR-7 est en mode fenêtre. La seule méthode **IOverlay** implémentée par le code PIN est **GetWindowHandle**, ce qui permet à une application d’obtenir un handle vers la fenêtre vidéo du filtre. Toutes les autres méthodes **IOverlay** retournent E \_ NOTIMPL. En mode sans fenêtre, le filtre ne crée pas de fenêtre vidéo, donc le code pin n’expose pas l’interface.

Une application peut fournir un objet aslocator-Presenter personnalisé qui expose les interfaces suivantes :

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (facultatif)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (facultatif)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (facultatif)

Pour plus d’informations sur les aslocateurs personnalisés, consultez [fourniture d’une Allocator-Presenter personnalisée pour VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Une application peut également fournir un compositeur de plug-in personnalisé qui expose l’interface suivante :

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Pour configurer VMR avec un compositeur personnalisé, appelez [**IVMRFilterConfig :: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




