---
title: Modèle de contrôle TextChild
description: Présente des recommandations et des conventions pour l’implémentation de ITextChildProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle TextChild est utilisé pour accéder à l’ancêtre le plus proche d’un élément qui prend en charge le modèle de contrôle Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- UI Automation, implémentation du modèle de contrôle TextChild
- UI Automation, modèle de contrôle TextChild
- UI Automation, ITextChildProvider
- ITextChildProvider
- implémentation des modèles de contrôle TextChild d’UI Automation
- Modèles de contrôle TextChild
- modèles de contrôle, ITextChildProvider
- modèles de contrôle, implémenter des TextChild UI Automation
- modèles de contrôle, TextChild
- interfaces, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729956"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="a6592-114">Modèle de contrôle TextChild</span><span class="sxs-lookup"><span data-stu-id="a6592-114">TextChild Control Pattern</span></span>

<span data-ttu-id="a6592-115">Présente des recommandations et des conventions pour l’implémentation de [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="a6592-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="a6592-116">Le modèle de contrôle **TextChild** est utilisé pour accéder à l’ancêtre le plus proche d’un élément qui prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="a6592-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="a6592-117">Supposons, par exemple, que le texte d’un document contient une image incorporée et un lien hypertexte, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="a6592-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![capture d’écran montrant du texte contenant une image incorporée et un lien hypertexte](images/textchild-pattern.png)

<span data-ttu-id="a6592-119">Si vous utilisez les outils d’automatisation d’interface utilisateur de Microsoft pour examiner l’arborescence UI Automation pour le contenu de ce document, il est possible qu’il affiche un élément de document avec un élément enfant qui représente l’image, et un autre élément enfant qui représente le lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="a6592-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="a6592-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a6592-120">For example:</span></span>

![capture d’écran montrant un exemple d’arborescence d’éléments UI Automation](images/textchild-pattern-tree.png)

<span data-ttu-id="a6592-122">En général, l’élément de document dans l’exemple précédent prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , mais pas les deux enfants de l’élément de document.</span><span class="sxs-lookup"><span data-stu-id="a6592-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="a6592-123">Si une application cliente UI Automation a une référence à l’élément image ou à l’élément Hyperlink, le client peut utiliser le modèle de contrôle **TextChild** comme un moyen pratique d’accéder au modèle TextControl exposé par l’élément de document conteneur.</span><span class="sxs-lookup"><span data-stu-id="a6592-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a6592-124">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="a6592-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a6592-125">Lorsque vous implémentez l’interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6592-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a6592-126">La propriété [**ITextChildProvider :: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) doit spécifier l’élément ancêtre le plus proche qui prend en charge l’interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , que les éléments situés plus haut dans la chaîne ancêtre prennent également en charge **ITextProvider**.</span><span class="sxs-lookup"><span data-stu-id="a6592-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="a6592-127">Un élément ne doit pas prendre en charge à la fois [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) et l’interface [ITextChildProvider \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="a6592-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="a6592-128">Un élément qui implémente [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) doit être un enfant ou un descendant d’un élément qui implémente [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span><span class="sxs-lookup"><span data-stu-id="a6592-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="a6592-129">Il n’est pas nécessaire que cet élément implémente également le [modèle de contrôle Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span><span class="sxs-lookup"><span data-stu-id="a6592-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="a6592-130">La propriété [**ITextChildProvider :: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) doit spécifier la même plage de texte que celle que l’élément de fournisseur de texte conteneur retourne lorsque sa fonction [**ITextProvider :: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) est appelée avec l’élément enfant Text en tant qu’élément enfant délimité.</span><span class="sxs-lookup"><span data-stu-id="a6592-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="a6592-131">Membres requis pour **ITextChildProvider**</span><span class="sxs-lookup"><span data-stu-id="a6592-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="a6592-132">Ces propriétés et méthodes sont requises pour implémenter l’interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="a6592-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="a6592-133">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="a6592-133">Required members</span></span>                                                     | <span data-ttu-id="a6592-134">Type de membre</span><span class="sxs-lookup"><span data-stu-id="a6592-134">Member type</span></span> | <span data-ttu-id="a6592-135">Notes</span><span class="sxs-lookup"><span data-stu-id="a6592-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a6592-136">**TextContainer**</span><span class="sxs-lookup"><span data-stu-id="a6592-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="a6592-137">Propriété</span><span class="sxs-lookup"><span data-stu-id="a6592-137">Property</span></span>    | <span data-ttu-id="a6592-138">Aucun</span><span class="sxs-lookup"><span data-stu-id="a6592-138">None</span></span>  |
| [<span data-ttu-id="a6592-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="a6592-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="a6592-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="a6592-140">Property</span></span>    | <span data-ttu-id="a6592-141">Aucun</span><span class="sxs-lookup"><span data-stu-id="a6592-141">None</span></span>  |



 

<span data-ttu-id="a6592-142">Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.</span><span class="sxs-lookup"><span data-stu-id="a6592-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6592-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6592-143">Related topics</span></span>

<span data-ttu-id="a6592-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a6592-144">**Conceptual**</span></span>

- [<span data-ttu-id="a6592-145">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6592-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="a6592-146">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="a6592-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="a6592-147">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="a6592-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)