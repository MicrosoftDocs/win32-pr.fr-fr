---
title: RPC asynchrone sur le protocole Named-Pipe
description: Si vous utilisez des canaux nommés (ncacn \_ NP) comme protocole de transport, vous devez éviter d’autoriser un grand nombre d’appels en attente d’inactivité sur le serveur.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941289"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="a1a24-103">RPC asynchrone sur le protocole Named-Pipe</span><span class="sxs-lookup"><span data-stu-id="a1a24-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="a1a24-104">Si vous utilisez des canaux nommés ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) comme protocole de transport, vous devez éviter d’autoriser un grand nombre d’appels en attente d’inactivité sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a1a24-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="a1a24-105">Avec les canaux nommés, chaque client qui attend une réponse aura un canal nommé en attente de lecture sur le serveur, chacun d’entre eux nécessitant une certaine quantité de mémoire du noyau.</span><span class="sxs-lookup"><span data-stu-id="a1a24-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="a1a24-106">Par exemple, vous ne souhaitez pas utiliser un appel de notification pour le nouveau courrier électronique avec le transport de canal nommé, car ce type d’appel reste en attente même lorsque les clients sont inactifs et que la mémoire du noyau peut être épuisée.</span><span class="sxs-lookup"><span data-stu-id="a1a24-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="a1a24-107">Notez qu’il ne s’agit pas d’un problème avec les autres protocoles orientés connexion, tels que [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).</span><span class="sxs-lookup"><span data-stu-id="a1a24-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="a1a24-108">Étant donné que les canaux nommés sont un protocole de transport, votre application peut les utiliser en spécifiant [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) comme protocole dans une liaison de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a1a24-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="a1a24-109">Pour plus d’informations sur les canaux nommés, consultez [canaux nommés](/windows/desktop/ipc/named-pipes).</span><span class="sxs-lookup"><span data-stu-id="a1a24-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="a1a24-110">Pour plus d’informations sur la création de liaisons de chaînes, consultez [utilisation des liaisons de chaînes](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="a1a24-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 