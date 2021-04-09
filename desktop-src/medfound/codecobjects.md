---
description: Objets codec
ms.assetid: c944e5df-c375-4bad-92dc-bb3d8c09b1b3
title: Objets codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a4f140c81f162aaee2ffc416ed1de96dfcb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749349"
---
# <a name="codec-objects"></a>Objets codec

Cette section décrit les encodeurs et les décodeurs pris en charge dans Microsoft Media Foundation. Cette section contient les rubriques suivantes :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aac-decoder.md"><strong>Décodeur AAC</strong></a></td>
<td>Un décodeur audio qui décode les profils de codage audio avancé (AAC) et d’efficacité élevée (HE-AAC) suivants :
<ul>
<li>Profil LC (Multichannel) MPEG-2 AAC</li>
<li>MPEG-4 HE-AAC v1 (Multichannel) avec le cœur AAC-LC.</li>
<li>MPEG-4 HE-AAC V2 (stéréo) avec le cœur AAC-LC.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="aac-encoder.md"><strong>Encodeur AAC</strong></a></td>
<td>Un encodeur audio qui encode le profil LC (Advanced Audio codage) de faible complexité.</td>
</tr>
<tr class="odd">
<td><a href="dv-video-decoder.md"><strong>Décodeur vidéo DV</strong></a></td>
<td>Décodeur vidéo qui décode la vidéo DV.</td>
</tr>
<tr class="even">
<td><a href="h-264-video-decoder.md"><strong>Décodeur vidéo H. 264</strong></a></td>
<td>Un décodeur vidéo qui décode la vidéo H. 264. Il prend en charge le décodage des profils de base, principal et élevé, jusqu’au niveau 5,1.</td>
</tr>
<tr class="odd">
<td><a href="h-264-video-encoder.md"><strong>Encodeur vidéo H. 264</strong></a></td>
<td>Un encodeur vidéo qui encode la vidéo H. 264. Il prend en charge les profils H. 264 suivants :
<ul>
<li>Profil de base</li>
<li>Profil Main</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="h-264-video-decoder.md"><strong>Décodeur vidéo H. 265/HEVC</strong></a></td>
<td>Un décodeur vidéo qui prend en charge le décodage du contenu H. 265/HEVC dans l’annexe B et peut être utilisé pour la lecture des fichiers MP4 et M2TS. Il prend en charge les profils H. 264 suivants :
<ul>
<li>Profil Main</li>
<li>Profil 10 principaux</li>
<li>Image toujours principale</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="h-264-video-encoder.md"><strong>Encodeur vidéo H. 265/HEVC</strong></a></td>
<td>Un encodeur vidéo qui encode le format H. 265/HEVC. Il prend en charge les profils H. 265 suivants :
<ul>
<li>Profil Main</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mpeg4part2videodecoder.md"><strong>Décodeur vidéo MPEG4 2e partie 2</strong></a></td>
<td>Décodeur vidéo MPEG-4 part 2.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediaaudiodecoder.md"><strong>Décodeur Windows Media Audio</strong></a></td>
<td>Décodeur qui décode les flux encodés par l’encodeur Windows Media Audio.</td>
</tr>
<tr class="even">
<td><a href="windowsmediaaudioencoder.md">Encodeur Windows Media Audio</a></td>
<td>Encodeur audio qui prend en charge trois catégories de sortie encodée :
<ul>
<li>standard</li>
<li>Professional</li>
<li>Lossless</li>
</ul>
La catégorie standard est pour l’encodage audio à usage général. La catégorie professionnel est l’encodage de l’audio multicanaux ou haute définition. La catégorie sans perte est destinée à compresser l’audio sans perdre les données d’origine.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediaaudiovoicedecoder.md"><strong>Décodeur vocal Windows Media Audio</strong></a></td>
<td>Décodeur qui décode les flux encodés par l’encodeur vocal Windows Media Audio.</td>
</tr>
<tr class="even">
<td><a href="windowsmediaaudiovoiceencoder.md">Encodeur vocal Windows Media Audio</a></td>
<td>Encodeur pour l’encodage audio contenant principalement de la parole.</td>
</tr>
<tr class="odd">
<td><a href="windows-media-mp3-decoder.md"><strong>Décodeur MP3 Windows Media</strong></a></td>
<td>Décodeur audio qui décode les formats audio suivants.
<ul>
<li>ISO/IEC 11172-3 (MPEG-1 audio) couche 3</li>
<li>ISO/IEC 13818-3 (MPEG-2 audio) couche 3, extension de fréquence d’échantillonnage faible</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="windowsmediampeg4decoder.md"><strong>Décodeur Windows Media MPEG4 v1/v2</strong></a></td>
<td>Décodeur qui implémente le décodage vidéo MPEG-4 v1/v2.</td>
</tr>
<tr class="odd">
<td><a href="windows-media-video-7-and-8-encoders.md"><strong>Windows Media Video encodeur 7/8</strong></a></td>
<td>Un encodeur vidéo qui implémente les versions précédentes de l’encodeur Windows Media Video.</td>
</tr>
<tr class="even">
<td><a href="windowsmediavideo9decoder.md">Décodeur Windows Media Video 9</a></td>
<td>Décodeur vidéo qui décode les flux encodés par l’encodeur Windows Media Video 9.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a></td>
<td>Un encodeur vidéo qui prend en charge trois catégories de sortie endoded :
<ul>
<li>Windows Media Video 9</li>
<li>Profil avancé Windows Media Video 9</li>
<li>Image Windows Media Video 9,1</li>
</ul>
La catégorie Windows Media Video 9 correspond à l’encodage vidéo à usage général. La catégorie de profil avancé est destinée à l’encodage d’une vidéo ou d’une vidéo haute définition conforme à la norme SMPTE du profil avancé VC-1. La catégorie image permet de convertir des images bitmap en vidéo dynamique.</td>
</tr>
<tr class="even">
<td><a href="windowsmediavideo9screendecoder.md"><strong>Décodeur d’écran Windows Media Video 9</strong></a></td>
<td>Décodeur qui décode les flux encodés par l’encodeur d’écran Windows Media Video 9.</td>
</tr>
<tr class="odd">
<td><a href="windowsmediavideo9screenencoder.md"><strong>Encodeur d’écran Windows Media Video 9</strong></a></td>
<td>Un encodeur pour l’encodage d’une vidéo d’application d’ordinateur (capture d’écran) ou d’autres vidéos hautement statiques.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de programmation Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



