---
description: 'En savoir plus sur : niveaux de suivi Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Niveaux de suivi Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531728"
---
# <a name="winsock-tracing-levels"></a>Niveaux de suivi Winsock

## <a name="levels-of-winsock-tracing"></a>Niveaux de suivi Winsock

Il existe deux niveaux de journalisation possibles dans le suivi Winsock :

-   Information
-   Commentaires

Le niveau d’information effectue le suivi des événements de création et de fermeture de socket, ainsi que toutes les erreurs qui se produisent sur le Socket.

Le niveau détaillé inclut les événements de niveau informations et ajoute un suivi supplémentaire pour les événements d’envoi et de réception. La journalisation documentée est utilisée pour intercepter les problèmes d’endommagement de la mémoire tampon, ainsi que les applications mal écrites.

Les informations ou le niveau de détail peuvent être utilisés avec le suivi d’événements réseau Winsock. Le suivi des modifications du catalogue Winsock ne prend en charge que le niveau d’information.

## <a name="information-event-tracing"></a>Suivi des événements d’informations

La liste suivante détaille les opérations de socket d’événements réseau Winsock qui sont suivies au niveau des informations :

-   Création de socket

    Un événement est enregistré dans une session de création de socket qui peut être utilisé pour suivre la durée de vie d’un Socket. Ces événements incluent également les sockets créés en acceptant des connexions sur un socket d’écoute.

-   Lier

    L’adresse IP locale est journalisée pour aider à mettre en corrélation les informations de suivi Winsock avec les appels de socket d’une application.

-   Se connecter

    L’adresse IP distante du socket connecté est journalisée pour aider à mettre en corrélation les informations de suivi Winsock avec les appels de socket d’une application.

-   Abandons et annulations initiés par Winsock

    À chaque fois que Winsock abandonne ou annule activement une demande, l’événement est consigné.

-   Réinitialisations initiées par le transport

    Chaque fois que le transport sous-jacent indique qu’une connexion a été réinitialisée, l’événement est consigné.

-   Erreurs d’envoi et de réception

    Chaque fois qu’un appel d’envoi ou de réception vers le transport sous-jacent échoue, l’événement est consigné.

-   Déconnexion et fermeture du socket

    Un événement est consigné lorsqu’un handle de socket est fermé.

## <a name="verbose-event-tracing"></a>Suivi des événements détaillés

Tous les événements d’information sont suivis au niveau détaillé. La liste suivante détaille les opérations de socket d’événements réseau Winsock supplémentaires qui sont suivies au niveau de détail :

-   Mémoires tampons d’envoi et de réception

    Les événements sont consignés dans les longueurs et les adresses de tampon d’utilisateur lorsque les appels d’envoi et de réception sont publiés dans Winsock, ainsi qu’à la fin de ces appels. Cela est utile pour diagnostiquer les problèmes de réutilisation de la mémoire tampon et pour une utilisation inefficace des mémoires tampons.

-   Options de socket

    Un événement est consigné lorsqu’une application modifie certaines valeurs d’option de Socket. Certaines des options journalisées incluent SO \_ SNDBUF, donc \_ RCVBUF, SIO active la mise en \_ \_ \_ file d’attente circulaire et FIONBIO.

-   WSAPoll et sélectionnez

    Un événement est consigné dans le journal de l’utilisation d’une application de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) et des appels [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) qui peuvent être utilisés pour rechercher des goulots d’étranglement de performances.

-   Abandons et annulations initiés par Winsock

    À chaque fois que Winsock abandonne ou annule activement une demande, l’événement est consigné.

-   Masque d’événement

    Un événement est consigné dans le journal du masque d’événement qu’une application inscrit pour l’utilisation de la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

-   Datagramme

    Un événement est consigné chaque fois qu’un datagramme arrive et qu’il n’y a pas d’espace de mémoire tampon dans lequel le copier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Détails du suivi d’événements réseau Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
