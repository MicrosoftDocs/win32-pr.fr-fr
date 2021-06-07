---
description: Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Élément Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432581"
---
# <a name="image-element"></a><span data-ttu-id="aa149-103">Élément Image</span><span class="sxs-lookup"><span data-stu-id="aa149-103">Image Element</span></span>

<span data-ttu-id="aa149-104">Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="aa149-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="aa149-105">Définition</span><span class="sxs-lookup"><span data-stu-id="aa149-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="aa149-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="aa149-106">Parent Elements</span></span>

[<span data-ttu-id="aa149-107">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="aa149-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="aa149-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="aa149-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="aa149-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aa149-109">Child Elements</span></span>

<span data-ttu-id="aa149-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aa149-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="aa149-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="aa149-111">Attributes</span></span>



| <span data-ttu-id="aa149-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="aa149-112">Attribute</span></span>  | <span data-ttu-id="aa149-113">Type</span><span class="sxs-lookup"><span data-stu-id="aa149-113">Type</span></span>                      | <span data-ttu-id="aa149-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa149-114">Required</span></span> | <span data-ttu-id="aa149-115">Description</span><span class="sxs-lookup"><span data-stu-id="aa149-115">Description</span></span>                                                                             | <span data-ttu-id="aa149-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="aa149-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="aa149-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="aa149-117">**Left**</span></span>   | <span data-ttu-id="aa149-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa149-118">**xs:integer**</span></span>            | <span data-ttu-id="aa149-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa149-119">Required</span></span> | <span data-ttu-id="aa149-120">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="aa149-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="aa149-121">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="aa149-121">Any integer.</span></span>              |
| <span data-ttu-id="aa149-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="aa149-122">**Top**</span></span>    | <span data-ttu-id="aa149-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa149-123">**xs:integer**</span></span>            | <span data-ttu-id="aa149-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa149-124">Required</span></span> | <span data-ttu-id="aa149-125">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="aa149-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="aa149-126">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="aa149-126">Any integer.</span></span>              |
| <span data-ttu-id="aa149-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="aa149-127">**Width**</span></span>  | <span data-ttu-id="aa149-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa149-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa149-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa149-129">Required</span></span> | <span data-ttu-id="aa149-130">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="aa149-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="aa149-131">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="aa149-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="aa149-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="aa149-132">**Height**</span></span> | <span data-ttu-id="aa149-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa149-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa149-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa149-134">Required</span></span> | <span data-ttu-id="aa149-135">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="aa149-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="aa149-136">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="aa149-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="aa149-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="aa149-137">Element Information</span></span>



|  <span data-ttu-id="aa149-138">Élément</span><span class="sxs-lookup"><span data-stu-id="aa149-138">Element</span></span>     | <span data-ttu-id="aa149-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa149-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="aa149-140">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="aa149-140">Element type</span></span> | <span data-ttu-id="aa149-141">ComplexType [**ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="aa149-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="aa149-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aa149-142">Namespace</span></span>    | <span data-ttu-id="aa149-143">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="aa149-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="aa149-144">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="aa149-144">Schema name</span></span>  | <span data-ttu-id="aa149-145">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="aa149-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="aa149-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa149-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa149-147">**Arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="aa149-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



