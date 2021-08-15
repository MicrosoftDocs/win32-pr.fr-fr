---
description: Filtre de décompresseur MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtre de décompresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f0587abe77d1f76df043a37bc8e54db91d65d81e00b0a2677268b6d61bc782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684939"
---
# <a name="mjpeg-decompressor-filter"></a>Filtre de décompresseur MJPEG

Ce filtre décode un flux vidéo de Motion JPEG en vidéo non compressée. Certaines caméras vidéo numériques produisent un flux vidéo JPEG motion.



| Étiquette | Valeur |
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



 

## <a name="remarks"></a>Remarques

Ce filtre est compatible avec Motion JPEG Video qui utilise le code FOURCC « MJPG ». Il ne peut pas décoder d’autres types de mouvement JPEG. Pour cela, vous devez utiliser un filtre de décodeur tiers.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



