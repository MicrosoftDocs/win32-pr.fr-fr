---
description: Transforme un tableau (x, y, z, 1) en une matrice donnée.
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: D3DXVec3TransformArray, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b515c98be82aa47801b333c4b25680e0e464b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322726"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a><span data-ttu-id="6629a-103">D3DXVec3TransformArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6629a-103">D3DXVec3TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="6629a-104">Transforme un tableau (x, y, z, 1) en une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="6629a-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6629a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6629a-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="6629a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6629a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6629a-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6629a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6629a-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6629a-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6629a-109">Pointeur vers le tableau [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6629a-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6629a-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6629a-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6629a-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6629a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6629a-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="6629a-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6629a-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6629a-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6629a-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6629a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6629a-115">Pointeur vers le tableau [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="6629a-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="6629a-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6629a-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6629a-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6629a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6629a-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6629a-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6629a-119">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6629a-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6629a-120">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6629a-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6629a-121">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="6629a-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6629a-122">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6629a-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6629a-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6629a-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6629a-124">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="6629a-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6629a-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6629a-125">Return value</span></span>

<span data-ttu-id="6629a-126">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6629a-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6629a-127">Pointeur vers un tableau transformé [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="6629a-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="6629a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="6629a-128">Remarks</span></span>

<span data-ttu-id="6629a-129">Cette fonction transforme *le tableau (* x, y, z, 1) par la matrice *PM*.</span><span class="sxs-lookup"><span data-stu-id="6629a-129">This function transforms the array *pV* (x, y, z, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="6629a-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="6629a-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6629a-131">De cette façon, la fonction **D3DXVec3TransformArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="6629a-131">In this way, the **D3DXVec3TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6629a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6629a-132">Requirements</span></span>



| <span data-ttu-id="6629a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6629a-133">Requirement</span></span> | <span data-ttu-id="6629a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6629a-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6629a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="6629a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6629a-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6629a-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6629a-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6629a-137">Library</span></span><br/> | <dl> <span data-ttu-id="6629a-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6629a-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6629a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6629a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6629a-140">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6629a-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
