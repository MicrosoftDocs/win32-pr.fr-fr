---
description: Transformation scalaire utilisée par le dessin ou InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Élément ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432431"
---
# <a name="scalartransform-element"></a><span data-ttu-id="9bff1-103">Élément ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="9bff1-103">ScalarTransform Element</span></span>

<span data-ttu-id="9bff1-104">Transformation scalaire utilisée par le [**dessin**](drawing-element.md) ou [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="9bff1-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="9bff1-105">Définition</span><span class="sxs-lookup"><span data-stu-id="9bff1-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="9bff1-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9bff1-106">Parent Elements</span></span>

[<span data-ttu-id="9bff1-107">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="9bff1-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="9bff1-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="9bff1-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="9bff1-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9bff1-109">Child Elements</span></span>

<span data-ttu-id="9bff1-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9bff1-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="9bff1-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="9bff1-111">Attributes</span></span>



| <span data-ttu-id="9bff1-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="9bff1-112">Attribute</span></span> | <span data-ttu-id="9bff1-113">Type</span><span class="sxs-lookup"><span data-stu-id="9bff1-113">Type</span></span>           | <span data-ttu-id="9bff1-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-114">Required</span></span> | <span data-ttu-id="9bff1-115">Description</span><span class="sxs-lookup"><span data-stu-id="9bff1-115">Description</span></span> | <span data-ttu-id="9bff1-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9bff1-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="9bff1-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="9bff1-117">**Mat1**</span></span>  | <span data-ttu-id="9bff1-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-118">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-119">Required</span></span> |             | <span data-ttu-id="9bff1-120">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-120">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="9bff1-121">**Mat2**</span></span>  | <span data-ttu-id="9bff1-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-122">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-123">Required</span></span> |             | <span data-ttu-id="9bff1-124">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-124">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="9bff1-125">**Mat3**</span></span>  | <span data-ttu-id="9bff1-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-126">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-127">Required</span></span> |             | <span data-ttu-id="9bff1-128">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-128">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="9bff1-129">**Mat4**</span></span>  | <span data-ttu-id="9bff1-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-130">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-131">Required</span></span> |             | <span data-ttu-id="9bff1-132">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-132">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="9bff1-133">**Mat5**</span></span>  | <span data-ttu-id="9bff1-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-134">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-135">Required</span></span> |             | <span data-ttu-id="9bff1-136">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-136">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="9bff1-137">**Mat6**</span></span>  | <span data-ttu-id="9bff1-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-138">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-139">Required</span></span> |             | <span data-ttu-id="9bff1-140">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-140">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="9bff1-141">**Mat7**</span></span>  | <span data-ttu-id="9bff1-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-142">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-143">Required</span></span> |             | <span data-ttu-id="9bff1-144">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-144">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="9bff1-145">**Mat8**</span></span>  | <span data-ttu-id="9bff1-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-146">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-147">Required</span></span> |             | <span data-ttu-id="9bff1-148">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-148">Any decimal number.</span></span> |
| <span data-ttu-id="9bff1-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="9bff1-149">**Mat9**</span></span>  | <span data-ttu-id="9bff1-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="9bff1-150">**xs:decimal**</span></span> | <span data-ttu-id="9bff1-151">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9bff1-151">Required</span></span> |             | <span data-ttu-id="9bff1-152">Tout nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="9bff1-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="9bff1-153">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9bff1-153">Element Information</span></span>



| <span data-ttu-id="9bff1-154">Élément</span><span class="sxs-lookup"><span data-stu-id="9bff1-154">Element</span></span>      | <span data-ttu-id="9bff1-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bff1-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="9bff1-156">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="9bff1-156">Element type</span></span> | <span data-ttu-id="9bff1-157">ComplexType [**ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="9bff1-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="9bff1-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9bff1-158">Namespace</span></span>    | <span data-ttu-id="9bff1-159">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="9bff1-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="9bff1-160">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="9bff1-160">Schema name</span></span>  | <span data-ttu-id="9bff1-161">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="9bff1-161">Journal Reader</span></span>                                                              |



 

 

 



