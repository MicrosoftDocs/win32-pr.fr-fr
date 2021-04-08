---
title: Élément DropDownButton
description: Représente un contrôle de bouton de Drop-Down standard.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Ruban des fenêtres d’élément DropDownButton
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729221"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="f9b07-104">Élément DropDownButton</span><span class="sxs-lookup"><span data-stu-id="f9b07-104">DropDownButton element</span></span>

<span data-ttu-id="f9b07-105">Représente un contrôle de [bouton](windowsribbon-controls-dropdownbutton.md) déroulant standard.</span><span class="sxs-lookup"><span data-stu-id="f9b07-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="f9b07-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f9b07-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="f9b07-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="f9b07-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9b07-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="f9b07-108">Attribute</span></span></th>
<th><span data-ttu-id="f9b07-109">Type</span><span class="sxs-lookup"><span data-stu-id="f9b07-109">Type</span></span></th>
<th><span data-ttu-id="f9b07-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9b07-110">Required</span></span></th>
<th><span data-ttu-id="f9b07-111">Description</span><span class="sxs-lookup"><span data-stu-id="f9b07-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9b07-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="f9b07-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="f9b07-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="f9b07-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="f9b07-114">Non</span><span class="sxs-lookup"><span data-stu-id="f9b07-114">No</span></span><br/></td>
<td><span data-ttu-id="f9b07-115">Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="f9b07-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="f9b07-116">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="f9b07-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f9b07-117">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="f9b07-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="f9b07-118">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="f9b07-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="f9b07-119">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="f9b07-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b07-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f9b07-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f9b07-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="f9b07-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f9b07-122">Non</span><span class="sxs-lookup"><span data-stu-id="f9b07-122">No</span></span><br/></td>
<td><span data-ttu-id="f9b07-123">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f9b07-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f9b07-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="f9b07-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f9b07-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="f9b07-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f9b07-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="f9b07-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f9b07-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="f9b07-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f9b07-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f9b07-128">Child elements</span></span>



| <span data-ttu-id="f9b07-129">Élément</span><span class="sxs-lookup"><span data-stu-id="f9b07-129">Element</span></span>                                                                             | <span data-ttu-id="f9b07-130">Description</span><span class="sxs-lookup"><span data-stu-id="f9b07-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f9b07-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="f9b07-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="f9b07-132">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-133">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="f9b07-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="f9b07-134">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f9b07-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="f9b07-136">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="f9b07-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f9b07-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="f9b07-138">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="f9b07-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="f9b07-140">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f9b07-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="f9b07-142">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-143">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="f9b07-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="f9b07-144">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="f9b07-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="f9b07-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="f9b07-146">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f9b07-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="f9b07-148">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f9b07-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="f9b07-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="f9b07-150">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f9b07-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f9b07-151">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f9b07-151">Parent elements</span></span>



| <span data-ttu-id="f9b07-152">Élément</span><span class="sxs-lookup"><span data-stu-id="f9b07-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f9b07-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="f9b07-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="f9b07-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f9b07-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="f9b07-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f9b07-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="f9b07-156">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="f9b07-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="f9b07-157">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="f9b07-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="f9b07-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="f9b07-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="f9b07-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f9b07-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f9b07-160">Notes</span><span class="sxs-lookup"><span data-stu-id="f9b07-160">Remarks</span></span>

<span data-ttu-id="f9b07-161">Facultatif ou obligatoire, en fonction de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="f9b07-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="f9b07-162">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b07-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="f9b07-163">**DropDownButton** prend en charge les [modes d’application](ribbon-applicationmodes.md) lorsqu’il est hébergé dans la colonne de gauche du menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="f9b07-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="f9b07-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) et [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) ne sont pas des éléments enfants valides de **DropDownButton** lorsque **DropDownButton** est un descendant de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="f9b07-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f9b07-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="f9b07-165">Examples</span></span>

<span data-ttu-id="f9b07-166">L’exemple suivant illustre le balisage de base pour **DropDownButton**.</span><span class="sxs-lookup"><span data-stu-id="f9b07-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="f9b07-167">Cette section de code montre les déclarations de commande **DropDownButton** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="f9b07-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="f9b07-168">Cette section de code montre les déclarations de contrôle **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="f9b07-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="f9b07-169">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f9b07-169">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f9b07-170">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9b07-170">Minimum supported system</span></span><br/> | <span data-ttu-id="f9b07-171">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9b07-171">Windows 7</span></span> |
| <span data-ttu-id="f9b07-172">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="f9b07-172">Can be empty</span></span>                        | <span data-ttu-id="f9b07-173">Non</span><span class="sxs-lookup"><span data-stu-id="f9b07-173">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="f9b07-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9b07-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b07-175">Contrôle de bouton déroulant</span><span class="sxs-lookup"><span data-stu-id="f9b07-175">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="f9b07-176">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="f9b07-176">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

