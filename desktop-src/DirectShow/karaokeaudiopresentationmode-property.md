---
description: La propriété KaraokeAudioPresentationMode définit ou récupère la combinaison d’orateurs de droite à gauche pour les canaux karaoké auxiliaires.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propriété KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af634a3beaade7e497cdc6d158ccf1121ebb09542bdec92ceaae823b1b91ccdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952378"
---
# <a name="karaokeaudiopresentationmode-property"></a>Propriété KaraokeAudioPresentationMode

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `KaraokeAudioPresentationMode` propriété définit ou récupère la combinaison d’orateurs de droite à gauche pour les canaux karaoké auxiliaires.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière contenant un jeu d’indicateurs binaires indiquant comment les canaux karaoké auxiliaires sont downmixeds aux haut-parleurs gauche et droit.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture avec une valeur par défaut de zéro.

Les canaux audio étant de base zéro, les canaux 0 et 1 représentent généralement les canaux de haut-parleur droit et gauche et les canaux 2 à 4 sont les trois canaux karaoké auxiliaires. Lorsque l’objet MSWebDVD passe en mode karaoké, il désactive automatiquement les canaux 2 et supérieurs. Utilisez des **opérations or au niveau du** bit pour définir le bit approprié afin d’envoyer un canal auxiliaire vers le haut-parleur gauche, le haut-parleur droit, les deux haut-parleurs (bits sur) ou aucun orateur (les deux bits sont désactivés). Ces bits sont désactivés par défaut chaque fois que le navigateur DVD passe en mode karaoké. La valeur des bits et leurs actions correspondantes sont indiquées dans le tableau suivant.



| Valeur  | Description                            |
|--------|----------------------------------------|
| 0x0004 | Downmix canal 2 vers le haut-parleur gauche  |
| 0x0008 | Downmix canal 3 vers le haut-parleur gauche  |
| 0x0010 | Downmix canal 4 vers le haut-parleur gauche  |
| 0x0400 | Downmix canal 2 vers le haut-parleur droit |
| 0x0800 | Downmix canal 3 vers le haut-parleur droit |
| 0x1000 | Downmix canal 4 vers le haut-parleur droit |



 

 

 



