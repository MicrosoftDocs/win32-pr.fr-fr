---
description: Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Élément Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530101"
---
# <a name="image-element"></a><span data-ttu-id="b6030-103">Élément Image</span><span class="sxs-lookup"><span data-stu-id="b6030-103">Image Element</span></span>

<span data-ttu-id="b6030-104">Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b6030-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="b6030-105">Définition</span><span class="sxs-lookup"><span data-stu-id="b6030-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="b6030-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b6030-106">Parent Elements</span></span>

[<span data-ttu-id="b6030-107">**Content**</span><span class="sxs-lookup"><span data-stu-id="b6030-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="b6030-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="b6030-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="b6030-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6030-109">Child Elements</span></span>

<span data-ttu-id="b6030-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="b6030-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="b6030-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="b6030-111">Attributes</span></span>



| <span data-ttu-id="b6030-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="b6030-112">Attribute</span></span>  | <span data-ttu-id="b6030-113">Type</span><span class="sxs-lookup"><span data-stu-id="b6030-113">Type</span></span>                      | <span data-ttu-id="b6030-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b6030-114">Required</span></span> | <span data-ttu-id="b6030-115">Description</span><span class="sxs-lookup"><span data-stu-id="b6030-115">Description</span></span>                                                                             | <span data-ttu-id="b6030-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b6030-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="b6030-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="b6030-117">**Left**</span></span>   | <span data-ttu-id="b6030-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b6030-118">**xs:integer**</span></span>            | <span data-ttu-id="b6030-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b6030-119">Required</span></span> | <span data-ttu-id="b6030-120">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b6030-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="b6030-121">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="b6030-121">Any integer.</span></span>              |
| <span data-ttu-id="b6030-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="b6030-122">**Top**</span></span>    | <span data-ttu-id="b6030-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b6030-123">**xs:integer**</span></span>            | <span data-ttu-id="b6030-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b6030-124">Required</span></span> | <span data-ttu-id="b6030-125">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b6030-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="b6030-126">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="b6030-126">Any integer.</span></span>              |
| <span data-ttu-id="b6030-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="b6030-127">**Width**</span></span>  | <span data-ttu-id="b6030-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b6030-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b6030-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b6030-129">Required</span></span> | <span data-ttu-id="b6030-130">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="b6030-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="b6030-131">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="b6030-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="b6030-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="b6030-132">**Height**</span></span> | <span data-ttu-id="b6030-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b6030-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b6030-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b6030-134">Required</span></span> | <span data-ttu-id="b6030-135">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="b6030-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="b6030-136">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="b6030-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="b6030-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6030-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="b6030-138">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b6030-138">Element type</span></span> | <span data-ttu-id="b6030-139">ComplexType [**ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="b6030-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b6030-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6030-140">Namespace</span></span>    | <span data-ttu-id="b6030-141">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="b6030-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="b6030-142">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="b6030-142">Schema name</span></span>  | <span data-ttu-id="b6030-143">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="b6030-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="b6030-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6030-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6030-145">**Arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="b6030-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



