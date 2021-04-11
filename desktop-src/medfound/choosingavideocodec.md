---
description: Choix d’un codec vidéo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Choix d’un codec vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201177"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Choix d’un codec vidéo (Microsoft Media Foundation)

L’encodeur Windows Media Video 9 prend en charge trois catégories de sortie encodée : profil principal, profil avancé et image. La catégorie de profil principale fournit une compression vidéo générale pour un contenu vidéo complexe, tel que des films ou des vidéos musicales. Les fonctionnalités du profil principal fournissent un large éventail de paramètres d’encodage. Vous pouvez utiliser le profil principal pour créer une vidéo avec des débits très faibles pour la livraison sur des appareils portables ou, à l’autre extrémité du spectre, vous pouvez l’utiliser pour créer une vidéo haute définition pour le cinéma numérique.

L’importance des algorithmes d’encodage dans le profil principal est sur le contenu vidéo dynamique, mais ils conviennent également à d’autres contenus vidéo. Le profil principal doit être votre catégorie par défaut pour le contenu vidéo. Pour répondre à des besoins spécifiques, vous pouvez utiliser la catégorie de profil avancé, la catégorie d’image ou un encodeur distinct appelé « encodeur d’écran Windows Media Video 9 ». Le tableau suivant répertorie les quatre options.



<table>
<thead>
<tr class="header">
<th>Objectif</th>
<th>Codec</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Encodage vidéo à usage général</td>
<td><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a><dl> Profil Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Encodage d’une vidéo ou d’une vidéo haute définition conforme à la norme SMPTE du profil avancé VC-1</td>
<td><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a><dl> Profil avancé<br />
</dl></td>
</tr>
<tr class="odd">
<td>Conversion d’images bitmap en vidéo dynamique</td>
<td><a href="windowsmediavideo9encoder.md">Encodeur Windows Media Video 9</a><dl> Image<br />
</dl></td>
</tr>
<tr class="even">
<td>Encodage d’une vidéo d’application d’ordinateur (capture d’écran) ou autre vidéo hautement statique</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Encodeur d’écran Windows Media Video 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 



