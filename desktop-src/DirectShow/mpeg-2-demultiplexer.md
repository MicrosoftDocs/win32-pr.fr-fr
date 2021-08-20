---
description: Ce filtre démultiplexe les flux de transport MPEG-2 et les flux de programme qui sont fournis en mode push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Démultiplexeur MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4648a456e8f7fa43274486111973fa2255ab29e4e674bc249e1c2a3c64a7b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152979"
---
# <a name="mpeg-2-demultiplexer"></a>Démultiplexeur MPEG-2

Ce filtre démultiplexe les flux de transport MPEG-2 et les flux de programme qui sont fournis en mode push. à partir de Windows XP, ce filtre prend également en charge les flux de programme en mode par extraction (lecture de fichier). Sur les plateformes antérieures, utilisez le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) pour les flux de programme en mode par extraction. Ce filtre peut être utilisé dans n’importe quel type de graphique de filtre, y compris un graphique de filtre TV numérique BDA.

> [!Note]  
> Le démultiplexeur MPEG-2 ne prend pas en charge la recherche avec précision de trame.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td>Tous les modes :<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><strong>ISpecifyPropertyPages</strong></li>
</ul>
Mode push uniquement :<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>Type majeur : MEDIATYPE_STREAM<br/> Sous-type<br/>
<ul>
<li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li>
</ul>
Pour plus d’informations, consultez <a href="mpeg-2-demultiplexer-media-types.md"><strong>types de média MPEG-2 DEMULTIPLEXEUR</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Les flux élémentaires audio et vidéo doivent avoir un type MEDIATYPE_Audio ou MEDIATYPE_Video principal.<br/> Pour plus d’informations, consultez <a href="mpeg-2-demultiplexer-media-types.md"><strong>types de média MPEG-2 DEMULTIPLEXEUR</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>mode Push uniquement : <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br/> Mode par extraction uniquement : <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br/></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_MPEG2Demultiplexer</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Disponible à des fins de test uniquement. Utiliser l’interface <strong>ISpecifyPropertyPages</strong> pour accéder aux pages de propriétés</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>mpg2splt.ax</td>
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



 

## <a name="remarks"></a>Remarques

Pour sortir des flux de données audio et vidéo élémentaires, le demux doit recevoir les flux PCR et SCR. Du côté de l’entrée, cela signifie qu’un flux de transport doit contenir les tables PAT et VPM qui définissent le PID du flux PCR. et les flux de programme doivent contenir au moins un en-tête pack.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




