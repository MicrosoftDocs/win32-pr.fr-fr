---
description: Contient un paragraphe.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Élément paragraph (Windows.ui.xaml.documents. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432231"
---
# <a name="paragraph-element"></a><span data-ttu-id="454ba-103">Élément paragraph</span><span class="sxs-lookup"><span data-stu-id="454ba-103">Paragraph Element</span></span>

<span data-ttu-id="454ba-104">Contient un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="454ba-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="454ba-105">Définition</span><span class="sxs-lookup"><span data-stu-id="454ba-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="454ba-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="454ba-106">Parent Elements</span></span>

[<span data-ttu-id="454ba-107">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="454ba-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="454ba-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="454ba-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="454ba-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="454ba-109">Child Elements</span></span>

[<span data-ttu-id="454ba-110">**Spline**</span><span class="sxs-lookup"><span data-stu-id="454ba-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="454ba-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="454ba-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="454ba-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="454ba-112">Attributes</span></span>



| <span data-ttu-id="454ba-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="454ba-113">Attribute</span></span>       | <span data-ttu-id="454ba-114">Type</span><span class="sxs-lookup"><span data-stu-id="454ba-114">Type</span></span>                      | <span data-ttu-id="454ba-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-115">Required</span></span> | <span data-ttu-id="454ba-116">Description</span><span class="sxs-lookup"><span data-stu-id="454ba-116">Description</span></span>                                                                             | <span data-ttu-id="454ba-117">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="454ba-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="454ba-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="454ba-118">**Left**</span></span>        | <span data-ttu-id="454ba-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="454ba-119">**xs:integer**</span></span>            | <span data-ttu-id="454ba-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-120">Required</span></span> | <span data-ttu-id="454ba-121">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="454ba-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="454ba-122">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="454ba-122">Any integer.</span></span>              |
| <span data-ttu-id="454ba-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="454ba-123">**Top**</span></span>         | <span data-ttu-id="454ba-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="454ba-124">**xs:integer**</span></span>            | <span data-ttu-id="454ba-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-125">Required</span></span> | <span data-ttu-id="454ba-126">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="454ba-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="454ba-127">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="454ba-127">Any integer.</span></span>              |
| <span data-ttu-id="454ba-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="454ba-128">**Width**</span></span>       | <span data-ttu-id="454ba-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="454ba-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="454ba-130">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-130">Required</span></span> | <span data-ttu-id="454ba-131">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="454ba-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="454ba-132">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="454ba-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="454ba-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="454ba-133">**Height**</span></span>      | <span data-ttu-id="454ba-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="454ba-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="454ba-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-135">Required</span></span> | <span data-ttu-id="454ba-136">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="454ba-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="454ba-137">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="454ba-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="454ba-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="454ba-138">**BlockNumber**</span></span> | <span data-ttu-id="454ba-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="454ba-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="454ba-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-140">Required</span></span> | <span data-ttu-id="454ba-141">Numéro de bloc.</span><span class="sxs-lookup"><span data-stu-id="454ba-141">Block number.</span></span>                                                                           | <span data-ttu-id="454ba-142">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="454ba-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="454ba-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="454ba-143">**LineNumber**</span></span>  | <span data-ttu-id="454ba-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="454ba-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="454ba-145">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="454ba-145">Required</span></span> | <span data-ttu-id="454ba-146">Ligne sur laquelle le paragraphe commence.</span><span class="sxs-lookup"><span data-stu-id="454ba-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="454ba-147">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="454ba-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="454ba-148">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="454ba-148">Element Information</span></span>



|  <span data-ttu-id="454ba-149">Élément</span><span class="sxs-lookup"><span data-stu-id="454ba-149">Element</span></span>     | <span data-ttu-id="454ba-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="454ba-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="454ba-151">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="454ba-151">Element type</span></span> | <span data-ttu-id="454ba-152">ComplexType [**ParagraphType**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="454ba-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="454ba-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="454ba-153">Namespace</span></span>    | <span data-ttu-id="454ba-154">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="454ba-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="454ba-155">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="454ba-155">Schema name</span></span>  | <span data-ttu-id="454ba-156">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="454ba-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="454ba-157">Spécifications</span><span class="sxs-lookup"><span data-stu-id="454ba-157">Requirements</span></span>



| <span data-ttu-id="454ba-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="454ba-158">Requirement</span></span> | <span data-ttu-id="454ba-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="454ba-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="454ba-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="454ba-160">Header</span></span><br/> | <dl> <span data-ttu-id="454ba-161"><dt>Windows.ui.xaml.documents. h</dt></span><span class="sxs-lookup"><span data-stu-id="454ba-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




