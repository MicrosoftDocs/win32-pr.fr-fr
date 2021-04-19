---
description: Contient des informations de titre sur la note du journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Titre, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545126"
---
# <a name="title-element"></a><span data-ttu-id="c8769-103">Titre, élément</span><span class="sxs-lookup"><span data-stu-id="c8769-103">Title Element</span></span>

<span data-ttu-id="c8769-104">Contient des informations de titre sur la note du journal.</span><span class="sxs-lookup"><span data-stu-id="c8769-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="c8769-105">Définition</span><span class="sxs-lookup"><span data-stu-id="c8769-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="c8769-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c8769-106">Parent Elements</span></span>

[<span data-ttu-id="c8769-107">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="c8769-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="c8769-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c8769-108">Child Elements</span></span>

[<span data-ttu-id="c8769-109">**Partie titlearea**</span><span class="sxs-lookup"><span data-stu-id="c8769-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="c8769-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c8769-110">Attributes</span></span>



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
<th><span data-ttu-id="c8769-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="c8769-111">Attribute</span></span></th>
<th><span data-ttu-id="c8769-112">Type</span><span class="sxs-lookup"><span data-stu-id="c8769-112">Type</span></span></th>
<th><span data-ttu-id="c8769-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c8769-113">Required</span></span></th>
<th><span data-ttu-id="c8769-114">Description</span><span class="sxs-lookup"><span data-stu-id="c8769-114">Description</span></span></th>
<th><span data-ttu-id="c8769-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c8769-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8769-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="c8769-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="c8769-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="c8769-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="c8769-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c8769-118">Required</span></span></td>
<td><span data-ttu-id="c8769-119">Spécifie le type de bordure entourant le titre de la note.</span><span class="sxs-lookup"><span data-stu-id="c8769-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8769-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="c8769-120">None</span></span></li>
<li><span data-ttu-id="c8769-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="c8769-121">SolidSquare</span></span></li>
<li><span data-ttu-id="c8769-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="c8769-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="c8769-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="c8769-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="c8769-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="c8769-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="c8769-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="c8769-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8769-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="c8769-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="c8769-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="c8769-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="c8769-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c8769-128">Required</span></span></td>
<td><span data-ttu-id="c8769-129">Définit si le titre contient une date ou non.</span><span class="sxs-lookup"><span data-stu-id="c8769-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="c8769-130">Aucun</span><span class="sxs-lookup"><span data-stu-id="c8769-130">None</span></span></li>
<li><span data-ttu-id="c8769-131">Court</span><span class="sxs-lookup"><span data-stu-id="c8769-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8769-132"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="c8769-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="c8769-133"><a href="colortype-simple-type.md"><strong>ColorType, simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8769-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="c8769-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c8769-134">Optional</span></span></td>
<td><span data-ttu-id="c8769-135">Spécifie la couleur de l'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c8769-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="c8769-136">Voir <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c8769-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="c8769-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c8769-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="c8769-138">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c8769-138">Element type</span></span> | <span data-ttu-id="c8769-139">ComplexType [**TitleType**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="c8769-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="c8769-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8769-140">Namespace</span></span>    | <span data-ttu-id="c8769-141">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="c8769-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="c8769-142">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="c8769-142">Schema name</span></span>  | <span data-ttu-id="c8769-143">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="c8769-143">Journal Reader</span></span>                                          |



 

 

 



