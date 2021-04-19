---
description: Contient un ensemble d’éléments&\# 8212 ; Paragraph, InkWord, Drawing, text, image ou Flag&\# 8212 ; qui sont regroupés dans la note du journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Élément, nœud
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516887"
---
# <a name="groupnode-element"></a><span data-ttu-id="54bf2-103">Élément, nœud</span><span class="sxs-lookup"><span data-stu-id="54bf2-103">GroupNode Element</span></span>

<span data-ttu-id="54bf2-104">Contient un ensemble d’éléments ([**paragraphe**](paragraph-element.md), [**InkWord**](inkword-element.md), [**dessin**](drawing-element.md), [**texte**](text-element.md), [**image**](image-element.md)ou [**indicateur**](flag-element.md)) regroupés dans la note du journal.</span><span class="sxs-lookup"><span data-stu-id="54bf2-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="54bf2-105">Définition</span><span class="sxs-lookup"><span data-stu-id="54bf2-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="54bf2-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="54bf2-106">Parent Elements</span></span>

[<span data-ttu-id="54bf2-107">**Content**</span><span class="sxs-lookup"><span data-stu-id="54bf2-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="54bf2-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="54bf2-108">Child Elements</span></span>

[<span data-ttu-id="54bf2-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="54bf2-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="54bf2-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="54bf2-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="54bf2-111">**Schéma**</span><span class="sxs-lookup"><span data-stu-id="54bf2-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="54bf2-112">**Texte**</span><span class="sxs-lookup"><span data-stu-id="54bf2-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="54bf2-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="54bf2-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="54bf2-114">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="54bf2-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="54bf2-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="54bf2-115">Attributes</span></span>



| <span data-ttu-id="54bf2-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="54bf2-116">Attribute</span></span>  | <span data-ttu-id="54bf2-117">Type</span><span class="sxs-lookup"><span data-stu-id="54bf2-117">Type</span></span>                      | <span data-ttu-id="54bf2-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="54bf2-118">Required</span></span> | <span data-ttu-id="54bf2-119">Description</span><span class="sxs-lookup"><span data-stu-id="54bf2-119">Description</span></span>                                                                             | <span data-ttu-id="54bf2-120">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="54bf2-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="54bf2-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="54bf2-121">**Left**</span></span>   | <span data-ttu-id="54bf2-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="54bf2-122">**xs:integer**</span></span>            | <span data-ttu-id="54bf2-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="54bf2-123">Required</span></span> | <span data-ttu-id="54bf2-124">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="54bf2-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="54bf2-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="54bf2-125">Any integer.</span></span>              |
| <span data-ttu-id="54bf2-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="54bf2-126">**Top**</span></span>    | <span data-ttu-id="54bf2-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="54bf2-127">**xs:integer**</span></span>            | <span data-ttu-id="54bf2-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="54bf2-128">Required</span></span> | <span data-ttu-id="54bf2-129">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="54bf2-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="54bf2-130">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="54bf2-130">Any integer.</span></span>              |
| <span data-ttu-id="54bf2-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="54bf2-131">**Width**</span></span>  | <span data-ttu-id="54bf2-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="54bf2-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="54bf2-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="54bf2-133">Required</span></span> | <span data-ttu-id="54bf2-134">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="54bf2-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="54bf2-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="54bf2-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="54bf2-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="54bf2-136">**Height**</span></span> | <span data-ttu-id="54bf2-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="54bf2-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="54bf2-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="54bf2-138">Required</span></span> | <span data-ttu-id="54bf2-139">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="54bf2-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="54bf2-140">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="54bf2-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="54bf2-141">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="54bf2-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="54bf2-142">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="54bf2-142">Element type</span></span> | <span data-ttu-id="54bf2-143">ComplexType [**GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="54bf2-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="54bf2-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="54bf2-144">Namespace</span></span>    | <span data-ttu-id="54bf2-145">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="54bf2-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="54bf2-146">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="54bf2-146">Schema name</span></span>  | <span data-ttu-id="54bf2-147">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="54bf2-147">Journal Reader</span></span>                                                  |



 

 

 



