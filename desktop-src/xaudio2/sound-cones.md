---
description: Modèle qui décrit le niveau sonore du son orienté.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Cônes audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523414"
---
# <a name="sound-cones"></a>Cônes audio

Modèle qui décrit le niveau sonore du son orienté.

Un son sans orientation a la même amplitude à une distance donnée dans toutes les directions. Un son dont l’orientation est la plus forte dans le sens de l’orientation. Le modèle qui décrit le niveau sonore du son orienté est appelé cône de son. Les cônes audio sont constitués d’un cône intérieur (ou interne) et d’un cône extérieur (ou externe). L’angle du cône extérieur doit toujours être égal ou supérieur à l’angle conique intérieur.

À n’importe quel angle dans le cône interne, le volume du son est défini sur le volume de cône interne. Cela prend en compte le volume de base de la mémoire tampon, la distance de l’écouteur, l’orientation de l’écouteur si l’écouteur a son propre cône, et ainsi de suite.

À tout angle à l’extérieur du cône externe, le volume normal est atténué par un facteur défini par l’application. Le niveau de volume du cône extérieur est exprimé sous la forme d’une échelle linéaire de l’amplitude : 1,0 f ne représente aucune atténuation appliquée au signal d’origine, 0,5 f indique une atténuation de 6 dB, et 0,0 f génère un silence. L’amplification (volume > 1,0 f) est également autorisée et n’est pas ancrée. La plage de volumes valide est en fait 0,0 f à 2,0 f.

Entre le cône interne et le cône externe est une zone de transition du volume intérieur au volume extérieur. Le volume s’approche du volume externe du cône lorsque l’angle augmente.

Les cônes peuvent affecter des paramètres autres que le volume. Le filtre passe-bas et le niveau d’envoi de réverbération peuvent également être affectés, ce qui rend la technique encore plus spectaculaire. Par exemple, avec un cône sur l’écouteur, vous pouvez spécifier tous les sons situés derrière l’écouteur se trouver un peu atténué, et avoir un contenu de réverbe vers direct légèrement supérieur. Celles-ci fournissent des indications supplémentaires que le son est derrière l’utilisateur. Cela améliore le réalisme.

L’illustration suivante montre le concept de cônes audio.

![cônes audio](images/common-audio-concepts-sound-cones.png)

La création correcte de cônes audio peut ajouter des effets spectaculaires à votre application. Par exemple, vous pouvez positionner une source sonore au centre d’une pièce, en définissant son orientation vers une porte ouverte dans un couloir. Définissez ensuite l’angle du cône intérieur afin qu’il s’étende à la largeur de la porte, rendez le cône extérieur un peu plus grand, puis définissez le volume conique extérieur sur inaudible. Un écouteur se déplaçant le long du couloir commence à entendre le son uniquement lorsqu’il est près de la porte. Le son sera le plus fort, car l’écouteur passe devant la porte ouverte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts audio courants](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**\_Cône X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



