---
description: Filtre de décodage vidéo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtre de décodage vidéo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12aead5f8238064198c31566a1e2ca1fde75931
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195500"
---
# <a name="dv-video-decoder-filter"></a>Filtre de décodage vidéo DV

Ce filtre décode un flux vidéo numérique (DV) en vidéo non compressée.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong> | 
| Types de média de broche d’entrée | <ul><li>MEDIATYPE_Video</li><li>MEDIASUBTYPE_dvsd</li><li>FORMAT_VideoInfo, FORMAT_DvInfo</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | <strong>Type principal</strong>: MEDIATYPE_Video<strong>sous-types</strong>:<br /><ul><li>MEDIASUBTYPE_YUY2</li><li>MEDIASUBTYPE_UYVY</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li><li>MEDIASUBTYPE_ARGB32</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_Y41P</li></ul><strong>Types de format</strong>:<br /> Format_VideoInfo, Format_VideoInfo2<br /> | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_DVVideoCodec | 
| CLSID de page de propriétés | CLSID_DVDecPropertiesPage | 
| Exécutable | qdv.dll | 
| <a href="merit.md">Mérite</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Notes

Utilisez l’interface [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) pour définir la résolution du décodage sur complète, demi-taille, quart de taille ou une taille d’un huitième.

**Entrelacement**: les versions antérieures du décodeur désentrelacent toujours la vidéo. À partir de DirectX 9,0, le décodeur vidéo DV peut préserver l’entrelacement. Cela permet à la vidéo entrelacée d’être désentrelacée par le convertisseur de mixage vidéo (VMR), afin d’améliorer la qualité de rendu. Pour utiliser cette fonctionnalité, le filtre en aval doit prendre en charge les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indiqués par ce format \_ de valeur VideoInfo2 dans le membre **formatType** de la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Au niveau de la résolution complète, les indicateurs de désentrelacement (**dwInterlace**) dans la structure **VIDEOINFOHEADER2** sont définis sur `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , indiquant les champs entrelacés. À demi-résolution ou moins, **dwInterlace** est défini à zéro, ce qui indique les images progressives.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




