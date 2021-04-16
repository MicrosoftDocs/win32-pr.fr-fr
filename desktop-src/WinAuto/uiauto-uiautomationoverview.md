---
title: Vue d'ensemble d'UI Automation
description: Microsoft UI Automation est une infrastructure d’accessibilité pour Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- UI Automation, à propos de
- UI Automation, accessibilité
- UI Automation, composants
- UI Automation, API du fournisseur
- UI Automation, API client
- UI Automation, fichiers d’en-tête
- UI Automation, modèle
- components
- accessibilité
- API du fournisseur
- API client
- fichiers d'en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381450"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="c22c1-115">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-115">UI Automation Overview</span></span>

<span data-ttu-id="c22c1-116">Microsoft UI Automation est une infrastructure d’accessibilité pour Windows.</span><span class="sxs-lookup"><span data-stu-id="c22c1-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="c22c1-117">Il fournit un accès par programme à la plupart des éléments d’interface utilisateur sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="c22c1-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="c22c1-118">Il permet aux produits de technologie d’assistance, tels que les lecteurs d’écran, de fournir des informations sur l’interface utilisateur aux utilisateurs finaux et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard.</span><span class="sxs-lookup"><span data-stu-id="c22c1-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="c22c1-119">UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c22c1-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="c22c1-120">UI Automation était d’abord disponible dans Windows XP dans le cadre de l’infrastructure Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="c22c1-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c22c1-121">Bien qu’une API C++ non managée ait également été publiée à ce moment-là, l’utilité des fonctions clientes était limitée en raison de problèmes d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="c22c1-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="c22c1-122">Pour Windows 7, l’API a été réécrite dans le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="c22c1-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="c22c1-123">Bien que les fonctions de bibliothèque introduites dans la version antérieure d’UI Automation soient toujours documentées, elles ne doivent pas être utilisées dans les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="c22c1-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="c22c1-124">Les applications clientes UI Automation peuvent être écrites avec l’assurance qu’elles fonctionneront sur plusieurs infrastructures de contrôle Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c22c1-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="c22c1-125">Le noyau UI Automation masque les différences dans les infrastructures qui sous-tendent les différents éléments de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c22c1-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="c22c1-126">Par exemple, la propriété de **contenu** d’un bouton Windows Presentation Foundation (WPF), la propriété **Caption** d’un bouton Microsoft Win32 et la propriété **ALT** d’une image HTML sont toutes mappées à une seule propriété, **Name**, dans la vue UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="c22c1-127">UI Automation fournit toutes les fonctionnalités de Windows XP, Windows Server 2003 et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="c22c1-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="c22c1-128">Les fournisseurs UI Automation sont des composants qui implémentent la prise en charge d’UI Automation sur les contrôles et offrent une certaine prise en charge pour les applications clientes Microsoft Active Accessibility, par le biais d’un service de pontage intégré.</span><span class="sxs-lookup"><span data-stu-id="c22c1-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="c22c1-129">UI Automation n’active pas la communication entre les processus démarrés par différents utilisateurs via la commande **exécuter en tant que** .</span><span class="sxs-lookup"><span data-stu-id="c22c1-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="c22c1-130">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c22c1-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c22c1-131">Composants UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="c22c1-132">Fichiers d’en-tête UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="c22c1-133">Modèle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="c22c1-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c22c1-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="c22c1-135">Composants UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-135">UI Automation Components</span></span>

