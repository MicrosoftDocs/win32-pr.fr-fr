---
description: Il existe deux ingrédients pour déterminer le comportement d’emprunt d’identité de l’autorité que le client accorde explicitement au serveur via un niveau d’emprunt d’identité et la capacité des serveurs à masquer sa propre identité lors des appels au nom des clients.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Masquage (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748084"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="c07ee-103">Masquage (services de composants)</span><span class="sxs-lookup"><span data-stu-id="c07ee-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="c07ee-104">Il existe deux ingrédients pour déterminer le comportement de l’emprunt d’identité : l’autorité que le client accorde explicitement au serveur via un niveau d’emprunt d’identité et la capacité du serveur à masquer sa propre identité lors des appels au nom du client.</span><span class="sxs-lookup"><span data-stu-id="c07ee-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="c07ee-105">Cette dernière fonctionnalité est connue sous le nom de *masquage*.</span><span class="sxs-lookup"><span data-stu-id="c07ee-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="c07ee-106">Le masquage porte sur l’identité de sécurité sous laquelle le serveur effectue des appels.</span><span class="sxs-lookup"><span data-stu-id="c07ee-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="c07ee-107">Lorsque le serveur emprunte l’identité du client, il dispose d’un accès direct aux informations d’identification de sécurité du client.</span><span class="sxs-lookup"><span data-stu-id="c07ee-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="c07ee-108">Dans un sens très local, le thread serveur prend l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="c07ee-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="c07ee-109">Toutefois, lorsque le serveur effectue des appels en dehors de son processus, l’identité du client ne sera pas nécessairement projetée en tant qu’identité sous laquelle l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="c07ee-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="c07ee-110">Lorsque le masquage est activé, les appels effectués par le serveur qui emprunte l’identité du client peuvent être effectués sous l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="c07ee-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="c07ee-111">Lorsque le masquage est désactivé, les appels par le serveur sont effectués sous l’identité du serveur.</span><span class="sxs-lookup"><span data-stu-id="c07ee-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="c07ee-112">En outre, il existe deux formes de masquage, le masquage *statique* et le *masquage dynamique*, qui peuvent être décrits comme suit :</span><span class="sxs-lookup"><span data-stu-id="c07ee-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="c07ee-113">Emprunt d’identité avec masquage statique.</span><span class="sxs-lookup"><span data-stu-id="c07ee-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="c07ee-114">L’identité du client d’origine (réalisée en tant que jeton de thread du serveur) peut être présentée une seule fois à un serveur en aval sur un appel à l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), en définissant l’identité du client d’origine une seule fois sur le proxy, et ce jeton de thread sera utilisé lors des appels de méthode suivants.</span><span class="sxs-lookup"><span data-stu-id="c07ee-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="c07ee-115">Emprunt d’identité avec masquage dynamique.</span><span class="sxs-lookup"><span data-stu-id="c07ee-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="c07ee-116">L’identité du client d’origine est découverte en tant que jeton de thread du serveur sur chaque appel de méthode au serveur en aval.</span><span class="sxs-lookup"><span data-stu-id="c07ee-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="c07ee-117">En effet, l’identité présentée peut être déterminée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="c07ee-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="c07ee-118">La surcharge requise pour effectuer cette opération peut être considérablement plus coûteuse.</span><span class="sxs-lookup"><span data-stu-id="c07ee-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="c07ee-119">Pour les applications COM+, la configuration par défaut est pour la fonctionnalité de voilage dynamique.</span><span class="sxs-lookup"><span data-stu-id="c07ee-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="c07ee-120">Cela peut être modifié par programme et administrativement.</span><span class="sxs-lookup"><span data-stu-id="c07ee-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="c07ee-121">Bien que le masquage dynamique puisse avoir une surcharge des performances, il offre la flexibilité qui est généralement requise dans les circonstances qui nécessitent l’utilisation de l’emprunt d’identité en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="c07ee-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="c07ee-122">Pour plus d’informations sur le masquage et les descriptions précises des comportements possibles, consultez [masquage](/windows/desktop/com/cloaking) dans la documentation com.</span><span class="sxs-lookup"><span data-stu-id="c07ee-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c07ee-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c07ee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c07ee-124">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="c07ee-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="c07ee-125">Exigences côté client pour l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="c07ee-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="c07ee-126">Exigences côté serveur pour l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="c07ee-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
