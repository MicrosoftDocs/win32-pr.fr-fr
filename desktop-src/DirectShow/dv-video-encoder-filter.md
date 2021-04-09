---
description: Filtre d’encodeur vidéo DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtre d’encodeur vidéo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950010"
---
# <a name="dv-video-encoder-filter"></a>Filtre d’encodeur vidéo DV

Ce filtre encode un flux vidéo non compressé en vidéo numérique (DV). Il fournit une interface personnalisée, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), pour définir la résolution et le format d’encodage.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td><ul>
<li>Type majeur : MEDIATYPE_VideoThe sous-types suivants sont valides :<br/>
<ul>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
</ul></li>
<li>Type de format : FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td><ul>
<li>Type majeur : MEDIATYPE_Video</li>
<li>Sous-type : MEDIASUBTYPE_dvsd</li>
<li>Type de format : FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_DVVideoEnc</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>CLSID_DVEncPropertiesPage</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_VideoCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Pour la vidéo 16 bits (MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565), l’entrée doit être 720 x 480 pixels pour NTSC, ou 720 x 576 pixels pour PAL. Pour les vidéos 24 bits, il n’y a aucune contrainte de taille sur l’entrée.

La sortie est toujours 720 x 480 pour NTSC ou 720 x 576 pour PAL ; la vidéo 24 bits est mise à l’échelle pour s’adapter à ces dimensions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




