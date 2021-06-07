---
description: Contient le contenu d’une page de journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Élément de contenu [lecteur de journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432151"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="df4d8-103">Lecteur du journal des éléments de contenu \[\]</span><span class="sxs-lookup"><span data-stu-id="df4d8-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="df4d8-104">Contient le contenu d’une page de journal.</span><span class="sxs-lookup"><span data-stu-id="df4d8-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="df4d8-105">Définition</span><span class="sxs-lookup"><span data-stu-id="df4d8-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="df4d8-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="df4d8-106">Parent Elements</span></span>

[<span data-ttu-id="df4d8-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="df4d8-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="df4d8-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="df4d8-108">Child Elements</span></span>

[<span data-ttu-id="df4d8-109">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="df4d8-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="df4d8-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="df4d8-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="df4d8-111">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="df4d8-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="df4d8-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="df4d8-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="df4d8-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="df4d8-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="df4d8-114">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="df4d8-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="df4d8-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="df4d8-115">Attributes</span></span>



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
<th><span data-ttu-id="df4d8-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="df4d8-116">Attribute</span></span></th>
<th><span data-ttu-id="df4d8-117">Type</span><span class="sxs-lookup"><span data-stu-id="df4d8-117">Type</span></span></th>
<th><span data-ttu-id="df4d8-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df4d8-118">Required</span></span></th>
<th><span data-ttu-id="df4d8-119">Description</span><span class="sxs-lookup"><span data-stu-id="df4d8-119">Description</span></span></th>
<th><span data-ttu-id="df4d8-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="df4d8-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df4d8-121"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="df4d8-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="df4d8-122"><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="df4d8-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="df4d8-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df4d8-123">Required</span></span></td>
<td><span data-ttu-id="df4d8-124">Si le type est &quot; inerte &quot; , le contenu ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="df4d8-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df4d8-125">Normal</span><span class="sxs-lookup"><span data-stu-id="df4d8-125">Normal</span></span></li>
<li><span data-ttu-id="df4d8-126">Inertes</span><span class="sxs-lookup"><span data-stu-id="df4d8-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="df4d8-127">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="df4d8-127">Element Information</span></span>



|  <span data-ttu-id="df4d8-128">Élément</span><span class="sxs-lookup"><span data-stu-id="df4d8-128">Element</span></span>     | <span data-ttu-id="df4d8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="df4d8-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="df4d8-130">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="df4d8-130">Element type</span></span> | <span data-ttu-id="df4d8-131">ComplexType [**ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="df4d8-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="df4d8-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df4d8-132">Namespace</span></span>    | <span data-ttu-id="df4d8-133">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="df4d8-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="df4d8-134">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="df4d8-134">Schema name</span></span>  | <span data-ttu-id="df4d8-135">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="df4d8-135">Journal Reader</span></span>                                              |



 

 

 




