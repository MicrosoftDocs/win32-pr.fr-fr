---
description: Contrôles du volume de session
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Contrôles du volume de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe45dce825dedd116c8f9c65684ac665eb6483f95dec3d247071f66408e8ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758889"
---
# <a name="session-volume-controls"></a>Contrôles du volume de session

Comme expliqué précédemment, les clients WASAPI peuvent contrôler individuellement le niveau de volume de chaque [session audio](audio-sessions.md). WASAPI applique le paramètre de volume pour une session uniformément à tous les flux de la session. Chaque niveau de volume est une valeur comprise entre 0,0 et 1,0, où 0,0 indique un silence et 1,0 indique un volume complet (aucune atténuation).

Un client crée implicitement une session en affectant le premier flux à cette session. Le niveau de volume par défaut de la nouvelle session est 1,0. Comme nous l’avons vu précédemment, l’utilisateur peut ajuster le niveau de volume de la session par le biais de l’interface utilisateur d’un programme de contrôle (par exemple, sndvol) qui est un client WASAPI. Les paramètres de contrôle sont persistants.

En plus des paramètres de volume contrôlés par le client, le système applique ses propres paramètres de volume aux sessions. Ces paramètres sont basés sur la stratégie audio et changent dynamiquement en réponse aux modifications apportées aux flux qui composent la combinaison audio globale. Pour plus d’informations sur la stratégie audio, consultez [composants audio en mode utilisateur](user-mode-audio-components.md).

Le logiciel système qui implémente le contrôle du volume pour chaque flux multiplie les échantillons PCM dans le flux par le niveau de volume effectif. Le niveau de volume effectif est le résultat de la multiplication des paramètres du volume du client et du système. Ainsi, la modification qui en résulte dans l’amplitude du signal est une combinaison linéaire des niveaux du client et du volume système. Par exemple, si le niveau de volume client est 0,8 et que le niveau de volume système est 0,5, le niveau de volume effectif est (0,8)<sup>.</sup> (0,5) = 0,4.

Notez que le bruit perçu n’est pas linéaire en ce qui concerne l’amplitude du signal. Au lieu de cela, le niveau sonore varie approximativement en tant que logarithme du volume v :

intensité sonore en décibels = 20<sup>.</sup> log ₁ ₀ (v)

Par conséquent, la définition de v = 0,5 atténue le volume d’origine du signal d’origine (le signal avant l’application du niveau de volume) par 6 décibels, le paramètre v = 0,25 atténue le signal par 12 décibels, et ainsi de suite. Un volume niveau v = 1,0, correspondant à 0 décibels, ne modifie pas le niveau de signal d’origine.

Les applications audio avec des interfaces utilisateur pour contrôler le niveau de volume affichent généralement des curseurs qui génèrent des modifications de l’intensité perçue qui sont proportionnelles aux modifications de la position du curseur. Pour produire une relation linéaire entre la position de curseur et le bruit perçus, l’application doit définir une relation non linéaire entre le niveau de volume v et la position du curseur. Pour plus d’informations, consultez [contrôles de volume à cônes audio](audio-tapered-volume-controls.md).

Comme expliqué précédemment, le programme de contrôle de volume système, sndvol, affiche des curseurs de volume pour les sessions audio qui sont lues sur chaque périphérique de rendu audio. Ces curseurs s’affichent dans la zone de groupe intitulée **applications** dans la fenêtre SndVol. En règle générale, chaque session contient tous les flux de lecture à partir d’une fenêtre d’application particulière. À travers les curseurs de la fenêtre sndvol, les utilisateurs contrôlent les niveaux de volume des applications audio individuelles.

En règle générale, une application doit assigner tous ses flux de lecture à la même session audio. WASAPI n’empêche pas une application de distribuer ses flux de lecture entre plusieurs sessions. Toutefois, la prolifération résultante des curseurs de volume dans sndvol peut dérouter les utilisateurs.

En guise d’option, une fenêtre d’application peut afficher un curseur de volume. Le curseur application doit refléter l’état du curseur sndvol correspondant à tout moment. Ainsi, si l’utilisateur modifie le niveau de volume en déplaçant le curseur dans la fenêtre de l’application, le curseur correspondant dans la fenêtre sndvol doit se déplacer de pair avec le curseur de l’application. De même, si l’utilisateur déplace le curseur sndvol, le curseur application doit se déplacer de pair avec le curseur sndvol.

