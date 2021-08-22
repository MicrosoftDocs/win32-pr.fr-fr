---
description: L’une des responsabilités les plus importantes d’un fournisseur de services de transport de données est celle qui consiste à fournir des indications au client lorsque certains événements réseau se sont produits.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notification des événements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6fb24f746cbb03860bbd28c1028d92d7865a29c44baedaf2c227cb48536cd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794759"
---
# <a name="notification-of-network-events"></a>Notification des événements réseau

L’une des responsabilités les plus importantes d’un fournisseur de services de transport de données est celle qui consiste à fournir des indications au client lorsque certains événements réseau se sont produits. La liste des événements réseau définis se compose des éléments suivants :

-   **FD \_ Connexion : une** connexion à un hôte distant ou à une session de multidiffusion a été effectuée.
-   **FD \_ ACCEPTER**: un hôte distant effectue une demande de connexion.
-   **FD \_ LECTURE**: les données réseau sont arrivées et peuvent être lues.
-   **FD \_ WRITE**: l’espace est disponible dans les tampons du fournisseur de services afin que des données supplémentaires puissent désormais être envoyées.
-   **FD \_ OOB**: les données hors bande sont disponibles pour la lecture.
-   **FD \_ FERMER**: l’hôte distant a fermé la connexion.
-   **FD \_ QOS**: une modification a eu lieu dans les niveaux de QoS négocié.
-   **FD \_ \_QoS de groupe**: réservé.
-   **FD \_ \_ \_ Changement** de l’interface de routage : une interface locale qui doit être utilisée pour atteindre la destination spécifiée dans l' **interface de routage SIO modification de l' \_ \_ \_ IOCTL** a changé.
-   **FD \_ \_ \_ Modification** de la liste d’adresses : la liste des adresses locales auxquelles l’application peut se lier a changé.

Le jeu d’événements réseau énumérés ci-dessus est parfois appelé événements **FD \_ xxx** . L’indication de l’occurrence d’un ou plusieurs de ces événements réseau peut être donnée de plusieurs façons, selon la manière dont le client demande la notification.

 

 



