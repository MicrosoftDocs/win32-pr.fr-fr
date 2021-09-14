---
description: Filtre de couleur VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtre de couleur VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094602"
---
# <a name="vga-16-color-ditherer-filter"></a>Filtre de couleur VGA 16

Le filtre de couleur VGA 16 est converti à partir d’un type de couleur RVB en un affichage de couleurs de 4 bits, de sorte que les flux vidéo AVI et MPEG peuvent être affichés sur des moniteurs 16 couleurs plus anciens. Ce filtre est inséré dans le graphique entre un filtre de décompresseur et un filtre de convertisseur vidéo.



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Types de média de broche de sortie                   | \_Vidéo MediaType, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ tramé                                                                                                                                      |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                  |
| Exécutable                               | quartz.dll                                                                                                                                         |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                                                                    |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



