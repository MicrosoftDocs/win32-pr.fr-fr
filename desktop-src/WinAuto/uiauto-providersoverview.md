---
title: Vue d'ensemble des fournisseurs UI Automation
description: Cette rubrique fournit une vue d’ensemble de la façon dont les développeurs de contrôles implémentent des fournisseurs UI Automation.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- UI Automation, vue d’ensemble des fournisseurs
- UI Automation, types de fournisseurs
- UI Automation, concepts du fournisseur
- fournisseurs, à propos de
- fournisseurs, types
- fournisseurs, concepts
- fournisseurs, éléments
- fournisseurs, navigation
- fournisseurs, vues
- fournisseurs, infrastructures
- fournisseurs, fragments
- fournisseurs, hôtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939847"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="0cba0-115">Vue d'ensemble des fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="0cba0-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="0cba0-116">Un fournisseur Microsoft UI Automation est un objet logiciel qui expose un élément de l’interface utilisateur d’une application de sorte que les applications clientes d’accessibilité puissent récupérer des informations sur l’élément et appeler ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="0cba0-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="0cba0-117">En général, chaque contrôle ou autre élément distinct d’une interface utilisateur a un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cba0-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="0cba0-118">Microsoft propose un fournisseur pour chacun des contrôles standard fournis avec Microsoft Win32, Windows Forms et Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="0cba0-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="0cba0-119">Cela signifie que les contrôles standard sont exposés automatiquement aux clients UI Automation. vous n’avez pas besoin d’implémenter d’interfaces d’accessibilité pour les contrôles standard.</span><span class="sxs-lookup"><span data-stu-id="0cba0-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="0cba0-120">Si votre application comprend des contrôles personnalisés, vous devez implémenter des fournisseurs UI Automation pour ces contrôles afin de les rendre accessibles aux applications clientes d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="0cba0-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="0cba0-121">Vous devez également implémenter des fournisseurs pour les contrôles tiers qui n’incluent pas de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cba0-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="0cba0-122">Implémentez un fournisseur en implémentant des interfaces de fournisseur UI Automation et des interfaces de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0cba0-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="0cba0-123">Cette rubrique fournit une vue d’ensemble de la façon dont les développeurs de contrôles implémentent des fournisseurs UI Automation.</span><span class="sxs-lookup"><span data-stu-id="0cba0-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="0cba0-124">Il comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="0cba0-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="0cba0-125">Types de fournisseurs</span><span class="sxs-lookup"><span data-stu-id="0cba0-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="0cba0-126">Concepts de fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="0cba0-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   [<span data-ttu-id="0cba0-127">Éléments</span><span class="sxs-lookup"><span data-stu-id="0cba0-127">Elements</span></span>](#elements)
    -   [<span data-ttu-id="0cba0-128">Frameworks</span><span class="sxs-lookup"><span data-stu-id="0cba0-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="0cba0-129">Fragments</span><span class="sxs-lookup"><span data-stu-id="0cba0-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="0cba0-130">Hôtes</span><span class="sxs-lookup"><span data-stu-id="0cba0-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="0cba0-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cba0-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="0cba0-132">Types de fournisseurs</span><span class="sxs-lookup"><span data-stu-id="0cba0-132">Types of Providers</span></span>

<span data-ttu-id="0cba0-133">Les fournisseurs UI Automation se répartissent en deux catégories : les fournisseurs côté serveur et les fournisseurs côté client (ou *proxy*).</span><span class="sxs-lookup"><span data-stu-id="0cba0-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="0cba0-134">Un fournisseur côté serveur est un objet, tel qu’un contrôle personnalisé, qui contient sa propre implémentation native des interfaces de fournisseur UI Automation pertinentes.</span><span class="sxs-lookup"><span data-stu-id="0cba0-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="0cba0-135">Un fournisseur côté serveur communique avec les applications clientes à travers la limite de processus en exposant son implémentation des interfaces de fournisseur au noyau UI Automation, qui traite les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="0cba0-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="0cba0-136">Pour plus d’informations sur les fournisseurs côté serveur, consultez [implémentation d’un fournisseur UI Automation Server-Side](uiauto-serversideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="0cba0-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="0cba0-137">Un fournisseur côté client, ou proxy, est un objet qui implémente des interfaces de fournisseur UI Automation pour le compte d’un contrôle ne comprend pas une implémentation complète de son propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cba0-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="0cba0-138">Sans proxy, ce type de contrôle est largement opaque pour l’Automation d’interface utilisateur, qui peut fournir uniquement les informations de base disponibles à partir du handle de fenêtre (**HWND**), telles que l’emplacement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0cba0-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="0cba0-139">En règle générale, les fournisseurs de proxy communiquent avec l’application à travers la limite de processus en envoyant et en recevant des messages Windows.</span><span class="sxs-lookup"><span data-stu-id="0cba0-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="0cba0-140">Pour plus d’informations, consultez [implémentation d’un fournisseur UI Automation Client-Side (proxy)](uiauto-clientsideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="0cba0-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="0cba0-141">Concepts de fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="0cba0-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="0cba0-142">Cette section fournit de brèves explications sur certains concepts clés que vous devez comprendre pour pouvoir implémenter des fournisseurs UI Automation.</span><span class="sxs-lookup"><span data-stu-id="0cba0-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="0cba0-143">Éléments</span><span class="sxs-lookup"><span data-stu-id="0cba0-143">Elements</span></span>

<span data-ttu-id="0cba0-144">Les éléments UI Automation sont des parties de l’interface utilisateur, généralement des fenêtres ou des contrôles, qui sont visibles par les clients UI Automation.</span><span class="sxs-lookup"><span data-stu-id="0cba0-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="0cba0-145">Les fenêtres d’application, les volets, les boutons, les info-bulles, les zones de liste et les éléments de liste en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="0cba0-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="0cba0-146">Les éléments UI Automation sont exposés aux clients sous la forme d’une arborescence.</span><span class="sxs-lookup"><span data-stu-id="0cba0-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="0cba0-147">UI Automation construit l’arborescence en naviguant d’un élément à un autre.</span><span class="sxs-lookup"><span data-stu-id="0cba0-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="0cba0-148">La navigation est activée par le fournisseur pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="0cba0-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="0cba0-149">Chaque élément peut pointer vers son propre élément parent, ses éléments frères et ses premier et dernier éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="0cba0-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="0cba0-150">Un client peut voir l’arborescence UI Automation dans trois vues principales, comme décrit dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="0cba0-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="0cba0-151">Affichage</span><span class="sxs-lookup"><span data-stu-id="0cba0-151">View</span></span>         | <span data-ttu-id="0cba0-152">Description</span><span class="sxs-lookup"><span data-stu-id="0cba0-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="0cba0-153">Affichage brut</span><span class="sxs-lookup"><span data-stu-id="0cba0-153">Raw view</span></span>     | <span data-ttu-id="0cba0-154">Comprend tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="0cba0-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="0cba0-155">Vue de contrôle</span><span class="sxs-lookup"><span data-stu-id="0cba0-155">Control view</span></span> | <span data-ttu-id="0cba0-156">Comprend des éléments qui sont des contrôles.</span><span class="sxs-lookup"><span data-stu-id="0cba0-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="0cba0-157">Vue de contenu</span><span class="sxs-lookup"><span data-stu-id="0cba0-157">Content view</span></span> | <span data-ttu-id="0cba0-158">Comprend des éléments de contrôle qui fournissent des informations à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cba0-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="0cba0-159">Il incombe à l’implémentation du fournisseur de définir un élément comme élément de contenu ou élément de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0cba0-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="0cba0-160">Les éléments de contrôle peuvent être ou non également des éléments de contenu, mais tous les éléments de contenu sont des éléments de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0cba0-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="0cba0-161">Pour plus d’informations sur la vue client de l’arborescence, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0cba0-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="0cba0-162">Frameworks</span><span class="sxs-lookup"><span data-stu-id="0cba0-162">Frameworks</span></span>

<span data-ttu-id="0cba0-163">Une infrastructure est un composant qui gère les contrôles enfants, les tests de positionnement et le rendu dans une zone de l’écran.</span><span class="sxs-lookup"><span data-stu-id="0cba0-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="0cba0-164">Par exemple, une fenêtre Win32, souvent appelée **HWND**, peut servir d’infrastructure contenant plusieurs éléments UI Automation, tels qu’une barre de menus, une barre d’État et des boutons.</span><span class="sxs-lookup"><span data-stu-id="0cba0-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="0cba0-165">Les contrôles de conteneur Win32, tels que les zones de liste et les contrôles d’arborescence, sont considérés comme des infrastructures, car ils contiennent leur propre code pour restituer des éléments enfants et effectuer des tests de positionnement sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="0cba0-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="0cba0-166">En revanche, une zone de liste WPF n’est pas une infrastructure, car le rendu et le test de positionnement sont gérés par la fenêtre conteneur.</span><span class="sxs-lookup"><span data-stu-id="0cba0-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="0cba0-167">L’interface utilisateur d’une application peut être composée de différentes infrastructures.</span><span class="sxs-lookup"><span data-stu-id="0cba0-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="0cba0-168">Par exemple, un **HWND** dans une application peut contenir du HTML dynamique (DHTML) qui peut à son tour contenir un composant tel qu’une zone de liste déroulante dans un **HWND**.</span><span class="sxs-lookup"><span data-stu-id="0cba0-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="0cba0-169">Fragments</span><span class="sxs-lookup"><span data-stu-id="0cba0-169">Fragments</span></span>

<span data-ttu-id="0cba0-170">Une sous-arborescence complète d’éléments d’une infrastructure particulière est appelée un fragment.</span><span class="sxs-lookup"><span data-stu-id="0cba0-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="0cba0-171">L’élément au niveau du nœud racine de la sous-arborescence est appelé racine de fragment.</span><span class="sxs-lookup"><span data-stu-id="0cba0-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="0cba0-172">Une racine de fragment n’a pas de parent, mais elle est hébergée dans une autre infrastructure, généralement une fenêtre Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="0cba0-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="0cba0-173">Hôtes</span><span class="sxs-lookup"><span data-stu-id="0cba0-173">Hosts</span></span>

<span data-ttu-id="0cba0-174">Le nœud racine de chaque fragment doit être hébergé dans un élément, généralement une fenêtre Win32 (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="0cba0-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="0cba0-175">Le bureau est une exception et il n’est hébergé dans aucun autre élément.</span><span class="sxs-lookup"><span data-stu-id="0cba0-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="0cba0-176">L’hôte d’un contrôle personnalisé est le **HWND** du contrôle lui-même, et non la fenêtre d’application ou toute autre fenêtre qui peut contenir des groupes de contrôles de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="0cba0-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="0cba0-177">L’hôte d’un fragment joue un rôle important dans la fourniture de services UI Automation.</span><span class="sxs-lookup"><span data-stu-id="0cba0-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="0cba0-178">Il permet la navigation vers la racine de fragment et fournit des propriétés par défaut afin que le fournisseur personnalisé n’ait pas à les implémenter.</span><span class="sxs-lookup"><span data-stu-id="0cba0-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cba0-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cba0-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0cba0-180">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0cba0-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0cba0-181">Implémentation d’un fournisseur UI Automation Client-Side</span><span class="sxs-lookup"><span data-stu-id="0cba0-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="0cba0-182">Implémentation d’un fournisseur UI Automation Server-Side</span><span class="sxs-lookup"><span data-stu-id="0cba0-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="0cba0-183">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="0cba0-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




