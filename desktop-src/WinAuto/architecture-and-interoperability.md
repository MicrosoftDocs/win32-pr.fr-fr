---
title: Architecture et interopérabilité
description: Cette rubrique décrit brièvement l’architecture de Microsoft Active Accessibility et Microsoft UI Automation, ainsi que les composants qui permettent l’interopérabilité entre les applications basées sur les deux technologies différentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104101185"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="07ad1-103">Architecture et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="07ad1-103">Architecture and Interoperability</span></span>

<span data-ttu-id="07ad1-104">Cette rubrique décrit brièvement l’architecture de Microsoft Active Accessibility et Microsoft UI Automation, ainsi que les composants qui permettent l’interopérabilité entre les applications basées sur les deux technologies différentes.</span><span class="sxs-lookup"><span data-stu-id="07ad1-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="07ad1-105">Pour plus d’informations sur l’interopérabilité entre Microsoft Active Accessibility et UI Automation, consultez [infrastructure commune](common-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="07ad1-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="07ad1-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="07ad1-107">Architecture de Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="07ad1-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="07ad1-108">Architecture d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="07ad1-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="07ad1-109">Interopérabilité entre Microsoft Active Accessibility et UI Automation</span><span class="sxs-lookup"><span data-stu-id="07ad1-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="07ad1-110">Interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="07ad1-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="07ad1-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07ad1-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="07ad1-112">Architecture de Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="07ad1-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="07ad1-113">Microsoft Active Accessibility expose des informations de base sur les contrôles tels que le nom du contrôle, l’emplacement à l’écran et le type de contrôle, ainsi que des informations d’État telles que la visibilité et l’état activé/désactivé.</span><span class="sxs-lookup"><span data-stu-id="07ad1-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="07ad1-114">L’interface utilisateur est représentée sous la forme d’une hiérarchie d’objets accessibles. les modifications et les actions sont représentées en tant que WinEvents.</span><span class="sxs-lookup"><span data-stu-id="07ad1-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="07ad1-115">Microsoft Active Accessibility comprend les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="07ad1-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="07ad1-116">Objet accessible : élément d’interface utilisateur logique (tel qu’un bouton) qui est représenté par une interface COM (Component Object Model) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un identificateur enfant entier (childID).</span><span class="sxs-lookup"><span data-stu-id="07ad1-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="07ad1-117">WinEvents : système d’événements qui permet aux serveurs de notifier les clients lorsqu’un objet accessible change.</span><span class="sxs-lookup"><span data-stu-id="07ad1-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="07ad1-118">Pour plus d’informations, consultez [winEvents](winevents-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="07ad1-119">OLEACC.dll : la bibliothèque de liens dynamiques au moment de l’exécution qui fournit l’API Microsoft Active Accessibility et l’infrastructure du système d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="07ad1-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="07ad1-120">OLEACC implémente les objets proxy qui fournissent des informations d’accessibilité par défaut pour les éléments d’interface utilisateur standard, y compris les contrôles utilisateur, les menus utilisateur et les contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="07ad1-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="07ad1-121">Pour Microsoft Active Accessibility, le composant système de l’infrastructure d’accessibilité (OLEACC) permet la communication entre les technologies d’assistance (outils d’accessibilité) et les applications, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="07ad1-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![Illustration montrant comment les outils d’accessibilité interagissent avec les applications](images/msaaarch.gif)

<span data-ttu-id="07ad1-123">Les applications (serveurs Microsoft Active Accessibility) fournissent des informations d’accessibilité de l’interface utilisateur aux outils (clients Microsoft Active Accessibility), qui interagissent avec l’interface utilisateur pour le compte des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07ad1-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="07ad1-124">La limite de code est à la fois une limite de programmation et de processus.</span><span class="sxs-lookup"><span data-stu-id="07ad1-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="07ad1-125">Architecture d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="07ad1-125">UI Automation Architecture</span></span>

<span data-ttu-id="07ad1-126">Avec UI Automation, le composant principal d’UI Automation (UIAutomationCore.dll) est chargé à la fois dans les processus des outils d’accessibilité et des applications.</span><span class="sxs-lookup"><span data-stu-id="07ad1-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="07ad1-127">Le composant principal gère la communication entre processus, fournit des services de niveau supérieur tels que la recherche d’éléments par valeurs de propriété, et active l’extraction ou la mise en cache en bloc des propriétés, ce qui offre de meilleures performances que l’implémentation de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="07ad1-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="07ad1-128">UI Automation comprend des objets proxy qui fournissent des informations sur l’interface utilisateur sur les éléments d’interface utilisateur standard, tels que les contrôles utilisateur, les menus utilisateur et les contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="07ad1-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="07ad1-129">Il comprend également des proxies qui permettent aux clients UI Automation d’accéder aux informations de l’interface utilisateur auprès des serveurs Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="07ad1-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="07ad1-130">L’illustration suivante montre les relations entre les différents compontents d’automatisation d’interface utilisateur utilisés dans les outils d’accessibilité (clients) et dans les applications (fournisseurs).</span><span class="sxs-lookup"><span data-stu-id="07ad1-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![Illustration montrant comment les composants des outils d’accessibilité interagissent avec ceux des applications](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="07ad1-132">Interopérabilité entre Microsoft Active Accessibility et UI Automation</span><span class="sxs-lookup"><span data-stu-id="07ad1-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="07ad1-133">L’automatisation de l’interface utilisateur de Microsoft Active Accessibility Bridge permet aux clients Microsoft Active Accessibility d’accéder aux fournisseurs UI Automation en convertissant le modèle objet UI Automation en modèle objet Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="07ad1-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="07ad1-134">L’illustration suivante montre le rôle du pont UI Automation-à-Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="07ad1-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![illustration illustrant le fonctionnement d’UI Automation avec les outils et applications d’accessibilité](images/uiatomsaabridge.gif)

<span data-ttu-id="07ad1-136">De même, le proxy d’automatisation Microsoft Active Accessibility-to-UI traduit les modèles d’objet serveur basés sur Microsoft Active Accessibility pour les clients UI Automation.</span><span class="sxs-lookup"><span data-stu-id="07ad1-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="07ad1-137">L’illustration suivante montre le rôle du proxy Automation de Microsoft Active Accessibility à UI.</span><span class="sxs-lookup"><span data-stu-id="07ad1-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![illustration illustrant le fonctionnement du proxy UI Automation avec les outils et applications d’accessibilité](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="07ad1-139">Interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="07ad1-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="07ad1-140">L’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permet aux applications ou bibliothèques d’interface utilisateur existantes d’étendre leur modèle objet Microsoft Active Accessibility pour prendre en charge l’Automation d’interface utilisateur sans réécrire l’implémentation de zéro.</span><span class="sxs-lookup"><span data-stu-id="07ad1-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="07ad1-141">Avec **IAccessibleEx**, vous pouvez implémenter uniquement les propriétés UI Automation supplémentaires et les modèles de contrôle nécessaires pour décrire entièrement l’interface utilisateur et ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="07ad1-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="07ad1-142">Étant donné que le proxy Automation de Microsoft Active Accessibility à l’interface utilisateur traduit les modèles objet des serveurs Microsoft Active Accessibility compatibles avec [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)en tant que modèles objet UI Automation, les clients UI Automation n’ont pas besoin d’effectuer d’autres tâches.</span><span class="sxs-lookup"><span data-stu-id="07ad1-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="07ad1-143">L’interface **IAccessibleEx** peut également permettre aux clients Microsoft Active Accessibilitys in-process d’interagir directement avec les fournisseurs UI Automation.</span><span class="sxs-lookup"><span data-stu-id="07ad1-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="07ad1-144">Pour plus d’informations, consultez [l’interface IAccessibleEx](iaccessibleex.md).</span><span class="sxs-lookup"><span data-stu-id="07ad1-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07ad1-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07ad1-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07ad1-146">Vue d’ensemble de l’API Windows Automation</span><span class="sxs-lookup"><span data-stu-id="07ad1-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="07ad1-147">Interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="07ad1-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="07ad1-148">Considérations relatives à la sécurité pour les technologies d’assistance</span><span class="sxs-lookup"><span data-stu-id="07ad1-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




