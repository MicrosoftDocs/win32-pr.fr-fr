---
description: Les rappels des composants hébergés sont ceux qui rendent l’hébergement possible. Toutefois, il est possible que le composant que vous hébergez ait activé un autre contexte d’activation qu’il utilise pour accéder à ses propres plug-ins ou composants.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Utilisation de rappels à partir de composants hébergés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb13e61b83ba52f0f8dd5265b11585e8366c0e8558d45c5738f179d43df2eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884599"
---
# <a name="using-callbacks-from-hosted-components"></a>Utilisation de rappels à partir de composants hébergés

Les rappels des composants hébergés sont ceux qui rendent l’hébergement possible. Toutefois, il est possible que le composant que vous hébergez ait activé un autre contexte d’activation qu’il utilise pour accéder à ses propres plug-ins ou composants. Dans ce cas, si le composant hébergé laisse un contexte d’activation sur la pile qui fait référence à son propre objet COM, l’application d’hébergement peut appeler [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet qu’il s’attend à avoir sa propre implémentation et à la place recevoir l’objet du composant hébergé. Pour éviter cet héritage des contextes d’activation, une bonne application d’hébergement doit activer d’abord son propre contexte d’activation connu pendant un rappel.

Prenons l’exemple suivant qui protège le code de l’application d’hébergement :

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

Cela garantit qu’un contexte d’activation correct est défini avant de passer la requête sur une implémentation interne de **FUNCT**. Votre propre implémentation peut avoir l’implémentation Inline réelle, mais la méthode précédente garantit une plus grande interopérabilité en créant simplement des wrappers délégués. Il est recommandé d’utiliser une méthode similaire lors de l’exposition de rappels normaux (non-COM).

 

 
