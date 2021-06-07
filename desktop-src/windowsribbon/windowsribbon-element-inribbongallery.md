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
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443370"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="212ac-105">Élément InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="212ac-105">InRibbonGallery element</span></span>

<span data-ttu-id="212ac-106">Représente la [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md), un contrôle basé sur la galerie qui expose un sous-ensemble par défaut d’éléments directement dans le ruban.</span><span class="sxs-lookup"><span data-stu-id="212ac-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="212ac-107">Tous les éléments restants sont affichés lorsque l’utilisateur clique sur un bouton de menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="212ac-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="212ac-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="212ac-108">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="212ac-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="212ac-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="212ac-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="212ac-110">Attribute</span></span></th>
<th><span data-ttu-id="212ac-111">Type</span><span class="sxs-lookup"><span data-stu-id="212ac-111">Type</span></span></th>
<th><span data-ttu-id="212ac-112">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="212ac-112">Required</span></span></th>
<th><span data-ttu-id="212ac-113">Description</span><span class="sxs-lookup"><span data-stu-id="212ac-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="212ac-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-115">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="212ac-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="212ac-116">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-116">No</span></span><br/></td>
<td><span data-ttu-id="212ac-117">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="212ac-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="212ac-118">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="212ac-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="212ac-119">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="212ac-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="212ac-120">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="212ac-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="212ac-121">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="212ac-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="212ac-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="212ac-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="212ac-124">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-124">No</span></span><br/></td>
<td><span data-ttu-id="212ac-125">Détermine si la ressource d’image de grande taille ou de petite taille de la commande est affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="212ac-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="212ac-126">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="212ac-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="212ac-127">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="212ac-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="212ac-128">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="212ac-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="212ac-129">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="212ac-129">Default.</span></span> <br/> </dd> <span data-ttu-id="212ac-130"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="212ac-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="212ac-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-133">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-133">No</span></span><br/></td>
<td><span data-ttu-id="212ac-134">Avec <em>ItemWidth</em>, détermine la taille de l’image d’élément affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="212ac-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="212ac-135">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à</span><span class="sxs-lookup"><span data-stu-id="212ac-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="212ac-136">.</span><span class="sxs-lookup"><span data-stu-id="212ac-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="212ac-137">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="212ac-138">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="212ac-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="212ac-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-141">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-141">No</span></span><br/></td>
<td><span data-ttu-id="212ac-142">Avec <em>ItemHeight</em>, détermine la taille de l’image d’élément affichée dans le contrôle Gallery.</span><span class="sxs-lookup"><span data-stu-id="212ac-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="212ac-143">S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à</span><span class="sxs-lookup"><span data-stu-id="212ac-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="212ac-144">.</span><span class="sxs-lookup"><span data-stu-id="212ac-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="212ac-145">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="212ac-146">La valeur par défaut est -1.</span><span class="sxs-lookup"><span data-stu-id="212ac-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="212ac-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-149">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-149">No</span></span><br/></td>
<td><span data-ttu-id="212ac-150">Spécifie le nombre maximal de colonnes que le <strong>InRibbonGallery</strong> affiche, par exemple, dans la liste déroulante <em>grande</em> disposition de groupe.</span><span class="sxs-lookup"><span data-stu-id="212ac-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="212ac-151">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="212ac-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-154">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-154">No</span></span><br/></td>
<td><span data-ttu-id="212ac-155">Spécifie le nombre maximal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la disposition de groupe de <em>taille moyenne</em> , avant de passer à une <em>grande</em> disposition.</span><span class="sxs-lookup"><span data-stu-id="212ac-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="212ac-156">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="212ac-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-159">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-159">No</span></span><br/></td>
<td><span data-ttu-id="212ac-160">Spécifie le nombre maximal de lignes pour la disposition des éléments <strong>InRibbonGallery</strong> .</span><span class="sxs-lookup"><span data-stu-id="212ac-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="212ac-161">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="212ac-162">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="212ac-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="212ac-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-165">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-165">No</span></span><br/></td>
<td><span data-ttu-id="212ac-166">Spécifie le nombre minimal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la <em>grande</em> disposition de groupe, avant de passer au mode <em>moyen</em>.</span><span class="sxs-lookup"><span data-stu-id="212ac-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="212ac-167">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="212ac-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="212ac-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="212ac-170">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-170">No</span></span><br/></td>
<td><span data-ttu-id="212ac-171">Spécifie le nombre minimal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la disposition de groupe de <em>taille moyenne</em> , avant de basculer vers <em>Small</em>.</span><span class="sxs-lookup"><span data-stu-id="212ac-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="212ac-172">
<dt><span></span><span></span><strong></strong> (XS : Integer)</span><span class="sxs-lookup"><span data-stu-id="212ac-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="212ac-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="212ac-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="212ac-175">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-175">No</span></span><br/></td>
<td><span data-ttu-id="212ac-176">Spécifie l’emplacement d’affichage de l’étiquette de l’élément par rapport à l’image.</span><span class="sxs-lookup"><span data-stu-id="212ac-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="212ac-177">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="212ac-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="212ac-178">
<dt><span></span><span></span><strong></strong> Ballon</span><span class="sxs-lookup"><span data-stu-id="212ac-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="212ac-179"><dt><span></span><span></span><strong></strong> Cuir</span><span class="sxs-lookup"><span data-stu-id="212ac-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="212ac-180"><dt><span></span><span></span><strong></strong> Gauche</span><span class="sxs-lookup"><span data-stu-id="212ac-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="212ac-181"><dt><span></span><span></span><strong></strong> Éviter</span><span class="sxs-lookup"><span data-stu-id="212ac-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="212ac-182"><dt><span></span><span></span><strong></strong> Approprié</span><span class="sxs-lookup"><span data-stu-id="212ac-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="212ac-183"><dt><span></span><span></span><strong></strong> Coin</span><span class="sxs-lookup"><span data-stu-id="212ac-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="212ac-184"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="212ac-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="212ac-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="212ac-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="212ac-186">Non</span><span class="sxs-lookup"><span data-stu-id="212ac-186">No</span></span><br/></td>
<td><span data-ttu-id="212ac-187">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="212ac-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="212ac-188">
<dt><span></span><span></span><strong></strong> Contenus</span><span class="sxs-lookup"><span data-stu-id="212ac-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="212ac-189"><dt><span></span><span></span><strong></strong> Commandes</span><span class="sxs-lookup"><span data-stu-id="212ac-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="212ac-190">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="212ac-190">Child elements</span></span>



