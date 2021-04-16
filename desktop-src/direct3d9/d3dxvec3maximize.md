---
description: Retourne un vecteur 3D composé des plus grands composants de deux vecteurs 3D.
ms.assetid: 8d3a5310-bee9-4dbd-bef3-8a0e1586f365
title: D3DXVec3Maximize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d86f3e54a6399693e37cc0c8970439558d82c9c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530873"
---
# <a name="d3dxvec3maximize-function"></a><span data-ttu-id="fe9e1-103">D3DXVec3Maximize fonction)</span><span class="sxs-lookup"><span data-stu-id="fe9e1-103">D3DXVec3Maximize function</span></span>

<span data-ttu-id="fe9e1-104">Retourne un vecteur 3D composé des plus grands composants de deux vecteurs 3D.</span><span class="sxs-lookup"><span data-stu-id="fe9e1-104">Returns a 3D vector that is made up of the largest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe9e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe9e1-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Maximize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="fe9e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe9e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe9e1-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fe9e1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9e1-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe9e1-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9e1-109">Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fe9e1-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe9e1-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe9e1-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9e1-111">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe9e1-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9e1-112">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="fe9e1-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe9e1-113">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe9e1-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe9e1-114">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe9e1-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9e1-115">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) source.</span><span class="sxs-lookup"><span data-stu-id="fe9e1-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe9e1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe9e1-116">Return value</span></span>

<span data-ttu-id="fe9e1-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe9e1-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe9e1-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) composée des plus grands composants des deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="fe9e1-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe9e1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fe9e1-119">Remarks</span></span>

<span data-ttu-id="fe9e1-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="fe9e1-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fe9e1-121">De cette façon, la fonction **D3DXVec3Maximize** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="fe9e1-121">In this way, the **D3DXVec3Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9e1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe9e1-122">Requirements</span></span>



| <span data-ttu-id="fe9e1-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe9e1-123">Requirement</span></span> | <span data-ttu-id="fe9e1-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe9e1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9e1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe9e1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fe9e1-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9e1-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe9e1-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe9e1-127">Library</span></span><br/> | <dl> <span data-ttu-id="fe9e1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe9e1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe9e1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe9e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9e1-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fe9e1-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fe9e1-131">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="fe9e1-131">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
</dt> </dl>

 

 




