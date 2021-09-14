---
description: Filtre de dessin AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtre de dessin AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44eb62bd686d0604f6a0c4966fa8af4a4ad0d69d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111506"
---
# <a name="avi-draw-filter"></a>Filtre de dessin AVI

Le filtre de dessin AVI est automatiquement placé dans un graphique de lecture au lieu du [décompresseur AVI](avi-decompressor-filter.md) lorsque la vidéo est sortie vers un moniteur de télévision NTSC externe.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Types de média de broche d’entrée | Type majeur : MEDIATYPE_VideoSubtypes :<br /><ul><li>MEDIASUBTYPE_MJPG</li><li>MEDIASUBTYPE_TVMJ</li><li>MEDIASUBTYPE_WAKE</li><li>MEDIASUBTYPE_CFCC</li><li>MEDIASUBTYPE_IJPG</li><li>MEDIASUBTYPE_Plum</li><li>MEDIASUBTYPE_DVCS</li><li>MEDIASUBTYPE_DVSD</li><li>MEDIASUBTYPE_MDVF</li><li>Type de format : FORMAT_VideoInfo</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | MEDIATYPE_Video, MEDIASUBTYPE_NULL | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_AVIDraw | 
| CLSID de page de propriétés | Aucune page de propriétés. | 
| Exécutable | quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_NORMAL + 100 | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Notes

Étant donné que le filtre de dessin AVI et le [filtre de capture VFW](vfw-capture-filter.md) se connectent tous deux au même matériel, ils ne peuvent pas se trouver dans le même graphique de filtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




