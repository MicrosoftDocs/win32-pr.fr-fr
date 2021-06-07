---
description: Contient un ensemble d’éléments&\# 8212 ; Paragraph, InkWord, Drawing, text, image ou Flag&\# 8212 ; qui sont regroupés dans la note du journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Élément, nœud
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432570"
---
# <a name="groupnode-element"></a><span data-ttu-id="04a3b-103">Élément, nœud</span><span class="sxs-lookup"><span data-stu-id="04a3b-103">GroupNode Element</span></span>

<span data-ttu-id="04a3b-104">Contient un ensemble d’éléments ([**paragraphe**](paragraph-element.md), [**InkWord**](inkword-element.md), [**dessin**](drawing-element.md), [**texte**](text-element.md), [**image**](image-element.md)ou [**indicateur**](flag-element.md)) regroupés dans la note du journal.</span><span class="sxs-lookup"><span data-stu-id="04a3b-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="04a3b-105">Définition</span><span class="sxs-lookup"><span data-stu-id="04a3b-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="04a3b-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="04a3b-106">Parent Elements</span></span>

[<span data-ttu-id="04a3b-107">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="04a3b-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="04a3b-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="04a3b-108">Child Elements</span></span>

[<span data-ttu-id="04a3b-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="04a3b-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="04a3b-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="04a3b-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="04a3b-111">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="04a3b-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="04a3b-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="04a3b-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="04a3b-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="04a3b-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="04a3b-114">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="04a3b-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="04a3b-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="04a3b-115">Attributes</span></span>



| <span data-ttu-id="04a3b-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="04a3b-116">Attribute</span></span>  | <span data-ttu-id="04a3b-117">Type</span><span class="sxs-lookup"><span data-stu-id="04a3b-117">Type</span></span>                      | <span data-ttu-id="04a3b-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="04a3b-118">Required</span></span> | <span data-ttu-id="04a3b-119">Description</span><span class="sxs-lookup"><span data-stu-id="04a3b-119">Description</span></span>                                                                             | <span data-ttu-id="04a3b-120">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="04a3b-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="04a3b-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="04a3b-121">**Left**</span></span>   | <span data-ttu-id="04a3b-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="04a3b-122">**xs:integer**</span></span>            | <span data-ttu-id="04a3b-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="04a3b-123">Required</span></span> | <span data-ttu-id="04a3b-124">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="04a3b-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="04a3b-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="04a3b-125">Any integer.</span></span>              |
| <span data-ttu-id="04a3b-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="04a3b-126">**Top**</span></span>    | <span data-ttu-id="04a3b-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="04a3b-127">**xs:integer**</span></span>            | <span data-ttu-id="04a3b-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="04a3b-128">Required</span></span> | <span data-ttu-id="04a3b-129">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="04a3b-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="04a3b-130">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="04a3b-130">Any integer.</span></span>              |
| <span data-ttu-id="04a3b-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="04a3b-131">**Width**</span></span>  | <span data-ttu-id="04a3b-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="04a3b-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="04a3b-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="04a3b-133">Required</span></span> | <span data-ttu-id="04a3b-134">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="04a3b-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="04a3b-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="04a3b-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="04a3b-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="04a3b-136">**Height**</span></span> | <span data-ttu-id="04a3b-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="04a3b-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="04a3b-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="04a3b-138">Required</span></span> | <span data-ttu-id="04a3b-139">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="04a3b-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="04a3b-140">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="04a3b-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="04a3b-141">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="04a3b-141">Element Information</span></span>



|  <span data-ttu-id="04a3b-142">Élément</span><span class="sxs-lookup"><span data-stu-id="04a3b-142">Element</span></span>     | <span data-ttu-id="04a3b-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="04a3b-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="04a3b-144">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="04a3b-144">Element type</span></span> | <span data-ttu-id="04a3b-145">ComplexType [**GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="04a3b-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="04a3b-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04a3b-146">Namespace</span></span>    | <span data-ttu-id="04a3b-147">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="04a3b-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="04a3b-148">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="04a3b-148">Schema name</span></span>  | <span data-ttu-id="04a3b-149">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="04a3b-149">Journal Reader</span></span>                                                  |



 

 

 



