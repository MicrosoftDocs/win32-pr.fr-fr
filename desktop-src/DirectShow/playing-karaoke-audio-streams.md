---
description: Lecture de l’audio karaoké Flux
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Lecture de l’audio karaoké Flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10912761034feb9ed82c85625324cd3091514b2c492c66b4e49af711d7d2152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213299"
---
# <a name="playing-karaoke-audio-streams"></a>Lecture de l’audio karaoké Flux

Le navigateur DVD peut lire DVD-Video disques avec des flux audio karaoké, mais la lecture karaoké requiert également un décodeur qui prend en charge le mixage de karaoké multicanal. Plus précisément, le décodeur doit prendre en charge le [**jeu de propriétés Karaoké DVD**](dvd-karaoke-property-set.md) ( \_ propriété am \_ DVDKARAOKE).

Les disques de karaoké sont un type de DVD-Video disque et ont la même structure de navigation. Les chansons sont généralement mises en forme en tant que titres, et les titres peuvent être regroupés en jeux de titres en fonction de l’intervenant, du style musical ou d’autres critères. La principale différence entre le karaoké et les autres types de DVD-Videos est le flux audio. Les disques de karaoké contiennent tous un son multicanal, généralement Dolby AC-3. Les canaux 0 et 1 contiennent toujours la musique instrumentale d’arrière-plan, tandis que les canaux 2 à 5 peuvent contenir n’importe quelle combinaison de voix de guide, de Melodies de guide et d’effets sonores. Une application karaoké peut contrôler le haut-parleur du volume et de la destination pour chaque canal auxiliaire.

Lorsque le navigateur DVD détecte du contenu de karaoké sur un disque et passe en mode karaoké, il informe le décodeur, qui doit ensuite désactiver les trois canaux supérieurs (les canaux auxiliaires) jusqu’à ce qu’ils soient explicitement activés par une application. Les tâches de base d’une application de karaoké sont les suivantes :

1.  Déterminez le nombre de canaux auxiliaires et leur contenu à l’aide des méthodes [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .
2.  Fournissez une interface utilisateur qui affiche le contenu du canal et permet aux utilisateurs d’activer ou de désactiver un canal auxiliaire à tout moment, à l’aide de [**IDvdControl2 :: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).

Ces étapes sont illustrées dans l’exemple d’application de DVD dans DVDCore. cpp, dans la méthode **GetAudioAttributes** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



