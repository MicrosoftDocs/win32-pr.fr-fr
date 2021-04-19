---
description: Ajoute deux vecteurs 3D.
ms.assetid: 2979e291-786b-4bc9-b584-421f08db949a
title: D3DXVec3Add, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16fb06c5e7b32506a94a5828fe7f5e1305afff7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522381"
---
# <a name="d3dxvec3add-function"></a><span data-ttu-id="718c4-103">D3DXVec3Add fonction)</span><span class="sxs-lookup"><span data-stu-id="718c4-103">D3DXVec3Add function</span></span>

<span data-ttu-id="718c4-104">Ajoute deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="718c4-104">Adds two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="718c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="718c4-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Add(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="718c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="718c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718c4-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="718c4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="718c4-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="718c4-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="718c4-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="718c4-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="718c4-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="718c4-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718c4-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="718c4-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="718c4-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="718c4-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="718c4-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="718c4-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718c4-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="718c4-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="718c4-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="718c4-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718c4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="718c4-116">Return value</span></span>

<span data-ttu-id="718c4-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="718c4-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="718c4-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est la somme des deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="718c4-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the sum of the two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="718c4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="718c4-119">Remarks</span></span>

<span data-ttu-id="718c4-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="718c4-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="718c4-121">De cette façon, la fonction **D3DXVec3Add** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="718c4-121">In this way, the **D3DXVec3Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="718c4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="718c4-122">Requirements</span></span>



| <span data-ttu-id="718c4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="718c4-123">Requirement</span></span> | <span data-ttu-id="718c4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="718c4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="718c4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="718c4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="718c4-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="718c4-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="718c4-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="718c4-127">Library</span></span><br/> | <dl> <span data-ttu-id="718c4-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="718c4-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="718c4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="718c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718c4-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="718c4-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="718c4-131">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="718c4-131">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> <dt>

[<span data-ttu-id="718c4-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="718c4-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




