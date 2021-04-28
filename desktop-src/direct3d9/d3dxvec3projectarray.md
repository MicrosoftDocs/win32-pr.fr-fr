---
description: D3DXVec3ProjectArray, fonction (D3dx9math. h)-projette un tableau (x, y, z, 0) à partir de l’espace d’objet dans l’espace de l’écran.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: D3DXVec3ProjectArray, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10f0e19ad5bdbff59d7386223c88ed867e8d0d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097807"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="bb51c-103">D3DXVec3ProjectArray, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bb51c-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="bb51c-104">Projette un tableau (x, y, z, 0) à partir de l’espace d’objet dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="bb51c-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb51c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb51c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="bb51c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb51c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb51c-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb51c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb51c-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="bb51c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-110">En *Progress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb51c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb51c-112">STRIDE entre les vecteurs dans le flux de données de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb51c-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-113">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb51c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb51c-115">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="bb51c-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-116">*VStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb51c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb51c-118">STRIDE entre les vecteurs dans le flux de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bb51c-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-119">*pViewport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-120">Type : **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb51c-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="bb51c-121">Pointeur vers une structure [**D3DVIEWPORT9**](d3dviewport9.md) , représentant la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="bb51c-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-122">*pProjection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-123">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb51c-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb51c-124">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="bb51c-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-125">*pview* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-126">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb51c-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb51c-127">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) , représentant la matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="bb51c-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-128">*pWorld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-129">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb51c-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb51c-130">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice universelle.</span><span class="sxs-lookup"><span data-stu-id="bb51c-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="bb51c-131">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb51c-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb51c-132">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb51c-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb51c-133">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="bb51c-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb51c-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb51c-134">Return value</span></span>

<span data-ttu-id="bb51c-135">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb51c-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb51c-136">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le tableau projeté de l’espace de l’objet à l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="bb51c-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb51c-137">Notes </span><span class="sxs-lookup"><span data-stu-id="bb51c-137">Remarks</span></span>

<span data-ttu-id="bb51c-138">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="bb51c-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bb51c-139">De cette façon, la fonction **D3DXVec3ProjectArray** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="bb51c-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb51c-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb51c-140">Requirements</span></span>



| <span data-ttu-id="bb51c-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb51c-141">Requirement</span></span> | <span data-ttu-id="bb51c-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb51c-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb51c-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb51c-143">Header</span></span><br/>  | <dl> <span data-ttu-id="bb51c-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb51c-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bb51c-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb51c-145">Library</span></span><br/> | <dl> <span data-ttu-id="bb51c-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb51c-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb51c-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb51c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb51c-148">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="bb51c-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bb51c-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="bb51c-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
