---
description: Filtre de navigateur DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtre de navigateur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a395001daeac5f90be85bea972d1d4f118198ee4343960cb4eed0d958e1677aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016007"
---
# <a name="dvd-navigator-filter"></a>Filtre de navigateur DVD

Le filtre de navigateur DVD est le filtre source pour un graphique de filtre de lecture DVD-Video. Il ouvre tous les fichiers nécessaires dans un volume DVD-Video, parcourt les fichiers linéaires DVD-Video. VOB et analyse le flux de programme MPEG-2 résultant, en fractionnant le flux en trois broches de sortie (vidéo, audio, sous-image).

Le filtre de navigateur DVD implémente également les interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) qui permettent à une application de lecture de DVD de contrôler DVD-Video la lecture.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td>Non applicable.</td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Types de base :<br/>
<ul>
<li>Vidéo : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li>Audio : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li>Sous-image : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Types étendus :<br/> Vidéo :<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
</ul>
Audio :<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
</ul>
Sous-titres<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Pour activer les types étendus, appelez <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2 :: SetOption</strong></a> et définissez le <br/></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_DVDNavigator</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Aucune page de propriétés.</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_DO_NOT_USE</td>
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
</dt> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 




