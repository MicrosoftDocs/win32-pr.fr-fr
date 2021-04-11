---
title: Élément InRibbonGallery
description: Représente la Galerie de In-Ribbon, un contrôle basé sur la galerie qui expose un sous-ensemble par défaut d’éléments directement dans le ruban. Tous les éléments restants sont affichés lorsque l’utilisateur clique sur un bouton de menu déroulant.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Ruban des fenêtres d’élément InRibbonGallery
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "104030967"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="ddf89-105">Élément InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="ddf89-105">InRibbonGallery element</span></span>

<span data-ttu-id="ddf89-106">Représente la [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md), un contrôle basé sur la galerie qui expose un sous-ensemble par défaut d’éléments directement dans le ruban.</span><span class="sxs-lookup"><span data-stu-id="ddf89-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="ddf89-107">Tous les éléments restants sont affichés lorsque l’utilisateur clique sur un bouton de menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="ddf89-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="ddf89-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ddf89-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="ddf89-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="ddf89-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddf89-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="ddf89-110">Attribute</span></span></th>
<th><span data-ttu-id="ddf89-111">Type</span><span class="sxs-lookup"><span data-stu-id="ddf89-111">Type</span></span></th>
<th><span data-ttu-id="ddf89-112">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ddf89-112">Required</span></span></th>
<th><span data-ttu-id="ddf89-113">Description</span><span class="sxs-lookup"><span data-stu-id="ddf89-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddf89-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-115">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="ddf89-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ddf89-116">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-116">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-117">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ddf89-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ddf89-118">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="ddf89-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ddf89-119">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="ddf89-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ddf89-120">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="ddf89-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ddf89-121">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="ddf89-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf89-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="ddf89-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="ddf89-124">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-124">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-125">Détermine si la ressource d’image de grande taille ou de petite taille de la commande est affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="ddf89-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ddf89-126">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="ddf89-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="ddf89-127">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="ddf89-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="ddf89-128">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="ddf89-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ddf89-129">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ddf89-129">Default.</span></span> <br/> </dd> <span data-ttu-id="ddf89-130"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="ddf89-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf89-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-133">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-133">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-134">Avec <em>ItemWidth</em>, détermine la taille de l’image d’élément affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="ddf89-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ddf89-135">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à</span><span class="sxs-lookup"><span data-stu-id="ddf89-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="ddf89-136">.</span><span class="sxs-lookup"><span data-stu-id="ddf89-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="ddf89-137">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="ddf89-138">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="ddf89-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf89-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-141">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-141">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-142">Avec <em>ItemHeight</em>, détermine la taille de l’image d’élément affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="ddf89-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ddf89-143">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à</span><span class="sxs-lookup"><span data-stu-id="ddf89-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="ddf89-144">.</span><span class="sxs-lookup"><span data-stu-id="ddf89-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="ddf89-145">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="ddf89-146">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="ddf89-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf89-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-149">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-149">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-150">Spécifie le nombre maximal de colonnes que le <strong>InRibbonGallery</strong> affiche, par exemple, dans la liste déroulante <em>grande</em> disposition de groupe.</span><span class="sxs-lookup"><span data-stu-id="ddf89-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="ddf89-151">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf89-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-154">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-154">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-155">Spécifie le nombre maximal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la disposition de groupe de <em>taille moyenne</em> , avant de passer à une <em>grande</em> disposition.</span><span class="sxs-lookup"><span data-stu-id="ddf89-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="ddf89-156">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf89-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-159">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-159">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-160">Spécifie le nombre maximal de lignes pour la disposition des éléments <strong>InRibbonGallery</strong> .</span><span class="sxs-lookup"><span data-stu-id="ddf89-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="ddf89-161">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="ddf89-162">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="ddf89-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf89-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-165">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-165">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-166">Spécifie le nombre minimal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la <em>grande</em> disposition de groupe, avant de passer au mode <em>moyen</em>.</span><span class="sxs-lookup"><span data-stu-id="ddf89-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="ddf89-167">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf89-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddf89-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="ddf89-170">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-170">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-171">Spécifie le nombre minimal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la disposition de groupe de <em>taille moyenne</em> , avant de basculer vers <em>Small</em>.</span><span class="sxs-lookup"><span data-stu-id="ddf89-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="ddf89-172">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="ddf89-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddf89-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="ddf89-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="ddf89-175">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-175">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-176">Spécifie l’emplacement d’affichage de l’étiquette de l’élément par rapport à l’image.</span><span class="sxs-lookup"><span data-stu-id="ddf89-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="ddf89-177">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddf89-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="ddf89-178">
<dt><span></span><span></span><strong></strong> Ballon</span><span class="sxs-lookup"><span data-stu-id="ddf89-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ddf89-179"><dt><span></span><span></span><strong></strong> Cuir</span><span class="sxs-lookup"><span data-stu-id="ddf89-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ddf89-180"><dt><span></span><span></span><strong></strong> Gauche</span><span class="sxs-lookup"><span data-stu-id="ddf89-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ddf89-181"><dt><span></span><span></span><strong></strong> Éviter</span><span class="sxs-lookup"><span data-stu-id="ddf89-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ddf89-182"><dt><span></span><span></span><strong></strong> Approprié</span><span class="sxs-lookup"><span data-stu-id="ddf89-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ddf89-183"><dt><span></span><span></span><strong></strong> Coin</span><span class="sxs-lookup"><span data-stu-id="ddf89-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddf89-184"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="ddf89-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="ddf89-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddf89-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="ddf89-186">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-186">No</span></span><br/></td>
<td><span data-ttu-id="ddf89-187">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddf89-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="ddf89-188">
<dt><span></span><span></span><strong></strong> Contenus</span><span class="sxs-lookup"><span data-stu-id="ddf89-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ddf89-189"><dt><span></span><span></span><strong></strong> Commandes</span><span class="sxs-lookup"><span data-stu-id="ddf89-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ddf89-190">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ddf89-190">Child elements</span></span>



