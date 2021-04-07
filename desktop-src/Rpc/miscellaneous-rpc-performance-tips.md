---
title: Conseils sur les performances des appels RPC divers
description: Cette section décrit divers conseils relatifs aux performances pour le développement de serveurs RPC haute performance. Cette section fournit de nombreux conseils qui font référence au client RPC. Le développement d’un client RPC permet au serveur RPC d’effectuer moins de travail.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028843"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="eb8da-105">Conseils sur les performances des appels RPC divers</span><span class="sxs-lookup"><span data-stu-id="eb8da-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="eb8da-106">Cette section décrit divers conseils relatifs aux performances pour le développement de serveurs RPC haute performance.</span><span class="sxs-lookup"><span data-stu-id="eb8da-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="eb8da-107">Cette section fournit de nombreux conseils qui font référence au client RPC.</span><span class="sxs-lookup"><span data-stu-id="eb8da-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="eb8da-108">Le développement d’un client RPC permet au serveur RPC d’effectuer moins de travail.</span><span class="sxs-lookup"><span data-stu-id="eb8da-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="eb8da-109">Utiliser Kerberos</span><span class="sxs-lookup"><span data-stu-id="eb8da-109">Use Kerberos</span></span>

<span data-ttu-id="eb8da-110">Si la sécurité est utilisée, utilisez Kerberos.</span><span class="sxs-lookup"><span data-stu-id="eb8da-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="eb8da-111">Côté serveur, Kerberos n’a pas besoin d’accéder au KDC.</span><span class="sxs-lookup"><span data-stu-id="eb8da-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="eb8da-112">Cela déplace la charge de travail du serveur vers le client, ce qui permet d’obtenir des serveurs plus performants.</span><span class="sxs-lookup"><span data-stu-id="eb8da-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="eb8da-113">Utiliser le suivi des identités statiques</span><span class="sxs-lookup"><span data-stu-id="eb8da-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="eb8da-114">Si la sécurité est utilisée, essayez d’utiliser le suivi d’identité statique.</span><span class="sxs-lookup"><span data-stu-id="eb8da-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="eb8da-115">Le suivi des identités statiques est moins onéreux en termes d’utilisation des ressources que le suivi dynamique des identités.</span><span class="sxs-lookup"><span data-stu-id="eb8da-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="eb8da-116">Si l’identité du client change et que le serveur ne doit pas être conscient de la modification, utilisez le suivi dynamique au lieu de créer un handle de liaison différent pour chaque identité.</span><span class="sxs-lookup"><span data-stu-id="eb8da-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="eb8da-117">Toutefois, si l’identité est la même, assurez-vous que RPC est conscient de ce fait pour éviter que RPC vérifie l’identité modifiée à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="eb8da-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="eb8da-118">Utiliser la fonction RpcGetAuthorizationContextForClient</span><span class="sxs-lookup"><span data-stu-id="eb8da-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="eb8da-119">Si vous devez vérifier l’accès dans Windows XP, utilisez la fonction [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="eb8da-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="eb8da-120">Les contextes d’autorisation qui en résultent permettent des contrôles d’accès très rapides, qui sont mis en cache efficacement par le runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="eb8da-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="eb8da-121">Ne modifiez pas le jeton, sauf si nécessaire</span><span class="sxs-lookup"><span data-stu-id="eb8da-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="eb8da-122">Si le suivi dynamique des identités est utilisé, ne modifiez pas le jeton de thread/processus, sauf si cela est absolument nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eb8da-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="eb8da-123">Même s’il est modifié en paramètres précédemment, le jeton est souvent suffisamment différent du système de sécurité pour déclencher l’établissement d’un nouveau contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="eb8da-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="eb8da-124">Prendre en compte la sérialisation en mode mixte pour les handles de contexte</span><span class="sxs-lookup"><span data-stu-id="eb8da-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="eb8da-125">Le mode de sérialisation par défaut pour le handle de contexte est sérialisé (exclusif).</span><span class="sxs-lookup"><span data-stu-id="eb8da-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="eb8da-126">Envisagez d’effectuer tous les appels qui ne modifient pas l’état du handle de contexte en mode de sérialisation partagé.</span><span class="sxs-lookup"><span data-stu-id="eb8da-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="eb8da-127">Pour plus d’informations, consultez [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .</span><span class="sxs-lookup"><span data-stu-id="eb8da-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