| <span data-ttu-id="212ac-191">Élément</span><span class="sxs-lookup"><span data-stu-id="212ac-191">Element</span></span>                                                                                           | <span data-ttu-id="212ac-192">Description</span><span class="sxs-lookup"><span data-stu-id="212ac-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="212ac-193">**Activé**</span><span class="sxs-lookup"><span data-stu-id="212ac-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="212ac-194">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="212ac-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="212ac-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="212ac-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="212ac-196">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="212ac-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="212ac-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="212ac-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="212ac-198">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="212ac-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="212ac-199">**Bouton**</span><span class="sxs-lookup"><span data-stu-id="212ac-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="212ac-200">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="212ac-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="212ac-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="212ac-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="212ac-202">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="212ac-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="212ac-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="212ac-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="212ac-204">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="212ac-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="212ac-205">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="212ac-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="212ac-206">Élément</span><span class="sxs-lookup"><span data-stu-id="212ac-206">Element</span></span></th>
<th><span data-ttu-id="212ac-207">Description</span><span class="sxs-lookup"><span data-stu-id="212ac-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="212ac-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="212ac-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="212ac-209"><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a></span><span class="sxs-lookup"><span data-stu-id="212ac-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="212ac-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="212ac-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="212ac-211">Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="212ac-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="212ac-212">Remarques</span><span class="sxs-lookup"><span data-stu-id="212ac-212">Remarks</span></span>

<span data-ttu-id="212ac-213">facultatif.</span><span class="sxs-lookup"><span data-stu-id="212ac-213">Optional.</span></span>

<span data-ttu-id="212ac-214">Peut se produire au plus une fois pour chaque [**ControlGroup**](windowsribbon-element-controlgroup.md) ou élément de [**groupe**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="212ac-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="212ac-215">La capture d’écran suivante illustre le contrôle [de Galerie ruban dans le ruban](windowsribbon-controls-inribbongallery.md) de Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="212ac-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![capture d’écran d’un contrôle de galerie dans le ruban dans le ruban Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="212ac-217">Exemples</span><span class="sxs-lookup"><span data-stu-id="212ac-217">Examples</span></span>

<span data-ttu-id="212ac-218">L’exemple suivant illustre le balisage de base pour une [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="212ac-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="212ac-219">Cette section de code montre les déclarations de commande **InRibbonGallery** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="212ac-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


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



<span data-ttu-id="212ac-220">Cette section de code montre les déclarations de contrôle **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="212ac-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="212ac-221">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="212ac-221">Element information</span></span>


* <span data-ttu-id="212ac-222">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="212ac-222">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="212ac-223">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="212ac-223">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="212ac-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="212ac-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="212ac-225">Contrôle de galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="212ac-225">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="212ac-226">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="212ac-226">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="212ac-227">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="212ac-227">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





