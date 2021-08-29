---
description: Filtre de décompresseur AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtre de décompresseur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e7511c4243d2e36ff6270826201b4b6dc58246ed2a1d815f34ee14f9aff7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689479"
---
# <a name="avi-decompressor-filter"></a>Filtre de décompresseur AVI

Le filtre de décompresseur AVI permet aux codecs du gestionnaire de compression vidéo (VCM) de joindre un graphique de filtres. L’application n’a pas besoin d’ajouter le filtre au graphique de filtre ; elle est automatiquement extraite par le gestionnaire de Graph de filtre quand cela est nécessaire.

lorsque le gestionnaire de Graph de filtre crée un graphique pour afficher un fichier avi, il vérifie le FOURCC dans l’en-tête AVI du fichier pour déterminer si le flux vidéo est compressé. si c’est le cas, le gestionnaire de Graph de filtre ajoute le décompresseur AVI, qui recherche ensuite dans le registre un décompresseur installé pouvant gérer le fichier.

> [!Note]  
> les décompresseurs MPEG ne sont jamais implémentés en tant que codecs VCM, mais uniquement en tant que filtres de DirectShow natifs.

 

Sur son code PIN amont, le décompresseur AVI se connecte généralement au [séparateur AVI](avi-splitter-filter.md). Sur sa broche de sortie, il se connecte généralement au [convertisseur vidéo](video-renderer-filter.md) ou au [filtre MUX AVI](avi-mux-filter.md).



| Étiquette | Valeur |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Types de média de broche d’entrée                    | Type majeur : MEDIATYPE \_ VideoSubtype : doit correspondre au code FourCC pour le type de compression. Pour plus d’informations, consultez [codes FourCC](fourcc-codes.md).<br/> Type de format : FORMAT \_ videoinfo<br/> |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Types de média de broche de sortie                   | \_Vidéo MediaType, MEDIASUBTYPE \_ null, format \_ videoinfo                                                                                                                                                            |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| CLSID du filtre                             | CLSID \_ AVIDec                                                                                                                                                                                                      |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                                                                                  |
| Exécutable                               | quartz.dll                                                                                                                                                                                                         |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                                                                                                                                                      |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




