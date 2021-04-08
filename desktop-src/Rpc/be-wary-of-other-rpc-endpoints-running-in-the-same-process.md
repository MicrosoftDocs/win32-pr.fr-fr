---
title: Méfiez-vous des autres points de terminaison RPC s’exécutant dans le même processus
description: Lorsqu’une application réside dans un processus avec d’autres serveurs RPC, toutes les applications écoutent tous les protocoles.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673914"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Méfiez-vous des autres points de terminaison RPC s’exécutant dans le même processus

Lorsqu’une application réside dans un processus avec d’autres serveurs RPC, toutes les applications écoutent tous les protocoles. Par conséquent, si un composant appelle [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* uniquement pour les appels LRPC, il n’est pas nécessairement accessible sur les appels LRPC uniquement. Il peut être accessible par d’autres protocoles, car d’autres serveurs RPC du processus peuvent être à l’écoute sur des canaux ou des sockets (par exemple).

Comme pour les handles de contexte stricts, le fait de ne pas placer un autre point de terminaison dans le processus ne signifie pas qu’un autre point de terminaison n’existe pas. Quelle que soit la façon dont vous inscrivez votre serveur, il n’existe aucune association spéciale entre votre interface et votre point de terminaison. toutes les interfaces peuvent être appelées sur tous les points de terminaison de ce processus. C’est une autre raison pour laquelle le modèle de sécurité du point de terminaison est inefficace ; Si un descripteur de sécurité est placé sur un point de terminaison, les attaquants peuvent appeler l’interface sur un autre point de terminaison.

Pour garantir qu’un processus est appelé uniquement sur une séquence de protocole spécifique, enregistrez une fonction de rappel de sécurité et, dans cette fonction, vérifiez quelle séquence de protocole l’appel est effectué.

 

 




