---
description: Filtre de source de fichier (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtre de source de fichier (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109571"
---
# <a name="file-source-url-filter"></a>Filtre de source de fichier (URL)

Le filtre de source du fichier d’URL est un filtre de source asynchrone générique qui fonctionne avec n’importe quel fichier source qui peut être identifié par un Uniform Resource Locator (URL) et dont le type de média majeur est Stream. Cela comprend les fichiers AVI, MOV, MPEG et WAV. Le filtre en aval doit être un analyseur, tel que le [séparateur de flux MPEG-1](mpeg-1-stream-splitter-filter.md), le [séparateur AVI](avi-splitter-filter.md)ou l' [Analyseur de film QuickTime](quicktime-movie-parser-filter.md).



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Types de média de broche d’entrée                    | Non applicable                                                                                                                       |
| Interfaces pin d’entrée                     | Non applicable                                                                                                                       |
| Types de média de broche de sortie                   | Flux de MEDIATYPE \_ . Le sous-type dépend du format du média. (MEDIASUBTYPE \_ NULL si le filtre ne reconnaît pas le format.)         |
| Interfaces de broche de sortie                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID du filtre                             | CLSID \_ URLReader                                                                                                                     |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                     |
| Exécutable                               | quartz.dll                                                                                                                           |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                                                      |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                        |



 

## <a name="remarks"></a>Notes

Ce filtre utilise URLMon et prend en charge les pages de codes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



