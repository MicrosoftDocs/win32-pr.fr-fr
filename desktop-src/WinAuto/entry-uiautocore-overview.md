---
title: Notions de base d'UI Automation
description: Cette section décrit les concepts fondamentaux sur lesquels l’automatisation d’interface utilisateur est basée.
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- UI Automation, API Microsoft Win32
- UI Automation, API Win32
- UI Automation, fournisseurs
- UI Automation, applications clientes
- clients, Microsoft UI Automation pour Microsoft Win32 API
- clients, UI Automation pour l’API Microsoft Win32
- API Win32
- API Microsoft Win32
- UI Automation pour l’API Microsoft Win32
- API Microsoft UI Automation pour Microsoft Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380158"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="81b0b-113">Notions de base d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="81b0b-114">Microsoft UI Automation permet aux applications de technologie d’assistance et aux outils de test automatisés d’interagir avec les contrôles d’interface utilisateur d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="81b0b-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="81b0b-115">Cette section décrit les concepts fondamentaux sur lesquels l’automatisation d’interface utilisateur est basée.</span><span class="sxs-lookup"><span data-stu-id="81b0b-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="81b0b-116">L’API UI Automation est en deux parties.</span><span class="sxs-lookup"><span data-stu-id="81b0b-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="81b0b-117">Une partie est utilisée par les applications du *fournisseur UI Automation* , tandis que l’autre est utilisée par les applications *clientes UI Automation* .</span><span class="sxs-lookup"><span data-stu-id="81b0b-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="81b0b-118">L’API du fournisseur permet aux développeurs de contrôles personnalisés Microsoft Win32 et d’autres infrastructures de contrôle d’exposer ces contrôles à UI Automation et de les rendre visibles aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="81b0b-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="81b0b-119">L’API client permet aux applications d’interagir avec les contrôles dans d’autres applications et de récupérer des informations à leur sujet.</span><span class="sxs-lookup"><span data-stu-id="81b0b-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="81b0b-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="81b0b-120">In this section</span></span>

-   [<span data-ttu-id="81b0b-121">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="81b0b-122">UI Automation et Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="81b0b-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="81b0b-123">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="81b0b-124">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="81b0b-125">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="81b0b-126">Vue d'ensemble des propriétés UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="81b0b-127">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="81b0b-128">Propriétés personnalisées, événements et modèles de contrôle</span><span class="sxs-lookup"><span data-stu-id="81b0b-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="81b0b-129">Prise en charge d’UI Automation pour le contenu textuel</span><span class="sxs-lookup"><span data-stu-id="81b0b-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="81b0b-130">Prise en charge d’UI Automation pour le glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="81b0b-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="81b0b-131">Considérations relatives à la sécurité pour les technologies d’assistance</span><span class="sxs-lookup"><span data-stu-id="81b0b-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="81b0b-132">Meilleures pratiques pour l’utilisation de groupes sécurisés</span><span class="sxs-lookup"><span data-stu-id="81b0b-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="81b0b-133">Spécification UI Automation et promesse communautaire</span><span class="sxs-lookup"><span data-stu-id="81b0b-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="81b0b-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81b0b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81b0b-135">UI Automation</span><span class="sxs-lookup"><span data-stu-id="81b0b-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




