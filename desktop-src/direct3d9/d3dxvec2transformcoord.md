---
description: Transforme un vecteur 2D par une matrice donnée, en reprojetant le résultat dans w = 1.
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: D3DXVec2TransformCoord, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc047075cd2f9f6aba6903f85ea6960e78e0ba1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535818"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="80b33-103">D3DXVec2TransformCoord, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="80b33-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="80b33-104">Transforme un vecteur 2D par une matrice donnée, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="80b33-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80b33-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="80b33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80b33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b33-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="80b33-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80b33-108">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="80b33-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="80b33-109">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="80b33-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="80b33-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80b33-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b33-111">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="80b33-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="80b33-112">Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.</span><span class="sxs-lookup"><span data-stu-id="80b33-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="80b33-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80b33-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b33-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="80b33-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="80b33-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="80b33-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80b33-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80b33-116">Return value</span></span>

<span data-ttu-id="80b33-117">Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="80b33-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="80b33-118">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="80b33-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="80b33-119">Notes</span><span class="sxs-lookup"><span data-stu-id="80b33-119">Remarks</span></span>

<span data-ttu-id="80b33-120">Cette fonction transforme le vecteur, *PV* (x, y, 0, 1), par la matrice, *PM*, en projetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="80b33-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="80b33-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="80b33-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="80b33-122">De cette façon, la fonction **D3DXVec2TransformCoord** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="80b33-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b33-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80b33-123">Requirements</span></span>



| <span data-ttu-id="80b33-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80b33-124">Requirement</span></span> | <span data-ttu-id="80b33-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="80b33-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80b33-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="80b33-126">Header</span></span><br/>  | <dl> <span data-ttu-id="80b33-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b33-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="80b33-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80b33-128">Library</span></span><br/> | <dl> <span data-ttu-id="80b33-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80b33-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80b33-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b33-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b33-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="80b33-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="80b33-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="80b33-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="80b33-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="80b33-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




