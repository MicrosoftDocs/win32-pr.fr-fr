---
description: Contient des informations de titre sur la note du journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Titre, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432221"
---
# <a name="title-element"></a><span data-ttu-id="145ce-103">Titre, élément</span><span class="sxs-lookup"><span data-stu-id="145ce-103">Title Element</span></span>

<span data-ttu-id="145ce-104">Contient des informations de titre sur la note du journal.</span><span class="sxs-lookup"><span data-stu-id="145ce-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="145ce-105">Définition</span><span class="sxs-lookup"><span data-stu-id="145ce-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="145ce-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="145ce-106">Parent Elements</span></span>

[<span data-ttu-id="145ce-107">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="145ce-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="145ce-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="145ce-108">Child Elements</span></span>

[<span data-ttu-id="145ce-109">**Partie titlearea**</span><span class="sxs-lookup"><span data-stu-id="145ce-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="145ce-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="145ce-110">Attributes</span></span>



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
<th><span data-ttu-id="145ce-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="145ce-111">Attribute</span></span></th>
<th><span data-ttu-id="145ce-112">Type</span><span class="sxs-lookup"><span data-stu-id="145ce-112">Type</span></span></th>
<th><span data-ttu-id="145ce-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="145ce-113">Required</span></span></th>
<th><span data-ttu-id="145ce-114">Description</span><span class="sxs-lookup"><span data-stu-id="145ce-114">Description</span></span></th>
<th><span data-ttu-id="145ce-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="145ce-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="145ce-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="145ce-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="145ce-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="145ce-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="145ce-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="145ce-118">Required</span></span></td>
<td><span data-ttu-id="145ce-119">Spécifie le type de bordure entourant le titre de la note.</span><span class="sxs-lookup"><span data-stu-id="145ce-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="145ce-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="145ce-120">None</span></span></li>
<li><span data-ttu-id="145ce-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="145ce-121">SolidSquare</span></span></li>
<li><span data-ttu-id="145ce-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="145ce-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="145ce-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="145ce-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="145ce-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="145ce-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="145ce-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="145ce-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="145ce-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="145ce-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="145ce-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="145ce-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="145ce-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="145ce-128">Required</span></span></td>
<td><span data-ttu-id="145ce-129">Définit si le titre contient une date ou non.</span><span class="sxs-lookup"><span data-stu-id="145ce-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="145ce-130">Aucun</span><span class="sxs-lookup"><span data-stu-id="145ce-130">None</span></span></li>
<li><span data-ttu-id="145ce-131">Court</span><span class="sxs-lookup"><span data-stu-id="145ce-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="145ce-132"><strong>Couleur</strong></span><span class="sxs-lookup"><span data-stu-id="145ce-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="145ce-133"><a href="colortype-simple-type.md"><strong>ColorType, simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="145ce-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="145ce-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="145ce-134">Optional</span></span></td>
<td><span data-ttu-id="145ce-135">Spécifie la couleur de l'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="145ce-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="145ce-136">Voir <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="145ce-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="145ce-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="145ce-137">Element Information</span></span>



| <span data-ttu-id="145ce-138">Élément</span><span class="sxs-lookup"><span data-stu-id="145ce-138">Element</span></span>      | <span data-ttu-id="145ce-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="145ce-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="145ce-140">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="145ce-140">Element type</span></span> | <span data-ttu-id="145ce-141">ComplexType [**TitleType**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="145ce-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="145ce-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="145ce-142">Namespace</span></span>    | <span data-ttu-id="145ce-143">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="145ce-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="145ce-144">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="145ce-144">Schema name</span></span>  | <span data-ttu-id="145ce-145">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="145ce-145">Journal Reader</span></span>                                          |



 

 

 



