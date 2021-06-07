---
description: Définit les lignes de marge dessinées sur la page.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Élément Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547177a10fc3724f3b9bf3dde65f857d03f0f2a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432131"
---
# <a name="margin-element"></a><span data-ttu-id="d64d6-103">Élément Margin</span><span class="sxs-lookup"><span data-stu-id="d64d6-103">Margin Element</span></span>

<span data-ttu-id="d64d6-104">Définit les lignes de marge dessinées sur la page.</span><span class="sxs-lookup"><span data-stu-id="d64d6-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="d64d6-105">Définition</span><span class="sxs-lookup"><span data-stu-id="d64d6-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="d64d6-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d64d6-106">Parent Elements</span></span>

<span data-ttu-id="d64d6-107">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d64d6-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d64d6-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d64d6-108">Child Elements</span></span>

<span data-ttu-id="d64d6-109">Aucun..</span><span class="sxs-lookup"><span data-stu-id="d64d6-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="d64d6-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d64d6-110">Attributes</span></span>



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
<th><span data-ttu-id="d64d6-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="d64d6-111">Attribute</span></span></th>
<th><span data-ttu-id="d64d6-112">Type</span><span class="sxs-lookup"><span data-stu-id="d64d6-112">Type</span></span></th>
<th><span data-ttu-id="d64d6-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d64d6-113">Required</span></span></th>
<th><span data-ttu-id="d64d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="d64d6-114">Description</span></span></th>
<th><span data-ttu-id="d64d6-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d64d6-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d64d6-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="d64d6-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="d64d6-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d64d6-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d64d6-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d64d6-118">Required</span></span></td>
<td><span data-ttu-id="d64d6-119">Spécifie le type de ligne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="d64d6-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="d64d6-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="d64d6-120">None</span></span></li>
<li><span data-ttu-id="d64d6-121">Unie</span><span class="sxs-lookup"><span data-stu-id="d64d6-121">Solid</span></span></li>
<li><span data-ttu-id="d64d6-122">Tiret</span><span class="sxs-lookup"><span data-stu-id="d64d6-122">Dash</span></span></li>
<li><span data-ttu-id="d64d6-123">Points</span><span class="sxs-lookup"><span data-stu-id="d64d6-123">Dot</span></span></li>
<li><span data-ttu-id="d64d6-124">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="d64d6-124">DashDot</span></span></li>
<li><span data-ttu-id="d64d6-125">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="d64d6-125">DashDotDot</span></span></li>
<li><span data-ttu-id="d64d6-126">Double</span><span class="sxs-lookup"><span data-stu-id="d64d6-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d64d6-127"><strong>Couleur</strong></span><span class="sxs-lookup"><span data-stu-id="d64d6-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="d64d6-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="d64d6-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d64d6-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d64d6-129">Optional</span></span></td>
<td><span data-ttu-id="d64d6-130">Couleur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d64d6-130">Color of the element.</span></span></td>
<td><span data-ttu-id="d64d6-131">Valeur RVB hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="d64d6-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="d64d6-132">Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="d64d6-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="d64d6-133">Par exemple, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="d64d6-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d64d6-134"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="d64d6-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="d64d6-135">SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d64d6-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="d64d6-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d64d6-136">Optional</span></span></td>
<td><span data-ttu-id="d64d6-137">Indique la marge de gauche ou de droite.</span><span class="sxs-lookup"><span data-stu-id="d64d6-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="d64d6-138">Gauche</span><span class="sxs-lookup"><span data-stu-id="d64d6-138">Left</span></span></li>
<li><span data-ttu-id="d64d6-139">Right</span><span class="sxs-lookup"><span data-stu-id="d64d6-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d64d6-140"><strong>Espacement</strong></span><span class="sxs-lookup"><span data-stu-id="d64d6-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="d64d6-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d64d6-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="d64d6-142">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d64d6-142">Optional</span></span></td>
<td><span data-ttu-id="d64d6-143">Espacement entre les bords des pages et des marges.</span><span class="sxs-lookup"><span data-stu-id="d64d6-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="d64d6-144">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="d64d6-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="d64d6-145">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d64d6-145">Element Information</span></span>



|  <span data-ttu-id="d64d6-146">Élément</span><span class="sxs-lookup"><span data-stu-id="d64d6-146">Element</span></span>     | <span data-ttu-id="d64d6-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="d64d6-147">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="d64d6-148">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d64d6-148">Element type</span></span> | <span data-ttu-id="d64d6-149">ComplexType [**MarginType**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="d64d6-149">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d64d6-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d64d6-150">Namespace</span></span>    | <span data-ttu-id="d64d6-151">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="d64d6-151">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="d64d6-152">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="d64d6-152">Schema name</span></span>  | <span data-ttu-id="d64d6-153">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="d64d6-153">Journal Reader</span></span>                                            |



 

 

 




