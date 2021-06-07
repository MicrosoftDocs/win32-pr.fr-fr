---
description: Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Groupe ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432611"
---
# <a name="contentgroup-group"></a><span data-ttu-id="96edf-103">Groupe ContentGroup</span><span class="sxs-lookup"><span data-stu-id="96edf-103">ContentGroup Group</span></span>

<span data-ttu-id="96edf-104">Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.</span><span class="sxs-lookup"><span data-stu-id="96edf-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="96edf-105">Définition</span><span class="sxs-lookup"><span data-stu-id="96edf-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="96edf-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="96edf-106">Child Elements</span></span>

[<span data-ttu-id="96edf-107">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="96edf-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="96edf-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="96edf-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="96edf-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="96edf-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="96edf-110">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="96edf-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="96edf-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="96edf-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="96edf-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="96edf-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="96edf-113">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="96edf-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="96edf-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="96edf-114">Attributes</span></span>



| <span data-ttu-id="96edf-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="96edf-115">Attribute</span></span>  | <span data-ttu-id="96edf-116">Type</span><span class="sxs-lookup"><span data-stu-id="96edf-116">Type</span></span>                      | <span data-ttu-id="96edf-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96edf-117">Required</span></span> | <span data-ttu-id="96edf-118">Description</span><span class="sxs-lookup"><span data-stu-id="96edf-118">Description</span></span>                                                                                        | <span data-ttu-id="96edf-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="96edf-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="96edf-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="96edf-120">**Left**</span></span>   | <span data-ttu-id="96edf-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="96edf-121">**xs:integer**</span></span>            | <span data-ttu-id="96edf-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96edf-122">Required</span></span> | <span data-ttu-id="96edf-123">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="96edf-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="96edf-124">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="96edf-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="96edf-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="96edf-125">**Top**</span></span>    | <span data-ttu-id="96edf-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="96edf-126">**xs:integer**</span></span>            | <span data-ttu-id="96edf-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96edf-127">Required</span></span> | <span data-ttu-id="96edf-128">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="96edf-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="96edf-129">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="96edf-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="96edf-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="96edf-130">**Width**</span></span>  | <span data-ttu-id="96edf-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="96edf-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="96edf-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96edf-132">Required</span></span> | <span data-ttu-id="96edf-133">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="96edf-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="96edf-134">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="96edf-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="96edf-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="96edf-135">**Height**</span></span> | <span data-ttu-id="96edf-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="96edf-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="96edf-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96edf-137">Required</span></span> | <span data-ttu-id="96edf-138">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="96edf-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="96edf-139">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="96edf-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="96edf-140">Informations de type</span><span class="sxs-lookup"><span data-stu-id="96edf-140">Type Information</span></span>



|  <span data-ttu-id="96edf-141">Élément</span><span class="sxs-lookup"><span data-stu-id="96edf-141">Element</span></span>     | <span data-ttu-id="96edf-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="96edf-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="96edf-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="96edf-143">Namespace</span></span>   | <span data-ttu-id="96edf-144">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="96edf-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="96edf-145">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="96edf-145">Schema name</span></span> | <span data-ttu-id="96edf-146">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="96edf-146">Journal Reader</span></span>                             |



 

 

 




