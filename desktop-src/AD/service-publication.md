---
title: Publication de service
description: Les services se publient eux-mêmes à l’aide d’objets stockés dans Active Directory Domain Services.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- Publication de service Active Directory
- Active Directory, utilisation, publication de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b74c20077d0bc3dcce75b74df99abcda2f78ce23f22bdd78f997d3972c58c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183408"
---
# <a name="service-publication"></a>Publication de service

Les services se publient eux-mêmes à l’aide d’objets stockés dans Active Directory Domain Services. C’est ce que l’on appelle la *publication de service*. Les clients interrogent le répertoire pour localiser les services. C’est ce que l’on appelle le *Rendezvous client-service*. Cette section décrit les types d’objets d’annuaire utilisés pour la publication de service et explique comment ils sont utilisés pour le rendezvous client-service.

Cette section aborde les sujets suivants :

-   [Vue d’ensemble de la publication de service](about-service-publication.md)
-   [Problèmes de sécurité pour la publication de service](security-issues-for-service-publication.md)
-   [Objets point de connexion](connection-points.md)
-   [Publication avec des points de connexion de service (SCP)](publishing-with-service-connection-points.md)
-   [Informations à stocker dans un point de connexion de service](service-connection-point-properties.md)
-   [Où créer un point de connexion de service](where-to-create-a-service-connection-point.md)
-   [Publication de services de base de données, basés sur l’hôte et réplicables à l’aide de points de connexion de service](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [Création et gestion d’un point de connexion de service](creating-and-maintaining-a-service-connection-point.md)
-   [Comment un client interroge un SCP et l’utilise pour établir une liaison avec une instance de service](how-clients-find-and-use-a-service-connection-point.md)
-   [Utilisation des API RpcNs (RPC Name Service) pour publier un service RPC](publishing-with-the-rpc-name-service-rpcns.md)
-   [Windows inscription et résolution des sockets (RnR) pour publier un service Windows sockets](publishing-with-windows-sockets-registration-and-resolution.md)
-   [Publication de services COM dans le magasin de classes COM+](publishing-com-services.md)

Pour plus d’informations sur la façon dont les services et les clients s’authentifient mutuellement, consultez [authentification mutuelle à l’aide de Kerberos](mutual-authentication-using-kerberos.md). Pour plus d’informations sur les contextes de sécurité de service et les comptes d’ouverture de session, consultez [comptes d’ouverture de session de service](service-logon-accounts.md).

 

 




