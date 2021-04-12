---
description: Transforme le vecteur 3D normal par la matrice donnée.
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: D3DXVec3TransformNormal, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 602f366d3d7ccbcd37804226323d5584eed034f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323097"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="996cb-103">D3DXVec3TransformNormal, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="996cb-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="996cb-104">Transforme le vecteur 3D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="996cb-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="996cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="996cb-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="996cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="996cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996cb-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="996cb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="996cb-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="996cb-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="996cb-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="996cb-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="996cb-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="996cb-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996cb-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="996cb-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="996cb-112">Pointeur vers la structure D3DXVECTOR3 source.</span><span class="sxs-lookup"><span data-stu-id="996cb-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="996cb-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="996cb-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996cb-114">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="996cb-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="996cb-115">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="996cb-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996cb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="996cb-116">Return value</span></span>

<span data-ttu-id="996cb-117">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="996cb-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="996cb-118">Pointeur vers une structure D3DXVECTOR3 qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="996cb-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="996cb-119">Notes</span><span class="sxs-lookup"><span data-stu-id="996cb-119">Remarks</span></span>

<span data-ttu-id="996cb-120">Cette fonction transforme le vecteur (pV->x, pV->y, pV->z, 0) par la matrice vers laquelle pointe pM.</span><span class="sxs-lookup"><span data-stu-id="996cb-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="996cb-121">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="996cb-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="996cb-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="996cb-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="996cb-123">De cette façon, la fonction **D3DXVec3TransformNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="996cb-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="996cb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="996cb-124">Requirements</span></span>



| <span data-ttu-id="996cb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="996cb-125">Requirement</span></span> | <span data-ttu-id="996cb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="996cb-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="996cb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="996cb-127">Header</span></span><br/> | <dl> <span data-ttu-id="996cb-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="996cb-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996cb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="996cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996cb-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="996cb-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
