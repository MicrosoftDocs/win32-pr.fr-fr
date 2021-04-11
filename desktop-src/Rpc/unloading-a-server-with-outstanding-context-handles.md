---
title: Déchargement d’un serveur avec des handles de contexte en attente
description: Traditionnellement, le déchargement d’une DLL qui traite les appels RPC à l’aide de handles de contexte, sans arrêter au préalable le processus d’hébergement, a été problématique.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197295"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="47c2d-103">Déchargement d’un serveur avec des handles de contexte en attente</span><span class="sxs-lookup"><span data-stu-id="47c2d-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="47c2d-104">Traditionnellement, le déchargement d’une DLL qui traite les appels RPC à l’aide de handles de contexte, sans arrêter au préalable le processus d’hébergement, a été problématique.</span><span class="sxs-lookup"><span data-stu-id="47c2d-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="47c2d-105">Cela est dû au fait que la routine d’exécution n’est plus valide lorsque la DLL est déchargée.</span><span class="sxs-lookup"><span data-stu-id="47c2d-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="47c2d-106">Lorsqu’un client avec un handle de contexte précédemment ouvert échoue et que l’exécution de l’appel de procédure distante tente de fermer le descripteur de contexte, sa tentative d’appeler l’accès à la routine d’exécution ne respecte pas et le serveur tombe en panne.</span><span class="sxs-lookup"><span data-stu-id="47c2d-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="47c2d-107">À partir de Windows XP, une nouvelle API appelée [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="47c2d-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="47c2d-108">**RpcServerUnregisterIfEx** ferme les descripteurs de contexte ouverts par l’interface en cours d’annulation d’inscription ; la fonction [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="47c2d-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="47c2d-109">L’utilisation de **RpcServerUnregisterIfEx** n’est pas nécessaire lorsque l’ensemble du processus s’arrête, mais il est nécessaire si une ou plusieurs dll hébergeant les routines d’exécution sont déchargées alors que des handles de contexte en attente existent.</span><span class="sxs-lookup"><span data-stu-id="47c2d-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




