---
title: Écriture d’un client ou d’un serveur RPC sécurisé
description: Cette section présente les meilleures pratiques recommandées pour l’écriture d’un client ou d’un serveur RPC sécurisé.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Appel de procédure distante RPC, meilleures pratiques, écriture d’un client ou d’un serveur sécurisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031603"
---
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="69d2c-104">Écriture d’un client ou d’un serveur RPC sécurisé</span><span class="sxs-lookup"><span data-stu-id="69d2c-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="69d2c-105">Cette section présente les meilleures pratiques recommandées pour l’écriture d’un client ou d’un serveur RPC sécurisé.</span><span class="sxs-lookup"><span data-stu-id="69d2c-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="69d2c-106">Les informations contenues dans cette section s’appliquent à Windows 2000 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="69d2c-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="69d2c-107">Cette section s’applique à toutes les séquences de protocole, y compris [**Ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="69d2c-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="69d2c-108">Les développeurs ont tendance à penser que **Ncalrpc** n’est pas une cible probable pour une attaque, ce qui n’est pas le cas sur un serveur Terminal Server où des centaines d’utilisateurs peuvent accéder à un service, et compromettre ou même arrêter un service peut aboutir à l’obtention d’un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="69d2c-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="69d2c-109">Cette section est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="69d2c-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="69d2c-110">Le fournisseur de sécurité à utiliser</span><span class="sxs-lookup"><span data-stu-id="69d2c-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="69d2c-111">Contrôle de l’authentification du client</span><span class="sxs-lookup"><span data-stu-id="69d2c-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="69d2c-112">Choix d’un niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="69d2c-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="69d2c-113">Choix des options de QOS de sécurité</span><span class="sxs-lookup"><span data-stu-id="69d2c-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="69d2c-114">Erreur courante : en supposant que RpcServerRegisterAuthInfo empêche les utilisateurs non autorisés d’appeler votre serveur</span><span class="sxs-lookup"><span data-stu-id="69d2c-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="69d2c-115">Rappels</span><span class="sxs-lookup"><span data-stu-id="69d2c-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="69d2c-116">Sessions null</span><span class="sxs-lookup"><span data-stu-id="69d2c-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="69d2c-117">Utiliser l’indicateur/Robust</span><span class="sxs-lookup"><span data-stu-id="69d2c-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="69d2c-118">Techniques IDL pour une meilleure conception d’interface et de méthode</span><span class="sxs-lookup"><span data-stu-id="69d2c-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="69d2c-119">Handles de contexte strict et strict</span><span class="sxs-lookup"><span data-stu-id="69d2c-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="69d2c-120">Ne pas faire confiance à votre homologue</span><span class="sxs-lookup"><span data-stu-id="69d2c-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="69d2c-121">Ne pas utiliser la sécurité du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="69d2c-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="69d2c-122">Méfiez-vous des autres points de terminaison RPC s’exécutant dans le même processus</span><span class="sxs-lookup"><span data-stu-id="69d2c-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="69d2c-123">Vérifier que le serveur est bien celui qu’il prétend être</span><span class="sxs-lookup"><span data-stu-id="69d2c-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="69d2c-124">Utiliser des séquences de protocole courantes</span><span class="sxs-lookup"><span data-stu-id="69d2c-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="69d2c-125">Quelle est la sécurité de mon serveur RPC maintenant ?</span><span class="sxs-lookup"><span data-stu-id="69d2c-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 