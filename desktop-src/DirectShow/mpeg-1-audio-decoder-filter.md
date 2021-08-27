---
description: Filtre de décodage audio MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtre de décodage audio MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3c014497d8b3db5aaf3031250e78edd8b59cb2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983822"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Filtre de décodage audio MPEG-1

Décode les données MPEG-1 couche I et couche II en PCM.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | 
| Types de média de broche d’entrée | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Les sous-types suivants sont valides :<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_CMpegAudioCodec | 
| CLSID de page de propriétés | CLSID_MpegAudioDecoderPropertyPage | 
| Exécutable | quartz.dll | 
| <a href="merit.md">Mérite</a> | 0x03680001 | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




