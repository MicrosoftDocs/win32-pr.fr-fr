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
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540979"
---
# <a name="paragraph-element"></a><span data-ttu-id="66aa1-103">Élément paragraph</span><span class="sxs-lookup"><span data-stu-id="66aa1-103">Paragraph Element</span></span>

<span data-ttu-id="66aa1-104">Contient un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="66aa1-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="66aa1-105">Définition</span><span class="sxs-lookup"><span data-stu-id="66aa1-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="66aa1-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="66aa1-106">Parent Elements</span></span>

[<span data-ttu-id="66aa1-107">**Content**</span><span class="sxs-lookup"><span data-stu-id="66aa1-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="66aa1-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="66aa1-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="66aa1-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66aa1-109">Child Elements</span></span>

[<span data-ttu-id="66aa1-110">**Lignes**</span><span class="sxs-lookup"><span data-stu-id="66aa1-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="66aa1-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="66aa1-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="66aa1-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="66aa1-112">Attributes</span></span>



| <span data-ttu-id="66aa1-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="66aa1-113">Attribute</span></span>       | <span data-ttu-id="66aa1-114">Type</span><span class="sxs-lookup"><span data-stu-id="66aa1-114">Type</span></span>                      | <span data-ttu-id="66aa1-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-115">Required</span></span> | <span data-ttu-id="66aa1-116">Description</span><span class="sxs-lookup"><span data-stu-id="66aa1-116">Description</span></span>                                                                             | <span data-ttu-id="66aa1-117">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="66aa1-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="66aa1-118">**Left**</span><span class="sxs-lookup"><span data-stu-id="66aa1-118">**Left**</span></span>        | <span data-ttu-id="66aa1-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="66aa1-119">**xs:integer**</span></span>            | <span data-ttu-id="66aa1-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-120">Required</span></span> | <span data-ttu-id="66aa1-121">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="66aa1-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="66aa1-122">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="66aa1-122">Any integer.</span></span>              |
| <span data-ttu-id="66aa1-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="66aa1-123">**Top**</span></span>         | <span data-ttu-id="66aa1-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="66aa1-124">**xs:integer**</span></span>            | <span data-ttu-id="66aa1-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-125">Required</span></span> | <span data-ttu-id="66aa1-126">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="66aa1-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="66aa1-127">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="66aa1-127">Any integer.</span></span>              |
| <span data-ttu-id="66aa1-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="66aa1-128">**Width**</span></span>       | <span data-ttu-id="66aa1-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66aa1-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66aa1-130">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-130">Required</span></span> | <span data-ttu-id="66aa1-131">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="66aa1-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="66aa1-132">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="66aa1-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="66aa1-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="66aa1-133">**Height**</span></span>      | <span data-ttu-id="66aa1-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66aa1-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66aa1-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-135">Required</span></span> | <span data-ttu-id="66aa1-136">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="66aa1-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="66aa1-137">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="66aa1-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="66aa1-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="66aa1-138">**BlockNumber**</span></span> | <span data-ttu-id="66aa1-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66aa1-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66aa1-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-140">Required</span></span> | <span data-ttu-id="66aa1-141">Numéro de bloc.</span><span class="sxs-lookup"><span data-stu-id="66aa1-141">Block number.</span></span>                                                                           | <span data-ttu-id="66aa1-142">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="66aa1-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="66aa1-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="66aa1-143">**LineNumber**</span></span>  | <span data-ttu-id="66aa1-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66aa1-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66aa1-145">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66aa1-145">Required</span></span> | <span data-ttu-id="66aa1-146">Ligne sur laquelle le paragraphe commence.</span><span class="sxs-lookup"><span data-stu-id="66aa1-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="66aa1-147">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="66aa1-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="66aa1-148">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="66aa1-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="66aa1-149">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="66aa1-149">Element type</span></span> | <span data-ttu-id="66aa1-150">ComplexType [**ParagraphType**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="66aa1-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="66aa1-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66aa1-151">Namespace</span></span>    | <span data-ttu-id="66aa1-152">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="66aa1-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="66aa1-153">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="66aa1-153">Schema name</span></span>  | <span data-ttu-id="66aa1-154">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="66aa1-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="66aa1-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66aa1-155">Requirements</span></span>



| <span data-ttu-id="66aa1-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66aa1-156">Requirement</span></span> | <span data-ttu-id="66aa1-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="66aa1-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66aa1-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="66aa1-158">Header</span></span><br/> | <dl> <span data-ttu-id="66aa1-159"><dt>Windows.ui.xaml.documents. h</dt></span><span class="sxs-lookup"><span data-stu-id="66aa1-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




