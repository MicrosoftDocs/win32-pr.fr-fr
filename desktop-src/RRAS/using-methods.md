---
title: Utilisation de méthodes
description: Lorsqu’un client s’inscrit auprès du gestionnaire de tables de routage, il peut exporter un ensemble de méthodes. Ces méthodes sont utilisées par d’autres clients pour obtenir des informations spécifiques au client. Les méthodes permettent une communication privée entre les clients du gestionnaire de tables de routage.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940045"
---
# <a name="using-methods"></a>Utilisation de méthodes

Lorsqu’un client s’inscrit auprès du gestionnaire de tables de routage, il peut exporter un ensemble de méthodes. Ces méthodes sont utilisées par d’autres clients pour obtenir des informations spécifiques au client. Les méthodes permettent une communication privée entre les clients du gestionnaire de tables de routage.

Un client peut obtenir la liste des méthodes exportées par un autre client. Le client appelle la fonction [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , en fournissant le handle du client cible.

Chaque méthode exportée par un client est identifiée de manière unique par son identificateur de méthode. Chaque client peut exporter jusqu’à 32 méthodes. Chaque méthode correspond à un bit défini dans le membre **methodType** de la structure de la méthode d' [**exportation d' \_ entité \_ \_ RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) . Pour appeler plusieurs méthodes, le client doit exécuter un ou logique des identificateurs pour ces méthodes. La syntaxe et la sémantique des structures d’entrée et de sortie pour chaque protocole doivent être spécifiées lors de l’implémentation du protocole.

> [!Note]  
> Les valeurs d’identificateur de méthode qui correspondent à un bit défini dans la moitié inférieure du membre **methodType** (les 16 bits inférieurs) sont réservées par Microsoft.

 

Pour appeler la méthode d’un second client, un client appelle la fonction [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) . Le gestionnaire de table de routage arbitre toutes les demandes pour appeler les méthodes d’un client. Le gestionnaire de tables de routage effectue deux fonctions lorsqu’il arbitre entre les clients :

-   Empêcher le second client d’appeler une méthode pour un client qui annule l’inscription.
-   Maintien d’une demande d’appel lorsque les méthodes sont bloquées et autoriser la poursuite de la demande lorsque les méthodes sont débloquées.

Si un client doit empêcher d’autres clients d’exécuter ses méthodes, le client peut appeler [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods). Le gestionnaire de table de routage n’autorise pas le traitement d’un appel à [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) tant que le client n’a pas débloqué ses méthodes.

En général, les clients bloquent les méthodes lors de l’apport de modifications aux données privées échangées entre les clients. Les méthodes de blocage sont une action facultative. Un client peut également utiliser des verrous internes pour empêcher d’autres clients d’appeler des méthodes.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [obtenir et appeler les méthodes exportées pour un client](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




