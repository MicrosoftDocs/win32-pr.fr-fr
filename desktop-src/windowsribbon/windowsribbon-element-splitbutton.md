---
title: Élément SplitButton
description: Représente un contrôle de bouton partagé standard.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Ruban fenêtres d’élément SplitButton
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106536071"
---
# <a name="splitbutton-element"></a><span data-ttu-id="8a40a-104">Élément SplitButton</span><span class="sxs-lookup"><span data-stu-id="8a40a-104">SplitButton element</span></span>

<span data-ttu-id="8a40a-105">Représente un contrôle de [bouton partagé](windowsribbon-controls-splitbutton.md) standard.</span><span class="sxs-lookup"><span data-stu-id="8a40a-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="8a40a-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="8a40a-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="8a40a-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a40a-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8a40a-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="8a40a-108">Attribute</span></span></th>
<th><span data-ttu-id="8a40a-109">Type</span><span class="sxs-lookup"><span data-stu-id="8a40a-109">Type</span></span></th>
<th><span data-ttu-id="8a40a-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8a40a-110">Required</span></span></th>
<th><span data-ttu-id="8a40a-111">Description</span><span class="sxs-lookup"><span data-stu-id="8a40a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a40a-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="8a40a-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="8a40a-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="8a40a-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="8a40a-114">Non</span><span class="sxs-lookup"><span data-stu-id="8a40a-114">No</span></span><br/></td>
<td><span data-ttu-id="8a40a-115">Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="8a40a-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="8a40a-116">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="8a40a-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8a40a-117">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="8a40a-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="8a40a-118">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="8a40a-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="8a40a-119">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="8a40a-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a40a-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="8a40a-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="8a40a-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="8a40a-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="8a40a-122">Non</span><span class="sxs-lookup"><span data-stu-id="8a40a-122">No</span></span><br/></td>
<td><span data-ttu-id="8a40a-123">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8a40a-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="8a40a-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="8a40a-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8a40a-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="8a40a-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="8a40a-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="8a40a-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8a40a-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="8a40a-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8a40a-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a40a-128">Child elements</span></span>



| <span data-ttu-id="8a40a-129">Élément</span><span class="sxs-lookup"><span data-stu-id="8a40a-129">Element</span></span>                                                                                   | <span data-ttu-id="8a40a-130">Description</span><span class="sxs-lookup"><span data-stu-id="8a40a-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="8a40a-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="8a40a-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="8a40a-132">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8a40a-133">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="8a40a-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="8a40a-134">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8a40a-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="8a40a-136">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8a40a-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="8a40a-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="8a40a-138">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8a40a-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="8a40a-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="8a40a-140">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="8a40a-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="8a40a-142">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8a40a-143">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="8a40a-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="8a40a-144">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="8a40a-145">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="8a40a-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="8a40a-146">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="8a40a-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="8a40a-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="8a40a-148">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8a40a-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="8a40a-150">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="8a40a-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8a40a-151">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a40a-151">Parent elements</span></span>



| <span data-ttu-id="8a40a-152">Élément</span><span class="sxs-lookup"><span data-stu-id="8a40a-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="8a40a-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="8a40a-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="8a40a-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="8a40a-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="8a40a-155">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="8a40a-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="8a40a-156">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="8a40a-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="8a40a-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="8a40a-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="8a40a-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8a40a-159">Notes</span><span class="sxs-lookup"><span data-stu-id="8a40a-159">Remarks</span></span>

<span data-ttu-id="8a40a-160">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="8a40a-160">Optional.</span></span>

<span data-ttu-id="8a40a-161">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="8a40a-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="8a40a-162">**SplitButton** prend en charge les [modes d’application](ribbon-applicationmodes.md) lorsqu’il est hébergé dans la colonne de gauche du menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="8a40a-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="8a40a-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) et [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) ne sont pas des éléments enfants valides de [**DropDownButton**](windowsribbon-element-dropdownbutton.md) lorsque **DropDownButton** est un descendant de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="8a40a-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="8a40a-164">[**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) doit se produire une seule fois si les éléments suivants ne sont pas présents en tant qu’éléments enfants de **SplitButton**:</span><span class="sxs-lookup"><span data-stu-id="8a40a-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="8a40a-165">**Bouton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="8a40a-166">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="8a40a-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="8a40a-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="8a40a-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="8a40a-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="8a40a-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="8a40a-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="8a40a-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-170">**SplitButton**</span></span>
-   [<span data-ttu-id="8a40a-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="8a40a-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="8a40a-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="8a40a-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="8a40a-173">Ces contrôles sont traités comme des éléments enfants d’un seul élément [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a40a-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="8a40a-174">Exemples</span><span class="sxs-lookup"><span data-stu-id="8a40a-174">Examples</span></span>

<span data-ttu-id="8a40a-175">L’exemple suivant illustre le balisage de base pour le [bouton partagé](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="8a40a-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="8a40a-176">Cette section de code montre les déclarations de commande **SplitButton** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent pour l’élément **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="8a40a-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="8a40a-177">Cette section de code montre les déclarations de contrôle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="8a40a-177">This section of code shows the **SplitButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8a40a-178">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8a40a-178">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="8a40a-179">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a40a-179">Minimum supported system</span></span><br/> | <span data-ttu-id="8a40a-180">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a40a-180">Windows 7</span></span> |
| <span data-ttu-id="8a40a-181">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="8a40a-181">Can be empty</span></span>                        | <span data-ttu-id="8a40a-182">Non</span><span class="sxs-lookup"><span data-stu-id="8a40a-182">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="8a40a-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a40a-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a40a-184">Contrôle de bouton partagé</span><span class="sxs-lookup"><span data-stu-id="8a40a-184">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="8a40a-185">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="8a40a-185">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