Pour prendre en charge ce comportement, WASAPI implémente l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Lorsque l’utilisateur déplace le curseur application, l’application appelle la méthode [**ISimpleAudioVolume :: SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) pour ajuster le niveau de volume de la session en conséquence. Sndvol surveille les modifications de volume effectuées via cette méthode et reflète les modifications apportées aux curseurs de volume qu’il affiche. En outre, une application peut recevoir des notifications de modifications du volume de session que l’utilisateur effectue via sndvol. À cet effet, l’application implémente une interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) et inscrit l’interface auprès de WASAPI. Ensuite, chaque fois que l’utilisateur modifie le niveau de volume de session via sndvol, l’application reçoit un appel de notification via la méthode [**IAudioSessionEvents :: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) . Pour obtenir un exemple de code qui implémente une interface **IAudioSessionEvents** , consultez [événements de session audio](audio-session-events.md). Pour obtenir un exemple de code qui inscrit une interface **IAudioSessionEvents** , consultez [événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md).

L’interface **ISimpleAudioVolume** applique le même niveau de volume uniformément à tous les canaux dans une session audio. Bien que cette interface réponde aux exigences de contrôle de volume de la plupart des applications, certaines applications peuvent nécessiter des fonctionnalités de contrôle de volume plus spécialisées. L’interface [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) contrôle le volume d’un flux individuel dans une session par rapport aux autres flux de la session. **IAudioStreamVolume** permet également à un client de contrôler individuellement les niveaux de volume de tous les canaux dans le flux. Par exemple, une application peut utiliser cette fonctionnalité pour obtenir des effets audio tels que la simulation du mouvement spatial d’une source audio en panoramique de gauche à droite. Une autre interface spécialisée, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), contrôle les niveaux de volume des canaux individuels dans une session. Par exemple, une application peut utiliser **IChannelAudioVolume** pour implémenter des contrôles d’équilibre pour un système de son Stereophonic.

Les curseurs de volume de la zone **applications** dans sndvol reflètent uniquement les modifications de volume effectuées via l’interface **ISimpleAudioVolume** . Ils ne reflètent pas les modifications de volume effectuées par le biais des interfaces **IAudioStreamVolume** et **IChannelAudioVolume** . Bien que certaines applications puissent permettre aux utilisateurs de contrôler directement ou indirectement les paramètres de volume via **IAudioStreamVolume** et **IChannelAudioVolume**, les développeurs doivent éviter de présenter des curseurs d’application pour ces paramètres de volume que les utilisateurs sont susceptibles de confondre avec les curseurs de volume dans sndvol. Dans le cas contraire, un utilisateur peut déplacer un curseur d’application en attendant que la modification soit reflétée dans un curseur sndvol et se déformer quand aucune modification n’est apportée. Les développeurs peuvent éviter ce problème grâce à une conception d’interface utilisateur attentive.

Le niveau de volume effectif de n’importe quel canal dans le mixage secondaire de session, tel qu’il est entendu aux orateurs, est le produit des quatre facteurs de niveau de volume suivants :

-   Niveaux de volume par canal des flux de la session, que les clients peuvent contrôler via les méthodes dans l’interface **IAudioStreamVolume** .
-   Niveau de volume par canal de la session, que les clients peuvent contrôler via les méthodes dans l’interface **IChannelAudioVolume** .
-   Niveau de volume principal de la session, que les clients peuvent contrôler via les méthodes dans l’interface **ISimpleAudioVolume** .
-   Niveau de volume basé sur la stratégie de la session, que le système modifie dynamiquement à mesure que la combinaison globale change.

Chacun des quatre facteurs de niveau volume de la liste précédente est une valeur comprise entre 0,0 et 1,0, où 0,0 indique un silence et 1,0 indique un volume complet (aucune atténuation). Le niveau de volume effectif est également une valeur comprise entre 0,0 et 1,0.

Le moteur audio applique le niveau de volume effectif pour chaque canal aux canaux dans un flux de données avant de mélanger le flux avec les autres flux dans la session audio. Si des valeurs d’échantillon d’un canal dépassent 0 décibels après que le moteur audio les a multiplié par le niveau de volume effectif, le moteur découpe les exemples avant de les ajouter au mixage de la session.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles de volume](volume-controls.md)
</dt> </dl>

 

 



