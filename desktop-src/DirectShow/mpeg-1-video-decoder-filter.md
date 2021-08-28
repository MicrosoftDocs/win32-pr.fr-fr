---
description: Filtre de décodage vidéo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtre de décodage vidéo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468226"
---
# <a name="mpeg-1-video-decoder-filter"></a>Filtre de décodage vidéo MPEG-1

Décode une vidéo MPEG-1.




| | | Filtrer les interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Types de média de broche d’entrée | MEDIATYPE_Video, FORMAT_MPEGVideo<br /> Les sous-types suivants sont valides :<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a> | | Types de média de broche de sortie | Type majeur : <strong>MEDIATYPE_Video</strong>,<br /> Type de format : <strong>FORMAT_VideoInfo</strong> ou <strong>FORMAT_VideoInfo2</strong><br /> Sous-types<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | | Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID du filtre | <strong>CLSID_CMpegVideoCodec</strong> | | CLSID de page de propriétés | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | | Fichier exécutable | quartz.dll | | <a href="merit.md">Mérite</a> | 0x40000001 | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Remarques

Ce filtre peut décoder dans une surface DirectDraw. Le filtre utilise MMX si l’ordinateur prend en charge MMX.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




