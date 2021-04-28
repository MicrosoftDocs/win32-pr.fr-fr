---
description: D3DXPlaneTransformArray, fonction (D3dx9math. h)-transforme un tableau de plans par une matrice. Les vecteurs qui décrivent chaque plan doivent être normalisés.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: D3DXPlaneTransformArray, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bdbc845eda69d22f6e7097131f71b074a9b53985
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094127"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="f0851-104">D3DXPlaneTransformArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f0851-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="f0851-105">Transforme un tableau de plans par une matrice.</span><span class="sxs-lookup"><span data-stu-id="f0851-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="f0851-106">Les vecteurs qui décrivent chaque plan doivent être normalisés.</span><span class="sxs-lookup"><span data-stu-id="f0851-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0851-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0851-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="f0851-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0851-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0851-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0851-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0851-110">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0851-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f0851-111">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) qui contient le plan transformé résultant.</span><span class="sxs-lookup"><span data-stu-id="f0851-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="f0851-112">Consultez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f0851-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="f0851-113">En *Progress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f0851-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0851-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0851-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0851-115">STRIDE de chaque plan transformé.</span><span class="sxs-lookup"><span data-stu-id="f0851-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="f0851-116">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0851-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0851-117">Type : **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0851-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f0851-118">Pointeur vers la structure [**D3DXPLANE**](d3dxplane.md) d’entrée, qui contient le tableau de plans à transformer.</span><span class="sxs-lookup"><span data-stu-id="f0851-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="f0851-119">Le vecteur (a, b, c) qui décrit le plan doit être normalisé avant l’appel de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f0851-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="f0851-120">Consultez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f0851-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="f0851-121">*PStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0851-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0851-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0851-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0851-123">STRIDE de chaque plan non transformé.</span><span class="sxs-lookup"><span data-stu-id="f0851-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="f0851-124">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0851-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0851-125">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0851-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0851-126">Pointeur vers la structure source [**D3DXMATRIX**](d3dxmatrix.md) , qui contient la permutation inverse des valeurs de transformation.</span><span class="sxs-lookup"><span data-stu-id="f0851-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="f0851-127">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0851-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0851-128">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0851-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0851-129">Nombre de plans à transformer.</span><span class="sxs-lookup"><span data-stu-id="f0851-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0851-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0851-130">Return value</span></span>

<span data-ttu-id="f0851-131">Type : **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0851-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f0851-132">Pointeur vers une structure [**D3DXPLANE**](d3dxplane.md) représentant le plan transformé.</span><span class="sxs-lookup"><span data-stu-id="f0851-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="f0851-133">Il s’agit de la même valeur retournée dans le paramètre *moue* pour que cette fonction puisse être utilisée en tant que paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="f0851-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0851-134">Notes </span><span class="sxs-lookup"><span data-stu-id="f0851-134">Remarks</span></span>

<span data-ttu-id="f0851-135">Cet exemple transforme un plan en appliquant une échelle non uniforme.</span><span class="sxs-lookup"><span data-stu-id="f0851-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="f0851-136">Un plan est décrit par ax + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="f0851-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="f0851-137">Le premier plan est créé avec (a, b, c, d) = (0, 1, 1, 0), qui est un plan décrit par y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="f0851-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="f0851-138">Après la mise à l’échelle, le nouveau plan contient (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), qui affiche le nouveau plan à décrire par 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="f0851-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="f0851-139">Le paramètre *PM* contient la transposer inverse de la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="f0851-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="f0851-140">La permutation inverse est requise par cette méthode afin que le vecteur normal du plan transformé puisse également être correctement transformé.</span><span class="sxs-lookup"><span data-stu-id="f0851-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0851-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0851-141">Requirements</span></span>



| <span data-ttu-id="f0851-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0851-142">Requirement</span></span> | <span data-ttu-id="f0851-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0851-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0851-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0851-144">Header</span></span><br/>  | <dl> <span data-ttu-id="f0851-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0851-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f0851-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0851-146">Library</span></span><br/> | <dl> <span data-ttu-id="f0851-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0851-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0851-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0851-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0851-149">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f0851-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f0851-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="f0851-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="f0851-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="f0851-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="f0851-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="f0851-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="f0851-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="f0851-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="f0851-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="f0851-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="f0851-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="f0851-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
