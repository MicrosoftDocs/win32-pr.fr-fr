---
title: Élément VerticalMenuLayout
description: Représente une disposition verticale pour les éléments d’une galerie.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Ruban des fenêtres d’élément VerticalMenuLayout
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "103724341"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="5f010-104">Élément VerticalMenuLayout</span><span class="sxs-lookup"><span data-stu-id="5f010-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="5f010-105">Représente une disposition verticale pour les éléments d’une galerie.</span><span class="sxs-lookup"><span data-stu-id="5f010-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="5f010-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="5f010-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="5f010-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="5f010-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f010-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="5f010-108">Attribute</span></span></th>
<th><span data-ttu-id="5f010-109">Type</span><span class="sxs-lookup"><span data-stu-id="5f010-109">Type</span></span></th>
<th><span data-ttu-id="5f010-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5f010-110">Required</span></span></th>
<th><span data-ttu-id="5f010-111">Description</span><span class="sxs-lookup"><span data-stu-id="5f010-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f010-112"><strong>Manipulation</strong></span><span class="sxs-lookup"><span data-stu-id="5f010-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="5f010-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f010-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="5f010-114">Non</span><span class="sxs-lookup"><span data-stu-id="5f010-114">No</span></span><br/></td>
<td><span data-ttu-id="5f010-115">Une poignée de redimensionnement attachée à la liste déroulante de la Galerie.</span><span class="sxs-lookup"><span data-stu-id="5f010-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="5f010-116">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f010-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="5f010-117">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="5f010-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f010-118"><dt><span></span><span></span><strong></strong> Barr</span><span class="sxs-lookup"><span data-stu-id="5f010-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="5f010-119">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f010-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f010-120"><strong>IsMultipleHighlightingEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="5f010-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="5f010-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="5f010-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="5f010-122">Non</span><span class="sxs-lookup"><span data-stu-id="5f010-122">No</span></span><br/></td>
<td><span data-ttu-id="5f010-123"><strong>Windows 8 et versions ultérieures</strong></span><span class="sxs-lookup"><span data-stu-id="5f010-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="5f010-124">Met en surbrillance tous les éléments de la liste jusqu’à l’élément MouseOver actuel (au lieu de l’élément MouseOver uniquement), et y compris celui-ci.</span><span class="sxs-lookup"><span data-stu-id="5f010-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="5f010-125">Généralement utilisé pour plusieurs fonctionnalités d' <strong>annulation</strong> et de <strong>rétablissement</strong> .</span><span class="sxs-lookup"><span data-stu-id="5f010-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="5f010-126">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="5f010-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f010-127"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="5f010-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="5f010-128">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f010-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f010-129"><strong>Lignes</strong></span><span class="sxs-lookup"><span data-stu-id="5f010-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="5f010-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f010-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="5f010-131">Non</span><span class="sxs-lookup"><span data-stu-id="5f010-131">No</span></span><br/></td>
<td><span data-ttu-id="5f010-132">Spécifie le nombre de lignes d’élément à afficher sans défilement.</span><span class="sxs-lookup"><span data-stu-id="5f010-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="5f010-133">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="5f010-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="5f010-134">Entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="5f010-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="5f010-135">La valeur par défaut est <strong>-1</strong> qui spécifie d’afficher autant de lignes d’éléments que possible.</span><span class="sxs-lookup"><span data-stu-id="5f010-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5f010-136">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5f010-136">Child elements</span></span>

<span data-ttu-id="5f010-137">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="5f010-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5f010-138">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5f010-138">Parent elements</span></span>



| <span data-ttu-id="5f010-139">Élément</span><span class="sxs-lookup"><span data-stu-id="5f010-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f010-140">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5f010-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="5f010-141">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5f010-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="5f010-142">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5f010-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5f010-143">Notes</span><span class="sxs-lookup"><span data-stu-id="5f010-143">Remarks</span></span>

<span data-ttu-id="5f010-144">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5f010-144">Required.</span></span>

<span data-ttu-id="5f010-145">L’élément **VerticalMenuLayout** ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) doit se produire une seule fois pour chaque élément [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="5f010-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="5f010-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="5f010-146">Examples</span></span>

<span data-ttu-id="5f010-147">L’exemple suivant illustre le balisage de base pour un élément **VerticalMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="5f010-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="5f010-148">Cette section de code montre les déclarations de contrôle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="5f010-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="5f010-149">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5f010-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="5f010-150">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f010-150">Minimum supported system</span></span><br/> | <span data-ttu-id="5f010-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f010-151">Windows 7</span></span> |
| <span data-ttu-id="5f010-152">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="5f010-152">Can be empty</span></span>                        | <span data-ttu-id="5f010-153">Oui</span><span class="sxs-lookup"><span data-stu-id="5f010-153">Yes</span></span>       |



 

 





