---
description: Filtre de décompresseur AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtre de décompresseur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910097"
---
# <a name="avi-decompressor-filter"></a>Filtre de décompresseur AVI

Le filtre de décompresseur AVI permet aux codecs du gestionnaire de compression vidéo (VCM) de joindre un graphique de filtres. L’application n’a pas besoin d’ajouter le filtre au graphique de filtre ; elle est automatiquement extraite par le gestionnaire de graphique de filtre, si nécessaire.

Lorsque le gestionnaire de graphique de filtre crée un graphique pour afficher un fichier AVI, il vérifie le FOURCC dans l’en-tête AVI du fichier pour déterminer si le flux vidéo est compressé. Si c’est le cas, le gestionnaire de graphique de filtre ajoute le décompresseur AVI, qui recherche ensuite dans le registre un décompresseur installé pouvant gérer le fichier.

> [!Note]  
> Les décompresseurs MPEG ne sont jamais implémentés en tant que codecs VCM, mais uniquement en tant que filtres DirectShow natifs.

 

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

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 




