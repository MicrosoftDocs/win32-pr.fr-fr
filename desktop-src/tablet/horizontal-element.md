---
description: Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Élément horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432374"
---
# <a name="horizontal-element"></a><span data-ttu-id="c48ee-103">Élément horizontal</span><span class="sxs-lookup"><span data-stu-id="c48ee-103">Horizontal Element</span></span>

<span data-ttu-id="c48ee-104">Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.</span><span class="sxs-lookup"><span data-stu-id="c48ee-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="c48ee-105">Définition</span><span class="sxs-lookup"><span data-stu-id="c48ee-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="c48ee-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c48ee-106">Parent Elements</span></span>

[<span data-ttu-id="c48ee-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="c48ee-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="c48ee-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c48ee-108">Child Elements</span></span>

<span data-ttu-id="c48ee-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c48ee-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="c48ee-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c48ee-110">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48ee-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="c48ee-111">Attribute</span></span></th>
<th><span data-ttu-id="c48ee-112">Type</span><span class="sxs-lookup"><span data-stu-id="c48ee-112">Type</span></span></th>
<th><span data-ttu-id="c48ee-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c48ee-113">Required</span></span></th>
<th><span data-ttu-id="c48ee-114">Description</span><span class="sxs-lookup"><span data-stu-id="c48ee-114">Description</span></span></th>
<th><span data-ttu-id="c48ee-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c48ee-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c48ee-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="c48ee-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="c48ee-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="c48ee-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="c48ee-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c48ee-118">Required</span></span></td>
<td><span data-ttu-id="c48ee-119">Spécifie le type de ligne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="c48ee-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="c48ee-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="c48ee-120">None</span></span></li>
<li><span data-ttu-id="c48ee-121">Unie</span><span class="sxs-lookup"><span data-stu-id="c48ee-121">Solid</span></span></li>
<li><span data-ttu-id="c48ee-122">Tiret</span><span class="sxs-lookup"><span data-stu-id="c48ee-122">Dash</span></span></li>
<li><span data-ttu-id="c48ee-123">Points</span><span class="sxs-lookup"><span data-stu-id="c48ee-123">Dot</span></span></li>
<li><span data-ttu-id="c48ee-124">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="c48ee-124">DashDot</span></span></li>
<li><span data-ttu-id="c48ee-125">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="c48ee-125">DashDotDot</span></span></li>
<li><span data-ttu-id="c48ee-126">Double</span><span class="sxs-lookup"><span data-stu-id="c48ee-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c48ee-127"><strong>Couleur</strong></span><span class="sxs-lookup"><span data-stu-id="c48ee-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="c48ee-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="c48ee-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="c48ee-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c48ee-129">Optional</span></span></td>
<td><span data-ttu-id="c48ee-130">Couleur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c48ee-130">Color of the element.</span></span></td>
<td><span data-ttu-id="c48ee-131">Valeur RVB hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="c48ee-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="c48ee-132">Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="c48ee-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="c48ee-133">Par exemple, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="c48ee-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c48ee-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="c48ee-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="c48ee-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c48ee-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="c48ee-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c48ee-136">Optional</span></span></td>
<td><span data-ttu-id="c48ee-137">Espacement avant l’élément.</span><span class="sxs-lookup"><span data-stu-id="c48ee-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="c48ee-138">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c48ee-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c48ee-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="c48ee-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="c48ee-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c48ee-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="c48ee-141">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c48ee-141">Optional</span></span></td>
<td><span data-ttu-id="c48ee-142">Espacement entre cet élément et les éléments environnants.</span><span class="sxs-lookup"><span data-stu-id="c48ee-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="c48ee-143">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c48ee-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="c48ee-144">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c48ee-144">Element Information</span></span>



|  <span data-ttu-id="c48ee-145">Élément</span><span class="sxs-lookup"><span data-stu-id="c48ee-145">Element</span></span>     | <span data-ttu-id="c48ee-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="c48ee-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="c48ee-147">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c48ee-147">Element type</span></span> | [<span data-ttu-id="c48ee-148">**ComplexType HorizontalType**</span><span class="sxs-lookup"><span data-stu-id="c48ee-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="c48ee-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c48ee-149">Namespace</span></span>    | <span data-ttu-id="c48ee-150">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="c48ee-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="c48ee-151">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="c48ee-151">Schema name</span></span>  | <span data-ttu-id="c48ee-152">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="c48ee-152">Journal Reader</span></span>                                                    |



 

 

 




