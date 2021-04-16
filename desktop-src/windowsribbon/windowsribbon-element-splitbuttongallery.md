---
title: Élément SplitButtonGallery
description: Représente un contrôle de Galerie de boutons partagés avec un menu déroulant basé sur la Galerie.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Ruban des fenêtres d’élément SplitButtonGallery
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463478"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="3f1a5-104">Élément SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="3f1a5-104">SplitButtonGallery element</span></span>

<span data-ttu-id="3f1a5-105">Représente un contrôle de [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) avec un menu déroulant basé sur la Galerie.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="3f1a5-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3f1a5-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="3f1a5-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3f1a5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f1a5-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="3f1a5-108">Attribute</span></span></th>
<th><span data-ttu-id="3f1a5-109">Type</span><span class="sxs-lookup"><span data-stu-id="3f1a5-109">Type</span></span></th>
<th><span data-ttu-id="3f1a5-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3f1a5-110">Required</span></span></th>
<th><span data-ttu-id="3f1a5-111">Description</span><span class="sxs-lookup"><span data-stu-id="3f1a5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f1a5-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3f1a5-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="3f1a5-114">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-114">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-115">Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="3f1a5-116">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="3f1a5-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3f1a5-117">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="3f1a5-118">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="3f1a5-119">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f1a5-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="3f1a5-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3f1a5-122">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-122">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-123">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="3f1a5-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="3f1a5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3f1a5-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3f1a5-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3f1a5-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f1a5-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="3f1a5-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="3f1a5-130">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-130">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-131">Détermine si la ressource d’image de grande taille ou de petite taille de la commande est affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3f1a5-132">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="3f1a5-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="3f1a5-133">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="3f1a5-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3f1a5-134">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="3f1a5-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="3f1a5-135">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-135">Default.</span></span> <br/> </dd> <span data-ttu-id="3f1a5-136"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="3f1a5-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f1a5-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3f1a5-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3f1a5-139">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-139">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-140"><dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="3f1a5-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3f1a5-141">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f1a5-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3f1a5-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3f1a5-144">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-144">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-145"><dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="3f1a5-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3f1a5-146">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f1a5-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="3f1a5-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="3f1a5-149">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-149">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-150">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f1a5-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3f1a5-151">
<dt><span></span><span></span><strong></strong> Ballon</span><span class="sxs-lookup"><span data-stu-id="3f1a5-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3f1a5-152"><dt><span></span><span></span><strong></strong> Cuir</span><span class="sxs-lookup"><span data-stu-id="3f1a5-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3f1a5-153"><dt><span></span><span></span><strong></strong> Gauche</span><span class="sxs-lookup"><span data-stu-id="3f1a5-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3f1a5-154"><dt><span></span><span></span><strong></strong> Éviter</span><span class="sxs-lookup"><span data-stu-id="3f1a5-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3f1a5-155"><dt><span></span><span></span><strong></strong> Approprié</span><span class="sxs-lookup"><span data-stu-id="3f1a5-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3f1a5-156"><dt><span></span><span></span><strong></strong> Coin</span><span class="sxs-lookup"><span data-stu-id="3f1a5-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f1a5-157"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="3f1a5-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="3f1a5-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="3f1a5-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="3f1a5-159">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-159">No</span></span><br/></td>
<td><span data-ttu-id="3f1a5-160">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f1a5-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3f1a5-161">
<dt><span></span><span></span><strong></strong> Contenus</span><span class="sxs-lookup"><span data-stu-id="3f1a5-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3f1a5-162"><dt><span></span><span></span><strong></strong> Commandes</span><span class="sxs-lookup"><span data-stu-id="3f1a5-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3f1a5-163">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3f1a5-163">Child elements</span></span>



| <span data-ttu-id="3f1a5-164">Élément</span><span class="sxs-lookup"><span data-stu-id="3f1a5-164">Element</span></span>                                                                                                 | <span data-ttu-id="3f1a5-165">Description</span><span class="sxs-lookup"><span data-stu-id="3f1a5-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3f1a5-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="3f1a5-167">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="3f1a5-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3f1a5-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="3f1a5-169">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="3f1a5-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3f1a5-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="3f1a5-171">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="3f1a5-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3f1a5-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="3f1a5-173">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="3f1a5-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="3f1a5-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="3f1a5-175">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3f1a5-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="3f1a5-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="3f1a5-177">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="3f1a5-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3f1a5-178">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3f1a5-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f1a5-179">Élément</span><span class="sxs-lookup"><span data-stu-id="3f1a5-179">Element</span></span></th>
<th><span data-ttu-id="3f1a5-180">Description</span><span class="sxs-lookup"><span data-stu-id="3f1a5-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f1a5-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f1a5-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3f1a5-182"><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f1a5-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3f1a5-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f1a5-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="3f1a5-184">Lorsqu’il est contenu dans un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="3f1a5-185">Cet élément est uniquement pris en charge sur le premier niveau et ne doit pas avoir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f1a5-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f1a5-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="3f1a5-187">Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f1a5-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f1a5-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3f1a5-189">Notes</span><span class="sxs-lookup"><span data-stu-id="3f1a5-189">Remarks</span></span>

<span data-ttu-id="3f1a5-190">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-190">Optional.</span></span>

<span data-ttu-id="3f1a5-191">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="3f1a5-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="3f1a5-192">**SplitButtonGallery** prend en charge les [modes d’application](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="3f1a5-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="3f1a5-193">[Interface utilisateur \_ Le \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) de la valeur de la variable est utilisé par une application pour interroger l’État bascule du contrôle Button d’un **SplitButtonGallery**.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="3f1a5-194">La capture d’écran suivante illustre le contrôle de [Galerie de bouton partagé](windowsribbon-controls-splitbuttongallery.md) du ruban dans Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f1a5-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de Galerie de boutons partagés dans Microsoft Paint pour Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="3f1a5-196">Exemples</span><span class="sxs-lookup"><span data-stu-id="3f1a5-196">Examples</span></span>

<span data-ttu-id="3f1a5-197">L’exemple suivant illustre le balisage de base pour la [bibliothèque de boutons partagés](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="3f1a5-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="3f1a5-198">Cette section de code montre les déclarations de commande **SplitButtonGallery** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="3f1a5-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="3f1a5-199">Cette section de code montre les déclarations de contrôle **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="3f1a5-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="3f1a5-200">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3f1a5-200">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="3f1a5-201">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f1a5-201">Minimum supported system</span></span><br/> | <span data-ttu-id="3f1a5-202">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f1a5-202">Windows 7</span></span> |
| <span data-ttu-id="3f1a5-203">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="3f1a5-203">Can be empty</span></span>                        | <span data-ttu-id="3f1a5-204">Non</span><span class="sxs-lookup"><span data-stu-id="3f1a5-204">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="3f1a5-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f1a5-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1a5-206">Contrôle de la Galerie des boutons partagés</span><span class="sxs-lookup"><span data-stu-id="3f1a5-206">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="3f1a5-207">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="3f1a5-207">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="3f1a5-208">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="3f1a5-208">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="3f1a5-209">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="3f1a5-209">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

