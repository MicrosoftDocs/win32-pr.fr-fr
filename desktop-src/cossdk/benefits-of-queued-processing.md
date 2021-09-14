---
description: Avantages du traitement en file d’attente
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Avantages du traitement en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013010"
---
# <a name="benefits-of-queued-processing"></a>Avantages du traitement en file d’attente

Lors de la conception de nouvelles applications, les développeurs doivent prendre en compte les implications du codage des composants pour le traitement en temps réel (synchrone) et le traitement en file d’attente (asynchrone). Le choix dépend des exigences de l’application spécifique, tel que déterminé par la logique métier sous-jacente. En règle générale, le traitement en file d’attente offre les avantages suivants par rapport au traitement en temps réel :

-   Dépendance réduite à la disponibilité des composants
-   Durées de vie des composants plus courtes
-   Productivité ininterrompue lors de l’utilisation d’applications déconnectées
-   Fiabilité des messages
-   Planification de serveur efficace

## <a name="component-availability"></a>Disponibilité des composants

Dans une application de traitement en temps réel, si un seul composant de la transaction n’est pas disponible, peut-être en raison de problèmes de surcharge du serveur ou de mise en réseau, le processus entier est bloqué et ne peut pas se terminer. En revanche, une application utilisant le service de composants en file d’attente COM+ sépare la transaction en activités qui doivent être terminées maintenant et celles qui peuvent être terminées ultérieurement. Par exemple, les messages peuvent être mis en file d’attente pour un traitement ultérieur afin que le composant demandeur soit libre pour d’autres tâches.

## <a name="component-lifetimes"></a>Durées de vie des composants

Une application utilisant le service de composants en file d’attente permet au composant serveur de fonctionner indépendamment du client. Par conséquent, les composants serveur peuvent s’exécuter plus rapidement. Dans un système en temps réel, le composant serveur existe à partir du moment où il est créé jusqu’à ce que l’objet soit finalement libéré. Le serveur attend que le client effectue des appels de méthode et que les résultats soient retournés, ce qui inverse le cycle rapide des objets serveur et limite l’extensibilité du serveur.

## <a name="disconnected-applications"></a>Applications déconnectées

L’utilisation accrue des ordinateurs portables, des ordinateurs portables et des ordinateurs de poche a créé un besoin pour les applications qui utilisent occasionnellement des clients déconnectés ou des utilisateurs mobiles. Dans un système en file d’attente, ces utilisateurs peuvent continuer à travailler dans un scénario déconnecté ou lorsqu’ils ne sont pas connectés au serveur, et ils peuvent se connecter ultérieurement aux bases de données ou aux serveurs pour traiter leurs demandes. Par exemple, un vendeur peut prendre les commandes des clients et se connecter ultérieurement au service des expéditions pour traiter ces commandes.

Si vous disposez d’un composant qui peut être exécuté en mode connecté ou déconnecté, les messages sont en déplacement dans une direction et il est rarement nécessaire de basculer entre eux. Par exemple, dans le scénario de la commande, le composant expédition reçoit le message et le traite. Il peut générer un autre composant pour la facturation ou l’audit. Le client est validé avant le démarrage du serveur. Le message n’est pas envoyé tant que l’application n’est pas validée.

L’illustration suivante montre le déroulement des informations dans un scénario déconnecté.

![Diagramme qui montre le workflow d’informations entre le client et le serveur.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Fiabilité des messages

Message Queuing est un outil puissant qui utilise des techniques de base de données pour protéger les données de manière fiable. En cas de défaillance d’un serveur, Message Queuing garantit que les transactions sont restaurées afin que les messages ne soient pas perdus et que les données ne soient pas endommagées.

## <a name="server-scheduling"></a>Planification du serveur

Une application utilisant des composants en file d’attente est bien adaptée à l’exécution des composants décalés, qui diffère le travail non critique à une période creuse. Il s’agit du même concept utile que celui appliqué au traitement classique en mode batch. Des demandes similaires peuvent être différées pour une exécution contiguë par le serveur plutôt que de demander au serveur de réagir immédiatement à une grande variété de demandes.

 

 



