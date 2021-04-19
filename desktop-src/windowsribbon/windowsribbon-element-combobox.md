---
title: Élément ComboBox
description: Représente un contrôle de zone de liste déroulante.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Ruban des fenêtres d’élément de ComboBox
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "106510055"
---
# <a name="combobox-element"></a><span data-ttu-id="17675-104">Élément ComboBox</span><span class="sxs-lookup"><span data-stu-id="17675-104">ComboBox element</span></span>

<span data-ttu-id="17675-105">Représente un contrôle de [zone de liste déroulante](windowsribbon-controls-combobox.md) .</span><span class="sxs-lookup"><span data-stu-id="17675-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="17675-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="17675-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="17675-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="17675-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17675-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="17675-108">Attribute</span></span></th>
<th><span data-ttu-id="17675-109">Type</span><span class="sxs-lookup"><span data-stu-id="17675-109">Type</span></span></th>
<th><span data-ttu-id="17675-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="17675-110">Required</span></span></th>
<th><span data-ttu-id="17675-111">Description</span><span class="sxs-lookup"><span data-stu-id="17675-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17675-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="17675-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="17675-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="17675-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="17675-114">Non</span><span class="sxs-lookup"><span data-stu-id="17675-114">No</span></span><br/></td>
<td><span data-ttu-id="17675-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="17675-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="17675-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="17675-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="17675-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="17675-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="17675-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="17675-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="17675-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="17675-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17675-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="17675-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="17675-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="17675-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="17675-122">Non</span><span class="sxs-lookup"><span data-stu-id="17675-122">No</span></span><br/></td>
<td><span data-ttu-id="17675-123">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="17675-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="17675-124">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="17675-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="17675-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="17675-125">Default.</span></span> <br/> </dd> <span data-ttu-id="17675-126"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="17675-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17675-127"><strong>IsEditable</strong></span><span class="sxs-lookup"><span data-stu-id="17675-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="17675-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="17675-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="17675-129">Non</span><span class="sxs-lookup"><span data-stu-id="17675-129">No</span></span><br/></td>
<td><span data-ttu-id="17675-130">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="17675-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="17675-131">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="17675-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="17675-132">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="17675-132">Default.</span></span> <br/> </dd> <span data-ttu-id="17675-133"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="17675-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17675-134"><strong>ResizeType</strong></span><span class="sxs-lookup"><span data-stu-id="17675-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="17675-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="17675-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="17675-136">Non</span><span class="sxs-lookup"><span data-stu-id="17675-136">No</span></span><br/></td>
<td><span data-ttu-id="17675-137"><dt><span></span><span></span><strong></strong> (NoResize)</span><span class="sxs-lookup"><span data-stu-id="17675-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="17675-138">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="17675-138">Default.</span></span> <br/> </dd> <span data-ttu-id="17675-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span><span class="sxs-lookup"><span data-stu-id="17675-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="17675-140">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17675-140">Child elements</span></span>

<span data-ttu-id="17675-141">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="17675-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="17675-142">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17675-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17675-143">Élément</span><span class="sxs-lookup"><span data-stu-id="17675-143">Element</span></span></th>
<th><span data-ttu-id="17675-144">Description</span><span class="sxs-lookup"><span data-stu-id="17675-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17675-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="17675-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="17675-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="17675-148"><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="17675-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="17675-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17675-151">Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="17675-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17675-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="17675-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="17675-153">Notes</span><span class="sxs-lookup"><span data-stu-id="17675-153">Remarks</span></span>

<span data-ttu-id="17675-154">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="17675-154">Optional.</span></span>

<span data-ttu-id="17675-155">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="17675-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="17675-156">Étant donné que la **zone de liste déroulante** est exclusivement une galerie d’éléments, elle ne prend pas en charge les éléments de commande.</span><span class="sxs-lookup"><span data-stu-id="17675-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="17675-157">C’est également le seul contrôle de galerie qui ne prend pas en charge un espace de commande (une collection de commandes qui sont déclarées dans le balisage et répertoriées en bas d’une galerie d’éléments ou d’une bibliothèque de commandes).</span><span class="sxs-lookup"><span data-stu-id="17675-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="17675-158">Pour plus d’informations, consultez [utilisation des galeries](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="17675-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="17675-159">La capture d’écran suivante illustre un contrôle de [zone de liste déroulante](windowsribbon-controls-combobox.md) du ruban à partir de Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="17675-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![capture d’écran d’un contrôle de zone de liste déroulante dans le ruban Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="17675-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="17675-161">Examples</span></span>

<span data-ttu-id="17675-162">Les exemples suivants illustrent le balisage de base de la **zone de liste déroulante**.</span><span class="sxs-lookup"><span data-stu-id="17675-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="17675-163">Cette section de code montre les déclarations de commande de **liste déroulante** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément de **zone de liste déroulante** .</span><span class="sxs-lookup"><span data-stu-id="17675-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="17675-164">Cette section de code montre les déclarations de contrôle de **zone de liste déroulante** .</span><span class="sxs-lookup"><span data-stu-id="17675-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="17675-165">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="17675-165">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="17675-166">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17675-166">Minimum supported system</span></span><br/> | <span data-ttu-id="17675-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17675-167">Windows 7</span></span> |
| <span data-ttu-id="17675-168">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="17675-168">Can be empty</span></span>                        | <span data-ttu-id="17675-169">Oui</span><span class="sxs-lookup"><span data-stu-id="17675-169">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="17675-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17675-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17675-171">Contrôle Combo Box</span><span class="sxs-lookup"><span data-stu-id="17675-171">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="17675-172">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="17675-172">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





