---
description: Filtre de wrappers ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtre de wrappers ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516357"
---
# <a name="acm-wrapper-filter"></a>Filtre de wrappers ACM

Le filtre de wrapper ACM permet aux codecs du gestionnaire de compression audio (ACM) de joindre un graphique de filtre. Il peut agir soit comme filtre de décompression, soit comme filtre de compression.

En tant que filtre de décompression, le wrapper ACM apparaît dans la catégorie « filtres DirectShow » (CLSID \_ LegacyAmFilterCategory) et a un mérite de mérite \_ normal. Le type de support de connexion sur la broche d’entrée détermine le codec utilisé par le filtre. En règle générale, l’application n’a pas besoin d’ajouter le filtre au graphique de filtre ; elle est automatiquement extraite par le gestionnaire de graphique de filtre, si nécessaire. La décompression concerne uniquement les signaux audio PCM.

En tant que filtre de compression, le wrapper ACM apparaît dans la catégorie « compresseurs audio » (CLSID \_ AudioCompressorCategory) et a un mérite de mérite \_ n' \_ \_ utilise pas. Chaque codec s’affiche sous la forme d’une instance distincte. Pour la compression, vous ne pouvez pas créer directement le filtre avec CoCreateInstance. Au lieu de cela, vous devez utiliser l’énumérateur du périphérique système. Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. les combinaisons suivantes sont possibles :<br/>
<ul>
<li>Échantillons par seconde (kHz) : 44,1, 22,05, 11,025 ou 8,0.</li>
<li>Canaux : stéréo ou mono.</li>
<li>Bits par échantillon : 8 ou 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Aucune page de propriétés.</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_NORMAL ou MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 




