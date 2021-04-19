---
description: Ajoute deux vecteurs 4D.
ms.assetid: da807dc0-6a31-4315-a32d-a42062c22199
title: D3DXVec4Add, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62747cec15c4a9916dfb42572006cbb9fc908b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523853"
---
# <a name="d3dxvec4add-function"></a><span data-ttu-id="32664-103">D3DXVec4Add fonction)</span><span class="sxs-lookup"><span data-stu-id="32664-103">D3DXVec4Add function</span></span>

<span data-ttu-id="32664-104">Ajoute deux vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="32664-104">Adds two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="32664-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32664-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Add(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="32664-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32664-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32664-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="32664-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32664-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="32664-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="32664-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="32664-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32664-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32664-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32664-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="32664-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="32664-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="32664-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="32664-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32664-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32664-114">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="32664-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="32664-115">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="32664-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32664-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32664-116">Return value</span></span>

<span data-ttu-id="32664-117">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="32664-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="32664-118">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est la somme des deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="32664-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="32664-119">Notes</span><span class="sxs-lookup"><span data-stu-id="32664-119">Remarks</span></span>

<span data-ttu-id="32664-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="32664-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="32664-121">De cette façon, la fonction **D3DXVec4Add** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="32664-121">In this way, the **D3DXVec4Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32664-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32664-122">Requirements</span></span>



| <span data-ttu-id="32664-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32664-123">Requirement</span></span> | <span data-ttu-id="32664-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="32664-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32664-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="32664-125">Header</span></span><br/>  | <dl> <span data-ttu-id="32664-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="32664-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="32664-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32664-127">Library</span></span><br/> | <dl> <span data-ttu-id="32664-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32664-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32664-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32664-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32664-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="32664-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="32664-131">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="32664-131">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> <dt>

[<span data-ttu-id="32664-132">**D3DXVec4Scale**</span><span class="sxs-lookup"><span data-stu-id="32664-132">**D3DXVec4Scale**</span></span>](d3dxvec4scale.md)
</dt> </dl>

 

 




