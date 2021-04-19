---
description: Transforme un plan par une matrice. La matrice d’entrée est la permutation inverse de la transformation réelle.
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: D3DXPlaneTransform, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd82478d9fb1f08bb0320a8c84357efcdf20be26
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531311"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a><span data-ttu-id="4755b-104">D3DXPlaneTransform, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4755b-104">D3DXPlaneTransform function (D3dx9math.h)</span></span>

<span data-ttu-id="4755b-105">Transforme un plan par une matrice.</span><span class="sxs-lookup"><span data-stu-id="4755b-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="4755b-106">La matrice d’entrée est la permutation inverse de la transformation réelle.</span><span class="sxs-lookup"><span data-stu-id="4755b-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4755b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4755b-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4755b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4755b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4755b-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4755b-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4755b-110">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="4755b-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="4755b-111">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui contient le plan transformé résultant.</span><span class="sxs-lookup"><span data-stu-id="4755b-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="4755b-112">Consultez les exemples.</span><span class="sxs-lookup"><span data-stu-id="4755b-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="4755b-113">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4755b-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4755b-114">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="4755b-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="4755b-115">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) d’entrée, qui contient le plan qui sera transformé.</span><span class="sxs-lookup"><span data-stu-id="4755b-115">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="4755b-116">Le vecteur (a, b, c) qui décrit le plan doit être normalisé avant l’appel de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="4755b-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="4755b-117">Consultez les exemples.</span><span class="sxs-lookup"><span data-stu-id="4755b-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="4755b-118">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4755b-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4755b-119">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4755b-119">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4755b-120">Pointeur vers la structure source [**D3DXMATRIX**](d3dxmatrix.md) , qui contient les valeurs de transformation.</span><span class="sxs-lookup"><span data-stu-id="4755b-120">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="4755b-121">Cette matrice doit contenir la transposer inverse des valeurs de transformation.</span><span class="sxs-lookup"><span data-stu-id="4755b-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4755b-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4755b-122">Return value</span></span>

<span data-ttu-id="4755b-123">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="4755b-123">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="4755b-124">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) représentant le plan transformé.</span><span class="sxs-lookup"><span data-stu-id="4755b-124">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="4755b-125">Il s’agit de la même valeur retournée dans le paramètre moue pour que cette fonction puisse être utilisée en tant que paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="4755b-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="4755b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="4755b-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="4755b-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="4755b-127">Examples</span></span>

<span data-ttu-id="4755b-128">Cet exemple transforme un plan en appliquant une échelle non uniforme.</span><span class="sxs-lookup"><span data-stu-id="4755b-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="4755b-129">Un plan est décrit par ax + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="4755b-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="4755b-130">Le premier plan est créé avec (a, b, c, d) = (0, 1, 1, 0), qui est un plan décrit par y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="4755b-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="4755b-131">Après la mise à l’échelle, le nouveau plan contient (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), qui affiche le nouveau plan à décrire par 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="4755b-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="4755b-132">Le paramètre pM contient la transposer inverse de la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="4755b-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="4755b-133">La permutation inverse est requise par cette méthode afin que le vecteur normal du plan transformé puisse également être correctement transformé.</span><span class="sxs-lookup"><span data-stu-id="4755b-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="4755b-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4755b-134">Requirements</span></span>



| <span data-ttu-id="4755b-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4755b-135">Requirement</span></span> | <span data-ttu-id="4755b-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4755b-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4755b-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="4755b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4755b-138"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4755b-138"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4755b-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4755b-139">Library</span></span><br/> | <dl> <span data-ttu-id="4755b-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4755b-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4755b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4755b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4755b-142">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="4755b-142">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4755b-143">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="4755b-143">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="4755b-144">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="4755b-144">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="4755b-145">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="4755b-145">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="4755b-146">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="4755b-146">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="4755b-147">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="4755b-147">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="4755b-148">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="4755b-148">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




