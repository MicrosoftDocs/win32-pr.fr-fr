---
description: Définit les lignes de marge dessinées sur la page.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Élément Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210609"
---
# <a name="margin-element"></a><span data-ttu-id="7c7cd-103">Élément Margin</span><span class="sxs-lookup"><span data-stu-id="7c7cd-103">Margin Element</span></span>

<span data-ttu-id="7c7cd-104">Définit les lignes de marge dessinées sur la page.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="7c7cd-105">Définition</span><span class="sxs-lookup"><span data-stu-id="7c7cd-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="7c7cd-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7c7cd-106">Parent Elements</span></span>

<span data-ttu-id="7c7cd-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="7c7cd-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7c7cd-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7c7cd-108">Child Elements</span></span>

<span data-ttu-id="7c7cd-109">Aucun..</span><span class="sxs-lookup"><span data-stu-id="7c7cd-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="7c7cd-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c7cd-110">Attributes</span></span>



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
<th><span data-ttu-id="7c7cd-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="7c7cd-111">Attribute</span></span></th>
<th><span data-ttu-id="7c7cd-112">Type</span><span class="sxs-lookup"><span data-stu-id="7c7cd-112">Type</span></span></th>
<th><span data-ttu-id="7c7cd-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7c7cd-113">Required</span></span></th>
<th><span data-ttu-id="7c7cd-114">Description</span><span class="sxs-lookup"><span data-stu-id="7c7cd-114">Description</span></span></th>
<th><span data-ttu-id="7c7cd-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7c7cd-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7c7cd-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="7c7cd-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="7c7cd-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c7cd-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="7c7cd-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7c7cd-118">Required</span></span></td>
<td><span data-ttu-id="7c7cd-119">Spécifie le type de ligne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="7c7cd-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="7c7cd-120">None</span></span></li>
<li><span data-ttu-id="7c7cd-121">Unie</span><span class="sxs-lookup"><span data-stu-id="7c7cd-121">Solid</span></span></li>
<li><span data-ttu-id="7c7cd-122">Tiret</span><span class="sxs-lookup"><span data-stu-id="7c7cd-122">Dash</span></span></li>
<li><span data-ttu-id="7c7cd-123">Points</span><span class="sxs-lookup"><span data-stu-id="7c7cd-123">Dot</span></span></li>
<li><span data-ttu-id="7c7cd-124">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="7c7cd-124">DashDot</span></span></li>
<li><span data-ttu-id="7c7cd-125">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="7c7cd-125">DashDotDot</span></span></li>
<li><span data-ttu-id="7c7cd-126">Double</span><span class="sxs-lookup"><span data-stu-id="7c7cd-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c7cd-127"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="7c7cd-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="7c7cd-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="7c7cd-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="7c7cd-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7c7cd-129">Optional</span></span></td>
<td><span data-ttu-id="7c7cd-130">Couleur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-130">Color of the element.</span></span></td>
<td><span data-ttu-id="7c7cd-131">Valeur RVB hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="7c7cd-132">Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="7c7cd-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="7c7cd-133">Par exemple, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c7cd-134"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="7c7cd-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="7c7cd-135">SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c7cd-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="7c7cd-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7c7cd-136">Optional</span></span></td>
<td><span data-ttu-id="7c7cd-137">Indique la marge de gauche ou de droite.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="7c7cd-138">Gauche</span><span class="sxs-lookup"><span data-stu-id="7c7cd-138">Left</span></span></li>
<li><span data-ttu-id="7c7cd-139">Right</span><span class="sxs-lookup"><span data-stu-id="7c7cd-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c7cd-140"><strong>Espacement</strong></span><span class="sxs-lookup"><span data-stu-id="7c7cd-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="7c7cd-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="7c7cd-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="7c7cd-142">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7c7cd-142">Optional</span></span></td>
<td><span data-ttu-id="7c7cd-143">Espacement entre les bords des pages et des marges.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="7c7cd-144">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="7c7cd-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="7c7cd-145">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7c7cd-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="7c7cd-146">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7c7cd-146">Element type</span></span> | <span data-ttu-id="7c7cd-147">ComplexType [**MarginType**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="7c7cd-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="7c7cd-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c7cd-148">Namespace</span></span>    | <span data-ttu-id="7c7cd-149">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="7c7cd-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="7c7cd-150">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="7c7cd-150">Schema name</span></span>  | <span data-ttu-id="7c7cd-151">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="7c7cd-151">Journal Reader</span></span>                                            |



 

 

 




