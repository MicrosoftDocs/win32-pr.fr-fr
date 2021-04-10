---
title: RPC et le réseau
description: Cette section explique comment gérer la non-fiabilité du réseau lors de l’utilisation d’un appel de procédure distante, et explique comment les API de niveau RPC traduisent en activité réseau. La section fait référence uniquement aux \_ \_ séquences de protocole http ncacn IP TCP et ncacn \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Appel de procédure distante RPC, meilleures pratiques, RPC et le réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102096"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="b6b88-105">RPC et le réseau</span><span class="sxs-lookup"><span data-stu-id="b6b88-105">RPC and the Network</span></span>

<span data-ttu-id="b6b88-106">Cette section explique comment gérer la non-fiabilité du réseau lors de l’utilisation d’un appel de procédure distante, et explique comment les API de niveau RPC traduisent en activité réseau.</span><span class="sxs-lookup"><span data-stu-id="b6b88-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="b6b88-107">La section fait référence uniquement aux séquences de protocole [**\_ http**](/windows/desktop/Midl/ncacn-http) [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) et ncacn.</span><span class="sxs-lookup"><span data-stu-id="b6b88-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="b6b88-108">Cette section est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6b88-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="b6b88-109">Développement et déploiement sur le réseau</span><span class="sxs-lookup"><span data-stu-id="b6b88-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="b6b88-110">Prévention des blocages de Client-Side</span><span class="sxs-lookup"><span data-stu-id="b6b88-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="b6b88-111">Gestion des groupes de connexions réseau (associations)</span><span class="sxs-lookup"><span data-stu-id="b6b88-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="b6b88-112">Nettoyage des connexions inactives</span><span class="sxs-lookup"><span data-stu-id="b6b88-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="b6b88-113">Gestion de la perte de connectivité</span><span class="sxs-lookup"><span data-stu-id="b6b88-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="b6b88-114">Nettoyage côté serveur</span><span class="sxs-lookup"><span data-stu-id="b6b88-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 