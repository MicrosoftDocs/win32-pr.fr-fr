---
description: Retourne un vecteur 4D composé des plus grands composants de deux vecteurs 4D.
ms.assetid: a08ceba0-938c-42af-8f32-b1fd8c12d926
title: D3DXVec4Maximize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c145094deec5bdfdca123e6e494b18bbee01ce5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211971"
---
# <a name="d3dxvec4maximize-function"></a><span data-ttu-id="e8175-103">D3DXVec4Maximize fonction)</span><span class="sxs-lookup"><span data-stu-id="e8175-103">D3DXVec4Maximize function</span></span>

<span data-ttu-id="e8175-104">Retourne un vecteur 4D composé des plus grands composants de deux vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="e8175-104">Returns a 4D vector that is made up of the largest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8175-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8175-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Maximize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e8175-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8175-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e8175-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8175-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8175-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e8175-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e8175-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e8175-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8175-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8175-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8175-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e8175-112">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="e8175-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e8175-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8175-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8175-114">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8175-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e8175-115">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="e8175-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8175-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8175-116">Return value</span></span>

<span data-ttu-id="e8175-117">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8175-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e8175-118">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) composée des plus grands composants des deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="e8175-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8175-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e8175-119">Remarks</span></span>

<span data-ttu-id="e8175-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="e8175-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e8175-121">De cette façon, la fonction **D3DXVec4Maximize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="e8175-121">In this way, the **D3DXVec4Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8175-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8175-122">Requirements</span></span>



| <span data-ttu-id="e8175-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8175-123">Requirement</span></span> | <span data-ttu-id="e8175-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8175-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8175-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8175-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e8175-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8175-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e8175-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8175-127">Library</span></span><br/> | <dl> <span data-ttu-id="e8175-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8175-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8175-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8175-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8175-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e8175-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e8175-131">**D3DXVec4Minimize**</span><span class="sxs-lookup"><span data-stu-id="e8175-131">**D3DXVec4Minimize**</span></span>](d3dxvec4minimize.md)
</dt> </dl>

 

 




