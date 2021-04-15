---
description: Cette rubrique répertorie les méthodes TransformVectors de la classe Matrix. Pour obtenir la liste complète des méthodes de la classe Matrix, consultez Méthodes de matrice.
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: Méthodes Matrix. TransformVectors (Gdiplusmatrix. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982898"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="36804-104">Méthodes Matrix. TransformVectors</span><span class="sxs-lookup"><span data-stu-id="36804-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="36804-105">Cette rubrique répertorie les méthodes TransformVectors de la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="36804-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="36804-106">Pour obtenir la liste complète des méthodes de la classe **Matrix** , consultez [méthodes de matrice](-gdiplus-class-matrix-methods.md).</span><span class="sxs-lookup"><span data-stu-id="36804-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="36804-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="36804-107">Overload list</span></span>



| <span data-ttu-id="36804-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="36804-108">Method</span></span>                                                                                                 | <span data-ttu-id="36804-109">Description</span><span class="sxs-lookup"><span data-stu-id="36804-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36804-110">[**TransformVectors (point \* , int)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="36804-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="36804-111">La méthode [**Matrix :: TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) multiplie chaque vecteur d’un tableau par cette matrice.</span><span class="sxs-lookup"><span data-stu-id="36804-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="36804-112">Les éléments de translation de cette matrice (troisième ligne) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="36804-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="36804-113">Chaque vecteur est traité comme une matrice de lignes.</span><span class="sxs-lookup"><span data-stu-id="36804-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="36804-114">La multiplication est effectuée avec la matrice de lignes à gauche et cette matrice à droite.</span><span class="sxs-lookup"><span data-stu-id="36804-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="36804-115">[**TransformVectors (PointF \* , int)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36804-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="36804-116">La méthode [**Matrix :: TransformVectors**](/previous-versions//ms535319(v=vs.85)) multiplie chaque vecteur d’un tableau par cette matrice.</span><span class="sxs-lookup"><span data-stu-id="36804-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="36804-117">Les éléments de translation de cette matrice (troisième ligne) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="36804-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="36804-118">Chaque vecteur est traité comme une matrice de lignes.</span><span class="sxs-lookup"><span data-stu-id="36804-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="36804-119">La multiplication est effectuée avec la matrice de lignes à gauche et cette matrice à droite.</span><span class="sxs-lookup"><span data-stu-id="36804-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="36804-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="36804-120">Requirements</span></span>



| <span data-ttu-id="36804-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36804-121">Requirement</span></span> | <span data-ttu-id="36804-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="36804-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="36804-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="36804-123">Header</span></span><br/> | <dl> <span data-ttu-id="36804-124"><dt>Gdiplusmatrix. h</dt></span><span class="sxs-lookup"><span data-stu-id="36804-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
