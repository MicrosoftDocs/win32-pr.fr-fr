---
description: Transforme le vecteur 3D normal par la matrice donnée.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: D3DXVec3TransformNormal, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8dd0bf3fa2083d2cf0cc0cea72343f4774a586f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211909"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="33af9-103">D3DXVec3TransformNormal, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="33af9-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="33af9-104">Transforme le vecteur 3D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="33af9-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="33af9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33af9-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="33af9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33af9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33af9-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="33af9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33af9-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="33af9-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="33af9-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="33af9-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="33af9-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33af9-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33af9-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="33af9-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="33af9-112">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="33af9-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="33af9-113">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33af9-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33af9-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="33af9-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="33af9-115">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) source.</span><span class="sxs-lookup"><span data-stu-id="33af9-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33af9-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33af9-116">Return value</span></span>

<span data-ttu-id="33af9-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="33af9-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="33af9-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le vecteur transformé.</span><span class="sxs-lookup"><span data-stu-id="33af9-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="33af9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="33af9-119">Remarks</span></span>

<span data-ttu-id="33af9-120">Cette fonction transforme le vecteur (*PV*->x, *PV*->y, *PV*->z, 0) par la matrice vers laquelle pointe *PM*.</span><span class="sxs-lookup"><span data-stu-id="33af9-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="33af9-121">Si vous souhaitez transformer un normal, la matrice que vous transmettez à cette fonction doit être la transposer de l’inverse de la matrice que vous utiliseriez pour transformer un point.</span><span class="sxs-lookup"><span data-stu-id="33af9-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="33af9-122">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="33af9-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="33af9-123">De cette façon, la fonction **D3DXVec3TransformNormal** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="33af9-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="33af9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33af9-124">Requirements</span></span>



| <span data-ttu-id="33af9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33af9-125">Requirement</span></span> | <span data-ttu-id="33af9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="33af9-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33af9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="33af9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="33af9-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="33af9-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="33af9-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33af9-129">Library</span></span><br/> | <dl> <span data-ttu-id="33af9-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33af9-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33af9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33af9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33af9-132">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="33af9-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