<span data-ttu-id="c22c1-136">UI Automation comporte quatre composants principaux, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c22c1-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c22c1-137">Composant</span><span class="sxs-lookup"><span data-stu-id="c22c1-137">Component</span></span></th>
<th><span data-ttu-id="c22c1-138">Description</span><span class="sxs-lookup"><span data-stu-id="c22c1-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c22c1-139">API du fournisseur</span><span class="sxs-lookup"><span data-stu-id="c22c1-139">Provider API</span></span></td>
<td><span data-ttu-id="c22c1-140">Ensemble d’interfaces COM qui sont implémentées par les fournisseurs UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="c22c1-141">Les fournisseurs UI Automation sont des objets qui fournissent des informations sur les éléments d’interface utilisateur et répondent aux entrées par programmation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c22c1-142">API client</span><span class="sxs-lookup"><span data-stu-id="c22c1-142">Client API</span></span></td>
<td><span data-ttu-id="c22c1-143">Ensemble d’interfaces COM qui permettent aux applications clientes d’obtenir des informations sur l’interface utilisateur et d’envoyer des entrées à des contrôles.</span><span class="sxs-lookup"><span data-stu-id="c22c1-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c22c1-144">Les fonctions décrites dans <a href="uiauto-entry-cpfunctions.md">fonctions de modèle de contrôle déconseillées</a> et <a href="uiauto-entry-uianodefunctions.md">fonctions de nœud déconseillées</a> sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="c22c1-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="c22c1-145">Au lieu de cela, les applications clientes doivent utiliser les interfaces COM UI Automation décrites dans <a href="uiauto-entry-uiautoclientinterfaces.md">interfaces d’élément UI Automation pour les clients</a>.</span><span class="sxs-lookup"><span data-stu-id="c22c1-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c22c1-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="c22c1-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="c22c1-147">La bibliothèque Runtime, parfois appelée noyau UI Automation, gère la communication entre les fournisseurs et les clients.</span><span class="sxs-lookup"><span data-stu-id="c22c1-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c22c1-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="c22c1-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="c22c1-149">La bibliothèque Runtime pour Microsoft Active Accessibility et les objets proxy.</span><span class="sxs-lookup"><span data-stu-id="c22c1-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="c22c1-150">La bibliothèque fournit également des objets proxy utilisés par Microsoft Microsoft Active Accessibility au proxy UI Automation pour prendre en charge les contrôles Win32.</span><span class="sxs-lookup"><span data-stu-id="c22c1-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c22c1-151">Il existe deux façons d’utiliser UI Automation : pour créer la prise en charge des contrôles personnalisés à l’aide de l’API du fournisseur et pour créer des applications clientes qui utilisent le noyau UI Automation pour communiquer et récupérer des informations sur les éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c22c1-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="c22c1-152">Selon votre objectif, reportez-vous à différentes parties de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="c22c1-153">Si vous devez créer la prise en charge des contrôles personnalisés, consultez le [Guide du programmeur de fournisseur UI Automation](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="c22c1-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="c22c1-154">Si vous avez besoin de communiquer avec ou de récupérer des informations sur les éléments d’interface utilisateur, consultez le [Guide du programmeur du client UI Automation](uiauto-clientportal.md).</span><span class="sxs-lookup"><span data-stu-id="c22c1-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="c22c1-155">Fichiers d’en-tête UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-155">UI Automation Header Files</span></span>

<span data-ttu-id="c22c1-156">L’API UI Automation est définie dans plusieurs fichiers d’en-tête C/C++ différents inclus dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="c22c1-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c22c1-157">Les fichiers d’en-tête UI Automation sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="c22c1-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="c22c1-158">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c22c1-158">Header file</span></span>           | <span data-ttu-id="c22c1-159">Description</span><span class="sxs-lookup"><span data-stu-id="c22c1-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c22c1-160">UIAutomationClient. h</span><span class="sxs-lookup"><span data-stu-id="c22c1-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="c22c1-161">Définit les interfaces et les éléments de programmation associés utilisés par les clients UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="c22c1-162">UIAutomationCore. h</span><span class="sxs-lookup"><span data-stu-id="c22c1-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="c22c1-163">Définit les interfaces et les éléments de programmation associés utilisés par les fournisseurs UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="c22c1-164">UIAutomationCoreApi. h</span><span class="sxs-lookup"><span data-stu-id="c22c1-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="c22c1-165">Définit des constantes générales, des GUID, des types de données et des structures utilisés par des fournisseurs et des clients UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="c22c1-166">Elle contient également des définitions pour le nœud déconseillé et les fonctions de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c22c1-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="c22c1-167">UIAutomation. h</span><span class="sxs-lookup"><span data-stu-id="c22c1-167">UIAutomation.h</span></span>        | <span data-ttu-id="c22c1-168">Comprend tous les autres fichiers d’en-tête UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c22c1-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="c22c1-169">Étant donné que la plupart des applications UI Automation requièrent des éléments de tous les fichiers d’en-tête UI Automation, il est préférable d’inclure UIAutomation. h dans vos projets d’application UI Automation au lieu d’inclure chaque fichier individuellement.</span><span class="sxs-lookup"><span data-stu-id="c22c1-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="c22c1-170">Si vous développez une application qui utilise l’API UI Automation, vous devez inclure UIAutomation. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="c22c1-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="c22c1-171">Si votre application prend en charge Microsoft Active Accessibility, incluez le fichier d’en-tête oleacc. h.</span><span class="sxs-lookup"><span data-stu-id="c22c1-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="c22c1-172">Les applications UI Automation qui utilisent des GUID requièrent également le fichier d’en-tête Initguid. h.</span><span class="sxs-lookup"><span data-stu-id="c22c1-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="c22c1-173">Si nécessaire, Initguid. h doit être inclus avant UIAutomation. h.</span><span class="sxs-lookup"><span data-stu-id="c22c1-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="c22c1-174">Modèle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-174">UI Automation Model</span></span>

<span data-ttu-id="c22c1-175">UI Automation expose chaque élément de l’interface utilisateur aux applications clientes sous la forme d’un objet représenté par l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) .</span><span class="sxs-lookup"><span data-stu-id="c22c1-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="c22c1-176">Les éléments sont contenus dans une arborescence, avec le bureau comme élément racine.</span><span class="sxs-lookup"><span data-stu-id="c22c1-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="c22c1-177">Les clients peuvent filtrer l’affichage brut de l’arborescence sous la forme d’une vue de contrôle ou d’une vue de contenu.</span><span class="sxs-lookup"><span data-stu-id="c22c1-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="c22c1-178">Ces vues standard de la structure peuvent être consultées facilement à l’aide de l’application [Inspect](inspect-objects.md) qui est incluse dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c22c1-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="c22c1-179">Les applications peuvent également créer des vues personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c22c1-179">Applications can also create custom views.</span></span>

