---
description: Filtre de l’analyseur de film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtre de l’analyseur de film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e5d82b7e0f4da1365c7dcdf753463cb3c846e5fae82a839de0c21a5800bc5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747439"
---
# <a name="quicktime-movie-parser-filter"></a>Filtre de l’analyseur de film QuickTime

ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs. il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.

Le filtre de l’analyseur de film QuickTime fractionne les données Apple® QuickTime® en flux audio et vidéo. Il prend en charge QuickTime 2,0 et versions antérieures. La broche d’entrée se connecte à un filtre source, tel que le filtre de [source de fichier Async](file-source--async--filter.md) ou le filtre de [source du fichier d’URL](file-source--url--filter.md) . L’analyseur utilise le filtre de [décompresseur AVI](avi-decompressor-filter.md) ou [QT](qt-decompressor-filter.md) pour décompresser les fichiers QuickTime. Le filtre crée une broche de sortie pour le flux vidéo et une broche de sortie pour le flux audio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie ;</td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td><ul>
<li>MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</li>
<li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_QuickTimeParser</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Aucune page de propriétés.</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



