---
title: Équilibrage de charge RPC
description: Équilibrage de charge RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028653"
---
# <a name="rpc-load-balancing"></a>Équilibrage de charge RPC

L’équilibrage de charge Microsoft RPC est destiné à fournir une solution évolutive pour les scénarios qui exigent une charge élevée de [RPC sur](remote-procedure-calls-using-rpc-over-http.md) le trafic http. L’objectif principal du Load Balancer RPC est de garantir que le trafic RPC/HTTP peut être assuré par une batterie de serveurs pour améliorer l’évolutivité. Pour ce faire, RPC doit s’assurer que toutes les connexions à partir d’un processus client sont traitées par le même point de terminaison de serveur dans la batterie de serveurs. La Load Balancer RPC est implémentée en tant que service qui s’exécute conjointement avec le service proxy RPC sur HTTP.

Pour activer l’équilibrage de charge, le service d’équilibrage de charge RPC s’exécutant sur chacun des serveurs communique les uns avec les autres pour déterminer le serveur préféré pour la connexion cliente initiale. Ce processus est appelé arbitrage et se produit au moment de la connexion initiale du client. Pour réduire le trafic entre serveurs, le service d’équilibrage de charge RPC choisit le point de terminaison local pour traiter la connexion si le client n’est pas déjà associé à un serveur. Pour une connexion client donnée, le résultat de l’arbitrage est l’une des deux possibilités suivantes :

-   Si le client a déjà établi une connexion, le serveur qui reçoit d’abord la connexion traitera les connexions suivantes.
-   S’il s’agit de la première connexion du client, l’arbitrage se traduira par le serveur local qui gère la connexion et, par conséquent, par toutes les connexions du client. Cette information, une fois déterminée, est validée dans les autres services de Load Balancer RPC de la batterie de serveurs, en les informant du serveur qui gère toutes les demandes du client.

Cette section fournit une vue d’ensemble de l’équilibrage de charge RPC dans les rubriques suivantes :

-   [Déploiement de l’équilibrage de charge](deploying-load-balancing.md)
-   [Configuration de l’équilibrage de charge](configuring-load-balancing.md)
-   [Meilleures pratiques relatives à l’équilibrage de charge](load-balancing-best-practices.md)

## <a name="requirements"></a>Configuration requise

Le service équilibrage de charge RPC est pris en charge sur les serveurs exécutant Windows Server 2008 R2 ou version ultérieure et sur les clients qui exécutent Windows 7 ou versions ultérieures de Windows.

Le service de proxy RPC, le service d’équilibrage de charge RPC et les points de terminaison de serveur doivent tous être en cours d’exécution sur le même ordinateur. En outre, tous les serveurs de la batterie de serveurs doivent pouvoir traiter le point de terminaison demandé. Pour plus d’informations sur la configuration du service de proxy RPC et du service d’équilibrage de charge RPC, consultez [Configuration des ordinateurs pour RPC sur http](configuring-computers-for-rpc-over-http.md) et configuration de l' [équilibrage de charge](configuring-load-balancing.md), respectivement.

## <a name="limitations"></a>Limites

À ce stade, l’équilibrage de charge RPC ne prend en charge qu’une seule batterie de serveurs par ressource. Tous les serveurs de toutes les batteries de serveurs doivent également être en mesure de traiter toutes les ressources.

 

 




