---
title: Attributs de texte UI Automation
description: Cette rubrique décrit comment Microsoft UI Automation expose les propriétés de mise en forme et de style (attributs de texte) du contenu textuel et fournit une liste d’attributs de texte pris en charge.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- UI Automation, attributs de texte
- attributs de texte, à propos de
- attributs de texte, types variant
- attributs de texte, types de données
- UI Automation, liste d’attributs
- UI Automation, liste des attributs de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510692"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="34a19-109">Attributs de texte UI Automation</span><span class="sxs-lookup"><span data-stu-id="34a19-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="34a19-110">Cette rubrique décrit comment Microsoft UI Automation expose les propriétés de mise en forme et de style (*attributs de texte*) du contenu textuel et fournit une liste d’attributs de texte pris en charge.</span><span class="sxs-lookup"><span data-stu-id="34a19-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="34a19-111">Les fournisseurs UI Automation exposent des attributs de texte par le biais des méthodes [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) et [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) du modèle de contrôle [TextRange](uiauto-about-text-and-textrange-patterns.md) .</span><span class="sxs-lookup"><span data-stu-id="34a19-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="34a19-112">Les applications clientes utilisent la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) pour récupérer la valeur d’un attribut de texte particulier pour une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="34a19-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="34a19-113">Les clients peuvent utiliser la méthode [**IUIAutomationTextRange :: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) pour rechercher dans une plage de texte un texte ayant un attribut particulier.</span><span class="sxs-lookup"><span data-stu-id="34a19-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="34a19-114">Si un texte correspondant est trouvé, la méthode crée une nouvelle plage de texte qui contient le texte correspondant.</span><span class="sxs-lookup"><span data-stu-id="34a19-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="34a19-115">Les attributs de texte de la liste suivante sont pris en charge par le modèle de contrôle **TextRange** .</span><span class="sxs-lookup"><span data-stu-id="34a19-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="34a19-116">Les noms d’attributs sont dérivés des identificateurs d’attribut de texte UI Automation.</span><span class="sxs-lookup"><span data-stu-id="34a19-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="34a19-117">Par exemple, l’attribut **AnimationStyle** est identifié par les clients en tant que [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (défini dans UIAutomationClient. h) et par les fournisseurs comme **texte \_ \_ \_ GUID d’attribut AnimationStyle** (défini dans Uiautomationcoreapi. h).</span><span class="sxs-lookup"><span data-stu-id="34a19-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="34a19-118">Pour plus d’informations sur chaque attribut de texte pris en charge, consultez [**identificateurs d’attribut de texte**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="34a19-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="34a19-119">Certains des attributs répertoriés sont pris en charge à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="34a19-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="34a19-120">Consultez [**identificateurs d’attribut de texte**](uiauto-textattribute-ids.md) pour les notes relatives à la prise en charge des versions.</span><span class="sxs-lookup"><span data-stu-id="34a19-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="34a19-121">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="34a19-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="34a19-122">Attributs d'annotation</span><span class="sxs-lookup"><span data-stu-id="34a19-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="34a19-123">Attributs de police</span><span class="sxs-lookup"><span data-stu-id="34a19-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="34a19-124">Attributs de langage</span><span class="sxs-lookup"><span data-stu-id="34a19-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="34a19-125">Attribut de lien</span><span class="sxs-lookup"><span data-stu-id="34a19-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="34a19-126">Attributs de marge de page</span><span class="sxs-lookup"><span data-stu-id="34a19-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="34a19-127">Attributs d’alignement de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="34a19-128">Attributs de couleur de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="34a19-129">Attributs de décoration de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="34a19-130">Attributs de style de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="34a19-131">Attributs d’interaction et de sélection</span><span class="sxs-lookup"><span data-stu-id="34a19-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="34a19-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34a19-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="34a19-133">Attributs d'annotation</span><span class="sxs-lookup"><span data-stu-id="34a19-133">Annotation Attributes</span></span>

<span data-ttu-id="34a19-134">Les objets d’annotation et les types d’annotation sont disponibles par le biais des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="34a19-135">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-135">Attribute</span></span>             | <span data-ttu-id="34a19-136">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="34a19-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="34a19-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="34a19-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="34a19-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="34a19-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="34a19-141">Attributs de police</span><span class="sxs-lookup"><span data-stu-id="34a19-141">Font Attributes</span></span>

<span data-ttu-id="34a19-142">Le nom, la taille et le poids d’une police sont disponibles par le biais des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="34a19-143">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-143">Attribute</span></span>      | <span data-ttu-id="34a19-144">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="34a19-145">**FontName**</span></span>   | [<span data-ttu-id="34a19-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="34a19-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="34a19-147">**FontSize**</span></span>   | [<span data-ttu-id="34a19-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="34a19-149">**FontWeight**</span><span class="sxs-lookup"><span data-stu-id="34a19-149">**FontWeight**</span></span> | [<span data-ttu-id="34a19-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="34a19-151">Attributs de langage</span><span class="sxs-lookup"><span data-stu-id="34a19-151">Language Attributes</span></span>

<span data-ttu-id="34a19-152">Les informations relatives à la langue du texte sont disponibles par le biais des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="34a19-153">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-153">Attribute</span></span>              | <span data-ttu-id="34a19-154">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-155">**Culturel**</span><span class="sxs-lookup"><span data-stu-id="34a19-155">**Culture**</span></span>            | [<span data-ttu-id="34a19-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="34a19-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="34a19-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="34a19-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="34a19-159">Attribut de lien</span><span class="sxs-lookup"><span data-stu-id="34a19-159">Link Attribute</span></span>

<span data-ttu-id="34a19-160">L’attribut suivant fournit la plage de texte qui est la cible d’un lien dans un document.</span><span class="sxs-lookup"><span data-stu-id="34a19-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="34a19-161">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-161">Attribute</span></span> | <span data-ttu-id="34a19-162">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-163">**Lien**</span><span class="sxs-lookup"><span data-stu-id="34a19-163">**Link**</span></span>  | [<span data-ttu-id="34a19-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="34a19-165">Attributs de marge de page</span><span class="sxs-lookup"><span data-stu-id="34a19-165">Page Margin Attributes</span></span>

<span data-ttu-id="34a19-166">Les rectangles englobants d’une plage de texte n’exposent pas les coordonnées du texte dans la page.</span><span class="sxs-lookup"><span data-stu-id="34a19-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="34a19-167">Toutefois, un fournisseur peut exposer les informations sur les marges de page à l’aide des attributs de texte suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="34a19-168">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-168">Attribute</span></span>          | <span data-ttu-id="34a19-169">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="34a19-170">**MarginBottom**</span></span>   | [<span data-ttu-id="34a19-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="34a19-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="34a19-172">**MarginLeading**</span></span>  | [<span data-ttu-id="34a19-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="34a19-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="34a19-174">**MarginTop**</span></span>      | [<span data-ttu-id="34a19-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="34a19-176">**MarginTrailing**</span></span> | [<span data-ttu-id="34a19-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="34a19-178">Attributs d’alignement de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-178">Text Alignment Attributes</span></span>

<span data-ttu-id="34a19-179">Les informations relatives à l’alignement du texte, telles que la mise en retrait, les paramètres d’onglet et l’alignement horizontal, sont disponibles par le biais des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="34a19-180">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-180">Attribute</span></span>                   | <span data-ttu-id="34a19-181">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="34a19-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="34a19-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="34a19-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="34a19-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="34a19-186">**IndentationLeading**</span><span class="sxs-lookup"><span data-stu-id="34a19-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="34a19-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-188">**IndentationTrailing**</span><span class="sxs-lookup"><span data-stu-id="34a19-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="34a19-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="34a19-190">**Tabulations**</span><span class="sxs-lookup"><span data-stu-id="34a19-190">**Tabs**</span></span>                    | [<span data-ttu-id="34a19-191">**UIA \_ TabsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="34a19-192">Attributs de couleur de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-192">Text Color Attributes</span></span>

<span data-ttu-id="34a19-193">Les couleurs de texte de premier plan et d’arrière-plan sont disponibles via les attributs de texte suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="34a19-194">Les deux couleurs sont spécifiées en tant que type de données [**COLORREF**](/windows/desktop/gdi/colorref) .</span><span class="sxs-lookup"><span data-stu-id="34a19-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="34a19-195">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-195">Attribute</span></span>           | <span data-ttu-id="34a19-196">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="34a19-197">**BackgroundColor**</span></span> | [<span data-ttu-id="34a19-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="34a19-199">**ForegroundColor**</span></span> | [<span data-ttu-id="34a19-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="34a19-201">Attributs de décoration de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-201">Text Decoration Attributes</span></span>

<span data-ttu-id="34a19-202">Les décorations de texte incluent des zones telles que les puces, le soulignement et les animations.</span><span class="sxs-lookup"><span data-stu-id="34a19-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="34a19-203">Si le texte inclut des puces ou des nombres de début, le symbole ou le texte utilisé pour la puce ou le numéro doit être inclus dans le flux de texte, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="34a19-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="34a19-204">Des informations sur les décorations de texte sont disponibles par le biais des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="34a19-205">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-205">Attribute</span></span>              | <span data-ttu-id="34a19-206">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="34a19-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="34a19-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="34a19-209">**BulletStyle**</span><span class="sxs-lookup"><span data-stu-id="34a19-209">**BulletStyle**</span></span>        | [<span data-ttu-id="34a19-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="34a19-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="34a19-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="34a19-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="34a19-213">**OverlineColor**</span></span>      | [<span data-ttu-id="34a19-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="34a19-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="34a19-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="34a19-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="34a19-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="34a19-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="34a19-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="34a19-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="34a19-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="34a19-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="34a19-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="34a19-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="34a19-225">Attributs de style de texte</span><span class="sxs-lookup"><span data-stu-id="34a19-225">Text Style Attributes</span></span>

<span data-ttu-id="34a19-226">Des informations sur les styles de texte sont disponibles via les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="34a19-227">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-227">Attribute</span></span>         | <span data-ttu-id="34a19-228">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="34a19-229">**CapStyle**</span></span>      | [<span data-ttu-id="34a19-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="34a19-231">**IsHidden**</span></span>      | [<span data-ttu-id="34a19-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="34a19-233">**IsItalic**</span></span>      | [<span data-ttu-id="34a19-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="34a19-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="34a19-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="34a19-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="34a19-237">**IsSuperscript**</span></span> | [<span data-ttu-id="34a19-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="34a19-239">**IsSubscript**</span></span>   | [<span data-ttu-id="34a19-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="34a19-241">Attributs d’interaction et de sélection</span><span class="sxs-lookup"><span data-stu-id="34a19-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="34a19-242">Les informations relatives à la sélection de texte en cours dans la plage et l’état du focus sont disponibles via les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="34a19-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="34a19-243">Attribut</span><span class="sxs-lookup"><span data-stu-id="34a19-243">Attribute</span></span>              | <span data-ttu-id="34a19-244">Identificateur</span><span class="sxs-lookup"><span data-stu-id="34a19-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a19-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="34a19-245">**IsActive**</span></span>           | [<span data-ttu-id="34a19-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="34a19-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="34a19-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="34a19-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="34a19-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="34a19-249">**CaretPosition**</span></span>      | [<span data-ttu-id="34a19-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="34a19-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="34a19-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="34a19-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="34a19-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="34a19-253">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34a19-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="34a19-254">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="34a19-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="34a19-255">À propos du texte UI Automation et des modèles de contrôle TextRange</span><span class="sxs-lookup"><span data-stu-id="34a19-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="34a19-256">Modèles de contrôle Text et TextRange</span><span class="sxs-lookup"><span data-stu-id="34a19-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="34a19-257">Utilisation de contrôles textuels</span><span class="sxs-lookup"><span data-stu-id="34a19-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 