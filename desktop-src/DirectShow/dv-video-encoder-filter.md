---
description: Filtre d’encodeur vidéo DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtre d’encodeur vidéo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c89574ab257467e16b566fe899a5ab32384e48e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195483"
---
# <a name="dv-video-encoder-filter"></a>Filtre d’encodeur vidéo DV

Ce filtre encode un flux vidéo non compressé en vidéo numérique (DV). Il fournit une interface personnalisée, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), pour définir la résolution et le format d’encodage.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong> | 
| Types de média de broche d’entrée | <ul><li>Type majeur : MEDIATYPE_VideoThe sous-types suivants sont valides :<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Type de format : FORMAT_VideoInfo</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | <ul><li>Type majeur : MEDIATYPE_Video</li><li>Sous-type : MEDIASUBTYPE_dvsd</li><li>Type de format : FORMAT_VideoInfo</li></ul> | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_DVVideoEnc | 
| CLSID de page de propriétés | CLSID_DVEncPropertiesPage | 
| Exécutable | qdv.dll | 
| <a href="merit.md">Mérite</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Notes

Pour la vidéo 16 bits (MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565), l’entrée doit être 720 x 480 pixels pour NTSC, ou 720 x 576 pixels pour PAL. Pour les vidéos 24 bits, il n’y a aucune contrainte de taille sur l’entrée.

La sortie est toujours 720 x 480 pour NTSC ou 720 x 576 pour PAL ; la vidéo 24 bits est mise à l’échelle pour s’adapter à ces dimensions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




