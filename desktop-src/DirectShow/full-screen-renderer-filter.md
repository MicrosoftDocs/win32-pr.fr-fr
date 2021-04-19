---
description: Filtre de convertisseur plein écran
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filtre de convertisseur plein écran
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d580442887896f271b0f5b7fea5f7a33553f53f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515889"
---
# <a name="full-screen-renderer-filter"></a>Filtre de convertisseur plein écran

Le filtre de convertisseur plein écran fournit un rendu vidéo plein écran sur un matériel plus ancien. Les cartes vidéo plus récentes peuvent étirer la vidéo suffisamment efficacement pour que le convertisseur plein écran ne soit pas nécessaire. Par conséquent, l’utilisation de ce filtre est désormais déconseillée.

N’ajoutez pas manuellement ce filtre au graphique de filtre. Si une application appelle [**IVideoWindow ::p ut \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode), le gestionnaire de graphique de filtre sélectionne automatiquement le convertisseur de vidéo approprié pour le mode plein écran. La sélection est transparente pour l’application. Avec les cartes vidéo actuelles, il est peu probable que le gestionnaire de graphique de filtre sélectionne le convertisseur plein écran.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFullScreenVideoEx**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Types de média de broche de sortie                   | Non applicable                                                                                                                                                                                                                                     |
| Interfaces de broche de sortie                    | Non applicable                                                                                                                                                                                                                                     |
| CLSID du filtre                             | CLSID \_ ModexRenderer                                                                                                                                                                                                                               |
| CLSID de page de propriétés                      | CLSID \_ ModexProperties                                                                                                                                                                                                                             |
| Exécutable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                                                                                                                                                                    |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Notes

Le convertisseur plein écran prend en charge un ensemble statique de modes d’affichage. Toutefois, la carte vidéo sur le système de l’utilisateur ne prend peut-être pas en charge tous les modes. Pour déterminer si la carte prend en charge un mode particulier, appelez la méthode [**IFullScreenVideoEx :: IsModeAvailable**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) . Vous pouvez également désactiver un mode d’affichage particulier par programme, en appelant [**IFullScreenVideoEx :: SetEnabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled). Le convertisseur plein écran prend actuellement en charge les modes d’affichage indiqués dans le tableau suivant :



|      |       |        |           |
|------|-------|--------|-----------|
| Mode | Largeur | Hauteur | Profondeur de bit |
| 0    | 320   | 200    | 16        |
| 1    | 320   | 200    | 8         |
| 2    | 320   | 240    | 16        |
| 3    | 320   | 240    | 8         |
| 4    | 640   | 400    | 16        |
| 5    | 640   | 400    | 8         |
| 6    | 640   | 480    | 16        |
| 7    | 640   | 480    | 8         |
| 8    | 800   | 600    | 16        |
| 9    | 800   | 600    | 8         |
| 10   | 1 024  | 768    | 16        |
| 11   | 1 024  | 768    | 8         |
| 12   | 1152  | 864    | 16        |
| 13   | 1152  | 864    | 8         |
| 14   | 1 280  | 1 024   | 16        |
| 15   | 1 280  | 1 024   | 8         |



 

(Tous les modes sont RVB.) Toutefois, cette liste est sujette à modification. Utilisez la méthode [**IFullScreenVideoEx :: GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) pour obtenir des informations sur les modes. Le convertisseur plein écran choisit toujours le mode de résolution le plus bas disponible, limité par une propriété appelée *facteur de clip*, qui détermine la quantité de vidéo que le convertisseur plein écran est autorisé à découper. Pour plus d’informations, consultez [**IFullScreenVideoEx :: GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Lorsque l’application exécute ou interrompt le graphique de filtre, le convertisseur plein écran bascule en mode d’affichage choisi. Lorsque le graphique s’arrête, le convertisseur plein écran restaure le mode d’affichage d’origine.

Le convertisseur plein écran peut uniquement fonctionner en tant que fenêtre active de premier plan. Si l’utilisateur bascule vers une autre application, le convertisseur plein écran masque la vidéo en réduisant ou en masquant la fenêtre vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



