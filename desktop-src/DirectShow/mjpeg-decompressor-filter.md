---
description: Filtre de décompresseur MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtre de décompresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522455"
---
# <a name="mjpeg-decompressor-filter"></a>Filtre de décompresseur MJPEG

Ce filtre décode un flux vidéo de Motion JPEG en vidéo non compressée. Certaines caméras vidéo numériques produisent un flux vidéo JPEG motion.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Types de média de broche de sortie                   | \_vidéo MediaType, MEDIASUBTYPE \_ null                                                                                                               |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ MjpegDec                                                                                                                                    |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                                   |
| Exécutable                               | quartz.dll                                                                                                                                         |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                                                                                      |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Notes

Ce filtre est compatible avec Motion JPEG Video qui utilise le code FOURCC « MJPG ». Il ne peut pas décoder d’autres types de mouvement JPEG. Pour cela, vous devez utiliser un filtre de décodeur tiers.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



