---
description: Contient le contenu qui a été classifié par l’analyseur ou par l’utilisateur en tant que dessin.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Élément Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520183"
---
# <a name="drawing-element"></a><span data-ttu-id="73fc6-103">Élément Drawing</span><span class="sxs-lookup"><span data-stu-id="73fc6-103">Drawing Element</span></span>

<span data-ttu-id="73fc6-104">Contient le contenu qui a été classifié par l’analyseur ou par l’utilisateur en tant que dessin.</span><span class="sxs-lookup"><span data-stu-id="73fc6-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="73fc6-105">Définition</span><span class="sxs-lookup"><span data-stu-id="73fc6-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="73fc6-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="73fc6-106">Parent Elements</span></span>

[<span data-ttu-id="73fc6-107">**Content**</span><span class="sxs-lookup"><span data-stu-id="73fc6-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="73fc6-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="73fc6-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="73fc6-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="73fc6-109">Child Elements</span></span>

[<span data-ttu-id="73fc6-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="73fc6-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="73fc6-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="73fc6-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="73fc6-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="73fc6-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="73fc6-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="73fc6-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="73fc6-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="73fc6-114">Attributes</span></span>



| <span data-ttu-id="73fc6-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="73fc6-115">Attribute</span></span>  | <span data-ttu-id="73fc6-116">Type</span><span class="sxs-lookup"><span data-stu-id="73fc6-116">Type</span></span>                      | <span data-ttu-id="73fc6-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73fc6-117">Required</span></span> | <span data-ttu-id="73fc6-118">Description</span><span class="sxs-lookup"><span data-stu-id="73fc6-118">Description</span></span>                                                                             | <span data-ttu-id="73fc6-119">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="73fc6-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="73fc6-120">**Left**</span><span class="sxs-lookup"><span data-stu-id="73fc6-120">**Left**</span></span>   | <span data-ttu-id="73fc6-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="73fc6-121">**xs:integer**</span></span>            | <span data-ttu-id="73fc6-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73fc6-122">Required</span></span> | <span data-ttu-id="73fc6-123">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="73fc6-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="73fc6-124">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="73fc6-124">Any integer.</span></span>              |
| <span data-ttu-id="73fc6-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="73fc6-125">**Top**</span></span>    | <span data-ttu-id="73fc6-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="73fc6-126">**xs:integer**</span></span>            | <span data-ttu-id="73fc6-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73fc6-127">Required</span></span> | <span data-ttu-id="73fc6-128">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="73fc6-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="73fc6-129">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="73fc6-129">Any integer.</span></span>              |
| <span data-ttu-id="73fc6-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="73fc6-130">**Width**</span></span>  | <span data-ttu-id="73fc6-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="73fc6-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="73fc6-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73fc6-132">Required</span></span> | <span data-ttu-id="73fc6-133">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="73fc6-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="73fc6-134">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="73fc6-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="73fc6-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="73fc6-135">**Height**</span></span> | <span data-ttu-id="73fc6-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="73fc6-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="73fc6-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73fc6-137">Required</span></span> | <span data-ttu-id="73fc6-138">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="73fc6-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="73fc6-139">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="73fc6-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="73fc6-140">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="73fc6-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="73fc6-141">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="73fc6-141">Element type</span></span> | <span data-ttu-id="73fc6-142">ComplexType [**DrawingType**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="73fc6-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="73fc6-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73fc6-143">Namespace</span></span>    | <span data-ttu-id="73fc6-144">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="73fc6-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="73fc6-145">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="73fc6-145">Schema name</span></span>  | <span data-ttu-id="73fc6-146">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="73fc6-146">Journal Reader</span></span>                                              |



 

 

 



