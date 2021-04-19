---
description: Appel à l’extérieur d’un assembly
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Appel à l’extérieur d’un assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518744"
---
# <a name="calling-outside-an-assembly"></a><span data-ttu-id="748fe-103">Appel à l’extérieur d’un assembly</span><span class="sxs-lookup"><span data-stu-id="748fe-103">Calling Outside An Assembly</span></span>

<span data-ttu-id="748fe-104">Les composants hébergés doivent s’assurer que le contexte d’activation correct est actif lors d’un appel à l’extérieur du composant.</span><span class="sxs-lookup"><span data-stu-id="748fe-104">Hosted components should ensure that the correct activation context is active when calling outside the component.</span></span> <span data-ttu-id="748fe-105">Les appels dans du code externe qui a été trouvé en appelant [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) , puis [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), doivent être appelés avec le même contexte que celui utilisé pour le trouver.</span><span class="sxs-lookup"><span data-stu-id="748fe-105">Calls into outside code that was found by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) and then [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), should be called with the same context that was used to find it.</span></span> <span data-ttu-id="748fe-106">Les appels dans le code qui a été trouvé en dehors des contextes d’activation ou les rappels dans l’application d’hébergement doivent être appelés avec le contexte d’activation par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="748fe-106">Calls into code that was found outside of activation contexts, or calls back into the hosting application should be called with the application default activation context.</span></span>

<span data-ttu-id="748fe-107">La compilation avec prise en \_ charge de \_ l’isolation activée peut être utile lors de l’appel en dehors des composants hébergés.</span><span class="sxs-lookup"><span data-stu-id="748fe-107">Compiling with ISOLATION\_AWARE\_ENABLED defined may be useful when calling outside of hosted components.</span></span> <span data-ttu-id="748fe-108">Toutefois, cela signifie que seuls les appels aux API Windows sont isolés dans le contexte d’activation du composant.</span><span class="sxs-lookup"><span data-stu-id="748fe-108">However this means that only calls to Windows APIs are isolated to the component's activation context.</span></span> <span data-ttu-id="748fe-109">Cela suffit dans la plupart des cas, car les appels à des fonctions tierces n’ont pas de contexte activé avant d’être appelés.</span><span class="sxs-lookup"><span data-stu-id="748fe-109">This is sufficient for most cases because calls to third-party functions do not have a context activated before being called.</span></span> <span data-ttu-id="748fe-110">La compilation avec prise en charge de l’ISOLATION \_ \_ activée n’est pas utile si votre composant utilise plusieurs contextes d’activation avec différentes API de plateforme.</span><span class="sxs-lookup"><span data-stu-id="748fe-110">Compiling with ISOLATION\_AWARE\_ENABLED defined does not help if your component uses several activation contexts with various platform APIs.</span></span>

<span data-ttu-id="748fe-111">Pour l’implémenter, utilisez un activateur de contexte d’activation comme l’exemple présenté dans [isolation des composants](isolating-components.md).</span><span class="sxs-lookup"><span data-stu-id="748fe-111">To implement this, use an activation context activator like the example presented in [Isolating Components](isolating-components.md).</span></span> <span data-ttu-id="748fe-112">Ici, externes. manifest est l’ensemble de dépendances en dehors de celles sur lesquelles le composant a été créé ; peut-être contient peut-être une liste extensible de composants qui doivent être chargés et utilisés lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="748fe-112">Here externals.manifest is the set of dependencies outside those the component was built with; perhaps it contains some extendable list of components that are to be loaded and used during runtime.</span></span> <span data-ttu-id="748fe-113">Internalcontext. manifest contient le jeu de dépendances que le composant est sûr d’utiliser pendant sa durée de vie, et qui doit être défini dans tous les entryPoints à partir de l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="748fe-113">The internalcontext.manifest contains the set of dependencies that the component is sure to use during its lifetime, and which should be set in all entrypoints from the outside.</span></span> <span data-ttu-id="748fe-114">Notez que ce contexte interne est activé dans toutes les entryPoints, tandis que l’activateur de contexte est utilisé avec l’étendue C++ afin que le contexte approprié soit défini lors de l’appel des différents codes externes utilisés par ce composant.</span><span class="sxs-lookup"><span data-stu-id="748fe-114">Notice that this internal context is activated in all entrypoints, while the context activator is used with C++ scoping so that the proper context is set when calling out to the various outside code that this component uses.</span></span>

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
