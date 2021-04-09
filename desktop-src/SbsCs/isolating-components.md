---
description: Les composants bien créés ne perturbent pas l’environnement de l’application d’hébergement et ne perdent pas de contextes d’activation.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolation des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862338"
---
# <a name="isolating-components"></a><span data-ttu-id="ed9e6-103">Isolation des composants</span><span class="sxs-lookup"><span data-stu-id="ed9e6-103">Isolating Components</span></span>

<span data-ttu-id="ed9e6-104">Les composants bien créés ne perturbent pas l’environnement de l’application d’hébergement et ne perdent pas de contextes d’activation.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="ed9e6-105">Les composants bien créés effectuent leur propre gestion du contexte plutôt que de s’appuyer sur l’environnement de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="ed9e6-106">L’auteur du composant hébergé est dans la meilleure position pour savoir exactement quels autres assemblys le composant requiert.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="ed9e6-107">La base de l’application hôte pour fournir l’environnement approprié pour votre composant hébergé est une source probable d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="ed9e6-108">Au lieu de cela, créez un manifeste pour votre composant hébergé qui spécifie toutes ses dépendances, puis compilez en utilisant la prise en charge de l’ISOLATION \_ \_ activée.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="ed9e6-109">Cela garantit que les appels externes effectués par votre composant sont isolés et utilisent les versions appropriées.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="ed9e6-110">Étant donné que le contexte d’activation que la prise en charge de l’ISOLATION \_ \_ utilise est par dll, il est possible de l’utiliser dans plusieurs dll, chacune avec son propre manifeste appelant des dépendances.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="ed9e6-111">S’il n’est pas possible de compiler avec la prise en charge de l’ISOLATION \_ \_ activée, utilisez une solution semblable à celle présentée dans [utilisation de rappels à partir de composants hébergés](using-callbacks-from-hosted-components.md).</span><span class="sxs-lookup"><span data-stu-id="ed9e6-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="ed9e6-112">Vous devez activer votre propre contexte d’activation dans tous les points d’entrée que l’application d’hébergement peut appeler pour s’assurer que votre composant hébergé s’exécute entièrement avec le contexte d’activation correct.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="ed9e6-113">Vous pouvez utiliser un objet d’assistance C++ pour faciliter la modification de tous les entryPoints.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="ed9e6-114">Par exemple, vous pouvez utiliser une classe C++ telle que la suivante :</span><span class="sxs-lookup"><span data-stu-id="ed9e6-114">For example, you could use a C++ class such as the following:</span></span>


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



<span data-ttu-id="ed9e6-115">Vous pouvez ensuite l’utiliser dans votre composant, à l’aide d’une variable globale pour stocker le contexte d’activation qui doit être activé sur chaque point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="ed9e6-116">De cette façon, vous pouvez isoler votre composant de votre application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="ed9e6-116">In this way, you can isolate your component from your hosting application.</span></span>


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



 

 



