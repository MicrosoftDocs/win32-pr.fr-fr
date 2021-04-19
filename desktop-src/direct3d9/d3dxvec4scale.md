---
description: Met à l’échelle un vecteur 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: D3DXVec4Scale, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525886"
---
# <a name="d3dxvec4scale-function"></a><span data-ttu-id="3c315-103">D3DXVec4Scale fonction)</span><span class="sxs-lookup"><span data-stu-id="3c315-103">D3DXVec4Scale function</span></span>

<span data-ttu-id="3c315-104">Met à l’échelle un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="3c315-104">Scales a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c315-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c315-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="3c315-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c315-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3c315-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c315-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c315-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3c315-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3c315-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3c315-110">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c315-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c315-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c315-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3c315-112">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) source.</span><span class="sxs-lookup"><span data-stu-id="3c315-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3c315-113"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c315-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c315-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c315-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c315-115">Valeur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="3c315-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c315-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c315-116">Return value</span></span>

<span data-ttu-id="3c315-117">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c315-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3c315-118">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le vecteur mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="3c315-118">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c315-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3c315-119">Remarks</span></span>

<span data-ttu-id="3c315-120">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="3c315-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3c315-121">De cette façon, la fonction **D3DXVec4Scale** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="3c315-121">In this way, the **D3DXVec4Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c315-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c315-122">Requirements</span></span>



| <span data-ttu-id="3c315-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c315-123">Requirement</span></span> | <span data-ttu-id="3c315-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c315-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c315-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c315-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3c315-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c315-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3c315-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c315-127">Library</span></span><br/> | <dl> <span data-ttu-id="3c315-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c315-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c315-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c315-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c315-130">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="3c315-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3c315-131">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="3c315-131">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
</dt> <dt>

[<span data-ttu-id="3c315-132">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="3c315-132">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> </dl>

 

 
