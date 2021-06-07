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
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442880"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="e8e5e-104">Élément FlowMenuLayout</span><span class="sxs-lookup"><span data-stu-id="e8e5e-104">FlowMenuLayout element</span></span>

<span data-ttu-id="e8e5e-105">Représente une disposition horizontale avec des sauts de ligne pour les éléments d’une galerie.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="e8e5e-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e8e5e-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="e8e5e-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="e8e5e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8e5e-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="e8e5e-108">Attribute</span></span></th>
<th><span data-ttu-id="e8e5e-109">Type</span><span class="sxs-lookup"><span data-stu-id="e8e5e-109">Type</span></span></th>
<th><span data-ttu-id="e8e5e-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8e5e-110">Required</span></span></th>
<th><span data-ttu-id="e8e5e-111">Description</span><span class="sxs-lookup"><span data-stu-id="e8e5e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8e5e-112"><strong>Colonnes</strong></span><span class="sxs-lookup"><span data-stu-id="e8e5e-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="e8e5e-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e8e5e-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="e8e5e-114">Non</span><span class="sxs-lookup"><span data-stu-id="e8e5e-114">No</span></span><br/></td>
<td><span data-ttu-id="e8e5e-115">Spécifie le nombre d’éléments à afficher sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="e8e5e-116">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="e8e5e-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="e8e5e-117">Entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="e8e5e-118">La valeur par défaut est <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8e5e-119"><strong>Manipulation</strong></span><span class="sxs-lookup"><span data-stu-id="e8e5e-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="e8e5e-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8e5e-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="e8e5e-121">Non</span><span class="sxs-lookup"><span data-stu-id="e8e5e-121">No</span></span><br/></td>
<td><span data-ttu-id="e8e5e-122">Une poignée de redimensionnement attachée à la liste déroulante de la Galerie.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="e8e5e-123">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8e5e-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="e8e5e-124">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="e8e5e-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="e8e5e-125"><dt><span></span><span></span><strong></strong> Barr</span><span class="sxs-lookup"><span data-stu-id="e8e5e-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="e8e5e-126"><dt><span></span><span></span><strong></strong> Virage</span><span class="sxs-lookup"><span data-stu-id="e8e5e-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="e8e5e-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8e5e-128"><strong>Lignes</strong></span><span class="sxs-lookup"><span data-stu-id="e8e5e-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="e8e5e-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e8e5e-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="e8e5e-130">Non</span><span class="sxs-lookup"><span data-stu-id="e8e5e-130">No</span></span><br/></td>
<td><span data-ttu-id="e8e5e-131">Spécifie le nombre de lignes d’élément à afficher sans défilement.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="e8e5e-132">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="e8e5e-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="e8e5e-133">Entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="e8e5e-134">La valeur par défaut est <strong>-1</strong> qui spécifie d’afficher autant de lignes d’éléments que possible.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e8e5e-135">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e8e5e-135">Child elements</span></span>

<span data-ttu-id="e8e5e-136">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e8e5e-137">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e8e5e-137">Parent elements</span></span>



| <span data-ttu-id="e8e5e-138">Élément</span><span class="sxs-lookup"><span data-stu-id="e8e5e-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8e5e-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="e8e5e-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="e8e5e-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="e8e5e-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="e8e5e-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="e8e5e-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e8e5e-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8e5e-142">Remarks</span></span>

<span data-ttu-id="e8e5e-143">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-143">Required.</span></span>

<span data-ttu-id="e8e5e-144">L’élément [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou **FlowMenuLayout** doit se produire une seule fois pour chaque élément [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e5e-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="e8e5e-145">Les éléments sont organisés en fonction des propriétés de saut de ligne inhérentes aux attributs de *ligne* et de *colonne* .</span><span class="sxs-lookup"><span data-stu-id="e8e5e-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="e8e5e-146">Lorsque le contenu dépasse la longueur d’une seule ligne, le menu coupe les lignes, encapsule les lignes et aligne le contenu de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e8e5e-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="e8e5e-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="e8e5e-147">Examples</span></span>

<span data-ttu-id="e8e5e-148">L’exemple suivant illustre le balisage de base pour [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="e8e5e-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="e8e5e-149">Cette section de code illustre la déclaration de contrôle [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) avec une spécification **FlowMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="e8e5e-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e8e5e-150">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e8e5e-150">Element information</span></span>

* <span data-ttu-id="e8e5e-151">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8e5e-151">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e8e5e-152">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="e8e5e-152">**Can be empty**: Yes</span></span>


 

 





