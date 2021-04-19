---
description: Transformation scalaire utilisée par le dessin ou InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Élément ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523368"
---
# <a name="scalartransform-element"></a><span data-ttu-id="71f06-103">Élément ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="71f06-103">ScalarTransform Element</span></span>

<span data-ttu-id="71f06-104">Transformation scalaire utilisée par le [**dessin**](drawing-element.md) ou [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="71f06-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="71f06-105">Définition</span><span class="sxs-lookup"><span data-stu-id="71f06-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="71f06-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="71f06-106">Parent Elements</span></span>

[<span data-ttu-id="71f06-107">**Schéma**</span><span class="sxs-lookup"><span data-stu-id="71f06-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="71f06-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="71f06-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="71f06-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="71f06-109">Child Elements</span></span>

<span data-ttu-id="71f06-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="71f06-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="71f06-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="71f06-111">Attributes</span></span>



| <span data-ttu-id="71f06-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="71f06-112">Attribute</span></span> | <span data-ttu-id="71f06-113">Type</span><span class="sxs-lookup"><span data-stu-id="71f06-113">Type</span></span>           | <span data-ttu-id="71f06-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-114">Required</span></span> | <span data-ttu-id="71f06-115">Description</span><span class="sxs-lookup"><span data-stu-id="71f06-115">Description</span></span> | <span data-ttu-id="71f06-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="71f06-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="71f06-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="71f06-117">**Mat1**</span></span>  | <span data-ttu-id="71f06-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-118">**xs:decimal**</span></span> | <span data-ttu-id="71f06-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-119">Required</span></span> |             | <span data-ttu-id="71f06-120">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-120">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="71f06-121">**Mat2**</span></span>  | <span data-ttu-id="71f06-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-122">**xs:decimal**</span></span> | <span data-ttu-id="71f06-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-123">Required</span></span> |             | <span data-ttu-id="71f06-124">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-124">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="71f06-125">**Mat3**</span></span>  | <span data-ttu-id="71f06-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-126">**xs:decimal**</span></span> | <span data-ttu-id="71f06-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-127">Required</span></span> |             | <span data-ttu-id="71f06-128">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-128">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="71f06-129">**Mat4**</span></span>  | <span data-ttu-id="71f06-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-130">**xs:decimal**</span></span> | <span data-ttu-id="71f06-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-131">Required</span></span> |             | <span data-ttu-id="71f06-132">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-132">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="71f06-133">**Mat5**</span></span>  | <span data-ttu-id="71f06-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-134">**xs:decimal**</span></span> | <span data-ttu-id="71f06-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-135">Required</span></span> |             | <span data-ttu-id="71f06-136">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-136">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="71f06-137">**Mat6**</span></span>  | <span data-ttu-id="71f06-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-138">**xs:decimal**</span></span> | <span data-ttu-id="71f06-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-139">Required</span></span> |             | <span data-ttu-id="71f06-140">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-140">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="71f06-141">**Mat7**</span></span>  | <span data-ttu-id="71f06-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-142">**xs:decimal**</span></span> | <span data-ttu-id="71f06-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-143">Required</span></span> |             | <span data-ttu-id="71f06-144">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-144">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="71f06-145">**Mat8**</span></span>  | <span data-ttu-id="71f06-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-146">**xs:decimal**</span></span> | <span data-ttu-id="71f06-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-147">Required</span></span> |             | <span data-ttu-id="71f06-148">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-148">Any decimal number.</span></span> |
| <span data-ttu-id="71f06-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="71f06-149">**Mat9**</span></span>  | <span data-ttu-id="71f06-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="71f06-150">**xs:decimal**</span></span> | <span data-ttu-id="71f06-151">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71f06-151">Required</span></span> |             | <span data-ttu-id="71f06-152">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="71f06-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="71f06-153">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="71f06-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="71f06-154">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="71f06-154">Element type</span></span> | <span data-ttu-id="71f06-155">ComplexType [**ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="71f06-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="71f06-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="71f06-156">Namespace</span></span>    | <span data-ttu-id="71f06-157">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="71f06-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="71f06-158">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="71f06-158">Schema name</span></span>  | <span data-ttu-id="71f06-159">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="71f06-159">Journal Reader</span></span>                                                              |



 

 

 



