---
title: Élément MenuGroup
description: Représente un conteneur de contrôles à afficher dans une galerie, un menu ou une barre d’outils.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Ruban des fenêtres d’élément MenuGroup
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103680830"
---
# <a name="menugroup-element"></a><span data-ttu-id="edacf-104">Élément MenuGroup</span><span class="sxs-lookup"><span data-stu-id="edacf-104">MenuGroup element</span></span>

<span data-ttu-id="edacf-105">Représente un conteneur de contrôles à afficher dans une galerie, un menu ou une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="edacf-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="edacf-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="edacf-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="edacf-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="edacf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edacf-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="edacf-108">Attribute</span></span></th>
<th><span data-ttu-id="edacf-109">Type</span><span class="sxs-lookup"><span data-stu-id="edacf-109">Type</span></span></th>
<th><span data-ttu-id="edacf-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="edacf-110">Required</span></span></th>
<th><span data-ttu-id="edacf-111">Description</span><span class="sxs-lookup"><span data-stu-id="edacf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edacf-112"><strong>Classe</strong></span><span class="sxs-lookup"><span data-stu-id="edacf-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="edacf-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="edacf-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="edacf-114">Non</span><span class="sxs-lookup"><span data-stu-id="edacf-114">No</span></span><br/></td>
<td><span data-ttu-id="edacf-115">Spécifie la taille et le style de disposition des éléments dans l’interface utilisateur du menu.</span><span class="sxs-lookup"><span data-stu-id="edacf-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="edacf-116">Une ressource d’image peut être fournie en deux tailles (grande et petite) et associée à l’élément dans le balisage à l’aide des éléments de propriété <a href="windowsribbon-element-command-largeimages.md"><strong>Command. LargeImages</strong></a> et <a href="windowsribbon-element-command-smallimages.md"><strong>Command. SmallImages</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="edacf-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="edacf-117">Si une seule image est fournie, l’infrastructure la redimensionne si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="edacf-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="edacf-118">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="edacf-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="edacf-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span><span class="sxs-lookup"><span data-stu-id="edacf-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="edacf-120">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="edacf-120">Default.</span></span> <br/> <span data-ttu-id="edacf-121">Style : petites images et texte en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="edacf-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="edacf-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span><span class="sxs-lookup"><span data-stu-id="edacf-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="edacf-123">Style : grande image et texte en gras.</span><span class="sxs-lookup"><span data-stu-id="edacf-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="edacf-124">Si <strong>MenuGroup</strong> est un enfant de <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, l’attribut de <em>classe</em> est ignoré et un style <code>MajorItems</code> est appliqué par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="edacf-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edacf-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="edacf-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="edacf-126">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="edacf-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="edacf-127">Non</span><span class="sxs-lookup"><span data-stu-id="edacf-127">No</span></span><br/></td>
<td><span data-ttu-id="edacf-128">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="edacf-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="edacf-129">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="edacf-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="edacf-130">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="edacf-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="edacf-131">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="edacf-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="edacf-132">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="edacf-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="edacf-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="edacf-133">Child elements</span></span>



| <span data-ttu-id="edacf-134">Élément</span><span class="sxs-lookup"><span data-stu-id="edacf-134">Element</span></span>                                                                             | <span data-ttu-id="edacf-135">Description</span><span class="sxs-lookup"><span data-stu-id="edacf-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="edacf-136">**Button**</span><span class="sxs-lookup"><span data-stu-id="edacf-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="edacf-137">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-138">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="edacf-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="edacf-139">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="edacf-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="edacf-141">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="edacf-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="edacf-143">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-144">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="edacf-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="edacf-145">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-146">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="edacf-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="edacf-147">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-148">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="edacf-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="edacf-149">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="edacf-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="edacf-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="edacf-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="edacf-151">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-152">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="edacf-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="edacf-153">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="edacf-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="edacf-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="edacf-155">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="edacf-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="edacf-156">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="edacf-156">Parent elements</span></span>



| <span data-ttu-id="edacf-157">Élément</span><span class="sxs-lookup"><span data-stu-id="edacf-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edacf-158">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="edacf-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="edacf-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="edacf-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="edacf-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="edacf-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="edacf-161">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="edacf-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="edacf-162">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="edacf-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="edacf-163">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="edacf-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="edacf-164">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="edacf-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="edacf-165">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="edacf-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="edacf-166">Notes</span><span class="sxs-lookup"><span data-stu-id="edacf-166">Remarks</span></span>

<span data-ttu-id="edacf-167">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="edacf-167">Required.</span></span>

<span data-ttu-id="edacf-168">Doit se produire au moins une fois pour chaque élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)ou [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) .</span><span class="sxs-lookup"><span data-stu-id="edacf-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="edacf-169">Si [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) est l’élément parent, **MenuGroup** est soumis aux éléments enfants suivants : [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="edacf-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="edacf-170">Si [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)ou [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) est l’élément parent, **MenuGroup** est alors soumis aux éléments enfants suivants : [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="edacf-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="edacf-171">Si [**MiniToolbar**](windowsribbon-element-minitoolbar.md) est l’élément parent, **MenuGroup** est soumis aux éléments enfants suivants : [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="edacf-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="edacf-172">L’attribut Class n’est pas requis quand [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="edacf-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="edacf-173">L’infrastructure applique une valeur de MajorItems pour l’attribut de classe.</span><span class="sxs-lookup"><span data-stu-id="edacf-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="edacf-174">Lorsque [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) est l’élément parent, l’attribut de classe n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="edacf-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="edacf-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="edacf-175">Examples</span></span>

<span data-ttu-id="edacf-176">L’exemple suivant illustre le balisage de base pour le [**SplitButton**](windowsribbon-element-splitbutton.md) avec un élément **MenuGroup** .</span><span class="sxs-lookup"><span data-stu-id="edacf-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="edacf-177">Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et **MenuGroup** avec une grande ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="edacf-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="edacf-178">Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.</span><span class="sxs-lookup"><span data-stu-id="edacf-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="edacf-179">Cette section de code montre les déclarations de contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) et **MenuGroup** avec `StandardItems` et `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="edacf-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="edacf-180">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="edacf-180">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="edacf-181">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edacf-181">Minimum supported system</span></span><br/> | <span data-ttu-id="edacf-182">Windows 7</span><span class="sxs-lookup"><span data-stu-id="edacf-182">Windows 7</span></span> |
| <span data-ttu-id="edacf-183">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="edacf-183">Can be empty</span></span>                        | <span data-ttu-id="edacf-184">Non</span><span class="sxs-lookup"><span data-stu-id="edacf-184">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="edacf-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edacf-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edacf-186">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="edacf-186">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="edacf-187">Groupe de menus</span><span class="sxs-lookup"><span data-stu-id="edacf-187">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





