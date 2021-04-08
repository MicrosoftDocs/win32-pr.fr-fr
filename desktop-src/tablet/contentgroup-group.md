---
description: Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Groupe ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034874"
---
# <a name="contentgroup-group"></a><span data-ttu-id="15739-103">Groupe ContentGroup</span><span class="sxs-lookup"><span data-stu-id="15739-103">ContentGroup Group</span></span>

<span data-ttu-id="15739-104">Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.</span><span class="sxs-lookup"><span data-stu-id="15739-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="15739-105">Définition</span><span class="sxs-lookup"><span data-stu-id="15739-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="15739-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="15739-106">Child Elements</span></span>

[<span data-ttu-id="15739-107">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="15739-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="15739-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="15739-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="15739-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="15739-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="15739-110">**Schéma**</span><span class="sxs-lookup"><span data-stu-id="15739-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="15739-111">**Texte**</span><span class="sxs-lookup"><span data-stu-id="15739-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="15739-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="15739-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="15739-113">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="15739-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="15739-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="15739-114">Attributes</span></span>



| <span data-ttu-id="15739-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="15739-115">Attribute</span></span>  | <span data-ttu-id="15739-116">Type</span><span class="sxs-lookup"><span data-stu-id="15739-116">Type</span></span>                      | <span data-ttu-id="15739-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="15739-117">Required</span></span> | <span data-ttu-id="15739-118">Description</span><span class="sxs-lookup"><span data-stu-id="15739-118">Description</span></span>                                                                                        | <span data-ttu-id="15739-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="15739-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="15739-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="15739-120">**Left**</span></span>   | <span data-ttu-id="15739-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="15739-121">**xs:integer**</span></span>            | <span data-ttu-id="15739-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="15739-122">Required</span></span> | <span data-ttu-id="15739-123">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="15739-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="15739-124">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="15739-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="15739-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="15739-125">**Top**</span></span>    | <span data-ttu-id="15739-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="15739-126">**xs:integer**</span></span>            | <span data-ttu-id="15739-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="15739-127">Required</span></span> | <span data-ttu-id="15739-128">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="15739-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="15739-129">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="15739-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="15739-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="15739-130">**Width**</span></span>  | <span data-ttu-id="15739-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="15739-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="15739-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="15739-132">Required</span></span> | <span data-ttu-id="15739-133">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="15739-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="15739-134">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="15739-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="15739-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="15739-135">**Height**</span></span> | <span data-ttu-id="15739-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="15739-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="15739-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="15739-137">Required</span></span> | <span data-ttu-id="15739-138">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="15739-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="15739-139">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="15739-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="15739-140">Informations de type</span><span class="sxs-lookup"><span data-stu-id="15739-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="15739-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="15739-141">Namespace</span></span>   | <span data-ttu-id="15739-142">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="15739-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="15739-143">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="15739-143">Schema name</span></span> | <span data-ttu-id="15739-144">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="15739-144">Journal Reader</span></span>                             |



 

 

 




