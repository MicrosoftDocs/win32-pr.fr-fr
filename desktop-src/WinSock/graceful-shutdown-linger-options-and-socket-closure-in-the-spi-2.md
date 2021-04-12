---
description: Il est important de faire la distinction entre l’arrêt d’une connexion de socket et la fermeture d’un Socket.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Arrêt approprié, options du reste et fermeture des sockets dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743cae48977421c08611c79053520799420e9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526164"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Arrêt approprié, options du reste et fermeture des sockets dans le SPI

Il est important de faire la distinction entre l’arrêt d’une connexion de socket et la fermeture d’un Socket. L’arrêt d’une connexion de socket implique un échange de messages de protocole entre les deux points de terminaison, qui est ci-après dénommé « séquence d’arrêt ». Deux classes générales de séquences d’arrêt sont définies : normale et abandonnée. Dans une séquence d’arrêt appropriée, toutes les données qui ont été mises en file d’attente mais pas encore transmises peuvent être envoyées avant la fermeture de la connexion. Lors d’un arrêt abandonné, toutes les données non envoyées sont perdues. L’occurrence d’une séquence d’arrêt (normale ou abandonnée) peut également être utilisée pour fournir une \_ indication FD Close aux applications associées, ce qui signifie qu’un arrêt est en cours. En revanche, si vous fermez un socket, le handle de socket devient désalloué afin que l’application ne puisse plus référencer ou utiliser le socket de quelque manière que ce soit.

Dans Windows Sockets, la fonction [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) et la fonction [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) peuvent être utilisées pour initier une séquence d’arrêt, tandis que la fonction [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) est utilisée pour libérer les descripteurs de socket et libérer les ressources associées. Toutefois, une certaine confusion est due au fait que la fonction **WSPCloseSocket** entraînera implicitement une séquence d’arrêt si elle ne s’est pas déjà produite. En fait, il est devenu une pratique de programmation assez courante pour s’appuyer sur cette fonctionnalité et utiliser **WSPCloseSocket** pour initier la séquence d’arrêt et libérer le handle de Socket.

Pour faciliter cette utilisation, l’interface de Sockets fournit des contrôles par le biais du mécanisme d’option de socket qui permet au programmeur d’indiquer si la séquence d’arrêt implicite doit être normale ou abandonnée, et également si la fonction doit attendre la fin de l’exécution d’une séquence d’arrêt normale.

En définissant les valeurs appropriées pour les options de socket afin d’en \_ attendre, et donc \_ DONTLINGER, les types de comportement suivants peuvent être obtenus avec la fonction [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) .

-   Séquence d’arrêt abandonnée, retour immédiat de [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Arrêt correct, retarder le renvoi jusqu’à la fin de la séquence d’arrêt ou l’expiration d’un intervalle de temps spécifié. Si l’intervalle de temps expire avant la fin de la séquence d’arrêt appropriée, une séquence d’arrêt abandonnée se produit et [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) retourne.
-   Arrêt correct, retour immédiat et autoriser la fin de la séquence d’arrêt en arrière-plan. Il s'agit du comportement par défaut. Notez, toutefois, que l’application n’a aucun moyen de savoir quand (ou si) la séquence d’arrêt appropriée est terminée.

Une technique qui peut être utilisée pour réduire le risque de problèmes survenant lors de la destruction de la connexion ne s’appuie pas sur un arrêt implicite initié par [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)). Au lieu de cela, l’une des deux fonctions d’arrêt explicites ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) ou [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))) est utilisée. Cela entraîne \_ la réception d’une indication FD close par l’application homologue indiquant que toutes les données en attente ont été reçues. Pour illustrer cela, le tableau suivant présente les fonctions qui seraient appelées par les composants client et serveur d’une application, où le client est responsable de l’initialisation d’un arrêt approprié.

| Côté client                                                                                                                         | Côté serveur                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) appelle [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD \_ Send) pour signaler la fin de la session et ce client n’a plus de données à envoyer. |                                                                                                              |
|                                                                                                                                     | (2) reçoit FD \_ Close, ce qui indique un arrêt correct en cours et que toutes les données ont été reçues.        |
|                                                                                                                                     | (3) envoie toutes les données de réponse restantes.                                                                       |
| (5 ') obtient FD \_ Read et Invoke recv pour obtenir toutes les données de réponse envoyées par le serveur.                                                         | (4) appelle [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD \_ Send) pour indiquer que le serveur n’a plus de données à envoyer. |
| (5) reçoit l' \_ indication FD Close.                                                                                                  | (4 ') appelle [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) appelle [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

La séquence de minutage est conservée de l’étape (1) à l’étape (6) entre le client et le serveur. à l’exception des étapes (4 ') et (5 ') qui ont uniquement une importance locale dans le sens où l’étape (5) suit l’étape (5 ') côté client tandis que STEP (4 ') suit STEP (4) côté serveur, sans aucune relation de synchronisation avec le tiers distant.

 

 
