---
title: Utilisation de RPC asynchrone avec les canaux DCE
description: Microsoft RPC prend en charge l’utilisation de canaux DCE. Bien qu’ils partagent un nom similaire, les canaux DCE ne sont pas liés aux canaux nommés. Les canaux nommés sont un protocole de transport. Les canaux DCE sont une méthode indépendante du protocole de communication client/serveur.
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029164"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="c8150-106">Utilisation de RPC asynchrone avec les canaux DCE</span><span class="sxs-lookup"><span data-stu-id="c8150-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="c8150-107">Microsoft RPC prend en charge l’utilisation de canaux DCE.</span><span class="sxs-lookup"><span data-stu-id="c8150-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="c8150-108">Bien qu’ils partagent un nom similaire, les canaux DCE ne sont pas liés aux [canaux nommés](asynchronous-rpc-over-the-named-pipe-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="c8150-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="c8150-109">Les canaux nommés sont un protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="c8150-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="c8150-110">Les canaux DCE sont une méthode indépendante du protocole de communication client/serveur.</span><span class="sxs-lookup"><span data-stu-id="c8150-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="c8150-111">Cette section présente une discussion de RPC à l’aide de canaux DCE asynchrones.</span><span class="sxs-lookup"><span data-stu-id="c8150-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="c8150-112">Elle est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8150-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="c8150-113">Canaux asynchrones</span><span class="sxs-lookup"><span data-stu-id="c8150-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="c8150-114">Déclaration de canaux asynchrones</span><span class="sxs-lookup"><span data-stu-id="c8150-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="c8150-115">Gestion de canal asynchrone côté client</span><span class="sxs-lookup"><span data-stu-id="c8150-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="c8150-116">Gestion de canal asynchrone côté serveur</span><span class="sxs-lookup"><span data-stu-id="c8150-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="c8150-117">Pour obtenir un exemple d’application RPC de canal asynchrone, consultez l’exemple FileRep dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="c8150-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