| <span data-ttu-id="ddf89-191">Élément</span><span class="sxs-lookup"><span data-stu-id="ddf89-191">Element</span></span>                                                                                           | <span data-ttu-id="ddf89-192">Description</span><span class="sxs-lookup"><span data-stu-id="ddf89-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ddf89-193">**Activé**</span><span class="sxs-lookup"><span data-stu-id="ddf89-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="ddf89-194">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ddf89-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ddf89-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="ddf89-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="ddf89-196">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="ddf89-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="ddf89-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ddf89-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="ddf89-198">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="ddf89-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="ddf89-199">**Bouton**</span><span class="sxs-lookup"><span data-stu-id="ddf89-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="ddf89-200">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ddf89-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ddf89-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="ddf89-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="ddf89-202">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ddf89-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ddf89-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="ddf89-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="ddf89-204">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ddf89-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ddf89-205">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ddf89-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddf89-206">Élément</span><span class="sxs-lookup"><span data-stu-id="ddf89-206">Element</span></span></th>
<th><span data-ttu-id="ddf89-207">Description</span><span class="sxs-lookup"><span data-stu-id="ddf89-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddf89-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="ddf89-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ddf89-209"><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a></span><span class="sxs-lookup"><span data-stu-id="ddf89-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ddf89-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="ddf89-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ddf89-211">Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ddf89-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="ddf89-212">Notes</span><span class="sxs-lookup"><span data-stu-id="ddf89-212">Remarks</span></span>

<span data-ttu-id="ddf89-213">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ddf89-213">Optional.</span></span>

<span data-ttu-id="ddf89-214">Peut se produire au plus une fois pour chaque [**ControlGroup**](windowsribbon-element-controlgroup.md) ou élément de [**groupe**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf89-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="ddf89-215">La capture d’écran suivante illustre le contrôle [de Galerie ruban dans le ruban](windowsribbon-controls-inribbongallery.md) de Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ddf89-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de galerie dans le ruban dans le ruban Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="ddf89-217">Exemples</span><span class="sxs-lookup"><span data-stu-id="ddf89-217">Examples</span></span>

<span data-ttu-id="ddf89-218">L’exemple suivant illustre le balisage de base pour une [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="ddf89-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="ddf89-219">Cette section de code montre les déclarations de commande **InRibbonGallery** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="ddf89-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="ddf89-220">Cette section de code montre les déclarations de contrôle **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="ddf89-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ddf89-221">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ddf89-221">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ddf89-222">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddf89-222">Minimum supported system</span></span><br/> | <span data-ttu-id="ddf89-223">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ddf89-223">Windows 7</span></span> |
| <span data-ttu-id="ddf89-224">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="ddf89-224">Can be empty</span></span>                        | <span data-ttu-id="ddf89-225">Non</span><span class="sxs-lookup"><span data-stu-id="ddf89-225">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ddf89-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddf89-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf89-227">Contrôle de galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="ddf89-227">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="ddf89-228">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="ddf89-228">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="ddf89-229">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="ddf89-229">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





