---
description: Filtre de convertisseur d’espace colorimétrique
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtre de convertisseur d’espace colorimétrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0a519772a6d38971654cb92a895fcd95f5ecc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987062"
---
# <a name="color-space-converter-filter"></a>Filtre de convertisseur d’espace colorimétrique

Ce filtre de transformation convertit d’un type de couleur RVB en un autre type RVB, par exemple entre une couleur RVB de 24 et 8 bits. Étant donné que ce type de conversion est généralement géré plus efficacement au sein d’un décompresseur vidéo, l’utilisation principale du convertisseur d’espace colorimétrique est lorsque la source de flux est composée de trames RVB non compressées.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Types de média de broche d’entrée | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Les sous-types suivants sont valides :<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Les sous-types suivants sont valides :<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_Colour | 
| CLSID de page de propriétés | Aucune page de propriétés. | 
| Exécutable | quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




