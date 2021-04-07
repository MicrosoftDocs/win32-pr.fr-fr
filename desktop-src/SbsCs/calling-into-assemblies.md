---
description: Lors d’un appel dans le entryPoints d’un assembly, il est recommandé d’utiliser le même contexte d’activation qui était actif lors de la recherche de l’assembly.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Appeler dans des assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952220"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="a41ee-103">Appeler dans des assemblys</span><span class="sxs-lookup"><span data-stu-id="a41ee-103">Calling Into Assemblies</span></span>

<span data-ttu-id="a41ee-104">Lors d’un appel dans le entryPoints d’un assembly, il est recommandé d’utiliser le même contexte d’activation qui était actif lors de la recherche de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a41ee-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="a41ee-105">Au minimum, assurez-vous que le chargement du composant de l’assembly n’obtient pas accidentellement le contexte d’activation utilisé par votre application.</span><span class="sxs-lookup"><span data-stu-id="a41ee-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="a41ee-106">La fuite du contexte d’activation entre les limites des DLL peut entraîner des dépendances inattendues.</span><span class="sxs-lookup"><span data-stu-id="a41ee-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="a41ee-107">Ce n’est pas un problème si votre application compile la prise \_ en charge de l’isolation \_ activée, car dans ce cas, aucun contexte d’activation n’est actif par défaut.</span><span class="sxs-lookup"><span data-stu-id="a41ee-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="a41ee-108">Si vous ne compilez pas avec la prise en charge de l’ISOLATION \_ \_ activée, vous devez activer le contexte d’activation **null** ou le même contexte d’activation qui a été utilisé pour charger l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a41ee-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="a41ee-109">L’exemple suivant vérifie que la DLL hébergée s’exécute dans un contexte qu’elle reconnaît :</span><span class="sxs-lookup"><span data-stu-id="a41ee-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



