---
title: Button, élément (infrastructure de ruban Windows)
description: Représente un contrôle bouton.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Ruban des fenêtres d’élément de bouton
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c037a598a4a853db3203162bcdbe6cd71afca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101705"
---
# <a name="button-element"></a><span data-ttu-id="44b72-104">Button, élément</span><span class="sxs-lookup"><span data-stu-id="44b72-104">Button element</span></span>

<span data-ttu-id="44b72-105">Représente un contrôle [bouton](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="44b72-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="44b72-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="44b72-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="44b72-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="44b72-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44b72-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="44b72-108">Attribute</span></span></th>
<th><span data-ttu-id="44b72-109">Type</span><span class="sxs-lookup"><span data-stu-id="44b72-109">Type</span></span></th>
<th><span data-ttu-id="44b72-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="44b72-110">Required</span></span></th>
<th><span data-ttu-id="44b72-111">Description</span><span class="sxs-lookup"><span data-stu-id="44b72-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="44b72-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="44b72-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="44b72-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="44b72-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="44b72-114">Non</span><span class="sxs-lookup"><span data-stu-id="44b72-114">No</span></span><br/></td>
<td><span data-ttu-id="44b72-115">Cet attribut est valide uniquement lorsque l’élément <strong>Button</strong> est un enfant de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="44b72-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="44b72-116">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="44b72-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="44b72-117">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="44b72-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="44b72-118">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="44b72-118">Default.</span></span> <br/> </dd> <span data-ttu-id="44b72-119"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="44b72-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44b72-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="44b72-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="44b72-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="44b72-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="44b72-122">Non</span><span class="sxs-lookup"><span data-stu-id="44b72-122">No</span></span><br/></td>
<td><span data-ttu-id="44b72-123">Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="44b72-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="44b72-124">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="44b72-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="44b72-125">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="44b72-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="44b72-126">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="44b72-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="44b72-127">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="44b72-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44b72-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="44b72-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="44b72-129">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="44b72-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="44b72-130">Non</span><span class="sxs-lookup"><span data-stu-id="44b72-130">No</span></span><br/></td>
<td><span data-ttu-id="44b72-131">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="44b72-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="44b72-132">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="44b72-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="44b72-133">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="44b72-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="44b72-134">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="44b72-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="44b72-135">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="44b72-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="44b72-136">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44b72-136">Child elements</span></span>

<span data-ttu-id="44b72-137">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="44b72-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="44b72-138">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="44b72-138">Parent elements</span></span>



| <span data-ttu-id="44b72-139">Élément</span><span class="sxs-lookup"><span data-stu-id="44b72-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44b72-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="44b72-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="44b72-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="44b72-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="44b72-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="44b72-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="44b72-143">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="44b72-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="44b72-144">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="44b72-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="44b72-145">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="44b72-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="44b72-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="44b72-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="44b72-147">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="44b72-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="44b72-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="44b72-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="44b72-149">Notes</span><span class="sxs-lookup"><span data-stu-id="44b72-149">Remarks</span></span>

<span data-ttu-id="44b72-150">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44b72-150">Optional.</span></span>

<span data-ttu-id="44b72-151">Peut se produire au plus une fois pour chaque élément [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="44b72-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="44b72-152">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="44b72-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="44b72-153">Le **bouton** prend en charge les [modes d’application](ribbon-applicationmodes.md) lorsqu’il est hébergé dans la colonne de gauche du menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="44b72-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="44b72-154">Exemples</span><span class="sxs-lookup"><span data-stu-id="44b72-154">Examples</span></span>

<span data-ttu-id="44b72-155">L’exemple suivant illustre le balisage de base pour le **bouton**.</span><span class="sxs-lookup"><span data-stu-id="44b72-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="44b72-156">Cette section de code montre les déclarations de commande de **bouton** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **Button** .</span><span class="sxs-lookup"><span data-stu-id="44b72-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="44b72-157">Cette section de code montre les déclarations de contrôle de **bouton** .</span><span class="sxs-lookup"><span data-stu-id="44b72-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="44b72-158">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="44b72-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="44b72-159">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44b72-159">Minimum supported system</span></span><br/> | <span data-ttu-id="44b72-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44b72-160">Windows 7</span></span> |
| <span data-ttu-id="44b72-161">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="44b72-161">Can be empty</span></span>                        | <span data-ttu-id="44b72-162">Oui</span><span class="sxs-lookup"><span data-stu-id="44b72-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="44b72-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44b72-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b72-164">Contrôle Button</span><span class="sxs-lookup"><span data-stu-id="44b72-164">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="44b72-165">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="44b72-165">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

