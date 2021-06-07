---
description: Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal. Utilisé, par exemple, lorsque la note contient des lignes de grille.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Élément vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432121"
---
# <a name="vertical-element"></a><span data-ttu-id="503f7-104">Élément vertical</span><span class="sxs-lookup"><span data-stu-id="503f7-104">Vertical Element</span></span>

<span data-ttu-id="503f7-105">Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal.</span><span class="sxs-lookup"><span data-stu-id="503f7-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="503f7-106">Utilisé, par exemple, lorsque la note contient des lignes de grille.</span><span class="sxs-lookup"><span data-stu-id="503f7-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="503f7-107">Définition</span><span class="sxs-lookup"><span data-stu-id="503f7-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="503f7-108">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="503f7-108">Parent Elements</span></span>

[<span data-ttu-id="503f7-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="503f7-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="503f7-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="503f7-110">Child Elements</span></span>

<span data-ttu-id="503f7-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="503f7-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="503f7-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="503f7-112">Attributes</span></span>



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
<th><span data-ttu-id="503f7-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="503f7-113">Attribute</span></span></th>
<th><span data-ttu-id="503f7-114">Type</span><span class="sxs-lookup"><span data-stu-id="503f7-114">Type</span></span></th>
<th><span data-ttu-id="503f7-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="503f7-115">Required</span></span></th>
<th><span data-ttu-id="503f7-116">Description</span><span class="sxs-lookup"><span data-stu-id="503f7-116">Description</span></span></th>
<th><span data-ttu-id="503f7-117">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="503f7-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="503f7-118"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="503f7-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="503f7-119">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="503f7-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="503f7-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="503f7-120">Required</span></span></td>
<td><span data-ttu-id="503f7-121">Spécifie le type de ligne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="503f7-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="503f7-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="503f7-122">None</span></span></li>
<li><span data-ttu-id="503f7-123">Unie</span><span class="sxs-lookup"><span data-stu-id="503f7-123">Solid</span></span></li>
<li><span data-ttu-id="503f7-124">Tiret</span><span class="sxs-lookup"><span data-stu-id="503f7-124">Dash</span></span></li>
<li><span data-ttu-id="503f7-125">Points</span><span class="sxs-lookup"><span data-stu-id="503f7-125">Dot</span></span></li>
<li><span data-ttu-id="503f7-126">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="503f7-126">DashDot</span></span></li>
<li><span data-ttu-id="503f7-127">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="503f7-127">DashDotDot</span></span></li>
<li><span data-ttu-id="503f7-128">Double</span><span class="sxs-lookup"><span data-stu-id="503f7-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="503f7-129"><strong>Couleur</strong></span><span class="sxs-lookup"><span data-stu-id="503f7-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="503f7-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="503f7-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="503f7-131">Facultatif</span><span class="sxs-lookup"><span data-stu-id="503f7-131">Optional</span></span></td>
<td><span data-ttu-id="503f7-132">Couleur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="503f7-132">Color of the element.</span></span></td>
<td><span data-ttu-id="503f7-133">Valeur RVB hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="503f7-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="503f7-134">Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="503f7-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="503f7-135">Par exemple, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="503f7-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="503f7-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="503f7-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="503f7-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="503f7-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="503f7-138">Facultatif</span><span class="sxs-lookup"><span data-stu-id="503f7-138">Optional</span></span></td>
<td><span data-ttu-id="503f7-139">Espacement avant l’élément.</span><span class="sxs-lookup"><span data-stu-id="503f7-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="503f7-140">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="503f7-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="503f7-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="503f7-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="503f7-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="503f7-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="503f7-143">Facultatif</span><span class="sxs-lookup"><span data-stu-id="503f7-143">Optional</span></span></td>
<td><span data-ttu-id="503f7-144">Espacement entre cet élément et les éléments environnants.</span><span class="sxs-lookup"><span data-stu-id="503f7-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="503f7-145">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="503f7-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="503f7-146">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="503f7-146">Element Information</span></span>



|  <span data-ttu-id="503f7-147">Élément</span><span class="sxs-lookup"><span data-stu-id="503f7-147">Element</span></span>     | <span data-ttu-id="503f7-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="503f7-148">Value</span></span>                                                         |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="503f7-149">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="503f7-149">Element type</span></span> | <span data-ttu-id="503f7-150">ComplexType [**VerticalType**](verticaltype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="503f7-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="503f7-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="503f7-151">Namespace</span></span>    | <span data-ttu-id="503f7-152">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="503f7-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="503f7-153">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="503f7-153">Schema name</span></span>  | <span data-ttu-id="503f7-154">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="503f7-154">Journal Reader</span></span>                                                |



 

 

 




