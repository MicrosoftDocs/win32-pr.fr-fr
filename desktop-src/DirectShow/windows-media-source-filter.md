---
description: Filtre de source Windows Media
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Filtre de source Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211223"
---
# <a name="windows-media-source-filter"></a>Filtre de source Windows Media

Ce filtre est le filtre source hérité pour le contenu® Windows Media. Il est utilisé par le lecteur Windows Media 6,4. En général, la méthode la plus simple et la plus fiable pour utiliser ce filtre consiste à utiliser le contrôle ActiveX du lecteur Windows Media 6,4. La plupart des méthodes exposées par ce filtre sont également exposées par le biais du contrôle ActiveX. Pour plus d’informations, consultez le kit de développement logiciel (SDK) du lecteur Windows Media.

Lorsque ce filtre reçoit le nom d’un fichier ASF local ou une URL pour un fichier distant, il lit le fichier, analyse les flux compressés et crée une broche de sortie pour chacun d’eux. Ce filtre n’utilise pas le kit de développement logiciel (SDK) du format Windows Media. Il utilise les versions du codec installables des décodeurs Windows Media, et non pas les versions d’DMO. La broche de sortie audio se connecte toujours au filtre du gestionnaire ACM ASF et le code confidentiel vidéo se connecte toujours au gestionnaire ICM ASF. (Dans ce cas, ICM fait référence au nom d’origine du gestionnaire de compression vidéo.) Le filtre ne prend pas en charge la recherche.

Le diagramme suivant montre un graphique de filtre avec ce filtre.

![graphique de filtre de source Windows Media](images/wms-wmv-graph.png)

Pour assurer la compatibilité descendante avec le lecteur Windows Media 6,4, ce filtre est le filtre source par défaut pour les fichiers avec les extensions de fichier. WMA,. wmv et. ASF. Pour la lecture de fichiers, les applications plus récentes doivent utiliser le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) . Toutefois, le lecteur ASF WM ne prend pas en charge la lecture de contenu diffusé en continu.

Le moyen le plus simple pour une application de lire du contenu multimédia Windows en continu consiste à utiliser le kit de développement logiciel (SDK) du lecteur Windows Media. Une autre option consiste à utiliser le kit de développement logiciel (SDK) du format Windows Media. La tentative de création d’un joueur personnalisé basé sur le filtre de source Windows Media n’est pas recommandée.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Types de média de broche d’entrée                    | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfaces pin d’entrée                     | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Types de média de broche de sortie                   | Varie en fonction des flux dans le fichier ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfaces de broche de sortie                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| CLSID du filtre                             | Voir les notes                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Exécutable                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Notes

Le CLSID du filtre n’est pas défini dans qnetwork. h. Utilisez cette macro dans votre propre fichier d’en-tête :


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtre de lecteur ASF WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



