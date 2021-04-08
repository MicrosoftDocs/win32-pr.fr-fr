---
title: Fonctionnement du modèle d’objet de texte UI Automation
description: Cette rubrique décrit comment les applications clientes UI Automation Microsoft accèdent au contenu textuel d’un contrôle textuel.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clients, fonctionnement du modèle d’objet de texte UI Automation
- clients, contrôles textuels
- clients, plages de texte
- clients, modèle de contrôle de texte
- clients, modèle de contrôle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672426"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="303d1-108">Fonctionnement du modèle d’objet de texte UI Automation</span><span class="sxs-lookup"><span data-stu-id="303d1-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="303d1-109">Cette rubrique décrit comment les applications clientes UI Automation Microsoft accèdent au contenu textuel d’un contrôle textuel.</span><span class="sxs-lookup"><span data-stu-id="303d1-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="303d1-110">Modèle d’objet spécifique au contrôle</span><span class="sxs-lookup"><span data-stu-id="303d1-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="303d1-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="303d1-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="303d1-112">Les contrôles textuels exposent du contenu textuel aux applications clientes UI Automation via un modèle d’objet de texte simple.</span><span class="sxs-lookup"><span data-stu-id="303d1-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="303d1-113">Les applications clientes ont accès au modèle d’objet de texte par le biais des interfaces de modèle de contrôle [Text et TextRange](uiauto-about-text-and-textrange-patterns.md) , notamment [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) et [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span><span class="sxs-lookup"><span data-stu-id="303d1-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="303d1-114">Les applications clientes peuvent utiliser ces interfaces pour récupérer du contenu textuel, des attributs de texte et des objets incorporés, tels que des tables et des liens hypertexte à partir de contrôles textuels.</span><span class="sxs-lookup"><span data-stu-id="303d1-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="303d1-115">Les types de contrôle qui prennent en charge le modèle d’objet de texte UI Automation incluent les types de contrôle de [modification](uiauto-supporteditcontroltype.md) et de [document](uiauto-supportdocumentcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="303d1-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="303d1-116">D’autres types de contrôle comme [info-bulle](uiauto-supporttooltipcontroltype.md) et [texte](uiauto-supporttextcontroltype.md) peuvent également prendre en charge le modèle d’objet de texte, mais ils ne sont pas requis pour.</span><span class="sxs-lookup"><span data-stu-id="303d1-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="303d1-117">Le modèle d’objet de texte UI Automation n’offre aucun moyen d’insérer ou de modifier du texte.</span><span class="sxs-lookup"><span data-stu-id="303d1-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="303d1-118">Toutefois, certains contrôles permettent l’insertion ou la modification de texte par le biais de l’interface [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) , ou via une entrée directe au clavier.</span><span class="sxs-lookup"><span data-stu-id="303d1-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="303d1-119">Modèle d’objet spécifique au contrôle</span><span class="sxs-lookup"><span data-stu-id="303d1-119">Control-specific Object Model</span></span>

<span data-ttu-id="303d1-120">Un contrôle basé sur du texte qui implémente son propre Document Object Model (DOM) peut exposer le DOM en implémentant le modèle de contrôle [ObjectModel](uiauto-implementingobjectmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="303d1-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="303d1-121">L’exposition du DOM peut permettre aux applications clientes d’accéder plus ou plus au contenu d’un contrôle textuel.</span><span class="sxs-lookup"><span data-stu-id="303d1-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="303d1-122">Une application cliente peut découvrir si un contrôle textuel particulier implémente un DOM en extrayant l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) du contrôle.</span><span class="sxs-lookup"><span data-stu-id="303d1-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="303d1-123">Ensuite, appelez la méthode [**IUIAutomationElement :: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , en spécifiant l’identificateur de propriété [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) et un variant qui reçoit la valeur true si le contrôle implémente un DOM.</span><span class="sxs-lookup"><span data-stu-id="303d1-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="303d1-124">Pour accéder au DOM, appelez la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , en spécifiant l’identificateur de modèle de contrôle [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) et une variable qui reçoit l’interface [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) .</span><span class="sxs-lookup"><span data-stu-id="303d1-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="303d1-125">Appelez la méthode [**IUIAutomationObjectModelPattern :: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) pour récupérer l’interface DOM.</span><span class="sxs-lookup"><span data-stu-id="303d1-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="303d1-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="303d1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="303d1-127">Modèles de contrôle Text et TextRange</span><span class="sxs-lookup"><span data-stu-id="303d1-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="303d1-128">Prise en charge d’UI Automation pour le contenu textuel</span><span class="sxs-lookup"><span data-stu-id="303d1-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="303d1-129">Utilisation de contrôles textuels</span><span class="sxs-lookup"><span data-stu-id="303d1-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




