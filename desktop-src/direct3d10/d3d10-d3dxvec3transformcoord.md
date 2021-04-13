---
description: Transforme un vecteur 3D par une matrice donnée, en reprojetant le résultat dans w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: D3DXVec3TransformCoord, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a8fc7c7a00133e036921eabaa145dca01a12f042
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322965"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="7b502-103">D3DXVec3TransformCoord, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7b502-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="7b502-104">Transforme un vecteur 3D par une matrice donnée, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="7b502-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b502-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b502-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="7b502-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b502-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b502-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b502-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b502-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7b502-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7b502-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b502-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b502-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b502-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b502-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7b502-112">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="7b502-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b502-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b502-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b502-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b502-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b502-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="7b502-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b502-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b502-116">Return value</span></span>

<span data-ttu-id="7b502-117">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b502-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7b502-118">Pointeur vers une structure D3DXVECTOR3 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="7b502-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b502-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7b502-119">Remarks</span></span>

<span data-ttu-id="7b502-120">Cette fonction transforme le vecteur, pV (x, y, z, 1), par la matrice, pM, en projetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="7b502-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="7b502-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="7b502-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7b502-122">De cette façon, la fonction D3DXVec3TransformCoord peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="7b502-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b502-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b502-123">Requirements</span></span>



| <span data-ttu-id="7b502-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b502-124">Requirement</span></span> | <span data-ttu-id="7b502-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b502-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b502-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b502-126">Header</span></span><br/> | <dl> <span data-ttu-id="7b502-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b502-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b502-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b502-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b502-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="7b502-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
