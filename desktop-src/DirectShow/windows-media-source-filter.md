---
description: Windows Filtre de source de média
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Filtre de source de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa8e2c2f2e575a70d85fdce3d9b8d643e270f721
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238806"
---
# <a name="windows-media-source-filter"></a>Windows Filtre de source de média

ce filtre est le filtre source hérité pour Windows contenu multimédia®. elle est utilisée par Lecteur Windows Media 6,4. en général, la méthode la plus simple et la plus fiable pour utiliser ce filtre consiste à utiliser le contrôle Lecteur Windows Media 6,4 ActiveX. la plupart des méthodes exposées par ce filtre sont également exposées par le biais du contrôle ActiveX. pour plus d’informations, consultez le kit de développement logiciel (SDK) Lecteur Windows Media.

Lorsque ce filtre reçoit le nom d’un fichier ASF local ou une URL pour un fichier distant, il lit le fichier, analyse les flux compressés et crée une broche de sortie pour chacun d’eux. ce filtre n’utilise pas le kit de développement logiciel (SDK) Format multimédia Windows. il utilise les versions du codec installables des décodeurs Windows Media, et non pas les versions DMO. la broche de sortie audio se connecte toujours au filtre du gestionnaire ACM asf et le code confidentiel vidéo se connecte toujours au gestionnaire de ICM asf. (ICM dans ce cas fait référence au nom d’origine du gestionnaire de Compression vidéo.) Le filtre ne prend pas en charge la recherche.

Le diagramme suivant montre un graphique de filtre avec ce filtre.

![graphique de filtre de source Windows Media](images/wms-wmv-graph.png)

pour assurer la compatibilité descendante avec Lecteur Windows Media 6,4, ce filtre est le filtre source par défaut pour les fichiers avec les extensions de fichier. wma,. wmv et. asf. Pour la lecture de fichiers, les applications plus récentes doivent utiliser le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) . Toutefois, le lecteur ASF WM ne prend pas en charge la lecture de contenu diffusé en continu.

le moyen le plus simple pour une application de lire en continu Windows contenu multimédia est d’utiliser le kit de développement logiciel (SDK) Lecteur Windows Media. une autre option consiste à utiliser le kit de développement logiciel (SDK) de Format multimédia Windows. la tentative de création d’un lecteur personnalisé basé sur le filtre de Source du média Windows n’est pas recommandée.



| Étiquette | Valeur |
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



 

## <a name="remarks"></a>Remarques

Le CLSID du filtre n’est pas défini dans qnetwork. h. Utilisez cette macro dans votre propre fichier d’en-tête :


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtre de lecteur ASF WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



