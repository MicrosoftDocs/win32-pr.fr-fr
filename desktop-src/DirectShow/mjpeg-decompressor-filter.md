---
description: Filtre de décompresseur MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtre de décompresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910017"
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

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



