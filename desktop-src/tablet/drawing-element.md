---
description: Contient le contenu qui a été classifié par l’analyseur ou par l’utilisateur en tant que dessin.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Élément Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432511"
---
# <a name="drawing-element"></a><span data-ttu-id="45d59-103">Élément Drawing</span><span class="sxs-lookup"><span data-stu-id="45d59-103">Drawing Element</span></span>

<span data-ttu-id="45d59-104">Contient le contenu qui a été classifié par l’analyseur ou par l’utilisateur en tant que dessin.</span><span class="sxs-lookup"><span data-stu-id="45d59-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="45d59-105">Définition</span><span class="sxs-lookup"><span data-stu-id="45d59-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="45d59-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="45d59-106">Parent Elements</span></span>

[<span data-ttu-id="45d59-107">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="45d59-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="45d59-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="45d59-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="45d59-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="45d59-109">Child Elements</span></span>

[<span data-ttu-id="45d59-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="45d59-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="45d59-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="45d59-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="45d59-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="45d59-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="45d59-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="45d59-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="45d59-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="45d59-114">Attributes</span></span>



| <span data-ttu-id="45d59-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="45d59-115">Attribute</span></span>  | <span data-ttu-id="45d59-116">Type</span><span class="sxs-lookup"><span data-stu-id="45d59-116">Type</span></span>                      | <span data-ttu-id="45d59-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="45d59-117">Required</span></span> | <span data-ttu-id="45d59-118">Description</span><span class="sxs-lookup"><span data-stu-id="45d59-118">Description</span></span>                                                                             | <span data-ttu-id="45d59-119">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="45d59-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="45d59-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="45d59-120">**Left**</span></span>   | <span data-ttu-id="45d59-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="45d59-121">**xs:integer**</span></span>            | <span data-ttu-id="45d59-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="45d59-122">Required</span></span> | <span data-ttu-id="45d59-123">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="45d59-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="45d59-124">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="45d59-124">Any integer.</span></span>              |
| <span data-ttu-id="45d59-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="45d59-125">**Top**</span></span>    | <span data-ttu-id="45d59-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="45d59-126">**xs:integer**</span></span>            | <span data-ttu-id="45d59-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="45d59-127">Required</span></span> | <span data-ttu-id="45d59-128">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="45d59-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="45d59-129">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="45d59-129">Any integer.</span></span>              |
| <span data-ttu-id="45d59-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="45d59-130">**Width**</span></span>  | <span data-ttu-id="45d59-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="45d59-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="45d59-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="45d59-132">Required</span></span> | <span data-ttu-id="45d59-133">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="45d59-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="45d59-134">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="45d59-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="45d59-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="45d59-135">**Height**</span></span> | <span data-ttu-id="45d59-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="45d59-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="45d59-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="45d59-137">Required</span></span> | <span data-ttu-id="45d59-138">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="45d59-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="45d59-139">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="45d59-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="45d59-140">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="45d59-140">Element Information</span></span>



|  <span data-ttu-id="45d59-141">Élément</span><span class="sxs-lookup"><span data-stu-id="45d59-141">Element</span></span>     | <span data-ttu-id="45d59-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="45d59-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="45d59-143">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="45d59-143">Element type</span></span> | <span data-ttu-id="45d59-144">ComplexType [**DrawingType**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="45d59-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="45d59-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45d59-145">Namespace</span></span>    | <span data-ttu-id="45d59-146">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="45d59-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="45d59-147">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="45d59-147">Schema name</span></span>  | <span data-ttu-id="45d59-148">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="45d59-148">Journal Reader</span></span>                                              |



 

 

 



