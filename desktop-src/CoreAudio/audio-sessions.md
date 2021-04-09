---
description: Sessions audio
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Sessions audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ae67a3eafe7a76add2fad192823868304e860d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111558"
---
# <a name="audio-sessions"></a>Sessions audio

Une *session audio* est un groupe de flux audio associés qu’un client WASAPI peut gérer collectivement. Les clients peuvent contrôler le niveau de volume et l’État muet de chaque session individuelle. Le système applique les paramètres de volume et de silence spécifiés par le client uniformément à tous les flux de la session.

Lorsqu’un client Initialise un flux audio, il affecte le flux audio à une session audio. Pour plus d’informations, consultez [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Une session audio contient des flux de rendu ou des flux de capture, mais pas les deux. Par défaut, les paramètres volume et muet pour une session de rendu sont persistants entre les redémarrages du système. Les paramètres de volume et de sourdine pour une session de capture ne sont pas persistants. (Une session qui contient des flux qui fonctionnent en mode de bouclage est traitée de la même manière qu’une session de capture. Autrement dit, les paramètres de session ne sont pas persistants. Pour plus d’informations sur le mode de bouclage, consultez [enregistrement en boucle](loopback-recording.md).)

Chaque flux audio appartient à une seule session. Un client assigne un flux audio à une session particulière au moment où il initialise l’objet de flux. Le flux conserve son appartenance dans la session pendant la durée de vie du flux. Après la création d’un objet de flux, l’objet existe jusqu’à ce qu’un client libère la dernière référence comptée à l’objet, puis l’objet est supprimé.

Bien qu’un client ne puisse pas modifier la session à laquelle un flux existant est affecté, il peut obtenir un effet similaire en supprimant le flux (en publiant toutes les références à celui-ci), en créant un nouveau flux pour remplacer le flux supprimé et en assignant le nouveau flux à une autre session.

Chaque session de rendu représente un sous-ensemble des flux qui forment la combinaison globale qui s’exécute via un [périphérique de point de terminaison audio](audio-endpoint-devices.md)particulier. La combinaison globale combine toutes les sessions de toutes les applications qui partagent l’appareil.

Souvent, une application avec plusieurs flux affecte tous ses flux à la même session. Toutefois, l’application peut, en option, assigner différents flux à différentes sessions. Tout flux que l’application n’attribue pas explicitement à une session appartient à la session par défaut.

Les applications audio typiques doivent éviter de modifier les paramètres de volume et de sourdine pour les sessions. Au lieu de cela, les utilisateurs contrôlent ces paramètres par le biais des interfaces utilisateur des programmes de contrôle. Par exemple, dans Windows Vista, le programme fourni par le système, Sndvol.exe, affiche un contrôle du volume et un contrôle muet pour chaque session de rendu active ou récemment active dans le système. Grâce à ces contrôles, les utilisateurs peuvent ajuster les paramètres de volume et de silence pour toutes les sessions dans le système.

Le programme sndvol affiche actuellement des contrôles de volume pour les appareils de point de terminaison de rendu audio uniquement. Elle n’affiche pas de contrôles de volume pour les périphériques de capture audio.

Une session est active si elle contient un ou plusieurs flux actifs. Un flux actif est à l' *État en cours d’exécution*. Un flux inactif est à l' *état arrêté*. Une session devient active lorsque son premier flux devient actif. Une session devient inactive lorsque son dernier flux actif devient inactif. Une fois qu’une session a été inactive pendant un certain temps, le système fait passer l’état de la session de l’état inactif à expiré.

Sndvol affiche les contrôles de volume et de sourdine pour toutes les sessions de rendu actives et inactives. Sndvol supprime les contrôles de volume et de sourdine pour une session lorsque l’état de la session passe d’inactif à expiré, ou lorsque la session se termine. (Une session se termine lorsque le dernier de ses flux est supprimé ; autrement dit, lorsqu’un client libère le nombre de références final sur le dernier objet de flux restant dans la session.) La seule exception à cette règle concerne les sons de notification système. Sndvol affiche toujours les contrôles volume et muet pour les sons de notification système, quel que soit l’état de la session pour ces sons.

En règle générale, un flux appartient à une session qui couvre uniquement le processus qui contient l’application qui a créé le flux. Toutefois, les applications ont la possibilité de définir des sessions interprocessus qui combinent des flux de deux processus ou plus.

WASAPI prend en charge les sessions interprocessus principalement pour que :

-   Le programme sndvol peut présenter à l’utilisateur un contrôle de volume unique pour gérer les sons de notification système dans toutes les applications.
-   Un lecteur multimédia qui s’exécute dans un processus peut diffuser du contenu protégé vers un programme de déchiffrement qui s’exécute dans un autre processus.

Comme pour les paramètres de contrôle pour les sessions de rendu spécifiques au processus, les paramètres de contrôle pour les sessions de rendu inter-processus sont, par défaut, persistants au redémarrage du système. WASAPI fournit ce comportement principalement pour l’avantage des sons de notification système, qui doivent conserver les paramètres de volume et de silence de l’utilisateur lorsque la combinaison d’applications varie dans le temps.

Le programme sndvol libelle le contrôle du volume pour chaque session avec un nom d’affichage et une icône. Un client a la possibilité d’attribuer explicitement un nom complet et une icône à une session. Si le client ne fournit pas ces éléments, sndvol affiche à la place un nom par défaut et une icône par défaut. Le nom par défaut inclut des informations telles que le titre de la fenêtre de l’application. L’icône par défaut est l’icône de la fenêtre d’application. Dans le cas des sessions spécifiques au processus, ces valeurs par défaut fournissent des informations significatives aux utilisateurs. Notez qu’une session inter-processus peut être associée à plusieurs applications. Dans ce cas, seul le nom d’affichage et l’icône fournis par le client sont significatifs.

Bien que les paramètres volume et muet pour une session de rendu soient, par défaut, persistants au redémarrage du système, le nom complet et l’icône fournis par le client ne le sont pas. Pour vous assurer que sndvol affiche le nom et l’icône fournis par le client, le client doit assigner explicitement le nom et l’icône à la session au moment où le client affecte le premier flux à la session. Le système conserve le nom complet et l’icône d’une session uniquement jusqu’à ce que la session se termine.

Chaque session est identifiée par un GUID de session. Au moment où un client ouvre un flux, le client lui affecte ce flux de données. Le client fournit les deux éléments d’information suivants pour identifier cette session :

-   GUID de session.
-   Si la session est une session interprocessus ou spécifique au processus, une session spécifique au processus contient uniquement des flux du processus du client.

Ces informations sont suffisantes pour distinguer une session particulière de toutes les autres sessions dans le même ordinateur. Le GUID de session pour une session spécifique au processus identifie de façon unique la session uniquement dans l’étendue du processus propriétaire de la session. En revanche, le GUID de session pour une session inter-processus est unique dans l’étendue de tous les processus qui s’exécutent sur l’ordinateur.

Dans le cas d’une session spécifique au processus, le système utilise une combinaison de GUID de session et d’ID de processus pour identifier de manière unique la session dans l’étendue de l’ordinateur. Par conséquent, si les clients de deux processus distincts affectent leurs flux respectifs à deux sessions spécifiques à un processus avec des GUID de session identiques, le système traite les sessions comme étant séparées, car leurs ID de processus sont différents. En outre, si une session inter-processus utilise le même GUID de session qu’une ou plusieurs sessions spécifiques au processus, le système traite la session interprocessus comme distincte des sessions spécifiques au processus, même si elle partage le même GUID de session.

Par exemple, dans Windows Vista, les API de niveau supérieur telles que les fonctions **WaveOutXxx** Windows Multimedia et DirectSound attribuent généralement les flux audio qu’ils créent à la valeur par défaut, les sessions spécifiques au processus qui sont identifiées par le GUID de la valeur GUID de session \_ . Pour les clients de ces API, la session par défaut pour chaque processus client est distincte des sessions par défaut pour d’autres processus client, même si les sessions ont des GUID de session identiques. En outre, si une ou plusieurs applications attribuent des flux à la session interprocessus qui est identifiée par la valeur GUID de session GUID \_ null, le système traite cette session inter-processus comme distincte des sessions par défaut spécifiques au processus qui partagent le même GUID de session. En conséquence, le programme sndvol affiche un contrôle de volume distinct pour la session par défaut propre au processus, et il affiche un contrôle de volume supplémentaire pour la session interprocessus qui est identifiée par la valeur GUID de session GUID \_ null, si cette session existe.

Chaque session est associée à un seul périphérique de point de terminaison audio. Si deux sessions ont des GUID de session et des ID de processus identiques, mais sont associés à des appareils différents, le système traite les deux sessions comme étant séparées. Une session ne peut jamais contenir à la fois des flux de capture et de rendu, car un flux de capture peut être associé uniquement à un appareil de capture et un flux de rendu ne peut être associé qu’à un appareil de rendu.

Comme mentionné précédemment, les paramètres de volume et de sourdine pour une session sont persistants au redémarrage du système. Plusieurs instances d’une application peuvent créer des sessions spécifiques au processus avec des GUID de session identiques. Par le biais du programme sndvol, l’utilisateur peut sélectionner des paramètres de volume et de sourdine différents pour chacune de ces sessions. Une fois ces sessions terminées, le système conserve les paramètres de contrôle d’une seule de ces sessions : la dernière session à se terminer. Par la suite, si une nouvelle instance de l’application crée une session spécifique au processus avec le même GUID de session qu’auparavant, cette session hérite des paramètres de volume et de silence précédemment enregistrés.

Une application ne doit pas tenter d’ajouter un flux à ou contrôler le niveau de volume d’une session appartenant à une autre application non liée. En outre, une application ne doit pas tenter de contrôler le niveau de volume de la session gérée par le système pour les sons de notification. Toutefois, une application peut lire un son via la session système pour les sons de notification en appelant la fonction **PlaySound** . Pour plus d’informations, consultez [sons de notification pour les applications audio héritées](notification-sounds-for-legacy-audio-applications.md).

Une application peut s’inscrire pour recevoir des notifications lorsque l’état d’une session change. Pour plus d’informations, consultez [événements de session audio](audio-session-events.md).

Dans de rares cas, une application qui crée une session spécifique au processus peut avoir besoin de consolider le contrôle des sessions spécifiques au processus pour deux instances d’application ou plus sous un contrôle de volume unique dans sndvol. Pour plus d’informations, consultez [GROUPING Parameters](grouping-parameters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 



