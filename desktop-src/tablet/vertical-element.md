---
description: Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal. Utilisé, par exemple, lorsque la note contient des lignes de grille.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Élément vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318285"
---
# <a name="vertical-element"></a><span data-ttu-id="33b1c-104">Élément vertical</span><span class="sxs-lookup"><span data-stu-id="33b1c-104">Vertical Element</span></span>

<span data-ttu-id="33b1c-105">Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal.</span><span class="sxs-lookup"><span data-stu-id="33b1c-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="33b1c-106">Utilisé, par exemple, lorsque la note contient des lignes de grille.</span><span class="sxs-lookup"><span data-stu-id="33b1c-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="33b1c-107">Définition</span><span class="sxs-lookup"><span data-stu-id="33b1c-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="33b1c-108">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="33b1c-108">Parent Elements</span></span>

[<span data-ttu-id="33b1c-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="33b1c-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="33b1c-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="33b1c-110">Child Elements</span></span>

<span data-ttu-id="33b1c-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="33b1c-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="33b1c-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="33b1c-112">Attributes</span></span>



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
<th><span data-ttu-id="33b1c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="33b1c-113">Attribute</span></span></th>
<th><span data-ttu-id="33b1c-114">Type</span><span class="sxs-lookup"><span data-stu-id="33b1c-114">Type</span></span></th>
<th><span data-ttu-id="33b1c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="33b1c-115">Required</span></span></th>
<th><span data-ttu-id="33b1c-116">Description</span><span class="sxs-lookup"><span data-stu-id="33b1c-116">Description</span></span></th>
<th><span data-ttu-id="33b1c-117">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="33b1c-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33b1c-118"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="33b1c-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="33b1c-119">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="33b1c-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="33b1c-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="33b1c-120">Required</span></span></td>
<td><span data-ttu-id="33b1c-121">Spécifie le type de ligne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="33b1c-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="33b1c-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="33b1c-122">None</span></span></li>
<li><span data-ttu-id="33b1c-123">Unie</span><span class="sxs-lookup"><span data-stu-id="33b1c-123">Solid</span></span></li>
<li><span data-ttu-id="33b1c-124">Tiret</span><span class="sxs-lookup"><span data-stu-id="33b1c-124">Dash</span></span></li>
<li><span data-ttu-id="33b1c-125">Points</span><span class="sxs-lookup"><span data-stu-id="33b1c-125">Dot</span></span></li>
<li><span data-ttu-id="33b1c-126">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="33b1c-126">DashDot</span></span></li>
<li><span data-ttu-id="33b1c-127">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="33b1c-127">DashDotDot</span></span></li>
<li><span data-ttu-id="33b1c-128">Double</span><span class="sxs-lookup"><span data-stu-id="33b1c-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33b1c-129"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="33b1c-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="33b1c-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="33b1c-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="33b1c-131">Facultatif</span><span class="sxs-lookup"><span data-stu-id="33b1c-131">Optional</span></span></td>
<td><span data-ttu-id="33b1c-132">Couleur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="33b1c-132">Color of the element.</span></span></td>
<td><span data-ttu-id="33b1c-133">Valeur RVB hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="33b1c-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="33b1c-134">Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="33b1c-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="33b1c-135">Par exemple, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="33b1c-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33b1c-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="33b1c-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="33b1c-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="33b1c-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="33b1c-138">Facultatif</span><span class="sxs-lookup"><span data-stu-id="33b1c-138">Optional</span></span></td>
<td><span data-ttu-id="33b1c-139">Espacement avant l’élément.</span><span class="sxs-lookup"><span data-stu-id="33b1c-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="33b1c-140">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="33b1c-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33b1c-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="33b1c-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="33b1c-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="33b1c-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="33b1c-143">Facultatif</span><span class="sxs-lookup"><span data-stu-id="33b1c-143">Optional</span></span></td>
<td><span data-ttu-id="33b1c-144">Espacement entre cet élément et les éléments environnants.</span><span class="sxs-lookup"><span data-stu-id="33b1c-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="33b1c-145">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="33b1c-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="33b1c-146">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="33b1c-146">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="33b1c-147">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="33b1c-147">Element type</span></span> | <span data-ttu-id="33b1c-148">ComplexType [**VerticalType**](verticaltype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="33b1c-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="33b1c-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33b1c-149">Namespace</span></span>    | <span data-ttu-id="33b1c-150">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="33b1c-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="33b1c-151">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="33b1c-151">Schema name</span></span>  | <span data-ttu-id="33b1c-152">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="33b1c-152">Journal Reader</span></span>                                                |



 

 

 




