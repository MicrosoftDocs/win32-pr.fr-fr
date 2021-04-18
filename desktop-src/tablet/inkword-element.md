---
description: Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Élément InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536682"
---
# <a name="inkword-element"></a><span data-ttu-id="56212-103">Élément InkWord</span><span class="sxs-lookup"><span data-stu-id="56212-103">InkWord Element</span></span>

<span data-ttu-id="56212-104">Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.</span><span class="sxs-lookup"><span data-stu-id="56212-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="56212-105">Définition</span><span class="sxs-lookup"><span data-stu-id="56212-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="56212-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="56212-106">Parent Elements</span></span>

[<span data-ttu-id="56212-107">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="56212-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="56212-108">**Lignes**</span><span class="sxs-lookup"><span data-stu-id="56212-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="56212-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="56212-109">Child Elements</span></span>

[<span data-ttu-id="56212-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="56212-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="56212-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="56212-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="56212-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="56212-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="56212-113">**Garantir**</span><span class="sxs-lookup"><span data-stu-id="56212-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="56212-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="56212-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="56212-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="56212-115">Attributes</span></span>



| <span data-ttu-id="56212-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="56212-116">Attribute</span></span>  | <span data-ttu-id="56212-117">Type</span><span class="sxs-lookup"><span data-stu-id="56212-117">Type</span></span>                      | <span data-ttu-id="56212-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="56212-118">Required</span></span> | <span data-ttu-id="56212-119">Description</span><span class="sxs-lookup"><span data-stu-id="56212-119">Description</span></span>                                                                             | <span data-ttu-id="56212-120">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="56212-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="56212-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="56212-121">**Left**</span></span>   | <span data-ttu-id="56212-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="56212-122">**xs:integer**</span></span>            | <span data-ttu-id="56212-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="56212-123">Required</span></span> | <span data-ttu-id="56212-124">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="56212-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="56212-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="56212-125">Any integer.</span></span>              |
| <span data-ttu-id="56212-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="56212-126">**Top**</span></span>    | <span data-ttu-id="56212-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="56212-127">**xs:integer**</span></span>            | <span data-ttu-id="56212-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="56212-128">Required</span></span> | <span data-ttu-id="56212-129">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="56212-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="56212-130">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="56212-130">Any integer.</span></span>              |
| <span data-ttu-id="56212-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="56212-131">**Width**</span></span>  | <span data-ttu-id="56212-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="56212-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="56212-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="56212-133">Required</span></span> | <span data-ttu-id="56212-134">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="56212-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="56212-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="56212-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="56212-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="56212-136">**Height**</span></span> | <span data-ttu-id="56212-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="56212-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="56212-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="56212-138">Required</span></span> | <span data-ttu-id="56212-139">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="56212-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="56212-140">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="56212-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="56212-141">Le mappage de coordonnées internes du mot d’encre est l’unité métrique anglaise et un multiplicateur de 2,54 doit être utilisé par votre application pour convertir les valeurs de largeur et de hauteur en unités HIMETRIC utilisées par les API de la plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="56212-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="56212-142">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="56212-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="56212-143">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="56212-143">Element type</span></span> | <span data-ttu-id="56212-144">ComplexType [**InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="56212-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="56212-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="56212-145">Namespace</span></span>    | <span data-ttu-id="56212-146">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="56212-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="56212-147">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="56212-147">Schema name</span></span>  | <span data-ttu-id="56212-148">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="56212-148">Journal Reader</span></span>                                              |



 

 

 



