---
description: Séparateur MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Séparateur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200797"
---
# <a name="mpeg-2-splitter"></a>Séparateur MPEG-2

À compter de Microsoft® Windows® XP, le filtre de séparateur MPEG-2 est déconseillé. Utilisez plutôt le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) .

Sur les plateformes antérieures, utilisez le séparateur MPEG-2 pour les flux de programme MPEG-2 fournis en mode par extraction qui contiennent au moins l’un des types de flux suivants : MPEG-2 Video ; Audio MPEG-2 ; AC3 audio codé comme défini pour la vidéo sur DVD ; ou le fichier audio PCM encodé comme défini pour la vidéo DVD. Ce filtre analyse les flux, crée une broche de sortie pour chaque flux et génère les paquets audio ou vidéo MPEG compressés dans un filtre de décodeur MPEG-2.

Pour les flux de programme et de transport remis en mode push, utilisez le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md), sur toutes les plateformes.

> [!Note]  
> Le séparateur MPEG-2 ne prend pas en charge la recherche avec une précision de trame.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td><ul>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Dépend du type de flux. Voir <a href="mpeg-2-splitter-media-types.md">types de média MPEG-2 Splitter</a></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Non applicable</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Utilisation du séparateur MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



