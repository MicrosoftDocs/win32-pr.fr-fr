---
title: Vue d'ensemble des types de contrôle UI Automation
description: Les types de contrôle Microsoft UI Automation sont des propriétés qui servent d’identificateurs connus qui indiquent le type de contrôle représenté par un élément d’interface utilisateur particulier, tel qu’une zone de liste déroulante ou un bouton.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- UI Automation, vue d’ensemble des types de contrôle
- UI Automation, UIA_LocalizedControlTypePropertyId propriété
- types de contrôle, à propos de
- types de contrôle, conditions requises
- types de contrôle, conditions préalables
- types de contrôles, prédéfinis
- types de contrôles, propriété UIA_LocalizedControlTypePropertyId
- types de contrôles prédéfinis
- UIA_LocalizedControlTypePropertyId, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507938"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="d3f5d-112">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d3f5d-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="d3f5d-113">Les types de contrôle Microsoft UI Automation sont des propriétés qui servent d’identificateurs connus qui indiquent le type de contrôle représenté par un élément d’interface utilisateur particulier, tel qu’une zone de liste déroulante ou un bouton.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="d3f5d-114">Les applications clientes utilisent le type pour identifier les fonctionnalités d’un contrôle et pour déterminer comment interagir avec lui.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="d3f5d-115">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3f5d-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d3f5d-116">Conditions requises pour le type de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d3f5d-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="d3f5d-117">Propriété LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="d3f5d-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="d3f5d-118">Types de contrôle UI Automation actuels</span><span class="sxs-lookup"><span data-stu-id="d3f5d-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="d3f5d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3f5d-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="d3f5d-120">Conditions requises pour le type de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d3f5d-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="d3f5d-121">Chaque type de contrôle UI Automation possède un ensemble de conditions qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="d3f5d-122">Lorsqu’un fournisseur assigne un type de contrôle à un contrôle, le fournisseur doit s’assurer que le contrôle remplit toutes les conditions associées à ce type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="d3f5d-123">Les conditions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3f5d-123">The conditions include the following:</span></span>

-   <span data-ttu-id="d3f5d-124">Modèles de contrôle UI Automation : chaque type de contrôle a un ensemble de modèles de contrôle que le contrôle doit prendre en charge, un jeu facultatif et un ensemble que le contrôle ne doit pas prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="d3f5d-125">Valeurs de propriété UI Automation : chaque type de contrôle possède un jeu de propriétés que le contrôle doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="d3f5d-126">Événements UI Automation : chaque type de contrôle possède un jeu d’événements que le contrôle doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="d3f5d-127">Structure de l’arborescence UI Automation : chaque type de contrôle définit la façon dont le contrôle doit apparaître dans la structure de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="d3f5d-128">Lorsqu’un contrôle répond aux conditions d’un type de contrôle particulier, la valeur de la propriété [**IUIAutomationElement :: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (ou [**IUIAutomationElement :: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indique ce type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="d3f5d-129">Si votre contrôle ne répond pas aux spécifications d’un type de contrôle particulier, utilisez [**UIA \_ CUSTOMCONTROLTYPEID**](uiauto-controltype-ids.md) comme ID de type de contrôle et décrivez complètement le contrôle à l’aide des modèles de contrôle et des propriétés appropriés.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="d3f5d-130">Vous pouvez également définir la propriété [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) sur une chaîne qui décrit le mieux le type de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="d3f5d-131">Propriété LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="d3f5d-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="d3f5d-132">Si vous utilisez un type de contrôle prédéfini pour décrire votre contrôle, utilisez la valeur par défaut pour la propriété [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) et autoriser UI Automation à fournir une chaîne localisée pour que les fournisseurs exposent correctement.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="d3f5d-133">Si vous ne pouvez pas utiliser un type de contrôle prédéfini pour décrire votre contrôle, définissez la propriété **UIA \_ LocalizedControlTypePropertyId** sur une chaîne localisée qui décrit avec précision le type de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="d3f5d-134">La chaîne doit être concise, mais suffisamment précise qu’une technologie d’assistance comme un lecteur d’écran peut l’utiliser dans l’interface utilisateur pour informer l’utilisateur du type du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="d3f5d-135">Types de contrôle UI Automation actuels</span><span class="sxs-lookup"><span data-stu-id="d3f5d-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="d3f5d-136">Les rubriques suivantes décrivent les types de contrôle UI Automation.</span><span class="sxs-lookup"><span data-stu-id="d3f5d-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="d3f5d-137">Pour chaque type de contrôle, la description comprend l’ensemble de conditions qu’un contrôle du type donné doit prendre en charge :</span><span class="sxs-lookup"><span data-stu-id="d3f5d-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="d3f5d-138">Type de contrôle AppBar</span><span class="sxs-lookup"><span data-stu-id="d3f5d-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="d3f5d-139">Button (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="d3f5d-140">Calendar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="d3f5d-141">CheckBox (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="d3f5d-142">ComboBox (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="d3f5d-143">DataGrid (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="d3f5d-144">DataItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="d3f5d-145">Document (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="d3f5d-146">Modifier le type de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3f5d-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="d3f5d-147">Group (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="d3f5d-148">Header (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="d3f5d-149">Type de contrôle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="d3f5d-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="d3f5d-150">HYPERLINK (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="d3f5d-151">Image (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="d3f5d-152">List (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="d3f5d-153">ListItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-153">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="d3f5d-154">Menu (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="d3f5d-155">BarreMenus (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="d3f5d-156">MenuItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="d3f5d-157">Pane (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="d3f5d-158">ProgressBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="d3f5d-159">RadioButton (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="d3f5d-160">ScrollBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="d3f5d-161">Type de contrôle SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="d3f5d-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="d3f5d-162">Separator (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="d3f5d-163">Slider (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="d3f5d-164">Spinner (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="d3f5d-165">SplitButton (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="d3f5d-166">StatusBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="d3f5d-167">Tab (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="d3f5d-168">TabItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="d3f5d-169">Table (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="d3f5d-170">Text (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="d3f5d-171">Thumb (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="d3f5d-172">TitleBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="d3f5d-173">ToolBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="d3f5d-174">ToolTip (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="d3f5d-175">Tree (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="d3f5d-176">TreeItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="d3f5d-177">Window (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d3f5d-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="d3f5d-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3f5d-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d3f5d-179">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="d3f5d-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3f5d-180">Identificateurs de type de contrôle</span><span class="sxs-lookup"><span data-stu-id="d3f5d-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="d3f5d-181">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d3f5d-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d3f5d-182">Prise en charge des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d3f5d-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="d3f5d-183">Prise en charge d'UI Automation pour les contrôles standard</span><span class="sxs-lookup"><span data-stu-id="d3f5d-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="d3f5d-184">Notions de base d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="d3f5d-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 