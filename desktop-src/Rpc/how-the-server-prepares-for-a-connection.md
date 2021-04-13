---
title: Préparation d’une connexion par le serveur
description: Quand un programme serveur commence à s’exécuter, il doit d’abord inscrire l’interface ou les interfaces qu’il contient avec la bibliothèque Runtime RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310353"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="21235-103">Préparation d’une connexion par le serveur</span><span class="sxs-lookup"><span data-stu-id="21235-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="21235-104">Quand un programme serveur commence à s’exécuter, il doit d’abord inscrire l’interface ou les interfaces qu’il contient avec la bibliothèque Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="21235-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="21235-105">Il crée ensuite les informations de liaison nécessaires.</span><span class="sxs-lookup"><span data-stu-id="21235-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="21235-106">Le programme serveur doit également inscrire le ou les points de terminaison qu’il écoute.</span><span class="sxs-lookup"><span data-stu-id="21235-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="21235-107">Il peut ensuite commencer à écouter les appels des clients.</span><span class="sxs-lookup"><span data-stu-id="21235-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="21235-108">Ce processus est illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="21235-108">This process is illustrated in the following diagram.</span></span>

![une application serveur RPC se prépare aux connexions clientes](images/srvrcon.png)

<span data-ttu-id="21235-110">Selon la conception choisie, une application serveur peut choisir un autre ensemble d’étapes. l’exemple précédent et l’illustration ci-dessus fournissent une approche.</span><span class="sxs-lookup"><span data-stu-id="21235-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="21235-111">Cette section fournit des informations sur les étapes qu’un processus serveur doit effectuer pour préparer une connexion.</span><span class="sxs-lookup"><span data-stu-id="21235-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="21235-112">La discussion comprend les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="21235-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="21235-113">Inscription de l’interface</span><span class="sxs-lookup"><span data-stu-id="21235-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="21235-114">Mise à disposition du serveur sur le réseau</span><span class="sxs-lookup"><span data-stu-id="21235-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="21235-115">Inscription des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="21235-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="21235-116">Écoute des appels clients</span><span class="sxs-lookup"><span data-stu-id="21235-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




