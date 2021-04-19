---
description: Détermine le produit croisé de deux vecteurs 3D.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: D3DXVec3Cross, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522352"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="c88f8-103">D3DXVec3Cross fonction)</span><span class="sxs-lookup"><span data-stu-id="c88f8-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="c88f8-104">Détermine le produit croisé de deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="c88f8-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c88f8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="c88f8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c88f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c88f8-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c88f8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c88f8-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88f8-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c88f8-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c88f8-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c88f8-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c88f8-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88f8-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c88f8-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c88f8-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="c88f8-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c88f8-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c88f8-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88f8-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c88f8-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c88f8-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="c88f8-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c88f8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c88f8-116">Return value</span></span>

<span data-ttu-id="c88f8-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c88f8-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c88f8-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le produit croisé de deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="c88f8-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88f8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c88f8-119">Remarks</span></span>

<span data-ttu-id="c88f8-120">Cette fonction détermine le produit croisé avec le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c88f8-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="c88f8-121">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="c88f8-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c88f8-122">De cette façon, la fonction **D3DXVec3Cross** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c88f8-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88f8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c88f8-123">Requirements</span></span>



| <span data-ttu-id="c88f8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c88f8-124">Requirement</span></span> | <span data-ttu-id="c88f8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c88f8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c88f8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c88f8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c88f8-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c88f8-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c88f8-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c88f8-128">Library</span></span><br/> | <dl> <span data-ttu-id="c88f8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c88f8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c88f8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c88f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88f8-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c88f8-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c88f8-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="c88f8-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




