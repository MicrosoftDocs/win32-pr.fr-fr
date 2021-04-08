---
description: Transforme un tableau de plans par une matrice. Les vecteurs qui décrivent chaque plan doivent être normalisés.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: D3DXPlaneTransformArray, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043142"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="f10f3-104">D3DXPlaneTransformArray, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f10f3-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="f10f3-105">Transforme un tableau de plans par une matrice.</span><span class="sxs-lookup"><span data-stu-id="f10f3-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="f10f3-106">Les vecteurs qui décrivent chaque plan doivent être normalisés.</span><span class="sxs-lookup"><span data-stu-id="f10f3-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f10f3-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="f10f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f10f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f10f3-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f10f3-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f10f3-110">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f10f3-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="f10f3-111">Pointeur vers la structure [**D3DXPLANE**](d3d10-d3dxplane.md) qui contient le plan transformé résultant.</span><span class="sxs-lookup"><span data-stu-id="f10f3-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="f10f3-112">Consultez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f10f3-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="f10f3-113">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f10f3-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f10f3-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f10f3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f10f3-115">STRIDE de chaque plan transformé.</span><span class="sxs-lookup"><span data-stu-id="f10f3-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="f10f3-116">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f10f3-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f10f3-117">Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="f10f3-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="f10f3-118">Pointeur vers la structure D3DXPLANE d’entrée, qui contient le tableau de plans à transformer.</span><span class="sxs-lookup"><span data-stu-id="f10f3-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="f10f3-119">Le vecteur (a, b, c) qui décrit le plan doit être normalisé avant l’appel de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f10f3-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="f10f3-120">Consultez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f10f3-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="f10f3-121">*PStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f10f3-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f10f3-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f10f3-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f10f3-123">STRIDE de chaque plan non transformé.</span><span class="sxs-lookup"><span data-stu-id="f10f3-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="f10f3-124">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f10f3-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f10f3-125">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f10f3-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f10f3-126">Pointeur vers la structure source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , qui contient la permutation inverse des valeurs de transformation.</span><span class="sxs-lookup"><span data-stu-id="f10f3-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="f10f3-127">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f10f3-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f10f3-128">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f10f3-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f10f3-129">Nombre de plans à transformer.</span><span class="sxs-lookup"><span data-stu-id="f10f3-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f10f3-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f10f3-130">Return value</span></span>

<span data-ttu-id="f10f3-131">Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f10f3-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="f10f3-132">Pointeur vers une structure D3DXPLANE représentant le plan transformé.</span><span class="sxs-lookup"><span data-stu-id="f10f3-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="f10f3-133">Il s’agit de la même valeur retournée dans le paramètre moue pour que cette fonction puisse être utilisée en tant que paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="f10f3-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f10f3-134">Notes</span><span class="sxs-lookup"><span data-stu-id="f10f3-134">Remarks</span></span>

<span data-ttu-id="f10f3-135">Cet exemple transforme un plan en appliquant une échelle non uniforme.</span><span class="sxs-lookup"><span data-stu-id="f10f3-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="f10f3-136">Un plan est décrit par ax + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="f10f3-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="f10f3-137">Le premier plan est créé avec (a, b, c, d) = (0, 1, 1, 0), qui est un plan décrit par y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="f10f3-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="f10f3-138">Après la mise à l’échelle, le nouveau plan contient (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), qui affiche le nouveau plan à décrire par 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="f10f3-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="f10f3-139">Le paramètre pM contient la transposer inverse de la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="f10f3-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="f10f3-140">La permutation inverse est requise par cette méthode afin que le vecteur normal du plan transformé puisse également être correctement transformé.</span><span class="sxs-lookup"><span data-stu-id="f10f3-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="f10f3-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f10f3-141">Requirements</span></span>



| <span data-ttu-id="f10f3-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f10f3-142">Requirement</span></span> | <span data-ttu-id="f10f3-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="f10f3-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f10f3-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="f10f3-144">Header</span></span><br/>  | <dl> <span data-ttu-id="f10f3-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f10f3-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f10f3-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f10f3-146">Library</span></span><br/> | <dl> <span data-ttu-id="f10f3-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f10f3-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f10f3-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f10f3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f10f3-149">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f10f3-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
