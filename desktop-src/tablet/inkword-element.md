---
description: Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Élément InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432391"
---
# <a name="inkword-element"></a><span data-ttu-id="bbf40-103">Élément InkWord</span><span class="sxs-lookup"><span data-stu-id="bbf40-103">InkWord Element</span></span>

<span data-ttu-id="bbf40-104">Contient des informations sur un mot manuscrit donné dans la note du journal, notamment la position, les alternatives et les données d’encre réelles.</span><span class="sxs-lookup"><span data-stu-id="bbf40-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="bbf40-105">Définition</span><span class="sxs-lookup"><span data-stu-id="bbf40-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="bbf40-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bbf40-106">Parent Elements</span></span>

[<span data-ttu-id="bbf40-107">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="bbf40-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="bbf40-108">**Spline**</span><span class="sxs-lookup"><span data-stu-id="bbf40-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="bbf40-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bbf40-109">Child Elements</span></span>

[<span data-ttu-id="bbf40-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="bbf40-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="bbf40-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="bbf40-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="bbf40-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="bbf40-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="bbf40-113">**Garantir**</span><span class="sxs-lookup"><span data-stu-id="bbf40-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="bbf40-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="bbf40-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="bbf40-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="bbf40-115">Attributes</span></span>



| <span data-ttu-id="bbf40-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="bbf40-116">Attribute</span></span>  | <span data-ttu-id="bbf40-117">Type</span><span class="sxs-lookup"><span data-stu-id="bbf40-117">Type</span></span>                      | <span data-ttu-id="bbf40-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bbf40-118">Required</span></span> | <span data-ttu-id="bbf40-119">Description</span><span class="sxs-lookup"><span data-stu-id="bbf40-119">Description</span></span>                                                                             | <span data-ttu-id="bbf40-120">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="bbf40-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="bbf40-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="bbf40-121">**Left**</span></span>   | <span data-ttu-id="bbf40-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="bbf40-122">**xs:integer**</span></span>            | <span data-ttu-id="bbf40-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bbf40-123">Required</span></span> | <span data-ttu-id="bbf40-124">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="bbf40-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="bbf40-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="bbf40-125">Any integer.</span></span>              |
| <span data-ttu-id="bbf40-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="bbf40-126">**Top**</span></span>    | <span data-ttu-id="bbf40-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="bbf40-127">**xs:integer**</span></span>            | <span data-ttu-id="bbf40-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bbf40-128">Required</span></span> | <span data-ttu-id="bbf40-129">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="bbf40-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="bbf40-130">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="bbf40-130">Any integer.</span></span>              |
| <span data-ttu-id="bbf40-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="bbf40-131">**Width**</span></span>  | <span data-ttu-id="bbf40-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="bbf40-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="bbf40-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bbf40-133">Required</span></span> | <span data-ttu-id="bbf40-134">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="bbf40-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="bbf40-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="bbf40-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="bbf40-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="bbf40-136">**Height**</span></span> | <span data-ttu-id="bbf40-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="bbf40-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="bbf40-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bbf40-138">Required</span></span> | <span data-ttu-id="bbf40-139">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="bbf40-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="bbf40-140">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="bbf40-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="bbf40-141">Le mappage de coordonnées internes du mot d’encre est l’unité métrique anglaise et un multiplicateur de 2,54 doit être utilisé par votre application pour convertir les valeurs de largeur et de hauteur en unités HIMETRIC utilisées par les API de la plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="bbf40-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="bbf40-142">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bbf40-142">Element Information</span></span>



|  <span data-ttu-id="bbf40-143">Élément</span><span class="sxs-lookup"><span data-stu-id="bbf40-143">Element</span></span>     | <span data-ttu-id="bbf40-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbf40-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="bbf40-145">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="bbf40-145">Element type</span></span> | <span data-ttu-id="bbf40-146">ComplexType [**InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="bbf40-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="bbf40-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bbf40-147">Namespace</span></span>    | <span data-ttu-id="bbf40-148">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="bbf40-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="bbf40-149">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="bbf40-149">Schema name</span></span>  | <span data-ttu-id="bbf40-150">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="bbf40-150">Journal Reader</span></span>                                              |



 

 

 



