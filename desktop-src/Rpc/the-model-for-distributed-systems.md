---
title: Modèle pour les systèmes distribués
description: Traditionnellement, le fait de disposer d’un système monolithique s’exécutant sur plusieurs ordinateurs signifiait le fractionnement du système en composants distincts du client et du serveur.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859b2a0a83e7f12bd7caf372e60acf2736a114a0cdf46893830032a47a548019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924170"
---
# <a name="the-model-for-distributed-systems"></a>Modèle pour les systèmes distribués

Traditionnellement, le fait de disposer d’un système monolithique s’exécutant sur plusieurs ordinateurs signifiait le fractionnement du système en composants distincts du client et du serveur. Dans ces systèmes, le composant client gérait l’interface utilisateur et le serveur a fourni le traitement principal, tel que l’accès à la base de données, l’impression, etc. À mesure que les ordinateurs proliféraient, chutent et étaient connectés par des réseaux à bande passante jamais supérieure, le fractionnement des systèmes logiciels en plusieurs composants est devenu plus pratique, chaque composant s’exécutant sur un autre ordinateur et effectuant une fonction spécialisée. Cette approche simplifie le développement, la gestion, l’administration et améliore souvent les performances et la robustesse, car la défaillance d’un ordinateur n’a pas nécessairement désactivé l’ensemble du système.

Dans de nombreux cas, le système apparaît au client sous la forme d’un Cloud opaque qui effectue les opérations nécessaires, même si le système distribué est composé de nœuds individuels, comme illustré dans la figure suivante.

![les clients accèdent aux services d’un système de serveurs RPC qui apparaît comme Cloud opaque pour les clients externes](images/indy-nodes.png)

L’opacité du Cloud est maintenue car les opérations informatiques sont appelées pour le compte du client. Ainsi, les clients peuvent localiser un ordinateur (un *nœud*) dans le Cloud et demander une opération donnée. lors de l’exécution de l’opération, cet ordinateur peut appeler des fonctionnalités sur d’autres ordinateurs dans le Cloud sans exposer les étapes supplémentaires, ou l’ordinateur sur lequel ils ont été exécutés, au client.

Avec ce paradigme, les mécanismes d’un système distribué et similaire au Cloud peuvent être répartis en nombreux échanges de paquets individuels ou conversations entre les nœuds individuels.

Les systèmes client-serveur traditionnels ont deux nœuds avec des rôles et des responsabilités fixes. Les systèmes distribués modernes peuvent comporter plus de deux nœuds, et leurs rôles sont souvent dynamiques. Dans une conversation, un nœud peut être un client, alors que dans une autre conversation, le nœud peut être le serveur. Dans de nombreux cas, le consommateur ultime de la fonctionnalité exposée est un client avec un utilisateur assis dans un clavier, qui regarde la sortie. Dans d’autres cas, le système distribué fonctionne sans assistance, en effectuant des opérations en arrière-plan.

Le système distribué ne dispose peut-être pas de clients et de serveurs dédiés pour chaque échange de paquets particulier, mais il est important de se souvenir qu’il existe un appelant, (ou initiateur, qui est souvent appelé client). Il y a également le destinataire de l’appel (souvent appelé serveur). Il n’est pas nécessaire d’avoir des échanges de paquets bidirectionnels dans le format de demande-réponse d’un système distribué. souvent, les messages ne sont envoyés qu’une seule fois.

 

 




