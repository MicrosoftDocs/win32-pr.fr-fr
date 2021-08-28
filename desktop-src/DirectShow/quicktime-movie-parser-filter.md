---
description: Filtre de l’analyseur de film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtre de l’analyseur de film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a65ba14cb748eb10c6afddf3e4747f11d68a4f9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476715"
---
# <a name="quicktime-movie-parser-filter"></a>Filtre de l’analyseur de film QuickTime

ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs. il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.

Le filtre de l’analyseur de film QuickTime fractionne les données Apple® QuickTime® en flux audio et vidéo. Il prend en charge QuickTime 2,0 et versions antérieures. La broche d’entrée se connecte à un filtre source, tel que le filtre de [source de fichier Async](file-source--async--filter.md) ou le filtre de [source du fichier d’URL](file-source--url--filter.md) . L’analyseur utilise le filtre de [décompresseur AVI](avi-decompressor-filter.md) ou [QT](qt-decompressor-filter.md) pour décompresser les fichiers QuickTime. Le filtre crée une broche de sortie pour le flux vidéo et une broche de sortie pour le flux audio.




| | | Filtrer les interfaces | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Types de média de broche d’entrée | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie ; | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Types de média de broche de sortie | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</li></ul> | | Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID du filtre | CLSID_QuickTimeParser | | CLSID de page de propriétés | Aucune page de propriétés. | | Fichier exécutable | quartz.dll | | <a href="merit.md">Mérite</a> | MERIT_NORMAL | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



