---
description: D3DXVec3TransformCoord, fonction (D3DX10Math. h)-transforme un vecteur 3D en une matrice donnée, en reprojetant le résultat dans w = 1.
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
ms.openlocfilehash: 5b3e763d87503f9ca71911ad40ccf3c6ae9ca722
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108097"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="ce04f-103">D3DXVec3TransformCoord, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ce04f-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="ce04f-104">Transforme un vecteur 3D par une matrice donnée, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="ce04f-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce04f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce04f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="ce04f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce04f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce04f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce04f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce04f-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce04f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ce04f-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ce04f-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ce04f-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce04f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce04f-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce04f-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ce04f-112">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="ce04f-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce04f-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce04f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce04f-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce04f-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ce04f-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="ce04f-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce04f-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce04f-116">Return value</span></span>

<span data-ttu-id="ce04f-117">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce04f-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ce04f-118">Pointeur vers une structure D3DXVECTOR3 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="ce04f-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce04f-119">Notes </span><span class="sxs-lookup"><span data-stu-id="ce04f-119">Remarks</span></span>

<span data-ttu-id="ce04f-120">Cette fonction transforme le vecteur, pV (x, y, z, 1), par la matrice, pM, en projetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="ce04f-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="ce04f-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="ce04f-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ce04f-122">De cette façon, la fonction D3DXVec3TransformCoord peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ce04f-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce04f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce04f-123">Requirements</span></span>



| <span data-ttu-id="ce04f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce04f-124">Requirement</span></span> | <span data-ttu-id="ce04f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce04f-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce04f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce04f-126">Header</span></span><br/> | <dl> <span data-ttu-id="ce04f-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce04f-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce04f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce04f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce04f-129">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ce04f-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
