---
description: Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Élément horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751893"
---
# <a name="horizontal-element"></a><span data-ttu-id="c1eab-103">Élément horizontal</span><span class="sxs-lookup"><span data-stu-id="c1eab-103">Horizontal Element</span></span>

<span data-ttu-id="c1eab-104">Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.</span><span class="sxs-lookup"><span data-stu-id="c1eab-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="c1eab-105">Définition</span><span class="sxs-lookup"><span data-stu-id="c1eab-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="c1eab-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1eab-106">Parent Elements</span></span>

[<span data-ttu-id="c1eab-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="c1eab-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="c1eab-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1eab-108">Child Elements</span></span>

<span data-ttu-id="c1eab-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="c1eab-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="c1eab-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c1eab-110">Attributes</span></span>



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
<th><span data-ttu-id="c1eab-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="c1eab-111">Attribute</span></span></th>
<th><span data-ttu-id="c1eab-112">Type</span><span class="sxs-lookup"><span data-stu-id="c1eab-112">Type</span></span></th>
<th><span data-ttu-id="c1eab-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c1eab-113">Required</span></span></th>
<th><span data-ttu-id="c1eab-114">Description</span><span class="sxs-lookup"><span data-stu-id="c1eab-114">Description</span></span></th>
<th><span data-ttu-id="c1eab-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c1eab-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1eab-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="c1eab-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="c1eab-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1eab-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="c1eab-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c1eab-118">Required</span></span></td>
<td><span data-ttu-id="c1eab-119">Spécifie le type de ligne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="c1eab-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="c1eab-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="c1eab-120">None</span></span></li>
<li><span data-ttu-id="c1eab-121">Unie</span><span class="sxs-lookup"><span data-stu-id="c1eab-121">Solid</span></span></li>
<li><span data-ttu-id="c1eab-122">Tiret</span><span class="sxs-lookup"><span data-stu-id="c1eab-122">Dash</span></span></li>
<li><span data-ttu-id="c1eab-123">Points</span><span class="sxs-lookup"><span data-stu-id="c1eab-123">Dot</span></span></li>
<li><span data-ttu-id="c1eab-124">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="c1eab-124">DashDot</span></span></li>
<li><span data-ttu-id="c1eab-125">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="c1eab-125">DashDotDot</span></span></li>
<li><span data-ttu-id="c1eab-126">Double</span><span class="sxs-lookup"><span data-stu-id="c1eab-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1eab-127"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="c1eab-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="c1eab-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="c1eab-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="c1eab-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c1eab-129">Optional</span></span></td>
<td><span data-ttu-id="c1eab-130">Couleur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c1eab-130">Color of the element.</span></span></td>
<td><span data-ttu-id="c1eab-131">Valeur RVB hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="c1eab-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="c1eab-132">Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="c1eab-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="c1eab-133">Par exemple, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="c1eab-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1eab-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="c1eab-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="c1eab-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c1eab-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="c1eab-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c1eab-136">Optional</span></span></td>
<td><span data-ttu-id="c1eab-137">Espacement avant l’élément.</span><span class="sxs-lookup"><span data-stu-id="c1eab-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="c1eab-138">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c1eab-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1eab-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="c1eab-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="c1eab-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c1eab-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="c1eab-141">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c1eab-141">Optional</span></span></td>
<td><span data-ttu-id="c1eab-142">Espacement entre cet élément et les éléments environnants.</span><span class="sxs-lookup"><span data-stu-id="c1eab-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="c1eab-143">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c1eab-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="c1eab-144">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c1eab-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="c1eab-145">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c1eab-145">Element type</span></span> | [<span data-ttu-id="c1eab-146">**ComplexType HorizontalType**</span><span class="sxs-lookup"><span data-stu-id="c1eab-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="c1eab-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1eab-147">Namespace</span></span>    | <span data-ttu-id="c1eab-148">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="c1eab-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="c1eab-149">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="c1eab-149">Schema name</span></span>  | <span data-ttu-id="c1eab-150">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="c1eab-150">Journal Reader</span></span>                                                    |



 

 

 