<span data-ttu-id="c22c1-180">Un élément UI Automation expose les propriétés du contrôle ou de l’élément d’interface qu’il représente.</span><span class="sxs-lookup"><span data-stu-id="c22c1-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="c22c1-181">L’une de ces propriétés est le type de contrôle, qui définit l’apparence et les fonctionnalités de base du contrôle ou de l’élément d’interface utilisateur sous la forme d’une entité reconnaissable unique, par exemple, un bouton ou une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="c22c1-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="c22c1-182">Pour plus d’informations sur les types de contrôle, consultez [UI Automation Control types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c22c1-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="c22c1-183">En outre, un élément UI Automation expose un ou plusieurs modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c22c1-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="c22c1-184">Un modèle de contrôle fournit un ensemble de propriétés spécifiques à un type de contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="c22c1-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="c22c1-185">Un modèle de contrôle expose également des méthodes qui permettent aux applications clientes d’obtenir plus d’informations sur l’élément et de fournir une entrée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="c22c1-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="c22c1-186">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c22c1-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="c22c1-187">Il n’existe pas de correspondance un-à-un entre les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c22c1-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="c22c1-188">Un modèle de contrôle peut être pris en charge par plusieurs types de contrôle, et un contrôle peut prendre en charge plusieurs modèles de contrôle, dont chacun expose différents aspects de son comportement.</span><span class="sxs-lookup"><span data-stu-id="c22c1-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="c22c1-189">Par exemple, une zone de liste déroulante possède au moins deux modèles de contrôle : un qui représente sa capacité de développement et de réduction, et l’autre qui représente le mécanisme de sélection.</span><span class="sxs-lookup"><span data-stu-id="c22c1-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="c22c1-190">Toutefois, un contrôle ne peut présenter qu’un seul type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c22c1-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="c22c1-191">UI Automation fournit des informations aux applications clientes via des événements.</span><span class="sxs-lookup"><span data-stu-id="c22c1-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="c22c1-192">Contrairement à WinEvents, les événements UI Automation ne sont pas basés sur un mécanisme de diffusion.</span><span class="sxs-lookup"><span data-stu-id="c22c1-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="c22c1-193">Les clients UI Automation s’inscrivent pour des notifications d’événements spécifiques et peuvent demander que des propriétés spécifiques et des informations de modèle de contrôle soient passées à leurs gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="c22c1-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="c22c1-194">En outre, un événement UI Automation contient une référence à l’élément qui l’a déclenché.</span><span class="sxs-lookup"><span data-stu-id="c22c1-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="c22c1-195">Les fournisseurs peuvent améliorer les performances en déclenchant des événements de manière sélective, selon que des clients les écoutent ou non.</span><span class="sxs-lookup"><span data-stu-id="c22c1-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="c22c1-196">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c22c1-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c22c1-197">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c22c1-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c22c1-198">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c22c1-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c22c1-199">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c22c1-200">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c22c1-201">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="c22c1-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





