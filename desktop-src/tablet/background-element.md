---
description: Contient l’arrière-plan d’un élément JournalDocument ou d’un élément JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Élément d’arrière-plan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530662"
---
# <a name="background-element"></a><span data-ttu-id="3ee07-103">Élément d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="3ee07-103">Background Element</span></span>

<span data-ttu-id="3ee07-104">Contient l’arrière-plan d’un élément [**JournalDocument**](journaldocument-element.md) ou d’un élément [**JournalPage**](journalpage-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3ee07-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="3ee07-105">Définition</span><span class="sxs-lookup"><span data-stu-id="3ee07-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="3ee07-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3ee07-106">Parent Elements</span></span>

[<span data-ttu-id="3ee07-107">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="3ee07-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="3ee07-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3ee07-108">Child Elements</span></span>

[<span data-ttu-id="3ee07-109">**Image**</span><span class="sxs-lookup"><span data-stu-id="3ee07-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="3ee07-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ee07-110">Attributes</span></span>



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
<th><span data-ttu-id="3ee07-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="3ee07-111">Attribute</span></span></th>
<th><span data-ttu-id="3ee07-112">Type</span><span class="sxs-lookup"><span data-stu-id="3ee07-112">Type</span></span></th>
<th><span data-ttu-id="3ee07-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3ee07-113">Required</span></span></th>
<th><span data-ttu-id="3ee07-114">Description</span><span class="sxs-lookup"><span data-stu-id="3ee07-114">Description</span></span></th>
<th><span data-ttu-id="3ee07-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3ee07-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ee07-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="3ee07-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="3ee07-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="3ee07-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="3ee07-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3ee07-118">Required</span></span></td>
<td><span data-ttu-id="3ee07-119">Spécifie le style de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3ee07-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ee07-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="3ee07-120">None</span></span></li>
<li><span data-ttu-id="3ee07-121">Unie</span><span class="sxs-lookup"><span data-stu-id="3ee07-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ee07-122"><strong>Color</strong></span><span class="sxs-lookup"><span data-stu-id="3ee07-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="3ee07-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</span><span class="sxs-lookup"><span data-stu-id="3ee07-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="3ee07-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3ee07-124">Optional</span></span></td>
<td><span data-ttu-id="3ee07-125">Spécifie la couleur de l'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3ee07-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="3ee07-126">Voir <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span><span class="sxs-lookup"><span data-stu-id="3ee07-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="3ee07-127">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3ee07-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="3ee07-128">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="3ee07-128">Element type</span></span> | <span data-ttu-id="3ee07-129">ComplexType [**BackgroundType**](backgroundtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="3ee07-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="3ee07-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ee07-130">Namespace</span></span>    | <span data-ttu-id="3ee07-131">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="3ee07-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="3ee07-132">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="3ee07-132">Schema name</span></span>  | <span data-ttu-id="3ee07-133">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="3ee07-133">Journal Reader</span></span>                                                    |



 

 

 



