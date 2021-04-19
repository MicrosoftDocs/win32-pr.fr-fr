---
description: Filtre de compresseur MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtre de compresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517162"
---
# <a name="mjpeg-compressor-filter"></a>Filtre de compresseur MJPEG

Ce filtre compresse un flux vidéo non compressé à l’aide de la compression Motion JPEG.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Types de média de broche d’entrée                    | \_vidéo MediaType, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Types de média de broche de sortie                   | \_Vidéo MediaType, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfaces de broche de sortie                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                                                                                                                                   |
| Exécutable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Notes

Ce filtre encode à l’aide du sous-type de média MEDIASUBTYPE \_ MJPG, qui correspond au code FourCC « MJPG ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



