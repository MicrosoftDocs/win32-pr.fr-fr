---
description: Les applications peuvent gérer un contexte d’activation en appelant directement les fonctions de contexte d’activation.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Utilisation de l’API de contexte d’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112694"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="fd05e-103">Utilisation de l’API de contexte d’activation</span><span class="sxs-lookup"><span data-stu-id="fd05e-103">Using the Activation Context API</span></span>

<span data-ttu-id="fd05e-104">Les applications peuvent gérer un [contexte d’activation](activation-contexts.md) en appelant directement les fonctions de contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd05e-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="fd05e-105">Les contextes d’activation sont des structures de données en mémoire.</span><span class="sxs-lookup"><span data-stu-id="fd05e-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="fd05e-106">Le système peut utiliser les informations du contexte d’activation pour rediriger une application afin de charger une version de DLL particulière, une instance d’objet COM ou une version de fenêtre personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fd05e-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="fd05e-107">Pour plus d’informations, consultez [Référence du contexte d’activation](activation-context-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fd05e-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="fd05e-108">L’interface de programmation d’applications (API) peut être utilisée pour gérer le contexte d’activation et créer des objets de nom de version avec des [manifestes](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="fd05e-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="fd05e-109">Les deux scénarios suivants illustrent comment une application peut gérer un contexte d’activation en appelant directement les fonctions de contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd05e-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="fd05e-110">Toutefois, dans la plupart des cas, le contexte d’activation est géré par le système.</span><span class="sxs-lookup"><span data-stu-id="fd05e-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="fd05e-111">Les développeurs d’applications et les fournisseurs d’assemblys n’ont généralement pas besoin d’effectuer des appels à la pile pour gérer le contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd05e-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="fd05e-112">Processus et applications qui implémentent des couches d’indirection ou de répartition.</span><span class="sxs-lookup"><span data-stu-id="fd05e-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="fd05e-113">Par exemple, un utilisateur qui gère les contextes d’activation dans la boucle d’événements.</span><span class="sxs-lookup"><span data-stu-id="fd05e-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="fd05e-114">Chaque fois que vous accédez à la fenêtre, par exemple en déplaçant la souris sur la fenêtre, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) est appelé, ce qui active le contexte d’activation actuel pour la ressource, comme indiqué dans le fragment de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fd05e-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="fd05e-115">HANDLE hActCtx ;</span><span class="sxs-lookup"><span data-stu-id="fd05e-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="fd05e-116">CreateWindow ();</span><span class="sxs-lookup"><span data-stu-id="fd05e-116">CreateWindow();</span></span>  
    <span data-ttu-id="fd05e-117">...</span><span class="sxs-lookup"><span data-stu-id="fd05e-117">...</span></span>  
    <span data-ttu-id="fd05e-118">GetCurrentActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="fd05e-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="fd05e-119">...</span><span class="sxs-lookup"><span data-stu-id="fd05e-119">...</span></span>  
    <span data-ttu-id="fd05e-120">ReleaseActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="fd05e-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="fd05e-121">Dans le fragment de code suivant, la fonction API active les contextes d’activation appropriés avant d’appeler [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span><span class="sxs-lookup"><span data-stu-id="fd05e-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="fd05e-122">Quand **CallWindowProc** est appelé, il utilise ce contexte pour transmettre un message à Windows.</span><span class="sxs-lookup"><span data-stu-id="fd05e-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="fd05e-123">Lorsque toutes les opérations de ressource sont terminées, la fonction désactive le contexte.</span><span class="sxs-lookup"><span data-stu-id="fd05e-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="fd05e-124">ULONG \_ ptr ulpCookie ;</span><span class="sxs-lookup"><span data-stu-id="fd05e-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="fd05e-125">HANDLE hActCtx ;</span><span class="sxs-lookup"><span data-stu-id="fd05e-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="fd05e-126">if (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="fd05e-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="fd05e-127">{</span><span class="sxs-lookup"><span data-stu-id="fd05e-127">{</span></span>  
    <span data-ttu-id="fd05e-128">...</span><span class="sxs-lookup"><span data-stu-id="fd05e-128">...</span></span>  
    <span data-ttu-id="fd05e-129">CallWindowProc(...);</span><span class="sxs-lookup"><span data-stu-id="fd05e-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="fd05e-130">...</span><span class="sxs-lookup"><span data-stu-id="fd05e-130">...</span></span>  
    <span data-ttu-id="fd05e-131">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="fd05e-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="fd05e-132">}</span><span class="sxs-lookup"><span data-stu-id="fd05e-132">}</span></span>  
    </dl>

-   <span data-ttu-id="fd05e-133">Couche de répartition de délégation.</span><span class="sxs-lookup"><span data-stu-id="fd05e-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="fd05e-134">Ce scénario s’applique aux responsables qui gèrent plusieurs entités avec une couche API commune, telle qu’un gestionnaire de pilotes.</span><span class="sxs-lookup"><span data-stu-id="fd05e-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="fd05e-135">Bien qu’il n’ait pas encore été implémenté, il s’agit d’un exemple de pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="fd05e-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="fd05e-136">Dans ce scénario, la couche intermédiaire prend en charge le traitement des liaisons d’assembly.</span><span class="sxs-lookup"><span data-stu-id="fd05e-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="fd05e-137">Pour obtenir le pilote de liaison spécifique à la version, les éditeurs doivent fournir un manifeste et spécifier des dépendances sur des composants spécifiques dans ce manifeste.</span><span class="sxs-lookup"><span data-stu-id="fd05e-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="fd05e-138">L’application de base ne crée pas de liaison dynamique avec les composants ; au moment de l’exécution, le gestionnaire de pilotes gère les appels.</span><span class="sxs-lookup"><span data-stu-id="fd05e-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="fd05e-139">Lorsque le pilote ODBC est appelé en fonction de la chaîne de connexion, il charge le pilote approprié.</span><span class="sxs-lookup"><span data-stu-id="fd05e-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="fd05e-140">Il crée ensuite le contexte d’activation à l’aide des informations contenues dans le fichier manifeste de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="fd05e-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="fd05e-141">Sans le manifeste, l’action par défaut pour le pilote consiste à utiliser le même contexte que celui spécifié par l’application (dans cet exemple, la version 2 de MSVCRT).</span><span class="sxs-lookup"><span data-stu-id="fd05e-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="fd05e-142">Étant donné qu’un manifeste existe, un contexte d’activation distinct est établi.</span><span class="sxs-lookup"><span data-stu-id="fd05e-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="fd05e-143">Lorsque le pilote ODBC s’exécute, il est lié à la version 1 de l’assembly MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="fd05e-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="fd05e-144">Chaque fois que le gestionnaire de pilotes appelle la couche de répartition (par exemple, pour obtenir le jeu de données suivant), il utilise les assemblys appropriés en fonction du contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="fd05e-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="fd05e-145">Le fragment de code suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="fd05e-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="fd05e-146">HANDLE hActCtx ;</span><span class="sxs-lookup"><span data-stu-id="fd05e-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="fd05e-147">ULONG \_ ptr ulpCookie ;</span><span class="sxs-lookup"><span data-stu-id="fd05e-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="fd05e-148">ACTCTX ActCtxToCreate = {...};</span><span class="sxs-lookup"><span data-stu-id="fd05e-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="fd05e-149">hActCtx = CreateActCtx (&ActCtxToCreate);</span><span class="sxs-lookup"><span data-stu-id="fd05e-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="fd05e-150">...;</span><span class="sxs-lookup"><span data-stu-id="fd05e-150">...;</span></span>  
    <span data-ttu-id="fd05e-151">if (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="fd05e-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="fd05e-152">{</span><span class="sxs-lookup"><span data-stu-id="fd05e-152">{</span></span>  
    <span data-ttu-id="fd05e-153">...</span><span class="sxs-lookup"><span data-stu-id="fd05e-153">...</span></span>  
    <span data-ttu-id="fd05e-154">ConnectDb(...);</span><span class="sxs-lookup"><span data-stu-id="fd05e-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="fd05e-155">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="fd05e-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="fd05e-156">}</span><span class="sxs-lookup"><span data-stu-id="fd05e-156">}</span></span>  
    <span data-ttu-id="fd05e-157">...</span><span class="sxs-lookup"><span data-stu-id="fd05e-157">...</span></span>  
    <span data-ttu-id="fd05e-158">ReleaseActCtx(hActCtx);</span><span class="sxs-lookup"><span data-stu-id="fd05e-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
