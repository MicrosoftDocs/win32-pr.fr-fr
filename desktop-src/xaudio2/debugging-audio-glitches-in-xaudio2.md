---
description: Des problèmes peuvent se produire dans XAudio2, cette rubrique décrit comment ils sont signalés et certaines approches pour les résoudre.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Débogage des problèmes audio dans XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866494"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Débogage des problèmes audio dans XAudio2

Des problèmes peuvent se produire dans XAudio2, cette rubrique décrit comment ils sont signalés et certaines approches pour les résoudre.

Cette présentation couvre les rubriques suivantes :

-   [Causes de problèmes ou de problèmes de sortie audio](#causes-of-audio-output-problems-or-glitches)
-   [Comment XAudio2 signale les problèmes](#how-xaudio2-reports-problems)
-   [Approches de la résolution des problèmes](#approaches-to-fixing-problems)
-   [Rubriques connexes](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Causes de problèmes ou de problèmes de sortie audio

Des problèmes peuvent se produire dans la sortie XAudio2 pour plusieurs raisons.

-   Une voix source XAudio2 est en privé. Le client n’envoie pas de son actualisé suffisamment rapidement. Vous recevez un silence, car il n’a pas de données à lire.
-   XAudio2 dans son ensemble est surchargé. Elle prend plus de *x* ms pour produire *X* ms de l’audio. Vous obtenez des pertes, car XAudio2 ne peut pas produire de données aussi rapidement que le périphérique audio en a besoin. Il se peut que vous exécutiez trop de voix ou d’effets à la fois, en effectuant trop de tâches dans les rappels XAudio2 ou en effectuant des appels d’API XAudio2 trop fréquents.
-   Le thread de traitement audio s’arrête car l’implémentation du client d’un rappel XAudio2 fait des choses qui peuvent bloquer le thread. Par exemple, il peut accéder au disque, se synchroniser avec d’autres threads ou appeler d’autres fonctions qui peuvent se bloquer. Utilisez un thread d’arrière-plan de priorité inférieure que le rappel peut signaler pour effectuer ces tâches.
-   Le système dans son ensemble est surchargé. Les autres threads qui s’exécutent avec une priorité identique ou supérieure à XAudio2 font trop de travail. Ils sont en concurrence avec le thread audio pour le temps processeur.

## <a name="how-xaudio2-reports-problems"></a>Comment XAudio2 signale les problèmes

XAudio2 peut communiquer des problèmes dans la version de débogage de plusieurs façons.

-   Si une voix est déplacée, XAudio2 affiche un message dans ce formulaire.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Si le thread audio s’exécute trop longtemps, XAudio2 affiche un message dans ce formulaire.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    En règle générale, ce message s’affiche avec le message suivant.

-   Si le pilote audio ne peut pas alimenter de nouvelles données audio à temps, XAudio2 affiche un message dans ce formulaire.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   L’appel de [**IXAudio2 :: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fournit des données de performance XAudio2, notamment le nombre total de problèmes depuis le démarrage du moteur XAudio2.

## <a name="approaches-to-fixing-problems"></a>Approches de la résolution des problèmes

Les méthodes possibles pour réduire les problèmes audio sont les suivantes :

-   Dans le cas de la privation de voix : augmentez la quantité de données audio mises en file d’attente sur une voix. Vous pouvez utiliser [**IXAudio2SourceVoice :: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) pour découvrir le nombre de mémoires tampons mises en file d’attente à tout moment. Si vous voyez toujours des erreurs de privation de voix, mais que vous ne pouvez pas entendre de problème, assurez-vous que vous définissez la [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Signale** à \_ \_ la fin du \_ flux XAUDIO2 sur la mémoire tampon finale d’un son. Cela indique à XAudio2 de ne pas s’attendre à ce qu’un plus grand nombre de mémoires tampons soient nécessairement disponibles dès que celui-ci se termine.

    Dans les autres cas :

    -   Réduisez le nombre de voix et d’effets actifs dans le graphique, en particulier les effets coûteux tels que la réverbération.
    -   Désactivez les voix et les effets que vous n’utilisez pas.
    -   Utilisez les \_ indicateurs XAUDIO2 Voice \_ NOSRC et XAUDIO2 \_ voix \_ notonale dans [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), dans la mesure du possible. La conversion du taux d’échantillonnage est coûteuse.
    -   Réduisez le taux d’échantillonnage des voix individuelles. Par exemple, une voix de mixage secondaire hébergeant un effet de réverbération peut avoir un taux d’échantillonnage inférieur à celui de la voix source qui l’envoie. Des sons tels que des explosions et des gunshots qui n’ont pas besoin d’une haute fidélité peuvent également être enregistrés à des taux d’échantillonnage inférieurs.
    -   Assurez-vous que les implémentations de rappel fonctionnent aussi peu que possible et ne sont jamais bloquées.
    -   Effectuez moins d’appels à XAudio2. En règle générale, les paramètres audio n’ont pas besoin d’être mis à jour pour chaque image vidéo. Toutes les 30 ms suffisent. Vous devez éliminer les appels redondants, tels que le réglage du volume plusieurs fois en succession rapide.
    -   Réduisez l’utilisation globale du processeur par le jeu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de débogage](debugging-facilities.md)
</dt> <dt>

[Référence de programmation XAudio2](programming-reference.md)
</dt> </dl>

 

 
