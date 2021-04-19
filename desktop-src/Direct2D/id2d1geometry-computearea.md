---
title: Méthodes ID2D1Geometry ComputeArea
description: Calcule la zone de la géométrie.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Méthodes ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541537"
---
# <a name="id2d1geometrycomputearea-methods"></a><span data-ttu-id="61c36-104">ID2D1Geometry :: ComputeArea, méthodes</span><span class="sxs-lookup"><span data-stu-id="61c36-104">ID2D1Geometry::ComputeArea methods</span></span>

<span data-ttu-id="61c36-105">Calcule la zone de la géométrie.</span><span class="sxs-lookup"><span data-stu-id="61c36-105">Computes the area of the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="61c36-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="61c36-106">Overload list</span></span>



| <span data-ttu-id="61c36-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="61c36-107">Method</span></span>                                                                                                                      | <span data-ttu-id="61c36-108">Description</span><span class="sxs-lookup"><span data-stu-id="61c36-108">Description</span></span>                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c36-109">[**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span><span class="sxs-lookup"><span data-stu-id="61c36-109">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span></span>              | <span data-ttu-id="61c36-110">Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance par défaut.</span><span class="sxs-lookup"><span data-stu-id="61c36-110">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>    |
| <span data-ttu-id="61c36-111">[**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="61c36-111">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="61c36-112">Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance par défaut.</span><span class="sxs-lookup"><span data-stu-id="61c36-112">Computes the area of the geometry after it has been transformed by the specified matrix and flattened by using the default tolerance.</span></span><br/> |
| <span data-ttu-id="61c36-113">[**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="61c36-113">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="61c36-114">Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="61c36-114">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |
| <span data-ttu-id="61c36-115">[**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="61c36-115">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="61c36-116">Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="61c36-116">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="61c36-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="61c36-117">Examples</span></span>

<span data-ttu-id="61c36-118">L’exemple de code suivant utilise **ComputeArea** pour calculer la zone d’un cercle spécifié (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="61c36-118">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a><span data-ttu-id="61c36-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61c36-119">Requirements</span></span>



| <span data-ttu-id="61c36-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61c36-120">Requirement</span></span> | <span data-ttu-id="61c36-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="61c36-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61c36-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61c36-122">Library</span></span><br/> | <dl> <span data-ttu-id="61c36-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61c36-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="61c36-124">DLL</span><span class="sxs-lookup"><span data-stu-id="61c36-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="61c36-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61c36-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61c36-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61c36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c36-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="61c36-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

