---
title: Utilisation de Transport-Level sécurité sur le client
description: Le client spécifie comment le serveur emprunte l’identité du client lorsque le client établit la liaison de chaîne.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Appel de procédure distante RPC, tâches, à l’aide de la sécurité au niveau du transport sur le client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941287"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="49d9e-104">Utilisation de Transport-Level sécurité sur le client</span><span class="sxs-lookup"><span data-stu-id="49d9e-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="49d9e-105">Le client spécifie comment le serveur emprunte l’identité du client lorsque le client établit la liaison de chaîne.</span><span class="sxs-lookup"><span data-stu-id="49d9e-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="49d9e-106">Ces informations de QOS sont fournies en tant qu’option de point de terminaison dans la liaison de chaîne.</span><span class="sxs-lookup"><span data-stu-id="49d9e-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="49d9e-107">Le client peut spécifier le niveau d’emprunt d’identité, le suivi dynamique ou statique et l’indicateur d’efficacité uniquement.</span><span class="sxs-lookup"><span data-stu-id="49d9e-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="49d9e-108">**Pour fournir des informations de qualité de service pour le serveur**</span><span class="sxs-lookup"><span data-stu-id="49d9e-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="49d9e-109">Le client appelle [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) pour créer les chaînes du composant, y compris les options de point de terminaison, dans le contexte de liaison de chaîne correct.</span><span class="sxs-lookup"><span data-stu-id="49d9e-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="49d9e-110">Le client appelle [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour obtenir un nouveau handle de liaison et appliquer les informations de qualité de service pour le client.</span><span class="sxs-lookup"><span data-stu-id="49d9e-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="49d9e-111">Le client effectue des appels de procédure distante à l’aide du descripteur.</span><span class="sxs-lookup"><span data-stu-id="49d9e-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="49d9e-112">Microsoft RPC prend en charge les fonctionnalités de sécurité Windows uniquement sur [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) et [**Ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="49d9e-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="49d9e-113">Les options de sécurité pour les autres transports sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="49d9e-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="49d9e-114">Le client peut associer les paramètres de sécurité suivants à la liaison pour le transport de canal nommé [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) ou [**Ncalrpc**](/windows/desktop/Midl/ncalrpc):</span><span class="sxs-lookup"><span data-stu-id="49d9e-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="49d9e-115">Identification, emprunt d’identité ou anonyme.</span><span class="sxs-lookup"><span data-stu-id="49d9e-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="49d9e-116">Spécifie le type de sécurité utilisé.</span><span class="sxs-lookup"><span data-stu-id="49d9e-116">Specifies the type of security used.</span></span> <span data-ttu-id="49d9e-117">La valeur par défaut est emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="49d9e-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="49d9e-118">Dynamique ou statique.</span><span class="sxs-lookup"><span data-stu-id="49d9e-118">Dynamic or Static.</span></span> <span data-ttu-id="49d9e-119">Détermine si les informations de sécurité associées à un thread sont une copie des informations de sécurité créées au moment où l’appel de procédure distante est effectué (statique) ou un pointeur vers les informations de sécurité (dynamique).</span><span class="sxs-lookup"><span data-stu-id="49d9e-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="49d9e-120">Les informations de sécurité statiques ne changent pas.</span><span class="sxs-lookup"><span data-stu-id="49d9e-120">Static security information does not change.</span></span> <span data-ttu-id="49d9e-121">Le paramètre dynamique reflète les paramètres de sécurité actuels, y compris les modifications apportées après l’appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="49d9e-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="49d9e-122">Pour [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), la valeur par défaut pour les connexions de canaux nommés distants est statique, pour les connexions de canaux nommés locales, la valeur par défaut est dynamique.</span><span class="sxs-lookup"><span data-stu-id="49d9e-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="49d9e-123">**True** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="49d9e-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="49d9e-124">Spécifie la valeur de l’indicateur d’efficacité uniquement.</span><span class="sxs-lookup"><span data-stu-id="49d9e-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="49d9e-125">La valeur **true** indique que seuls les privilèges de jeton activés au moment de l’appel sont effectifs.</span><span class="sxs-lookup"><span data-stu-id="49d9e-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="49d9e-126">La valeur **false** indique que tous les privilèges sont disponibles et que l’application peut les modifier.</span><span class="sxs-lookup"><span data-stu-id="49d9e-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="49d9e-127">Une combinaison de ces paramètres peut être assignée à la liaison, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="49d9e-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="49d9e-128">Les paramètres de sécurité par défaut varient en fonction du protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="49d9e-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="49d9e-129">Pour plus d’informations sur la syntaxe des options de point de terminaison, consultez [point de terminaison](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="49d9e-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 