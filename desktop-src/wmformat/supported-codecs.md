---
title: Codecs pris en charge
description: Codecs pris en charge
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media Format SDK, codecs pris en charge
- Windows Media Format SDK, interface IWMCodecInfo3
- codecs, pris en charge
- IWMCodecInfo3, à propos de
- codecs, interface IWMCodecInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723587"
---
# <a name="supported-codecs"></a>Codecs pris en charge

Le kit de développement logiciel (SDK) Windows Media format prend en charge les codecs suivants, qui sont inclus lorsque vous installez le kit de développement logiciel (SDK).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codec</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Media Audio</td>
<td>Codec audio pour une utilisation générale dans l’encodage de données audio complexes, telles que la musique. Les versions les plus récentes de ce codec sont le codec Windows Media Audio 9 et le codec Windows Media Audio 9,1.<br/></td>
</tr>
<tr class="even">
<td>Windows Media Audio professionnel</td>
<td>Codec audio pour des données audio complexes, telles que la musique. Prend en charge l’encodage multicanaux et 24 bits. Il existe deux versions de ce codec :<br/>
<ul>
<li>Windows Media Audio 9 professionnel</li>
<li>Windows Media Audio 9,1 professionnel</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Media Audio sans perte</td>
<td>Codec audio pour l’encodage sans perte. Il existe deux versions de ce codec :<br/>
<ul>
<li>Windows Media Audio 9 sans perte</li>
<li>Windows Media Audio 9,1 sans perte</li>
</ul></td>
</tr>
<tr class="even">
<td>Voix Windows Media Audio 9</td>
<td>Codec audio optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit du codec préféré pour les flux composés principalement de mots prononcés. Pour le contenu mixte musical et vocal, ce codec peut modifier dynamiquement l’algorithme d’encodage utilisé pour obtenir une qualité optimale.</td>
</tr>
<tr class="odd">
<td>Windows Media Video 9</td>
<td>Codec vidéo pour une utilisation générale dans l’encodage d’une vidéo complexe, telle que des films.</td>
</tr>
<tr class="even">
<td>Profil avancé Windows Media Video 9</td>
<td>Codec vidéo incorporant des fonctionnalités d’encodage avancées, y compris l’encodage entrelacé.</td>
</tr>
<tr class="odd">
<td>Écran Windows Media Video 9</td>
<td>Codec vidéo optimisé pour l’encodage des captures d’écran séquentielles. Ce codec est souvent utilisé pour la formation ou le support logiciel en enregistrant des images de moniteur à mesure que des applications d’ordinateur sont utilisées.</td>
</tr>
<tr class="even">
<td>Image Windows Media Video</td>
<td>Codec vidéo pour convertir des images bitmap avec des informations de déformation en vidéo compressée. Il existe deux versions de ce codec :<br/>
<ul>
<li>Image Windows Media Video 9</li>
<li>Image Windows Media Video 9 v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Différentes versions des codecs vidéo et Windows Media Audio sont disponibles pour l’encodage en fonction de la version du kit de développement logiciel (SDK) du format Windows Media que vous installez. Lorsque vous utilisez les méthodes si l’interface [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) pour énumérer les codecs et les formats de codec, seules les dernières versions prises en charge sont énumérées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Choix d’une méthode d’encodage**](choosing-an-encoding-method.md)
</dt> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> </dl>

 

 





