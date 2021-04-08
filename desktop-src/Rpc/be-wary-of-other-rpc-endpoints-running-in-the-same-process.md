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
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a><span data-ttu-id="0df22-103">Méfiez-vous des autres points de terminaison RPC s’exécutant dans le même processus</span><span class="sxs-lookup"><span data-stu-id="0df22-103">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>

<span data-ttu-id="0df22-104">Lorsqu’une application réside dans un processus avec d’autres serveurs RPC, toutes les applications écoutent tous les protocoles.</span><span class="sxs-lookup"><span data-stu-id="0df22-104">When an application resides in a process with other RPC servers, all applications listen on all protocols.</span></span> <span data-ttu-id="0df22-105">Par conséquent, si un composant appelle [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* uniquement pour les appels LRPC, il n’est pas nécessairement accessible sur les appels LRPC uniquement.</span><span class="sxs-lookup"><span data-stu-id="0df22-105">As such, if a component calls [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* for LRPC only, it is not necessarily accessible over LRPC only.</span></span> <span data-ttu-id="0df22-106">Il peut être accessible par d’autres protocoles, car d’autres serveurs RPC du processus peuvent être à l’écoute sur des canaux ou des sockets (par exemple).</span><span class="sxs-lookup"><span data-stu-id="0df22-106">It may be accessible over other protocols, since other RPC servers in the process may be listening on pipes or sockets (for example).</span></span>

<span data-ttu-id="0df22-107">Comme pour les handles de contexte stricts, le fait de ne pas placer un autre point de terminaison dans le processus ne signifie pas qu’un autre point de terminaison n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0df22-107">Similar to strict context handles, not putting another endpoint in the process does not mean another endpoint does not exist.</span></span> <span data-ttu-id="0df22-108">Quelle que soit la façon dont vous inscrivez votre serveur, il n’existe aucune association spéciale entre votre interface et votre point de terminaison. toutes les interfaces peuvent être appelées sur tous les points de terminaison de ce processus.</span><span class="sxs-lookup"><span data-stu-id="0df22-108">Regardless of how you register your server, there is no special association between your interface and your endpoint; all interfaces are callable on all endpoints in that process.</span></span> <span data-ttu-id="0df22-109">C’est une autre raison pour laquelle le modèle de sécurité du point de terminaison est inefficace ; Si un descripteur de sécurité est placé sur un point de terminaison, les attaquants peuvent appeler l’interface sur un autre point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0df22-109">This is another reason why the endpoint security model is ineffective; if a security descriptor is placed on an endpoint, attackers can call the interface on another endpoint.</span></span>

<span data-ttu-id="0df22-110">Pour garantir qu’un processus est appelé uniquement sur une séquence de protocole spécifique, enregistrez une fonction de rappel de sécurité et, dans cette fonction, vérifiez quelle séquence de protocole l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="0df22-110">To ensure a process be called only on a specific protocol sequence, register a security callback function, and in that function, check on which protocol sequence the call is made.</span></span>

 

 




