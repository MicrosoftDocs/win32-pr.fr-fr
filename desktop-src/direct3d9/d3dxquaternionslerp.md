---
description: Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: D3DXQuaternionSlerp, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f0f43e22ddc46007c6f589dfc5fd8b45aa885643
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520315"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="47d4d-103">D3DXQuaternionSlerp, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="47d4d-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="47d4d-104">Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.</span><span class="sxs-lookup"><span data-stu-id="47d4d-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47d4d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="47d4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47d4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d4d-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="47d4d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47d4d-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="47d4d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47d4d-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="47d4d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="47d4d-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47d4d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d4d-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="47d4d-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47d4d-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="47d4d-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="47d4d-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47d4d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d4d-114">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="47d4d-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47d4d-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="47d4d-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="47d4d-116">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47d4d-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d4d-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47d4d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47d4d-118">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="47d4d-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d4d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47d4d-119">Return value</span></span>

<span data-ttu-id="47d4d-120">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="47d4d-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47d4d-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="47d4d-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d4d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="47d4d-122">Remarks</span></span>

<span data-ttu-id="47d4d-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="47d4d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="47d4d-124">De cette façon, la fonction **D3DXQuaternionSlerp** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="47d4d-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="47d4d-125">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="47d4d-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d4d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47d4d-126">Requirements</span></span>



| <span data-ttu-id="47d4d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47d4d-127">Requirement</span></span> | <span data-ttu-id="47d4d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="47d4d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47d4d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="47d4d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="47d4d-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="47d4d-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="47d4d-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47d4d-131">Library</span></span><br/> | <dl> <span data-ttu-id="47d4d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47d4d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47d4d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47d4d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d4d-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="47d4d-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
