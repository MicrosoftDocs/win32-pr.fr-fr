---
description: Filtre de décodeur de ligne 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtre de décodeur de ligne 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515525"
---
# <a name="line-21-decoder-filter"></a>Filtre de décodeur de ligne 21

Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

Ce filtre de décodeur de ligne 21 décode les données de la ligne 21 et dessine le texte de la légende sur les bitmaps.

La broche d’entrée se connecte à n’importe quel fournisseur de données de ligne 21, généralement un décodeur vidéo DVD ou le filtre de [décodeur CC](cc-decoder-filter.md) . Le décodeur CC fournit des données de ligne 21 à partir du VBI d’un signal de télévision analogique. La broche de sortie se connecte à un code PIN secondaire sur le [mélangeur de superposition](overlay-mixer-filter.md) ou à un autre convertisseur vidéo, tel que VMR.

Ce filtre accepte les données de ligne 21 dans le format de paire d’octets standard ou, pour les DVD, en tant que paquet pour l’ensemble du groupe d’images (GOP). Pour chaque groupe d’images dans le flux vidéo DVD, il peut y avoir un paquet de données utilisateur qui contient les informations d’en-tête de ce groupe d’images et les données de ligne 21. Le format des paires d’octets est défini dans la norme EIA/CEA-608-B ; Pour plus d’informations, reportez-vous à cette norme.

Deux versions de ce filtre sont disponibles :



| Filtrer            | CLSID                 |
|-------------------|-----------------------|
| Décodeur de ligne 21   | CLSID \_ Line21Decoder  |
| Décodeur de ligne 21 2 | CLSID \_ Line21Decoder2 |



 

Le filtre version 1 est utilisé sur les plateformes Microsoft® Windows® 95/98/me et Windows 2000. Le filtre de la version 2 est disponible dans Microsoft Windows XP et versions ultérieures, et est utilisé chaque fois que le convertisseur de mixage vidéo se trouve dans le graphique.

Les informations du tableau suivant s’appliquent aux deux versions du filtre :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>Type majeur : MEDIATYPE_AUXLine21DataSubtype :<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (ligne standard 21)</li>
<li>MEDIASUBTYPE_Line21_GOPPacket (ligne DVD 21)</li>
</ul>
Type de format : FORMAT_VideoInfo ou GUID_NULL<br/></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Type majeur : MEDIATYPE_VideoSubtype :<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
Type de format : FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>Voir le tableau précédent</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Aucun</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>Décodeur de ligne 21 : MERIT_NORMALLine 21 décodeur 2 : MERIT_NORMAL + 2<br/></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Sous-titres et télétexte](closed-captions-and-teletext.md)
</dt> <dt>

[Configuration du graphique de filtre DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




