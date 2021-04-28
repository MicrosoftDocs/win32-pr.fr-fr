---
description: 'Fonction D3DXQuaternionSlerp (D3dx9math. h) : interpole entre deux quaternions, à l’aide d’une interpolation linéaire sphérique.'
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
ms.openlocfilehash: fb9110da7fae4ebbf4609d361124dbbcdedfe59b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093937"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="ba365-103">D3DXQuaternionSlerp, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ba365-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="ba365-104">Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.</span><span class="sxs-lookup"><span data-stu-id="ba365-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba365-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba365-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="ba365-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba365-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba365-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba365-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba365-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ba365-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba365-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba365-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba365-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba365-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba365-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ba365-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="ba365-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ba365-113">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba365-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba365-114">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba365-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ba365-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="ba365-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ba365-116">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba365-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba365-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba365-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba365-118">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="ba365-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba365-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ba365-119">Return value</span></span>

<span data-ttu-id="ba365-120">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba365-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ba365-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="ba365-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba365-122">Notes </span><span class="sxs-lookup"><span data-stu-id="ba365-122">Remarks</span></span>

<span data-ttu-id="ba365-123">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="ba365-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ba365-124">De cette façon, la fonction **D3DXQuaternionSlerp** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ba365-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ba365-125">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="ba365-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba365-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba365-126">Requirements</span></span>



| <span data-ttu-id="ba365-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba365-127">Requirement</span></span> | <span data-ttu-id="ba365-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba365-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba365-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba365-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ba365-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba365-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ba365-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba365-131">Library</span></span><br/> | <dl> <span data-ttu-id="ba365-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba365-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba365-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba365-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba365-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ba365-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
