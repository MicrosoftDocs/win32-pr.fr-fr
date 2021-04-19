---
title: Élément FlowMenuLayout
description: Représente une disposition horizontale avec des sauts de ligne pour les éléments d’une galerie.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Ruban des fenêtres d’élément FlowMenuLayout
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106544150"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="b6ce0-104">Élément FlowMenuLayout</span><span class="sxs-lookup"><span data-stu-id="b6ce0-104">FlowMenuLayout element</span></span>

<span data-ttu-id="b6ce0-105">Représente une disposition horizontale avec des sauts de ligne pour les éléments d’une galerie.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="b6ce0-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b6ce0-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="b6ce0-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="b6ce0-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6ce0-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="b6ce0-108">Attribute</span></span></th>
<th><span data-ttu-id="b6ce0-109">Type</span><span class="sxs-lookup"><span data-stu-id="b6ce0-109">Type</span></span></th>
<th><span data-ttu-id="b6ce0-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b6ce0-110">Required</span></span></th>
<th><span data-ttu-id="b6ce0-111">Description</span><span class="sxs-lookup"><span data-stu-id="b6ce0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6ce0-112"><strong>Colonnes</strong></span><span class="sxs-lookup"><span data-stu-id="b6ce0-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="b6ce0-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b6ce0-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="b6ce0-114">Non</span><span class="sxs-lookup"><span data-stu-id="b6ce0-114">No</span></span><br/></td>
<td><span data-ttu-id="b6ce0-115">Spécifie le nombre d’éléments à afficher sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="b6ce0-116">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="b6ce0-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="b6ce0-117">Entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="b6ce0-118">La valeur par défaut est <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6ce0-119"><strong>Manipulation</strong></span><span class="sxs-lookup"><span data-stu-id="b6ce0-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="b6ce0-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="b6ce0-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="b6ce0-121">Non</span><span class="sxs-lookup"><span data-stu-id="b6ce0-121">No</span></span><br/></td>
<td><span data-ttu-id="b6ce0-122">Une poignée de redimensionnement attachée à la liste déroulante de la Galerie.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="b6ce0-123">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6ce0-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="b6ce0-124">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="b6ce0-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b6ce0-125"><dt><span></span><span></span><strong></strong> Barr</span><span class="sxs-lookup"><span data-stu-id="b6ce0-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b6ce0-126"><dt><span></span><span></span><strong></strong> Virage</span><span class="sxs-lookup"><span data-stu-id="b6ce0-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="b6ce0-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6ce0-128"><strong>Lignes</strong></span><span class="sxs-lookup"><span data-stu-id="b6ce0-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="b6ce0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b6ce0-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="b6ce0-130">Non</span><span class="sxs-lookup"><span data-stu-id="b6ce0-130">No</span></span><br/></td>
<td><span data-ttu-id="b6ce0-131">Spécifie le nombre de lignes d’élément à afficher sans défilement.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="b6ce0-132">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="b6ce0-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="b6ce0-133">Entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="b6ce0-134">La valeur par défaut est <strong>-1</strong> qui spécifie d’afficher autant de lignes d’éléments que possible.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b6ce0-135">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6ce0-135">Child elements</span></span>

<span data-ttu-id="b6ce0-136">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6ce0-137">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b6ce0-137">Parent elements</span></span>



| <span data-ttu-id="b6ce0-138">Élément</span><span class="sxs-lookup"><span data-stu-id="b6ce0-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6ce0-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="b6ce0-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="b6ce0-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="b6ce0-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="b6ce0-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="b6ce0-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b6ce0-142">Notes</span><span class="sxs-lookup"><span data-stu-id="b6ce0-142">Remarks</span></span>

<span data-ttu-id="b6ce0-143">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-143">Required.</span></span>

<span data-ttu-id="b6ce0-144">L’élément [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou **FlowMenuLayout** doit se produire une seule fois pour chaque élément [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="b6ce0-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="b6ce0-145">Les éléments sont organisés en fonction des propriétés de saut de ligne inhérentes aux attributs de *ligne* et de *colonne* .</span><span class="sxs-lookup"><span data-stu-id="b6ce0-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="b6ce0-146">Lorsque le contenu dépasse la longueur d’une seule ligne, le menu coupe les lignes, encapsule les lignes et aligne le contenu de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="b6ce0-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="b6ce0-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="b6ce0-147">Examples</span></span>

<span data-ttu-id="b6ce0-148">L’exemple suivant illustre le balisage de base pour [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce0-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="b6ce0-149">Cette section de code illustre la déclaration de contrôle [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) avec une spécification **FlowMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="b6ce0-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="b6ce0-150">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6ce0-150">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="b6ce0-151">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6ce0-151">Minimum supported system</span></span><br/> | <span data-ttu-id="b6ce0-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6ce0-152">Windows 7</span></span> |
| <span data-ttu-id="b6ce0-153">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b6ce0-153">Can be empty</span></span>                        | <span data-ttu-id="b6ce0-154">Oui</span><span class="sxs-lookup"><span data-stu-id="b6ce0-154">Yes</span></span>       |



 

 





