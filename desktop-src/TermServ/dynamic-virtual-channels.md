---
title: Canaux virtuels dynamiques
description: Les API de canal virtuel dynamique (DVC) étendent les API de canal virtuel existantes pour Services Bureau à distance, appelées API de canal virtuel statique (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379897"
---
# <a name="dynamic-virtual-channels"></a>Canaux virtuels dynamiques

Les API de canal virtuel dynamique (DVC) étendent les API de canal virtuel existantes pour Services Bureau à distance, appelées API de canal virtuel statique (SVC). Les API DVC répondent à plusieurs limitations qui existaient dans les API SVC entre le client et le serveur, par exemple :

-   Un nombre limité de canaux
-   Reconstruction des paquets

Les API DVC vous aident à implémenter des modules côté serveur et client d’une connexion Services Bureau à distance qui communiquent entre eux.

À l’instar de nombreuses autres architectures client/serveur, une connexion est établie sur la base d’un élément de données communément convenu sous le terme de point de terminaison. Un exemple similaire est le protocole TCP/IP, où un point de terminaison est établi via une combinaison d’adresse IP de serveur et de nom de port. Un autre exemple est canaux nommés, où un point de terminaison est une combinaison du nom du serveur et du nom du canal. Dans une connexion Services Bureau à distance, il n’y a que deux parties impliquées. Par conséquent, le point de terminaison se compose d’une simple chaîne arbitraire qui identifie de façon unique la connexion. À l’instar de TCP/IP et des canaux nommés, plusieurs connexions peuvent démarrer à partir du même nom de point de terminaison. Dans ce sens, les connexions n’ont pas de noms ; simplement un écouteur qui attend les demandes entrantes sur le point de terminaison.

Les API DVC se composent des éléments suivants :

-   API client

    Ces API sont disponibles dans le client Connexion Bureau à distance (RDC) sous la forme d’un plug-in. Le côté client est en mode passif, où il écoute les connexions entrantes, mais n’établit pas de connexion activement.

-   API serveur

    Ces API initialisent activement la connexion.

Pour plus d’informations sur l’écriture d’un module de canal virtuel dynamique (DVC), consultez détails de l' [implémentation DVC](dvc-implementation-details.md).

 

 




