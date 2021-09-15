---
description: Les composants bien créés ne perturbent pas l’environnement de l’application d’hébergement et ne perdent pas de contextes d’activation.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolation des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237948"
---
# <a name="isolating-components"></a>Isolation des composants

Les composants bien créés ne perturbent pas l’environnement de l’application d’hébergement et ne perdent pas de contextes d’activation. Les composants bien créés effectuent leur propre gestion du contexte plutôt que de s’appuyer sur l’environnement de l’application d’hébergement.

L’auteur du composant hébergé est dans la meilleure position pour savoir exactement quels autres assemblys le composant requiert. La base de l’application hôte pour fournir l’environnement approprié pour votre composant hébergé est une source probable d’erreurs. Au lieu de cela, créez un manifeste pour votre composant hébergé qui spécifie toutes ses dépendances, puis compilez en utilisant la prise en charge de l’ISOLATION \_ \_ activée. Cela garantit que les appels externes effectués par votre composant sont isolés et utilisent les versions appropriées. Étant donné que le contexte d’activation que la prise en charge de l’ISOLATION \_ \_ utilise est par dll, il est possible de l’utiliser dans plusieurs dll, chacune avec son propre manifeste appelant des dépendances.

S’il n’est pas possible de compiler avec la prise en charge de l’ISOLATION \_ \_ activée, utilisez une solution semblable à celle présentée dans [utilisation de rappels à partir de composants hébergés](using-callbacks-from-hosted-components.md).

Vous devez activer votre propre contexte d’activation dans tous les points d’entrée que l’application d’hébergement peut appeler pour s’assurer que votre composant hébergé s’exécute entièrement avec le contexte d’activation correct. Vous pouvez utiliser un objet d’assistance C++ pour faciliter la modification de tous les entryPoints. Par exemple, vous pouvez utiliser une classe C++ telle que la suivante :


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



Vous pouvez ensuite l’utiliser dans votre composant, à l’aide d’une variable globale pour stocker le contexte d’activation qui doit être activé sur chaque point d’entrée. De cette façon, vous pouvez isoler votre composant de votre application d’hébergement.


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



