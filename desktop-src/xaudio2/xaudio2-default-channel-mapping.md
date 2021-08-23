---
description: Un client XAudio2 dispose d’un contrôle total sur le mappage entre les canaux d’une voix et les canaux de chacune de ses voix de destination.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: Mappage de canal par défaut XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42bb2f67709586532a19d86a916d3b7852652e76f9b6ce1ae115f1fc670e37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025947"
---
# <a name="xaudio2-default-channel-mapping"></a>Mappage de canal par défaut XAudio2

Un client XAudio2 dispose d’un contrôle total sur le mappage entre les canaux d’une voix et les canaux de chacun de ses voicesIt de destination contrôle le mappage via l’utilisation de la méthode [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . Dans certains cas, toutefois, XAudio2 simplifie cette tâche en configurant automatiquement une matrice d’envoi par défaut. Pour ce faire, il utilise le masque de canal, le cas échéant, associé aux canaux audio d’une voix. Un masque de canal est une combinaison de \_ masques de bits d’orateur xxx comme défini dans X3DAudio. h et ailleurs. XAudio2 exige que les masques de canal aient la valeur 0 ou qu’ils aient le même nombre de bits que le nombre de canaux.

Le tableau suivant présente les exigences et les valeurs par défaut du masque de canal pour les formats pris en charge par XAudio2. 

| Format | Exigence de masque de canal             | Masque par défaut                        | Membre de structure correspondant                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | Le fichier peut contenir un masque de canal    | Le masque de canal est 0 ou absent        | WAVEFORMATEXTENSIBLE. dwChannelMask ou None (WAVEFORMATEX) |
| ADPCM  | Le fichier ne contient pas de masque de canal | Le masque de canal par défaut est toujours utilisé | Aucun (ADPCMWAVEFORMAT)                                    |



 

Pour les voix de mixage secondaire et de mastérisation, et pour les voix source sans masque de canal ou un masque de canal de 0, XAudio2 utilise les positions de haut-parleur par défaut en fonction du tableau suivant. 

| Canaux  | Positions des canaux implicites                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Mappe toujours à FrontLeft et FrontRight à pleine échelle dans les deux enceintes (cas particuliers pour les sons mono)                 |
| 2         | FrontLeft, FrontRight (configuration stéréo de base)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (configuration 2,1)                                                               |
| 4         | FrontLeft, FrontRight, Left, Right (Quadraphonic)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (configuration 5,0)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (configuration 5,1) (voir les remarques suivantes) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, recentrer (configuration 6,1)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, Left, Right, SideLeft, SideRight (Configuration 7,1)        |
| 9 ou plus | Aucune position implicite (mappage un-à-un)                                                                            |



 

Si une paire de voix donnée dans le graphique audio n’a pas de position de haut-parleur pour la voix source ou cible (une voix a plus de huit canaux), aucune voix n’est lisible tant que la voix source n’a pas d’ensemble de matrice d’envoi explicitement à l’aide de la méthode [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . L’appel de la méthode [**IXAudio2SourceVoice :: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) pour une voix échoue jusqu’à ce que vous procédiez à cette opération.

Si la voix source et la voix cible ont un nombre différent de positions de haut-parleur et que [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) n’a pas été appelé sur la voix source, XAudio2 envoie chaque canal source vers le haut-parleur (ou les haut-parleurs) cible le plus proche, de manière proportionnelle à la proximité du haut-parleur prévu. Il existe deux cas spéciaux où le comportement par défaut est différent.

1.  Si le son source est mono et est positionné au centre de l’orateur \_ \_ ou n’a pas de position définie, il est toujours envoyé à \_ l’avant-plan \_ gauche et au premier orateur, \_ \_ s’ils existent dans le son de sortie. S’ils n’existent pas, il revient au cas normal.
2.  Si la source et la destination sont toutes deux de type 6 canaux et sont positionnées sur l’une des configurations de l’orateur 5,1 standard (gauche + droite + centre + Sub + backt + Backeur ou Left + Right + Center + Sub + Side + lateral), les canaux sont mappés via un à un. En d’autres termes, SideLeft/Right et Left/Right sont traités de façon équivalente. Cela est dû au fait qu’il y a eu une confusion historique autour de ces configurations. Par conséquent, l’intention supposée est toujours de mapper un à un.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Voix](voices.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
