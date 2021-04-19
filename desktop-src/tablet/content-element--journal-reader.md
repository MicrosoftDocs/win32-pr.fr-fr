---
description: Contient le contenu d’une page de journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Élément de contenu [lecteur de journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529313"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="9e677-103">Lecteur du journal des éléments de contenu \[\]</span><span class="sxs-lookup"><span data-stu-id="9e677-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="9e677-104">Contient le contenu d’une page de journal.</span><span class="sxs-lookup"><span data-stu-id="9e677-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="9e677-105">Définition</span><span class="sxs-lookup"><span data-stu-id="9e677-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="9e677-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9e677-106">Parent Elements</span></span>

[<span data-ttu-id="9e677-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="9e677-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="9e677-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9e677-108">Child Elements</span></span>

[<span data-ttu-id="9e677-109">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="9e677-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="9e677-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="9e677-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="9e677-111">**Schéma**</span><span class="sxs-lookup"><span data-stu-id="9e677-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="9e677-112">**Texte**</span><span class="sxs-lookup"><span data-stu-id="9e677-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="9e677-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="9e677-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="9e677-114">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="9e677-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="9e677-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="9e677-115">Attributes</span></span>



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
<th><span data-ttu-id="9e677-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="9e677-116">Attribute</span></span></th>
<th><span data-ttu-id="9e677-117">Type</span><span class="sxs-lookup"><span data-stu-id="9e677-117">Type</span></span></th>
<th><span data-ttu-id="9e677-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9e677-118">Required</span></span></th>
<th><span data-ttu-id="9e677-119">Description</span><span class="sxs-lookup"><span data-stu-id="9e677-119">Description</span></span></th>
<th><span data-ttu-id="9e677-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="9e677-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e677-121"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="9e677-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="9e677-122"><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="9e677-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="9e677-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9e677-123">Required</span></span></td>
<td><span data-ttu-id="9e677-124">Si le type est &quot; inerte &quot; , le contenu ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="9e677-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="9e677-125">Normal</span><span class="sxs-lookup"><span data-stu-id="9e677-125">Normal</span></span></li>
<li><span data-ttu-id="9e677-126">Inertes</span><span class="sxs-lookup"><span data-stu-id="9e677-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="9e677-127">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9e677-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="9e677-128">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="9e677-128">Element type</span></span> | <span data-ttu-id="9e677-129">ComplexType [**ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="9e677-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="9e677-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e677-130">Namespace</span></span>    | <span data-ttu-id="9e677-131">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="9e677-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="9e677-132">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="9e677-132">Schema name</span></span>  | <span data-ttu-id="9e677-133">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="9e677-133">Journal Reader</span></span>                                              |



 

 

 




