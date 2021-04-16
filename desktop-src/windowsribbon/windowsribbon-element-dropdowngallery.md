---
title: Élément DropDownGallery
description: Représente un contrôle de Galerie Drop-Down avec un menu basé sur la Galerie.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Ruban des fenêtres d’élément DropDownGallery
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507950"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="9cf1d-104">Élément DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="9cf1d-104">DropDownGallery element</span></span>

<span data-ttu-id="9cf1d-105">Représente un contrôle de [Galerie](windowsribbon-controls-dropdowngallery.md) déroulante avec un menu basé sur la Galerie.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="9cf1d-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="9cf1d-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="9cf1d-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="9cf1d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cf1d-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="9cf1d-108">Attribute</span></span></th>
<th><span data-ttu-id="9cf1d-109">Type</span><span class="sxs-lookup"><span data-stu-id="9cf1d-109">Type</span></span></th>
<th><span data-ttu-id="9cf1d-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9cf1d-110">Required</span></span></th>
<th><span data-ttu-id="9cf1d-111">Description</span><span class="sxs-lookup"><span data-stu-id="9cf1d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf1d-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="9cf1d-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="9cf1d-114">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-114">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-115">Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="9cf1d-116">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="9cf1d-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9cf1d-117">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="9cf1d-118">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="9cf1d-119">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf1d-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="9cf1d-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="9cf1d-122">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-122">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-123">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="9cf1d-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="9cf1d-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9cf1d-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="9cf1d-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="9cf1d-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf1d-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="9cf1d-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="9cf1d-130">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-130">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-131">Détermine si la ressource d’image de grande taille ou de petite taille de la commande est affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9cf1d-132">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="9cf1d-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9cf1d-133">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="9cf1d-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="9cf1d-134">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="9cf1d-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9cf1d-135">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-135">Default.</span></span> <br/> </dd> <span data-ttu-id="9cf1d-136"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="9cf1d-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf1d-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9cf1d-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="9cf1d-139">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-139">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-140"><dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="9cf1d-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="9cf1d-141">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf1d-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9cf1d-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="9cf1d-144">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-144">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-145"><dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="9cf1d-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="9cf1d-146">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf1d-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="9cf1d-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="9cf1d-149">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-149">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-150">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cf1d-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="9cf1d-151">
<dt><span></span><span></span><strong></strong> Ballon</span><span class="sxs-lookup"><span data-stu-id="9cf1d-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="9cf1d-152"><dt><span></span><span></span><strong></strong> Cuir</span><span class="sxs-lookup"><span data-stu-id="9cf1d-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="9cf1d-153"><dt><span></span><span></span><strong></strong> Gauche</span><span class="sxs-lookup"><span data-stu-id="9cf1d-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="9cf1d-154"><dt><span></span><span></span><strong></strong> Éviter</span><span class="sxs-lookup"><span data-stu-id="9cf1d-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="9cf1d-155"><dt><span></span><span></span><strong></strong> Approprié</span><span class="sxs-lookup"><span data-stu-id="9cf1d-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="9cf1d-156"><dt><span></span><span></span><strong></strong> Coin</span><span class="sxs-lookup"><span data-stu-id="9cf1d-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf1d-157"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="9cf1d-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="9cf1d-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="9cf1d-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="9cf1d-159">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-159">No</span></span><br/></td>
<td><span data-ttu-id="9cf1d-160">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cf1d-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="9cf1d-161">
<dt><span></span><span></span><strong></strong> Contenus</span><span class="sxs-lookup"><span data-stu-id="9cf1d-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="9cf1d-162"><dt><span></span><span></span><strong></strong> Commandes</span><span class="sxs-lookup"><span data-stu-id="9cf1d-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9cf1d-163">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9cf1d-163">Child elements</span></span>



| <span data-ttu-id="9cf1d-164">Élément</span><span class="sxs-lookup"><span data-stu-id="9cf1d-164">Element</span></span>                                                                                           | <span data-ttu-id="9cf1d-165">Description</span><span class="sxs-lookup"><span data-stu-id="9cf1d-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9cf1d-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="9cf1d-167">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="9cf1d-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="9cf1d-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="9cf1d-169">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="9cf1d-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="9cf1d-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="9cf1d-171">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="9cf1d-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="9cf1d-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="9cf1d-173">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="9cf1d-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="9cf1d-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="9cf1d-175">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="9cf1d-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="9cf1d-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="9cf1d-177">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="9cf1d-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9cf1d-178">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9cf1d-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cf1d-179">Élément</span><span class="sxs-lookup"><span data-stu-id="9cf1d-179">Element</span></span></th>
<th><span data-ttu-id="9cf1d-180">Description</span><span class="sxs-lookup"><span data-stu-id="9cf1d-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf1d-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cf1d-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9cf1d-182"><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cf1d-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9cf1d-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cf1d-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cf1d-184">Lorsqu’il est contenu dans un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="9cf1d-185">Cet élément est uniquement pris en charge sur le premier niveau et ne doit pas avoir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf1d-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cf1d-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9cf1d-187">Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf1d-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cf1d-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="9cf1d-189">Notes</span><span class="sxs-lookup"><span data-stu-id="9cf1d-189">Remarks</span></span>

<span data-ttu-id="9cf1d-190">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-190">Optional.</span></span>

<span data-ttu-id="9cf1d-191">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf1d-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="9cf1d-192">**DropDownGallery** prend en charge les [modes d’application](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="9cf1d-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="9cf1d-193">La capture d’écran suivante illustre le contrôle de Galerie de la [liste](windowsribbon-controls-dropdowngallery.md) déroulante du ruban dans Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de la Galerie déroulante dans Microsoft Paint pour Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="9cf1d-195">Exemples</span><span class="sxs-lookup"><span data-stu-id="9cf1d-195">Examples</span></span>

<span data-ttu-id="9cf1d-196">L’exemple suivant illustre le balisage de base pour **DropDownGallery**.</span><span class="sxs-lookup"><span data-stu-id="9cf1d-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="9cf1d-197">Cette section de code montre les déclarations de commande **DropDownGallery** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="9cf1d-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="9cf1d-198">Cette section de code montre les déclarations de contrôle **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="9cf1d-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="9cf1d-199">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9cf1d-199">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9cf1d-200">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cf1d-200">Minimum supported system</span></span><br/> | <span data-ttu-id="9cf1d-201">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cf1d-201">Windows 7</span></span> |
| <span data-ttu-id="9cf1d-202">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="9cf1d-202">Can be empty</span></span>                        | <span data-ttu-id="9cf1d-203">Non</span><span class="sxs-lookup"><span data-stu-id="9cf1d-203">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="9cf1d-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cf1d-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf1d-205">**Contrôle de la Galerie déroulante**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-205">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="9cf1d-206">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="9cf1d-206">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="9cf1d-207">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="9cf1d-207">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="9cf1d-208">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="9cf1d-208">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

