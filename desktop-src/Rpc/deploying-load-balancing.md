---
title: Déploiement de l’équilibrage de charge
description: Déploiement de l’équilibrage de charge
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196565"
---
# <a name="deploying-load-balancing"></a>Déploiement de l’équilibrage de charge

L’environnement de déploiement classique et le cas d’usage sont utilisés par l’équilibrage de charge RPC, comme indiqué ci-dessous :![équilibrage de charge RPC](images/rpc-load-balancing.png)

1.  Le client RPC établit une connexion RPC/HTTP à la batterie de serveurs.
2.  La connexion est transférée via le réseau vers un équilibreur de charge frontale
3.  L’équilibreur de charge frontal choisit un serveur pour traiter la demande. Dans cet exemple, l’équilibreur de charge frontale transmet la connexion au serveur 1.
4.  Le service d’équilibrage de charge RPC arbitre la connexion. Il détermine qu’il s’agit de la première connexion du client et associe la connexion au serveur local, le serveur 1.
5.  Le client effectue une deuxième requête RPC/HTTP.
6.  La demande est transférée via le réseau à l’équilibreur de charge frontal.
7.  L’équilibreur de charge frontal choisit un serveur pour traiter la demande. Dans ce cas, l’équilibreur de charge frontal choisit le serveur 2 pour traiter la demande.
8.  Le service de Load Balancer RPC arbitre la connexion. Il reconnaît que les connexions à partir de ce client sont servies par le serveur 1.
9.  La connexion est transférée vers le serveur 1.

 

 




