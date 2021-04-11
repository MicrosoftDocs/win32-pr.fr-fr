---
description: Les rappels des composants hébergés sont ceux qui rendent l’hébergement possible. Toutefois, il est possible que le composant que vous hébergez ait activé un autre contexte d’activation qu’il utilise pour accéder à ses propres plug-ins ou composants.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Utilisation de rappels à partir de composants hébergés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112698"
---
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="40ca9-104">Utilisation de rappels à partir de composants hébergés</span><span class="sxs-lookup"><span data-stu-id="40ca9-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="40ca9-105">Les rappels des composants hébergés sont ceux qui rendent l’hébergement possible.</span><span class="sxs-lookup"><span data-stu-id="40ca9-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="40ca9-106">Toutefois, il est possible que le composant que vous hébergez ait activé un autre contexte d’activation qu’il utilise pour accéder à ses propres plug-ins ou composants.</span><span class="sxs-lookup"><span data-stu-id="40ca9-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="40ca9-107">Dans ce cas, si le composant hébergé laisse un contexte d’activation sur la pile qui fait référence à son propre objet COM, l’application d’hébergement peut appeler [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet qu’il s’attend à avoir sa propre implémentation et à la place recevoir l’objet du composant hébergé.</span><span class="sxs-lookup"><span data-stu-id="40ca9-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="40ca9-108">Pour éviter cet héritage des contextes d’activation, une bonne application d’hébergement doit activer d’abord son propre contexte d’activation connu pendant un rappel.</span><span class="sxs-lookup"><span data-stu-id="40ca9-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="40ca9-109">Prenons l’exemple suivant qui protège le code de l’application d’hébergement :</span><span class="sxs-lookup"><span data-stu-id="40ca9-109">Consider the following example that protects the hosting application's code:</span></span>

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

<span data-ttu-id="40ca9-110">Cela garantit qu’un contexte d’activation correct est défini avant de passer la requête sur une implémentation interne de **FUNCT**.</span><span class="sxs-lookup"><span data-stu-id="40ca9-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="40ca9-111">Votre propre implémentation peut avoir l’implémentation Inline réelle, mais la méthode précédente garantit une plus grande interopérabilité en créant simplement des wrappers délégués.</span><span class="sxs-lookup"><span data-stu-id="40ca9-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="40ca9-112">Il est recommandé d’utiliser une méthode similaire lors de l’exposition de rappels normaux (non-COM).</span><span class="sxs-lookup"><span data-stu-id="40ca9-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
