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
# <a name="calling-outside-an-assembly"></a>Appel à l’extérieur d’un assembly

Les composants hébergés doivent s’assurer que le contexte d’activation correct est actif lors d’un appel à l’extérieur du composant. Les appels dans du code externe qui a été trouvé en appelant [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) , puis [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), doivent être appelés avec le même contexte que celui utilisé pour le trouver. Les appels dans le code qui a été trouvé en dehors des contextes d’activation ou les rappels dans l’application d’hébergement doivent être appelés avec le contexte d’activation par défaut de l’application.

La compilation avec prise en \_ charge de \_ l’isolation activée peut être utile lors de l’appel en dehors des composants hébergés. Toutefois, cela signifie que seuls les appels aux API Windows sont isolés dans le contexte d’activation du composant. Cela suffit dans la plupart des cas, car les appels à des fonctions tierces n’ont pas de contexte activé avant d’être appelés. La compilation avec prise en charge de l’ISOLATION \_ \_ activée n’est pas utile si votre composant utilise plusieurs contextes d’activation avec différentes API de plateforme.

Pour l’implémenter, utilisez un activateur de contexte d’activation comme l’exemple présenté dans [isolation des composants](isolating-components.md). Ici, externes. manifest est l’ensemble de dépendances en dehors de celles sur lesquelles le composant a été créé ; peut-être contient peut-être une liste extensible de composants qui doivent être chargés et utilisés lors de l’exécution. Internalcontext. manifest contient le jeu de dépendances que le composant est sûr d’utiliser pendant sa durée de vie, et qui doit être défini dans tous les entryPoints à partir de l’extérieur. Notez que ce contexte interne est activé dans toutes les entryPoints, tandis que l’activateur de contexte est utilisé avec l’étendue C++ afin que le contexte approprié soit défini lors de l’appel des différents codes externes utilisés par ce composant.

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

 

 
