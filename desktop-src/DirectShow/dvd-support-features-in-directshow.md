---
description: Fonctionnalités de prise en charge des DVD dans DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Fonctionnalités de prise en charge des DVD dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f143bab35a8b9a4a0cb12af20c2c2c3b66a0822a24cfc054b1f5d30bd4bc3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107899"
---
# <a name="dvd-support-features-in-directshow"></a>Fonctionnalités de prise en charge des DVD dans DirectShow

La fonctionnalité du filtre de [navigateur DVD](dvd-navigator-filter.md) est exposée par le biais de deux interfaces, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), qui fournit les méthodes « Set » pour le navigateur DVD et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), qui fournit les méthodes « obtenir ».

Le navigateur DVD prend en charge les fonctionnalités suivantes :

-   Support karaoké : vous pouvez écrire une application DVD-karaoké à l’aide du navigateur DVD. (Cela nécessite un décodeur compatible).
-   Accès simplifié aux chaînes d’informations de texte du DVD : le navigateur DVD analyse ces chaînes et permet aux applications de les énumérer facilement, de les identifier et de les récupérer.
-   Contrôle du volume audio via [ **IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Prise en charge de la personnalisation du comportement du navigateur DVD lors de l’émission de la commande Stop : les applications peuvent indiquer au navigateur DVD de reprendre à partir de l’emplacement actuel lors du redémarrage du graphique de filtre ou de démarrer la lecture à partir du début du disque.
-   La prise en charge de l’audio Digital Theater Systems (DTS) et Sony Dynamic Digital Audio (SDD). Les flux audio DTS et SDD sont reconnus par le navigateur DVD et transmis au décodeur audio. (Un décodeur compatible DTS tiers ou compatible avec SDD est requis pour décoder et lire l’audio.)
-   Amélioration de la prise en charge des modifications du niveau parental : le navigateur DVD permet à une application d’accepter, de rejeter ou d’ignorer les commandes de modification du niveau parental sur le disque.
-   Options avancées pour la gestion de l’état du navigateur DVD et des commandes de synchronisation
-   Prise en charge du pas à pas détaillé, de la recherche et de la lecture inversée. Ces fonctionnalités nécessitent un décodeur vidéo qui les prend en charge.
-   La possibilité d’enregistrer l’emplacement actuel dans un titre et de le retourner à tout moment.
-   Prise en charge simplifiée des événements de temps dans les titres PGC non séquentiels : pour les titres de PGC non séquentiels, le navigateur DVD relaie les informations de code de temps brutes à l’application.
-   Informations de code d’heure. La structure du [**\_ \_ code temporel DVD HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) peut être utilisée à la place du format binaire codé décimal (BCD). **DVD \_ Le \_ code temporel HMSF** contient des membres faciles d’accès pour les heures, les minutes, les secondes et les frames, et peut être converti en/à partir d’un **ULong**.
-   La possibilité de contrôler si le graphique de filtre est vidé après une opération de recherche : les mémoires tampons de graphique peuvent contenir jusqu’à quelques secondes de vidéo à un moment donné. Vous pouvez faire en sorte que le graphique termine la lecture de la vidéo mise en mémoire tampon après une recherche, ou commence immédiatement au nouvel emplacement.
-   La possibilité de définir des valeurs dans les registres de paramètres généraux : une fonctionnalité avancée pour les personnes connaissant la spécification du DVD qui souhaitent implémenter des fonctionnalités avancées.
-   La possibilité de générer des identificateurs de disque numérique à des fins pratiques uniques

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>De quel arrière-plan ai-je besoin pour écrire une application DVD ?

Tous les développeurs d’applications doivent avoir une connaissance de base des fonctionnalités offertes par la technologie DVD, telles que les niveaux de gestion parental, les flux audio et de sous-image multiples et les blocs angulaires. Les [notions de base](dvd-basics.md) sur les DVD décrivent brièvement chacune de ces fonctionnalités. des descriptions plus complètes sont disponibles dans les publications tierces. Vous n’avez pas besoin de faire référence à la spécification DVD, sauf si vous envisagez d’implémenter des fonctionnalités avancées au-delà du jeu de commandes Annexe J.

les développeurs C/C++ qui utilisent DirectShow doivent être familiarisés avec les techniques de programmation de client com, telles que la création d’objets com et l’obtention et la libération de pointeurs d’interface com. Vous aurez peut-être également besoin d’une connaissance générale des opérations de graphique de filtre, car vous devrez peut-être accéder au graphique et le manipuler directement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



