---
description: Filtre de l’analyseur WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtre de l’analyseur WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa077f793feb9ecb534744e98441178ffe92933e4fcb55f4e7748ad775f1382c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903209"
---
# <a name="wave-parser-filter"></a>Filtre de l’analyseur WAVE

Le filtre de l’analyseur WAVE analyse les données audio au format WAV à partir des fichiers. wav,... ou. AIF. Le filtre amont doit être le filtre de [source de fichier Async](file-source--async--filter.md) , le filtre de [source du fichier d’URL](file-source--url--filter.md) ou un filtre de source asynchrone tiers compatible qui contient les données audio WAV. Le flux de sortie est données audio, que vous pouvez connecter directement à un filtre de rendu audio ou à un filtre de transformation audio intermédiaire.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>Type majeur : MEDIATYPE_StreamThe sous-types suivants sont valides :<br/>
<ul>
<li>MEDIASUBTYPE_AIFF</li>
<li>MEDIASUBTYPE_AU</li>
<li>MEDIASUBTYPE_WAVE</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Type majeur : MEDIATYPE_AudioSubtype : MEDIASUBTYPE_PCM ou un autre type de compression. (Voir <a href="audio-subtypes.md"><strong>sous-types audio</strong></a>.)<br/> Type de format : FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>{D51BD5A1-7548-11cf-A520-0080C77EF58A}</td>
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
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarques

Ce filtre prend en charge les types de fichiers suivants :

-   VAGUE (. wav)
-   AIFF et AIFF-C (. AIF)
-   Au (. au)

Toutefois, il présente les limitations suivantes au format audio :

-   L’audio doit être un PCM linéaire 8 bits ou 16 bits.
-   Pour les fichiers AIFF-C, l’audio doit être décompressé, dans l’ordre de primauté des octets de poids fort (type de compression « aucun »).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




