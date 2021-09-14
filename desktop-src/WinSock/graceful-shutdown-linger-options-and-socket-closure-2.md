---
description: La documentation suivante est fournie pour clarifier l’objet de la fermeture des connexions de socket qui ferment les sockets. Il est important de distinguer la différence entre l’arrêt d’une connexion de socket et la fermeture d’un Socket.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Arrêt approprié, options de maintien et fermeture de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008269"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Arrêt approprié, options de maintien et fermeture de socket

La documentation suivante est fournie pour clarifier l’objet de la fermeture des connexions de socket qui ferment les sockets. Il est important de distinguer la différence entre l’arrêt d’une connexion de socket et la fermeture d’un Socket.

L’arrêt d’une connexion de socket implique l’échange de messages de protocole entre les deux points de terminaison, ci-après dénommés « séquence d’arrêt ». Deux classes générales de séquences d’arrêt sont définies : normal et abortive (également appelé Hard). Dans une séquence d’arrêt appropriée, toutes les données qui ont été mises en file d’attente mais pas encore transmises peuvent être envoyées avant la fermeture de la connexion. Lors d’un arrêt abandonné, toutes les données non envoyées sont perdues. L’occurrence d’une séquence d’arrêt (normale ou abandonnée) peut également être utilisée pour fournir une \_ indication FD Close aux applications associées, ce qui signifie qu’un arrêt est en cours.

En revanche, si vous fermez un socket, le handle de socket devient désalloué afin que l’application ne puisse plus référencer ou utiliser le socket de quelque manière que ce soit.

dans Windows sockets, la fonction [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) et la fonction [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) peuvent être utilisées pour initier une séquence d’arrêt, tandis que la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) est utilisée pour libérer les descripteurs de socket et libérer les ressources associées. Toutefois, une certaine confusion est due au fait que la fonction **opération closesocket** provoque implicitement une séquence d’arrêt si elle ne s’est pas déjà produite. En fait, il est devenu une pratique de programmation assez courante pour s’appuyer sur cette fonctionnalité et pour utiliser **opération closesocket** à la fois pour initier la séquence d’arrêt et pour libérer le handle de Socket.

Pour faciliter cette utilisation, l’interface de Sockets fournit des contrôles par le biais du mécanisme d’option de socket qui permet au programmeur d’indiquer si la séquence d’arrêt implicite doit être normale ou abandonnée, et également si la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) doit rester en attente (ce qui n’est pas immédiatement terminé) pour permettre l’exécution d’une séquence d’arrêt normale. Ces différences importantes et les ramifications de l’utilisation de **opération closesocket** de cette façon ne sont toujours pas largement comprises.

En définissant les valeurs appropriées pour les options de socket afin d’en \_ attendre, et donc \_ DONTLINGER, les types de comportement suivants peuvent être obtenus avec la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) :

-   Séquence d’arrêt abandonnée, retour immédiat de [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).
-   Arrêt approprié, retardant le retour jusqu’à la fin de la séquence d’arrêt ou l’expiration d’un intervalle de temps spécifié. Si l’intervalle de temps expire avant la fin de la séquence d’arrêt appropriée, une séquence d’arrêt abandonnée se produit et [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) retourne.
-   Arrêt progressif, retour immédiat, ce qui permet à la séquence d’arrêt de se terminer en arrière-plan. Bien qu’il s’agisse du comportement par défaut, l’application n’a aucun moyen de savoir quand (ou si) la séquence d’arrêt appropriée est réellement terminée.

L’utilisation des options de \_ Socket SO et so \_ DONTLINGER et de la structure restante associée est abordée plus en détail dans les sections de référence sur les options de [](/windows/desktop/api/winsock/ns-winsock-linger) socket de socket [**série sur sol \_**](sol-socket-socket-options.md) et la structure de **Lingo** .

Une technique qui peut être utilisée pour réduire le risque de problèmes survenant au cours de la destruction de la connexion consiste à éviter d’utiliser un arrêt implicite initié par [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). Utilisez plutôt l’une des deux fonctions d’arrêt explicites, [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) ou [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect). Cela provoque à son tour \_ la réception d’une indication FD close par l’application homologue indiquant que toutes les données en attente ont été reçues. Pour illustrer cela, le tableau suivant présente les fonctions qui seraient appelées par les composants client et serveur d’une application, où le client est responsable de l’initialisation d’un arrêt approprié.

| Côté client                                                                                                                | Côté serveur                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) appelle [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) pour signaler la fin de la session et ce dernier n’a plus de données à envoyer. |                                                                                                       |
|                                                                                                                            | (2) reçoit FD \_ Close, ce qui indique un arrêt correct en cours et que toutes les données ont été reçues. |
|                                                                                                                            | (3) envoie toutes les données de réponse restantes.                                                                |
| (précision de minuterie locale uniquement) Obtient FD \_ Read et appelle [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) pour obtenir toutes les données de réponse envoyées par le serveur.  | (4) appelle [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) pour indiquer que le serveur n’a plus de données à envoyer.  |
| (5) reçoit l' \_ indication FD Close.                                                                                         | (précision de minuterie locale uniquement) Appelle [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .                       |
| (6) appelle [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                          |                                                                                                       |



 

 

 



