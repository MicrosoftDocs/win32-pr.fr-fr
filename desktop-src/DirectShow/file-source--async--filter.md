---
description: Filtre source de fichier (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtre source de fichier (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481648"
---
# <a name="file-source-async-filter"></a>Filtre source de fichier (Async)

Le filtre de source de fichier asynchrone ouvre et lit les fichiers locaux de nombreux formats de données différents et transmet les données à un filtre d’analyseur.

Pour télécharger des fichiers multimédias à partir du Web via HTTP, utilisez le filtre de [source de fichier (URL)](file-source--url--filter.md) . Pour lire des fichiers ASF, utilisez le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Types de média de broche d’entrée                    | Non applicable                                                                                                                       |
| Interfaces pin d’entrée                     | Non applicable                                                                                                                       |
| Types de média de broche de sortie                   | **MediaType \_ Flux** de. Le sous-type dépend du format du média. (**MEDIASUBTYPE \_ null** si le filtre ne reconnaît pas le format.) |
| Interfaces de broche de sortie                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID du filtre                             | **CLSID \_ AsyncReader**                                                                                                               |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                     |
| Exécutable                               | quartz.dll                                                                                                                           |
| [Mérite](merit.md)                       | **MÉRITE \_ improbable**                                                                                                                  |
| [Catégorie de filtre](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



